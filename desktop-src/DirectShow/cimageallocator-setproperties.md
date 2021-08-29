---
description: El método SetProperties especifica el número de búferes que se asignarán y el tamaño de cada búfer. Este método invalida el método CBaseAllocator::SetProperties.
ms.assetid: 8d419432-a9a7-44fb-b916-8dacd08eb6ec
title: Método CImageAllocator.SetProperties (Winutil.h)
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
ms.openlocfilehash: 1924db012ece5ad475a26e75315254ab5228c9cd50aa1dac74d39430f976a367
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119768215"
---
# <a name="cimageallocatorsetproperties-method"></a>Método CImageAllocator.SetProperties

El `SetProperties` método especifica el número de búferes que se asignarán y el tamaño de cada búfer. Este método invalida el [**método CBaseAllocator::SetProperties.**](cbaseallocator-setproperties.md)

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

Puntero a una [**estructura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contiene los requisitos del búfer.

</dd> <dt>

*pActual* 
</dt> <dd>

Puntero a una **estructura ALLOCATOR \_ PROPERTIES** que recibe las propiedades de búfer reales.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Este método llama [**a CImageAllocator::CheckSizes**](cimageallocator-checksizes.md) para validar el tamaño de búfer solicitado. También llama a la versión de clase base de `SetProperties` .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CImageAllocator (clase)**](cimageallocator.md)
</dt> </dl>

 

 




