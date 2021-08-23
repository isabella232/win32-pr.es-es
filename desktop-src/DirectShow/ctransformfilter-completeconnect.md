---
description: 'Método CTransformFilter.CompleteConnect: el método CompleteConnect completa una conexión de pin.'
ms.assetid: b687d2ee-4aee-4fae-bc2f-23ee037d0e6d
title: Método CTransformFilter.CompleteConnect (Transfrm.h)
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
ms.openlocfilehash: 7e708745231f320d143c55403a75178e78432a162c3c89fc2c5fe8fd62cdd8b6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119687315"
---
# <a name="ctransformfiltercompleteconnect-method"></a>Método CTransformFilter.CompleteConnect

El `CompleteConnect` método completa una conexión de pin.

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

Miembro del tipo [**enumerado \_ PIN DIRECTION,**](/windows/win32/api/strmif/ne-strmif-pin_direction) especificando qué pin en el filtro está realizando la conexión.

</dd> <dt>

*pReceivePin* 
</dt> <dd>

Puntero a la [**interfaz IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro pin en este intento de conexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Los [**métodos CTransformInputPin::CompleteConnect**](ctransforminputpin-completeconnect.md) y [**CTransformOutputPin::CompleteConnect**](ctransformoutputpin-completeconnect.md) llaman a este método durante el proceso de conexión de pin. Este método no hace nada en la clase base, pero la clase derivada puede invalidarla.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




