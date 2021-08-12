---
description: El método ReleaseBuffer devuelve un ejemplo multimedia a la lista de ejemplos de medios gratuitos. Este método implementa el método IMemAllocator::ReleaseBuffer.
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: Método CBaseAllocator.ReleaseBuffer (Amfilter.h)
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
ms.openlocfilehash: 5d1096cc7cd4ed31346b38719a3f622edf780408fd50262d93515f68d92b421d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118661511"
---
# <a name="cbaseallocatorreleasebuffer-method"></a>Método CBaseAllocator.ReleaseBuffer

El `ReleaseBuffer` método devuelve un ejemplo multimedia a la lista de ejemplos de medios gratuitos. Este método implementa el [**método IMemAllocator::ReleaseBuffer.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer)

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

Puntero a la [**interfaz IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) del objeto de ejemplo multimedia.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Observaciones

Cuando el recuento de referencias de un ejemplo multimedia alcanza cero, el ejemplo llama a **ReleaseBuffer** con sí mismo como parámetro. Este método realiza las siguientes acciones.

-   Devuelve el ejemplo multimedia a la lista libre ([**CBaseAllocator::m \_ lFree**](cbaseallocator-m-lfree.md)).
-   Llama al [**método CBaseAllocator::NotifySample,**](cbaseallocator-notifysample.md) que libera los subprocesos bloqueados en las llamadas al método [**CBaseAllocator::GetBuffer.**](cbaseallocator-getbuffer.md)
-   Si anteriormente se llamó al método [**CBaseAllocator::SetNotify,**](cbaseallocator-setnotify.md) llama al método **IMemAllocatorNotifyCallbackTemp::NotifyRelease.**
-   Cuando se publica el último ejemplo, si hay una llamada a [**CBaseAllocator::D ecommit**](cbaseallocator-decommit.md) pendiente, llama al método [**CBaseAllocator::Free**](cbaseallocator-free.md) para liberar la memoria del búfer. (En la clase base, **Free es** un método virtual puro).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




