---
description: The QueryAccept method determines whether the pin accepts a specified media type. This method implements the IPin::QueryAccept method.
ms.assetid: 7aa25b45-5116-474b-afee-1eddc8b7fd2a
title: CBasePin.QueryAccept method (Amfilter.h)
ms.topic: reference
ms.date: 4/26/2023
topic_type: 
- APIRef
- kbSyntax
api_name: 
- CBasePin.QueryAccept
api_type: 
- COM
api_location: 
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.custom: UpdateFrequency5
---

# CBasePin.QueryAccept method

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). **MediaPlayer** and **IMFMediaEngine** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The `QueryAccept` method determines whether the pin accepts a specified media type. This method implements the [**IPin::QueryAccept**](/windows/desktop/api/Strmif/nf-strmif-ipin-queryaccept) method.

## Syntax


```C++
HRESULT QueryAccept(
   const AM_MEDIA_TYPE *pmt
);
```



## Parameters

<dl> <dt>

*pmt* 
</dt> <dd>

Pointer to an [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure that specifies the media type.

</dd> </dl>

## Return value

Returns S\_OK if the media type is acceptable. Otherwise, returns S\_FALSE.

## Remarks

In the base class, this method delegates to the [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method. If **CheckMediaType** fails, `QueryAccept` returns S\_FALSE.

This method does not hold the pin's critical section ([**CBasePin::m\_pLock**](cbasepin-m-plock.md)). If your derived class dynamically modifies the set of acceptable media types, you should override this method to hold the critical section.

## Requirements



| Requirement | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CBasePin Class**](cbasepin.md)
</dt> </dl>

 

 




