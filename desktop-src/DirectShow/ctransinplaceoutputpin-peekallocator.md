---
description: 'Método CTransInPlaceOutputPin.PeekAllocator: el método PeekAllocator devuelve un puntero al asignador del pin. El método no incrementa el recuento de referencias en la interfaz .'
ms.assetid: 3653d472-059c-426c-8e81-4f7cbd1a8ec3
title: Método CTransInPlaceOutputPin.PeekAllocator (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cba87df1c4b9a3391d60e9458387e7b2bd4afd49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084603"
---
# <a name="ctransinplaceoutputpinpeekallocator-method"></a>CTransInPlaceOutputPin.PeekAllocator (método)

El `PeekAllocator` método devuelve un puntero al asignador del pin. El método no incrementa el recuento de referencias en la interfaz .

## <a name="syntax"></a>Sintaxis


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la variable [**miembro CBaseOutputPin::m \_ pAllocator.**](cbaseoutputpin-m-pallocator.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Streams.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransInPlaceOutputPin (clase)**](ctransinplaceoutputpin.md)
</dt> </dl>

 

 




