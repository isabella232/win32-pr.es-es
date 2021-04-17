---
description: El método Alloc asigna memoria a los búferes.
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: Método CMemAllocator. Alloc (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a142f6c0cea6cdb9b18507becabb909ce67b0fb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670758"
---
# <a name="cmemallocatoralloc-method"></a>CMemAllocator. Alloc (método)

El `Alloc` método asigna memoria a los búferes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                       | Descripción                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>              | Correcto.<br/>                          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>     | Memoria insuficiente.<br/>              |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | No se establecieron los requisitos de búfer.<br/> |



 

## <a name="remarks"></a>Observaciones

El método [**CBaseAllocator:: commit**](cbaseallocator-commit.md) llama a este método. Asigna un bloque de memoria contiguo suficiente para los requisitos de búfer proporcionados en el método [**CMemAllocator:: SetProperties**](cmemallocator-setproperties.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CMemAllocator**](cmemallocator.md)
</dt> </dl>

 

 




