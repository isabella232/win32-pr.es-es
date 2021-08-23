---
description: 'Método CTransformOutputPin.DecideBufferSize: el método DecideBufferSize establece los requisitos de búfer.'
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: Método CTransformOutputPin.DecideBufferSize (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3c6ea09c348fa465e1bffac2bdf426b635ed4cb4b76013a053ab775e78199612
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538225"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a>Método CTransformOutputPin.DecideBufferSize

El `DecideBufferSize` método establece los requisitos del búfer.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAlloc* 
</dt> <dd>

Puntero a la interfaz [**IMemAllocator del asignador.**](/windows/desktop/api/Strmif/nn-strmif-imemallocator)

</dd> <dt>

*ppropInputRequest* 
</dt> <dd>

Puntero a [**una estructura ALLOCATOR \_ PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contiene los requisitos de búfer del pin de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Comentarios

Este método invalida el método [**CBaseOutputPin::D ecideBufferSize.**](cbaseoutputpin-decidebuffersize.md) Llama al método [**CTransformFilter::D ecideBufferSize**](ctransformfilter-decidebuffersize.md) puro del filtro, que la clase derivada del filtro debe implementar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




