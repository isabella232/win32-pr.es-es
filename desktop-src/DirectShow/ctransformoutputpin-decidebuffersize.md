---
description: El método DecideBufferSize establece los requisitos de búfer.
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: Método CTransformOutputPin. DecideBufferSize (Transfrm. h)
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
ms.openlocfilehash: dc17314887094b7f62a43f38dd406d0ac9039de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661005"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a>CTransformOutputPin. DecideBufferSize, método

El `DecideBufferSize` método establece los requisitos de búfer.

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

Puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador.

</dd> <dt>

*ppropInputRequest* 
</dt> <dd>

Puntero a una estructura de [**\_ propiedades de asignador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contiene los requisitos de búfer del PIN de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) . Llama al método CTransformFilter virtual puro del filtro [**::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) , que debe implementar la clase derivada del filtro.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




