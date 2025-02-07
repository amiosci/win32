---
description: Uses the Microsoft Win32 SetThreadPriority function to set the priority of the thread to a new value.
ms.assetid: 5b8ad024-e651-47e5-b32a-c44d56c086cd
title: CMsgThread.SetThreadPriority method (Msgthrd.h)
ms.topic: reference
ms.date: 4/26/2023
topic_type: 
- APIRef
- kbSyntax
api_name: 
- CMsgThread.SetThreadPriority
api_type: 
- COM
api_location: 
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.custom: UpdateFrequency5
---

# CMsgThread.SetThreadPriority method

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). **MediaPlayer** and **IMFMediaEngine** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

Uses the Microsoft Win32 **SetThreadPriority** function to set the priority of the thread to a new value.

## Syntax


```C++
BOOL SetThreadPriority(
   int nPriority
);
```



## Parameters

<dl> <dt>

*nPriority* 
</dt> <dd>

Priority of the thread.

</dd> </dl>

## Return value

Returns one of the following values.



| Return code                                                                              | Description                               |
|------------------------------------------------------------------------------------------|-------------------------------------------|
| <dl> <dt>****TRUE****</dt> </dl>  | Priority was successfully set.<br/> |
| <dl> <dt>****FALSE****</dt> </dl> | Priority was not set.<br/>          |



 

## Remarks

The client and the worker thread can call this member function.

## Requirements



| Requirement | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Msgthrd.h (include Streams.h)</dt> </dl>                                                                                   |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CMsgThread Class**](cmsgthread.md)
</dt> </dl>

 

 




