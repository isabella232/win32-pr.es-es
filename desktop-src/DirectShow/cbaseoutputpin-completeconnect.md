---
description: 'Método CBaseOutputPin.CompleteConnect: el método CompleteConnect completa una conexión a un pin de entrada.'
ms.assetid: 44c28c71-2c69-40ca-9bc4-c10394475a0f
title: Método CBaseOutputPin.CompleteConnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd4bc52db99b88c4d6f16c549fbb558bb6423730
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127273167"
---
# <a name="cbaseoutputpincompleteconnect-method"></a>Método CBaseOutputPin.CompleteConnect

El `CompleteConnect` método completa una conexión a un pin de entrada.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntero al pin de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK si se realiza correctamente o un valor **HRESULT** que indica la causa del error.

## <a name="remarks"></a>Observaciones

Este método invalida el [**método CBasePin::CompleteConnect.**](cbasepin-completeconnect.md) Llama al [**método DecideAllocator,**](cbaseoutputpin-decideallocator.md) que selecciona el asignador de memoria que se va a usar para esta conexión.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseOutputPin (clase)**](cbaseoutputpin.md)
</dt> </dl>

 

 




