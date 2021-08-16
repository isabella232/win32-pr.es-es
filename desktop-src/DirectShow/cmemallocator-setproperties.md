---
description: El método SetProperties especifica el número de búferes que se asignarán y el tamaño de cada búfer.
ms.assetid: 01f63379-1d66-4a72-b87c-de55504b0bb4
title: Método CMemAllocator.SetProperties (Amfilter.h)
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
ms.openlocfilehash: 5c5a145e630101bda4d060058cde7bfd91796386f0915e9e5329f63ced43ef19
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117821970"
---
# <a name="cmemallocatorsetproperties-method"></a>Método CMemAllocator.SetProperties

El `SetProperties` método especifica el número de búferes que se asignarán y el tamaño de cada búfer.

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

Puntero a una [**estructura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contiene los requisitos de búfer.

</dd> <dt>

*pActual* 
</dt> <dd>

Puntero a una **estructura ALLOCATOR \_ PROPERTIES** que recibe las propiedades de búfer reales.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                                 | Descripción                                                           |
|-------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                        | Correcto.<br/>                                                   |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>                   | **Argumento de** puntero NULL.<br/>                                 |
| <dl> <dt>**VFW \_ E \_ YA \_ CONFIRMADO**</dt> </dl>   | No se puede cambiar la memoria asignada mientras el filtro está activo.<br/> |
| <dl> <dt>**VFW \_ E \_ BADALIGN**</dt> </dl>             | Se especificó una alineación no válida.<br/>                        |
| <dl> <dt>**BÚFERES \_ DE VFW E \_ \_ PENDIENTES**</dt> </dl> | Uno o varios búferes siguen activos.<br/>                      |



 

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CBaseAllocator::SetProperties.**](cbaseallocator-setproperties.md)

La alineación del búfer, especificada por el **miembro cbAlign** de la estructura **ALLOCATOR \_ PROPERTIES,** debe ser una potencia uniforme de dos.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMemAllocator (clase)**](cmemallocator.md)
</dt> </dl>

 

 




