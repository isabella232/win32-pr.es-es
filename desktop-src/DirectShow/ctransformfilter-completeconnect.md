---
description: El método CompleteConnect completa una conexión de PIN.
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: Método CTransformFilter. CompleteConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 630950cf9b05c08412394bf9270f2369b3f3b94b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660730"
---
# <a name="ctransformfiltercompleteconnect-method"></a>CTransformFilter. CompleteConnect, método

El `CompleteConnect` método completa una conexión de PIN.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CompleteConnect(
   PIN_DIRECTION direction,
   IPin          *pReceivePin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*direction* 
</dt> <dd>

Miembro del tipo enumerado de [**\_ dirección del PIN**](/windows/win32/api/strmif/ne-strmif-pin_direction) , que especifica el PIN del filtro que realiza la conexión.

</dd> <dt>

*pReceivePin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro PIN en este intento de conexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Los métodos [**CTransformInputPin:: CompleteConnect**](ctransforminputpin-completeconnect.md) y [**CTransformOutputPin:: CompleteConnect**](ctransformoutputpin-completeconnect.md) llaman a este método durante el proceso de conexión del PIN. Este método no hace nada en la clase base, pero la clase derivada puede invalidarlo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CTransformFilter**](ctransformfilter.md)
</dt> </dl>

 

 




