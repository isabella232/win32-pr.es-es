---
description: 'El método Connect conecta el PIN a otro PIN. Este método implementa el método IPin:: Connect.'
ms.assetid: 8ea99d2f-09da-4b15-a3b0-04ceb7888bc1
title: Método CBasePin. Connect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Connect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ed8bcdab7e0909e59e7d9ec00645786f8ce48c02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661273"
---
# <a name="cbasepinconnect-method"></a>CBasePin. Connect (método)

El `Connect` método conecta el PIN a otro PIN. Este método implementa el método [**IPin:: Connect**](/windows/desktop/api/Strmif/nf-strmif-ipin-connect) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT Connect(
         IPin          *pReceivePin,
   const AM_MEDIA_TYPE *pmt
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pReceivePin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN receptor.

</dd> <dt>

*p.p.* 
</dt> <dd>

Puntero a una estructura de [**\_ \_ tipo de medio am**](/windows/win32/api/strmif/ns-strmif-am_media_type) que especifica el tipo de medio para la conexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los de la tabla siguiente.



| Código devuelto                                                                                                  | Descripción                                                                        |
|--------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                         | Correcto.<br/>                                                                |
| <dl> <dt>**VFW \_ E \_ ya \_ conectado**</dt> </dl>    | El PIN ya está conectado.<br/>                                           |
| <dl> <dt>**VFW \_ E \_ no \_ hay \_ tipos aceptables**</dt> </dl> | No se pudo encontrar un tipo de medio aceptable.<br/>                                |
| <dl> <dt>**VFW \_ E \_ no \_ detenido**</dt> </dl>          | El filtro está activo y el PIN no admite la reconexión dinámica.<br/> |
| <dl> <dt>**\_tipo VFW \_ E \_ no \_ aceptado**</dt> </dl>   | El tipo de medio especificado no es aceptable.<br/>                             |



 

## <a name="remarks"></a>Observaciones

El parámetro *PMT* puede ser **null**. También puede especificar un tipo de medio parcial, con un valor de GUID \_ null para el tipo, subtipo o formato principal.

En la clase base, este método comprueba si el PIN ya está conectado y si el filtro está detenido. Delega el resto del proceso de conexión al método [**CBasePin:: AgreeMediaType**](cbasepin-agreemediatype.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBasePin**](cbasepin.md)
</dt> </dl>

 

 




