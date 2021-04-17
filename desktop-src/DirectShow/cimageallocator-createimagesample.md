---
description: El método CreateImageSample crea un ejemplo multimedia.
ms.assetid: dae71692-5cbc-4bc7-a363-41766ef17c58
title: Método CImageAllocator. CreateImageSample (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CreateImageSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 57463a7025ea816b6fe6bcaa8b964231458903de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660820"
---
# <a name="cimageallocatorcreateimagesample-method"></a>CImageAllocator. CreateImageSample, método

El `CreateImageSample` método crea un ejemplo multimedia.

## <a name="syntax"></a>Sintaxis


```C++
virtual CImageSample* CreateImageSample(
   LPBYTE pData,
   LONG   Length
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pData* 
</dt> <dd>

Puntero a un búfer de *longitud* de tamaño, asignado por el llamador.

</dd> <dt>

*Duración* 
</dt> <dd>

Longitud del búfer.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un objeto [**CImageSample**](cimagesample.md) .

## <a name="remarks"></a>Observaciones

Este método crea un nuevo ejemplo multimedia, implementado como un objeto **CImageSample** . El método [**IMediaSample:: GetPointer**](/windows/desktop/api/Strmif/nf-strmif-imediasample-getpointer) del ejemplo devuelve un puntero al búfer especificado en el parámetro *pdata* .

Si deriva una nueva clase de asignador de [**CImageAllocator**](cimageallocator.md) y una nueva clase de ejemplo multimedia de [**CImageSample**](cimagesample.md), debe invalidar este método para crear una instancia de la clase de ejemplo multimedia.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImageAllocator**](cimageallocator.md)
</dt> <dt>

[**CImageAllocator:: Alloc**](cimageallocator-alloc.md)
</dt> </dl>

 

 




