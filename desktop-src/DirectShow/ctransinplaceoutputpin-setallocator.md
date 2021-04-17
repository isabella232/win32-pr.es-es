---
description: El método SetAllocator especifica un asignador para la conexión.
ms.assetid: 6b8e80f9-3b0d-498f-b1b0-bae491c25e81
title: Método CTransInPlaceOutputPin. SetAllocator (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.SetAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aacc2680bebcdd7de74f6f357380066a8fd37f1f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660356"
---
# <a name="ctransinplaceoutputpinsetallocator-method"></a>CTransInPlaceOutputPin. SetAllocator, método

El `SetAllocator` método especifica un asignador para la conexión.

## <a name="syntax"></a>Sintaxis


```C++
void SetAllocator(
   IMemAllocator *pAllocator
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pAllocator* 
</dt> <dd>

Puntero a la interfaz [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) del asignador.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

El PIN de salida de este filtro nunca proporciona un asignador. Este método especifica el asignador para el PIN de salida. Establece el valor de la variable miembro [**CBaseOutputPin:: m \_ pAllocator**](cbaseoutputpin-m-pallocator.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>TRANSip. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransInPlaceOutputPin**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




