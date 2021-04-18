---
description: El método CompleteConnect notifica a la ventana que se ha conectado el PIN de entrada del representador.
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: Método CBaseWindow. CompleteConnect (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseWindow.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 15d5719ab78c3e95cd0128d4075797221af1f4c2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105679091"
---
# <a name="cbasewindowcompleteconnect-method"></a>CBaseWindow. CompleteConnect, método

El `CompleteConnect` método notifica a la ventana que el PIN de entrada del representador se ha conectado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ correcto.

## <a name="remarks"></a>Observaciones

Este método restablece la marca de activación de la ventana ([**CBaseWindow:: m \_ bActivated**](cbasewindow-m-bactivated.md)) en **false**. Cuando un representador de vídeo completa una conexión de PIN, puede llamar al método [**CBaseWindow:: ActivateWindow**](cbasewindow-activatewindow.md) para establecer el tamaño y la posición de la ventana. Para forzar que **ActivateWindow** vuelva a calcular estos atributos, primero llame al `CompleteConnect` método.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseWindow**](cbasewindow.md)
</dt> </dl>

 

 




