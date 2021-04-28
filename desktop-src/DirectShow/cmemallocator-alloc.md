---
description: 'Método CMemAllocator.Alloc: el método Alloc asigna memoria para los búferes.'
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: Método CMemAllocator.Alloc (Amfilter.h)
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
ms.openlocfilehash: 7d7de755aa3b8007a122e43529d16f5e39ca0cb8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099043"
---
# <a name="cmemallocatoralloc-method"></a>Método CMemAllocator.Alloc

El `Alloc` método asigna memoria para los búferes.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Alloc();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                       | Descripción                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>              | Correcto.<br/>                          |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>     | Memoria insuficiente.<br/>              |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | No se han establecido los requisitos de búfer.<br/> |



 

## <a name="remarks"></a>Comentarios

El método [**CBaseAllocator::Commit**](cbaseallocator-commit.md) llama a este método. Asigna un bloque contiguo de memoria suficiente para los requisitos de búfer especificados en el [**método CMemAllocator::SetProperties.**](cmemallocator-setproperties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CMemAllocator (clase)**](cmemallocator.md)
</dt> </dl>

 

 




