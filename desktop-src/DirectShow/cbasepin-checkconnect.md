---
description: El método CheckConnect determina si una conexión de PIN es adecuada.
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: Método CBasePin. CheckConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 24d5c221da417fd1fc2b3f9f140536f825b2f9d9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671634"
---
# <a name="cbasepincheckconnect-method"></a>CBasePin. CheckConnect, método

El `CheckConnect` método determina si una conexión de PIN es adecuada.

## <a name="syntax"></a>Sintaxis


```C++
virtual HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro PIN.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los valores **HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                               | Descripción                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                      | Correcto.<br/>                           |
| <dl> <dt>**\_ \_ dirección no válida de VFW E \_**</dt> </dl> | Las direcciones de PIN no son compatibles.<br/> |



 

## <a name="remarks"></a>Observaciones

Se llama a este método en ambos PIN al inicio del proceso de conexión. El PIN de conexión lo llama desde dentro del método [**CBasePin:: Connect**](cbasepin-connect.md) y el PIN receptor lo llama desde dentro del método [**CBasePin:: ReceiveConnection**](cbasepin-receiveconnection.md) .

Utilice este método para determinar si el PIN especificado por el parámetro *pPin* es adecuado para una conexión. La clase base devuelve un error si ambos PIN tienen la misma dirección (tanto de entrada como de salida). Las clases derivadas pueden invalidar este método para comprobar otras características del código PIN. Por ejemplo, la clase [**CBaseOutputPin**](cbaseoutputpin.md) consulta el PIN de entrada para su interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .

Si se produce un error en este método, se produce un error en la conexión y el PIN llama al método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) . Use **BreakConnect** para liberar los recursos obtenidos en `CheckConnect` . Por ejemplo, si `CheckConnect` llama al método **QueryInterface** , **BreakConnect** debe liberar la interfaz.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




