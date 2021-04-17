---
description: El método BreakConnect libera un código PIN de una conexión.
ms.assetid: cc384786-9cba-4f68-9c60-740205b35661
title: Método CTransformFilter. BreakConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: aec60322a4782d84e84dc2030b69f6c385783e98
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660303"
---
# <a name="ctransformfilterbreakconnect-method"></a>CTransformFilter. BreakConnect, método

El `BreakConnect` método libera un código PIN de una conexión.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT BreakConnect(
   PIN_DIRECTION dir
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*dir* 
</dt> <dd>

Miembro del tipo enumerado de [**\_ dirección del PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , que especifica qué conexión de PIN se interrumpió (entrada o salida).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Los métodos [**CTransformInputPin:: BreakConnect**](ctransforminputpin-breakconnect.md) y [**CTransformOutputPin:: BreakConnect**](ctransformoutputpin-breakconnect.md) llaman a este método cuando se interrumpe una conexión de PIN. Este método no hace nada en la clase base. Si invalida el método [**CheckConnect**](ctransformfilter-checkconnect.md) , Invalide este método para liberar los recursos obtenidos en el método **CheckConnect** , incluidos los punteros de interfaz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




