---
description: El método CompleteConnect completa una conexión a otro PIN.
ms.assetid: 10cbf29c-2e1a-419c-b0c0-c99f9a285810
title: Método CBasePin. CompleteConnect (Amfilter. h)
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
ms.openlocfilehash: 9068bf63d3168a8c6d9e1bca2ef709f63e80a3c0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671614"
---
# <a name="cbasepincompleteconnect-method"></a>CBasePin. CompleteConnect, método

El `CompleteConnect` método completa una conexión a otro PIN.

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

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro PIN.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Se llama a este método en ambos PIN al final del proceso de conexión. El PIN de conexión lo llama desde dentro del método [**CBasePin:: Connect**](cbasepin-connect.md) y el PIN receptor lo llama desde dentro del método [**CBasePin:: ReceiveConnection**](cbasepin-receiveconnection.md) .

En la clase base, este método simplemente devuelve S \_ correcto. Si una clase derivada tiene algún requisito para completar una conexión, debe invalidar este método. Por ejemplo, la clase [**CBaseOutputPin**](cbaseoutputpin.md) usa este método para decidir el asignador de memoria.

Si se produce un error en este método, también se produce un error en el intento de conexión general y el PIN se desconecta del PIN receptor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




