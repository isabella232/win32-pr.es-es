---
description: 'Método CTransformOutputPin.CheckConnect: el método CheckConnect determina si una conexión de pin es adecuada.'
ms.assetid: 3dae5c6d-720e-4445-b601-3bdfe32f4c21
title: Método CTransformOutputPin.CheckConnect (Transfrm.h)
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
ms.openlocfilehash: 190acd2fbab5206b114b57719d350e3ad5eac0c2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127255392"
---
# <a name="ctransformoutputpincheckconnect-method"></a>Método CTransformOutputPin.CheckConnect

El `CheckConnect` método determina si una conexión de pin es adecuada.

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

Puntero a la interfaz [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) del pin de salida.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.** Estos son algunos de los valores posibles.



| Código devuelto                                                                                  | Descripción                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>         | Correcto.<br/>                                 |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl> | El pin de entrada del filtro no está conectado.<br/> |



 

## <a name="remarks"></a>Observaciones

Este método invalida el [**método CBaseOutputPin::CheckConnect.**](cbaseoutputpin-checkconnect.md) Llama al método [**CTransformFilter::CheckConnect**](ctransformfilter-checkconnect.md) del filtro, que devuelve S \_ OK en la clase base. La clase derivada puede invalidar el **método CTransformFilter::CheckConnect** para realizar comprobaciones adicionales.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Transfrm.h (incluir Secuencias.h)</dt> </dl>                                                                                  |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



 

 




