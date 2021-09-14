---
description: 'Método CTransformOutputPin.DecideBufferSize: el método DecideBufferSize establece los requisitos del búfer.'
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
ms.openlocfilehash: 1bc84eaf5e95a19436de5429ce018352cdaa286e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255368"
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

## <a name="remarks"></a>Observaciones

Este método invalida el [**método CBaseOutputPin::D ecideBufferSize.**](cbaseoutputpin-decidebuffersize.md) Llama al método [**CTransformFilter::D ecideBufferSize**](ctransformfilter-decidebuffersize.md) virtual puro del filtro, que la clase derivada del filtro debe implementar.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




