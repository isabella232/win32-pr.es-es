---
description: 'Método CBasePin.CheckConnect: el método CheckConnect determina si una conexión de pin es adecuada.'
ms.assetid: 511a1594-f3f8-4725-afcd-f14f3a4ebf20
title: Método CBasePin.CheckConnect (Amfilter.h)
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
ms.openlocfilehash: 314d3e1ce0e73e60ea07bb4f7270fa04f69750c7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096053"
---
# <a name="cbasepincheckconnect-method"></a>Método CBasePin.CheckConnect

El `CheckConnect` método determina si una conexión de pin es adecuada.

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

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del otro pin.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los **valores HRESULT** que se muestran en la tabla siguiente.



| Código devuelto                                                                                               | Descripción                                   |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                      | Correcto.<br/>                           |
| <dl> <dt>**VFW \_ E DIRECCIÓN NO \_ \_ VÁLIDA**</dt> </dl> | Las direcciones del pin no son compatibles.<br/> |



 

## <a name="remarks"></a>Comentarios

Se llama a este método en ambos pines al principio del proceso de conexión. El pin de conexión lo llama desde el método [**CBasePin::Connect**](cbasepin-connect.md) y el pin receptor lo llama desde el método [**CBasePin::ReceiveConnection.**](cbasepin-receiveconnection.md)

Use este método para determinar si el pin especificado por el *parámetro pPin* es adecuado para una conexión. La clase base devuelve un error si ambos pines tienen la misma dirección (entrada o ambas salidas). Las clases derivadas pueden invalidar este método para comprobar otras características del pin. Por ejemplo, la [**clase CBaseOutputPin**](cbaseoutputpin.md) consulta la chincha de entrada para su [**interfaz IMemInputPin.**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)

Si se produce un error en este método, se produce un error en la conexión y el pin llama [**al método CBasePin::BreakConnect.**](cbasepin-breakconnect.md) Use **BreakConnect** para liberar los recursos obtenidos en `CheckConnect` . Por ejemplo, si `CheckConnect` llama al **método QueryInterface,** **BreakConnect** debe liberar la interfaz .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter.h (incluir Streams.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBasePin (clase)**](cbasepin.md)
</dt> </dl>

 

 




