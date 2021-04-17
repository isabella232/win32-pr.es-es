---
description: 'El método Alloc asigna memoria a los búferes. Este método invalida el método CBaseAllocator:: Alloc.'
ms.assetid: 4a246b4e-93b3-4adb-9f10-6b92d9f479eb
title: Método CImageAllocator. Alloc (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7acd13e2d2d09e6e491a2f338aef2fe7564b82b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660822"
---
# <a name="cimageallocatoralloc-method"></a>CImageAllocator. Alloc (método)

El `Alloc` método asigna memoria a los búferes. Este método invalida el método [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                   | Descripción                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | Correcto<br/>             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | Memoria insuficiente<br/> |



 

## <a name="remarks"></a>Observaciones

El método [**CBaseAllocator:: commit**](cbaseallocator-commit.md) llama a este método cuando el filtro confirma el asignador.

Este método crea una lista de ejemplos de medios, que se implementan como objetos [**CImageSample**](cimagesample.md) . Cada ejemplo contiene un mapa de bits independiente del dispositivo GDI mediante la función **CreateDIBSection** de GDI.

Internamente, este método llama a [**CImageAllocator:: CreateDIB**](cimageallocator-createdib.md) para crear cada DIB y [**CImageAllocator:: CreateImageSample**](cimageallocator-createimagesample.md) para crear cada ejemplo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImageAllocator**](cimageallocator.md)
</dt> </dl>

 

 




