---
description: El método CompleteConnect notifica a la ventana que se ha conectado el pin de entrada del representador.
ms.assetid: 82347ded-eb37-4360-9333-7c837d532115
title: Método CBaseWindow.CompleteConnect (Winutil.h)
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
ms.openlocfilehash: 5e04e0adf1d11a4878d860dd5c8a1eea9395095c71d8b5c86d6023a24ccdb28c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119016713"
---
# <a name="cbasewindowcompleteconnect-method"></a>Método CBaseWindow.CompleteConnect

El método notifica a la ventana que el pin de entrada `CompleteConnect` del representador se ha conectado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT CompleteConnect();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve S \_ OK.

## <a name="remarks"></a>Comentarios

Este método restablece la marca de activación de ventana ([**CBaseWindow::m \_ bActivated**](cbasewindow-m-bactivated.md)) a **FALSE.** Cuando un representador de vídeo completa una conexión de pin, podría llamar al método [**CBaseWindow::ActivateWindow**](cbasewindow-activatewindow.md) para establecer el tamaño y la posición de la ventana. Para forzar **a ActivateWindow** a volver a calcular estos atributos, llame primero al `CompleteConnect` método .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Winutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseWindow (clase)**](cbasewindow.md)
</dt> </dl>

 

 




