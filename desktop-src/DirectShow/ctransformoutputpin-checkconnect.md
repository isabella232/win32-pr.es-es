---
description: El método CheckConnect determina si una conexión de PIN es adecuada.
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: Método CTransformOutputPin. CheckConnect (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.CheckConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b9a20eb8d3e20679cb8805d3a1cd8e167ef0bfd5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680883"
---
# <a name="ctransformoutputpincheckconnect-method"></a>CTransformOutputPin. CheckConnect, método

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

Devuelve un valor **HRESULT** . Estos son algunos de los valores posibles.



| Código devuelto                                                                                  | Descripción                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>         | Correcto.<br/>                                 |
| <dl> <dt>**E \_ inesperado**</dt> </dl> | El PIN de entrada del filtro no está conectado.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método invalida el método [**CBaseOutputPin:: CheckConnect**](cbaseoutputpin-checkconnect.md) . Llama al método [**CTransformFilter:: CheckConnect**](ctransformfilter-checkconnect.md) del filtro, que devuelve s \_ OK en la clase base. La clase derivada puede invalidar el método **CTransformFilter:: CheckConnect** para realizar comprobaciones adicionales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm. h (incluir streams. h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



 

 




