---
description: 'Método CTransInPlaceInputPin.PeekAllocator: el método PeekAllocator devuelve un puntero al asignador del pin. El método no incrementa el recuento de referencias en la interfaz .'
ms.assetid: 67f1b872-4ae2-4fbe-9240-801ef8ae1e5b
title: Método CTransInPlaceInputPin.PeekAllocator (Transip.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: fbebca79b560ae2dfd10f95fc7b5f454228da017d6682b6f939ad504c624be72
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999155"
---
# <a name="ctransinplaceinputpinpeekallocator-method"></a>Método CTransInPlaceInputPin.PeekAllocator

El `PeekAllocator` método devuelve un puntero al asignador del pin. El método no incrementa el recuento de referencias en la interfaz .

## <a name="syntax"></a>Sintaxis


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la variable [**miembro CBaseInputPin::m \_ pAllocator.**](cbaseinputpin-m-pallocator.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transip.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransInPlaceInputPin (clase)**](ctransinplaceinputpin.md)
</dt> </dl>

 

 




