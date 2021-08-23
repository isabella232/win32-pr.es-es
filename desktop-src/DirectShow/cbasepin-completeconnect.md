---
description: 'Método CBasePin.CompleteConnect: el método CompleteConnect completa una conexión a otro pin.'
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Método CBasePin.CompleteConnect (Amfilter.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e31829829a99dc613cfeeeda7ad8a9871c1a3ec4fee99220b804b171bbdcdc29
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119074789"
---
# <a name="cbasepincompleteconnect-method"></a>Método CBasePin.CompleteConnect

El `CompleteConnect` método completa una conexión a otro pin.

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

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro pin.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Se llama a este método en ambos pines al final del proceso de conexión. El pin de conexión lo llama desde el método [**CBasePin::Conectar**](cbasepin-connect.md) y el pin receptor lo llama desde el método [**CBasePin::ReceiveConnection.**](cbasepin-receiveconnection.md)

En la clase base, este método simplemente devuelve S \_ OK. Si una clase derivada tiene algún requisito para completar una conexión, debe invalidar este método. Por ejemplo, la [**clase CBaseOutputPin**](cbaseoutputpin.md) usa este método para decidir el asignador de memoria.

Si se produce un error en este método, también se produce un error en el intento de conexión general y el pin se desconecta del pin receptor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




