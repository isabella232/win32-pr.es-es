---
description: 'El método ReleaseBuffer devuelve un ejemplo multimedia a la lista de ejemplos de medios disponibles. Este método implementa el método IMemAllocator:: ReleaseBuffer.'
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: Método CBaseAllocator. ReleaseBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.ReleaseBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e339f3a8186e845e28261633806a61b1b15c281
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690811"
---
# <a name="cbaseallocatorreleasebuffer-method"></a>CBaseAllocator. ReleaseBuffer, método

El `ReleaseBuffer` método devuelve un ejemplo multimedia a la lista de ejemplos de medios disponibles. Este método implementa el método [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReleaseBuffer(
   IMediaSample *pSample
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pSample* 
</dt> <dd>

Puntero a la interfaz [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del objeto de ejemplo multimedia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Cuando el recuento de referencias de un ejemplo multimedia llega a cero, el ejemplo llama a **ReleaseBuffer** con sí mismo como parámetro. Este método realiza las acciones siguientes.

-   Devuelve el ejemplo de medio a la lista libre ([**CBaseAllocator:: m \_ lFree**](cbaseallocator-m-lfree.md)).
-   Llama al método [**CBaseAllocator:: NotifySample**](cbaseallocator-notifysample.md) , que libera todos los subprocesos que están bloqueados en llamadas al método [**CBaseAllocator:: getBuffer**](cbaseallocator-getbuffer.md) .
-   Si se llamó previamente al método [**CBaseAllocator:: SetNotify**](cbaseallocator-setnotify.md) , llama al método **IMemAllocatorNotifyCallbackTemp:: NotifyRelease** .
-   Cuando se libera la última muestra, si hay una llamada pendiente [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) , llama al método [**CBaseAllocator:: Free**](cbaseallocator-free.md) para liberar la memoria del búfer. (En la clase base, **Free** es un método virtual puro).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




