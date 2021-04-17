---
description: El método CheckSizes comprueba las propiedades de asignador con el tipo de medio actual.
ms.assetid: 040b4ed0-c1cc-4995-a0f8-86efa493f84b
title: Método CImageAllocator. CheckSizes (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CheckSizes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 71184d4915911c29bff9d3a6fa9985942a4aaa44
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680516"
---
# <a name="cimageallocatorchecksizes-method"></a>CImageAllocator. CheckSizes, método

El `CheckSizes` método comprueba las propiedades de asignador con el tipo de medio actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckSizes(
   ALLOCATOR_PROPERTIES *pRequest
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pRequest* 
</dt> <dd>

Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que describe las propiedades de asignador solicitadas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                           | Descripción                                                                 |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                  | Las propiedades solicitadas son compatibles con el tipo de medio.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Las propiedades solicitadas no son compatibles con el tipo de medio.<br/> |
| <dl> <dt>**VFW \_ E \_ no \_ conectada**</dt> </dl> | El PIN propietario no está conectado.<br/>                                 |



 

## <a name="remarks"></a>Observaciones

Cuando el método devuelve, si el valor devuelto es S \_ OK, el miembro **cbBuffer** de *pRequest* contiene el tamaño de búfer real. Esto puede ser mayor que el tamaño solicitado, pero nunca será menor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImageAllocator**](cimageallocator.md)
</dt> </dl>

 

 




