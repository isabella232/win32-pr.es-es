---
description: 'Método CTransformInputPin.CompleteConnect: el método CompleteConnect completa una conexión a otro pin.'
ms.assetid: 568cee55-b9ea-4fc2-ac9d-0080b7de9790
title: Método CTransformInputPin.CompleteConnect (Transfrm.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 20f378479209b2614116ba25f51950923358f1b2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085013"
---
# <a name="ctransforminputpincompleteconnect-method"></a>Método CTransformInputPin.CompleteConnect

El `CompleteConnect` método completa una conexión a otro pin.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro pin.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK u otro valor **HRESULT.**

## <a name="remarks"></a>Comentarios

Este método invalida el [**método CBasePin::CompleteConnect.**](cbasepin-completeconnect.md) Llama al método [**CTransformFilter::CompleteConnect**](ctransformfilter-completeconnect.md) del filtro, que devuelve S \_ OK en la clase base. La clase derivada puede invalidar el **método CTransformFilter::CompleteConnect** para realizar comprobaciones adicionales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




