---
description: El método GetBuffer recupera un ejemplo multimedia que contiene un búfer. Este método implementa el método IMemAllocator::GetBuffer.
ms.assetid: 81694b9c-b325-47c8-94e4-f54d1329a684
title: Método CBaseAllocator.GetBuffer (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f965885d4a7a12e09c8875f71032ce2fded61bd2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127061788"
---
# <a name="cbaseallocatorgetbuffer-method"></a>Método CBaseAllocator.GetBuffer

El `GetBuffer` método recupera un ejemplo multimedia que contiene un búfer. Este método implementa el [**método IMemAllocator::GetBuffer.**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetBuffer(
   IMediaSample   **ppBuffer,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppBuffer* 
</dt> <dd>

Recibe un puntero a la interfaz [**IMediaSample del**](/windows/desktop/api/Strmif/nn-strmif-imediasample) búfer. El autor de la llamada debe liberar la interfaz .

</dd> <dt>

*pStartTime* 
</dt> <dd>

Puntero a la hora de inicio del ejemplo.

</dd> <dt>

*pEndTime* 
</dt> <dd>

Puntero a la hora de finalización del ejemplo.

</dd> <dt>

*dwFlags* 
</dt> <dd>

Combinación bit a bit de cero o más marcas. La clase base admite la marca siguiente.



| Value                                                                                                                                                          | Significado                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="AM_GBF_NOWAIT"></span><span id="am_gbf_nowait"></span><dl> <dt>**AM \_ GBF \_ NOWAIT**</dt> </dl> | No espere a que un búfer esté disponible. <br/> |



 

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT.**



| Código devuelto                                                                                           | Descripción                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Correcto.<br/>                     |
| <dl> <dt>**VFW \_ E \_ NO \_ CONFIRMADO**</dt> </dl> | No se ha confirmado el asignador.<br/> |
| <dl> <dt>**TIEMPO DE ESPERA DE VFW \_ E \_**</dt> </dl>        | agotado el tiempo de espera.<br/>                   |



 

## <a name="remarks"></a>Observaciones

A menos que el autor de la llamada especifique la marca **\_ \_ NOWAIT de AM GBF** en *dwFlags,* este método se bloquea hasta que el ejemplo siguiente esté disponible.

El ejemplo de medio recuperado tiene un puntero válido al búfer asignado. El autor de la llamada es responsable de establecer cualquier otra propiedad del ejemplo, como las marcas de tiempo, las horas de los medios o la propiedad de punto de sincronización. Para obtener más información, vea [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).

En la clase base, se omiten los parámetros *pStartTime* y *pEndTime.* Las clases derivadas pueden usar estos valores. Por ejemplo, el asignador del filtro [Representador](video-renderer-filter.md) de vídeo usa estos valores para sincronizar la conmutación entre las superficies de DirectDraw.

Si el método necesita esperar en un ejemplo, incrementa el recuento de objetos en espera ([**CBaseAllocator::m \_ lCount**](cbaseallocator-m-lcount.md)) y las llamadas a la función [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) en el semáforo ([**CBaseAllocator::m \_ hSem**](cbaseallocator-m-hsem.md)). Cuando un ejemplo está disponible, llama al método [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) en el asignador, lo que aumenta el recuento de semáforos en **m \_ lCount** (liberando así los subprocesos en espera) y establece **m \_ lCount** de nuevo en cero.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

