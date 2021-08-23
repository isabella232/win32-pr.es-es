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
ms.openlocfilehash: 93d3f367b0aa69fd2b5782e7cf3c830c30f140389d8611caadc7b70372762625
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119813796"
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
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | No se han establecido los requisitos del búfer.<br/> |



 

## <a name="remarks"></a>Comentarios

El método [**CBaseAllocator::Commit**](cbaseallocator-commit.md) llama a este método. Asigna un bloque contiguo de memoria suficiente para los requisitos de búfer especificados en el [**método CMemAllocator::SetProperties.**](cmemallocator-setproperties.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CMemAllocator (clase)**](cmemallocator.md)
</dt> </dl>

 

 




