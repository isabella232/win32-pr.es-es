---
description: El método CheckConnect determina si una conexión de PIN es adecuada.
ms.assetid: 50ab59ad-8ff7-4d7b-add3-b59203d93307
title: Método CBaseOutputPin. CheckConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3274e47e9a77d86f350c17aaca04ec0cdb95ef3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660798"
---
# <a name="cbaseoutputpincheckconnect-method"></a>CBaseOutputPin. CheckConnect, método

El `CheckConnect` método determina si una conexión de PIN es adecuada.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CheckConnect(
   IPin *pPin
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pPin* 
</dt> <dd>

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del PIN de entrada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve uno de los siguientes valores **HRESULT** .



| Código devuelto                                                                                               | Descripción                                                                 |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                      | Correcto.<br/>                                                         |
| <dl> <dt>**E \_ NOinterface**</dt> </dl>             | El PIN de entrada no es compatible con [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin).<br/> |
| <dl> <dt>**\_ \_ dirección no válida de VFW E \_**</dt> </dl> | Las direcciones de PIN no son compatibles.<br/>                               |



 

## <a name="remarks"></a>Observaciones

Este método llama al método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) de la clase base y, a continuación, consulta el PIN de entrada para su interfaz [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Amfilter. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseOutputPin**](cbaseoutputpin.md)
</dt> </dl>

 

 




