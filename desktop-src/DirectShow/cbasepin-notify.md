---
description: CBasePin.Notify method - The Notify method notifies the pin that a quality change is requested. This method implements the IQualityControl::Notify method.
ms.assetid: 5e9394d9-8d3c-4091-b45f-345a3f7270db
title: CBasePin.Notify method (Amfilter.h)
ms.topic: reference
ms.date: 4/26/2023
topic_type: 
- APIRef
- kbSyntax
api_name: 
- CBasePin.Notify
api_type: 
- COM
api_location: 
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.custom: UpdateFrequency5
---

# CBasePin.Notify method

\[The feature associated with this page, [DirectShow](/windows/win32/directshow/directshow), is a legacy feature. It has been superseded by [MediaPlayer](/uwp/api/Windows.Media.Playback.MediaPlayer) and [IMFMediaEngine](/windows/win32/api/mfmediaengine/nn-mfmediaengine-imfmediaengine). **MediaPlayer** and **IMFMediaEngine** have been optimized for Windows 10 and Windows 11. Microsoft strongly recommends that new code use **MediaPlayer** and **IMFMediaEngine** instead of **DirectShow**, when possible. Microsoft suggests that existing code that uses the legacy APIs be rewritten to use the new APIs if possible.\]

The `Notify` method notifies the pin that a quality change is requested. This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.

## Syntax


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## Parameters

<dl> <dt>

*pSelf* 
</dt> <dd>

Pointer to the [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface of the filter that delivered the quality-control message.

</dd> <dt>

*q* 
</dt> <dd>

Specifies a [**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.

</dd> </dl>

## Return value

The base class returns E\_NOTIMPL.

## Remarks

Output pins should override this method to accept quality-control messages.

If an external quality manager was installed (see [**CBasePin::SetSink**](cbasepin-setsink.md)), pass the message to that quality manager. Otherwise, the filter should handle the message itself, or pass the message upstream. For more information, see [Quality-Control Management](quality-control-management.md).

## Requirements



| Requirement | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Amfilter.h (include Streams.h)</dt> </dl>                                                                                  |
| Library<br/> | <dl> <dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt> </dl> |



## See also

<dl> <dt>

[**CBasePin Class**](cbasepin.md)
</dt> </dl>

 

 




