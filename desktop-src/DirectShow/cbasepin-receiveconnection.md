---
description: 'El método ReceiveConnection acepta una conexión desde otro PIN. Este método implementa el método IPin:: ReceiveConnection.'
ms.assetid: f17e7d93-ac45-4b8a-98c6-0c76ec7117c9
title: Método CBasePin. ReceiveConnection (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.ReceiveConnection
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d0a8134201af1d3c931121f59a20360020a53a0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660945"
---
# <a name="cbasepinreceiveconnection-method"></a>CBasePin. ReceiveConnection, método

El `ReceiveConnection` método acepta una conexión desde otro PIN. Este método implementa el método [**IPin:: ReceiveConnection**](/windows/desktop/api/Strmif/nf-strmif-ipin-receiveconnection) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT ReceiveConnection(
   IPin          *pConnector,
   AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pConnector* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN de conexión.

</dd> <dt>

*p.p.* 
</dt> <dd>

Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los de la tabla siguiente.



| Código devuelto                                                                                                | Descripción                                                                        |
|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | Correcto.<br/>                                                                |
| <dl> <dt>**\_puntero E**</dt> </dl>                  | Argumento de puntero **nulo** .<br/>                                              |
| <dl> <dt>**VFW \_ E \_ ya \_ conectado**</dt> </dl>  | El PIN ya está conectado.<br/>                                           |
| <dl> <dt>**VFW \_ E \_ no \_ detenido**</dt> </dl>        | El filtro está activo y el PIN no admite la reconexión dinámica.<br/> |
| <dl> <dt>**\_tipo VFW \_ E \_ no \_ aceptado**</dt> </dl> | El tipo de medio especificado no es aceptable.<br/>                             |



 

## <a name="remarks"></a>Observaciones

El PIN de salida llama a este método en el PIN de entrada. Si el PIN de entrada devuelve un código de error, se produce un error en la conexión.

En la clase base, este método realiza los pasos siguientes:

-   Comprueba si el PIN ya está conectado.
-   Comprueba si el filtro está detenido.
-   Llama al método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) para probar si el PIN de conexión es adecuado.
-   Llama al método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) para comprobar si el tipo de medio es aceptable.

Si todos estos pasos se realizan correctamente, el método llama a los métodos [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) y [**SetMediaType**](cbasepin-setmediatype.md) para completar la conexión. Estos métodos almacenan el tipo de medio y un puntero al terminal de salida.

Si se produce un error en **CheckConnect** o **CheckMediaType** , la clase base llama al método [**CBasePin:: BreakConnect**](cbasepin-breakconnect.md) para interrumpir la conexión y, a continuación, devuelve un código de error de `ReceiveConnection` .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




