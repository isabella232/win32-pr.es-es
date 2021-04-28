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
ms.openlocfilehash: d2251ba45c7a39ec9bf205fdd6643e02392e40e5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095173"
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
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CTransformFilter (clase)**](ctransformfilter.md)
</dt> </dl>

 

 




