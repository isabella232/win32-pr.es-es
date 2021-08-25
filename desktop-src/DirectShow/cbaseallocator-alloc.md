---
description: 'Método CBaseAllocator.Alloc: el método Alloc asigna memoria para los búferes.'
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: Método CBaseAllocator.Alloc (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 975f373136759a0950e5052413eccb501176e7876531208fd20380ee7d1fb10a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966724"
---
# <a name="cbaseallocatoralloc-method"></a>CBaseAllocator.Alloc (método)

El `Alloc` método asigna memoria para los búferes.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes **valores HRESULT.**



| Código devuelto                                                                                       | Descripción                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ FALSE**</dt> </dl>           | Los requisitos del búfer no han cambiado.<br/> |
| <dl> <dt>**S \_ OK**</dt> </dl>              | Los requisitos del búfer han cambiado.<br/>     |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | No se han establecido los requisitos del búfer.<br/>     |



 

## <a name="remarks"></a>Comentarios

El método [**CBaseAllocator::Commit**](cbaseallocator-commit.md) llama a este método.

En la clase base, este método no asigna memoria. Devuelve un error si no se han establecido los requisitos del búfer, S FALSE si los requisitos no han cambiado y S OK si los requisitos \_ \_ han cambiado.

Una clase derivada debe invalidar este método para realizar la asignación de memoria real. Normalmente, la clase derivada realizará los pasos siguientes:

1.  Llame a la implementación de la clase base para determinar si la memoria realmente necesita asignarse.
2.  Asigne memoria.
3.  Cree [**objetos CMediaSample**](cmediasample.md) que contengan fragmentos de memoria del paso 2.
4.  Agregue cada **objeto CMediaSample** a la lista de ejemplos gratuitos ([**CBaseAllocator::m \_ lFree**](cbaseallocator-m-lfree.md)).

Para obtener un ejemplo, [**vea CMemAllocator::Alloc**](cmemallocator-alloc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseAllocator (clase)**](cbaseallocator.md)
</dt> </dl>

 

 




