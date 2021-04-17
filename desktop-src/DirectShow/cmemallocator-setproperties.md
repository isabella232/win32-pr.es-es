---
description: El método SetProperties especifica el número de búferes que se van a asignar y el tamaño de cada búfer.
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: Método CMemAllocator. SetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8505916245cca81fdd84132e4523fe9dd03b971b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680353"
---
# <a name="cmemallocatorsetproperties-method"></a>CMemAllocator. SetProperties (método)

El `SetProperties` método especifica el número de búferes que se van a asignar y el tamaño de cada búfer.

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

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                                 | Descripción                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                        | Correcto.<br/>                                                   |
| <dl> <dt>**\_puntero E**</dt> </dl>                   | Argumento de puntero **nulo** .<br/>                                 |
| <dl> <dt>**VFW \_ E \_ ya \_ confirmado**</dt> </dl>   | No se puede cambiar la memoria asignada mientras el filtro está activo.<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | Se especificó una alineación no válida.<br/>                        |
| <dl> <dt>**\_ \_ búferes VFW E \_ pendientes**</dt> </dl> | Uno o más búferes siguen activos.<br/>                      |



 

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) .

La alineación del búfer, especificada por el miembro **cbAlign** de la estructura de **\_ propiedades de asignador** , debe ser una potencia uniforme de dos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




