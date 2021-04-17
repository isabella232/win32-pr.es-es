---
description: El método Alloc asigna memoria a los búferes.
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: Método CBaseAllocator. Alloc (Amfilter. h)
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
ms.openlocfilehash: b7510a108e69eb218a894b67dd5b62d94bfdbe6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670328"
---
# <a name="cbaseallocatoralloc-method"></a>CBaseAllocator. Alloc (método)

El `Alloc` método asigna memoria a los búferes.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** .



| Código devuelto                                                                                       | Descripción                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ false**</dt> </dl>           | Los requisitos de búfer no han cambiado.<br/> |
| <dl> <dt>**S \_ correcto**</dt> </dl>              | Los requisitos de búfer han cambiado.<br/>     |
| <dl> <dt>**VFW \_ E \_ SIZENOTSET**</dt> </dl> | No se establecieron los requisitos de búfer.<br/>     |



 

## <a name="remarks"></a>Observaciones

El método [**CBaseAllocator:: commit**](cbaseallocator-commit.md) llama a este método.

En la clase base, este método no asigna ninguna memoria. Devuelve un error si no se establecieron los requisitos de búfer, es \_ false si no se han cambiado los requisitos y \_ si los requisitos han cambiado.

Una clase derivada debe invalidar este método para realizar la asignación de memoria real. Normalmente, la clase derivada realizará los siguientes pasos:

1.  Llame a la implementación de la clase base para determinar si realmente es necesario asignar la memoria.
2.  Asigne memoria.
3.  Cree objetos [**CMediaSample**](cmediasample.md) que contengan fragmentos de memoria del paso 2.
4.  Agregue cada objeto **CMediaSample** a la lista de ejemplos gratuitos ([**CBaseAllocator:: m \_ lFree**](cbaseallocator-m-lfree.md)).

Para obtener un ejemplo, vea [**CMemAllocator:: Alloc**](cmemallocator-alloc.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseAllocator**](cbaseallocator.md)
</dt> </dl>

 

 




