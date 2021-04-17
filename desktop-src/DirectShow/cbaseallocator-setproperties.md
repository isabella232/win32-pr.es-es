---
description: 'El método SetProperties especifica el número de búferes que se van a asignar y el tamaño de cada búfer. Este método implementa el método IMemAllocator:: SetProperties.'
ms.assetid: f53c22a4-c01d-4d2f-81f0-bedf8f2ae5f0
title: Método CBaseAllocator. SetProperties (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 000da3ee359ad727e3af972fc4aa6d0dbbb9133e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690810"
---
# <a name="cbaseallocatorsetproperties-method"></a>CBaseAllocator. SetProperties (método)

El `SetProperties` método especifica el número de búferes que se van a asignar y el tamaño de cada búfer. Este método implementa el método [**IMemAllocator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) .

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

Devuelve uno de los siguientes valores **HRESULT** .



| Código devuelto                                                                                                 | Descripción                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                        | Correcto.<br/>                                                   |
| <dl> <dt>**\_puntero E**</dt> </dl>                   | Argumento de puntero **nulo** .<br/>                                 |
| <dl> <dt>**VFW \_ E \_ ya \_ confirmado**</dt> </dl>   | No se puede cambiar la memoria asignada mientras el filtro está activo.<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | Se especificó una alineación no válida.<br/>                        |
| <dl> <dt>**\_ \_ búferes VFW E \_ pendientes**</dt> </dl> | Uno o más búferes siguen activos.<br/>                      |



 

## <a name="remarks"></a>Observaciones

Este método especifica los requisitos de búfer, pero no asigna ningún búfer. Llame al método [**CBaseAllocator:: commit**](cbaseallocator-commit.md) para asignar búferes.

El autor de la llamada asigna dos estructuras de propiedades de ASIGNADOr \_ . El parámetro *pRequest* contiene los requisitos de búfer del llamador, incluido el número de búferes y el tamaño de cada búfer. Cuando el método devuelve, el parámetro *pActual* contiene las propiedades de búfer reales, tal como se establece en el asignador. En la clase base, suponiendo que el método se ejecuta correctamente, las propiedades reales siempre coinciden con las propiedades solicitadas. Las clases derivadas pueden invalidar este comportamiento.

El asignador no debe confirmarse y no debe tener búferes pendientes. En la clase base, la alineación debe ser igual a 1. La clase [**CMemAllocator**](cmemallocator.md) invalida este requisito.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




