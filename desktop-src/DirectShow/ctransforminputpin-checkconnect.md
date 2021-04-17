---
description: El método CheckConnect determina si una conexión de PIN es adecuada.
ms.assetid: b8ace40d-31f5-49b0-a4cd-6ece0f883d96
title: Método CTransformInputPin. CheckConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e10c174a4e295576cfa9ce902faeac889f5a6a9b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660688"
---
# <a name="ctransforminputpincheckconnect-method"></a>CTransformInputPin. CheckConnect, método

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

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del terminal de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** . Entre los valores posibles se incluyen los que se muestran en la tabla siguiente.



| Código devuelto                                                                                               | Descripción                    |
|-----------------------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                      | Correcto<br/>             |
| <dl> <dt>**\_ \_ dirección no válida de VFW E \_**</dt> </dl> | Dirección de PIN incorrecta<br/> |



 

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) . Llama al método [**CTransformFilter:: CheckConnect**](ctransformfilter-checkconnect.md) del filtro, que devuelve s \_ OK en la clase base. La clase derivada puede invalidar el método **CTransformFilter:: CheckConnect** para realizar comprobaciones adicionales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




