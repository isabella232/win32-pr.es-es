---
description: 'El método SetProperties especifica el número de búferes que se van a asignar y el tamaño de cada búfer. Este método invalida el método CBaseAllocator:: SetProperties.'
ms.assetid: 8d419432-a9a7-44fb-b916-8dacd08eb6ec
title: Método CImageAllocator. SetProperties (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c04501fe3511d9cdd45f3513c68082d2ffece0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661123"
---
# <a name="cimageallocatorsetproperties-method"></a>CImageAllocator. SetProperties (método)

El `SetProperties` método especifica el número de búferes que se van a asignar y el tamaño de cada búfer. Este método invalida el método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pRequest* 
</dt> <dd>

Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contiene los requisitos de búfer.

</dd> <dt>

*pActual* 
</dt> <dd>

Puntero a una estructura de **\_ propiedades de asignador** que recibe las propiedades de búfer reales.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método llama a [**CImageAllocator:: CheckSizes**](cimageallocator-checksizes.md) para validar el tamaño de búfer solicitado. También llama a la versión de la clase base de `SetProperties` .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CImageAllocator**](cimageallocator.md)
</dt> </dl>

 

 




