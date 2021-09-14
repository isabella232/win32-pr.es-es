---
description: El método CheckSizes comprueba las propiedades del asignador con el tipo de medio actual.
ms.assetid: 040b4ed0-c1cc-4995-a0f8-86efa493f84b
title: Método CImageAllocator.CheckSizes (Winutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127170042"
---
# <a name="cimageallocatorchecksizes-method"></a>Método CImageAllocator.CheckSizes

El `CheckSizes` método comprueba las propiedades del asignador con el tipo de medio actual.

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

Puntero a una [**estructura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que describe las propiedades de asignador solicitadas.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                           | Descripción                                                                 |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                  | Las propiedades solicitadas son compatibles con el tipo de medio.<br/>     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>          | Las propiedades solicitadas no son compatibles con el tipo de medio.<br/> |
| <dl> <dt>**VFW \_ E \_ NO \_ CONECTADO**</dt> </dl> | El pin propietario no está conectado.<br/>                                 |



 

## <a name="remarks"></a>Observaciones

Cuando el método devuelve un valor, si el valor devuelto es S OK, el \_ **miembro cbBuffer** de *pRequest* contiene el tamaño de búfer real. Puede ser mayor que el tamaño solicitado, pero nunca será menor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImageAllocator (clase)**](cimageallocator.md)
</dt> </dl>

 

 




