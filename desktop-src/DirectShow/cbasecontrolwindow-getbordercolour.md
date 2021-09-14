---
description: El método GetBorderColour recupera el color del borde de la ventana actual, m \_ BorderColour.
ms.assetid: 5cd9b834-5438-475e-9671-ee9917f9a485
title: Método CBaseControlWindow.GetBorderColour (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetBorderColour
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0ba6e1be9babf96d03235c49d9cde0f11cae1b83
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974006"
---
# <a name="cbasecontrolwindowgetbordercolour-method"></a>Método CBaseControlWindow.GetBorderColour

El `GetBorderColour` método recupera el color del borde de la ventana actual, **m \_ BorderColour**.

## <a name="syntax"></a>Sintaxis


```C++
COLORREF GetBorderColour();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve el color del borde.

## <a name="remarks"></a>Observaciones

Una aplicación puede establecer un rectángulo de destino para mostrar el vídeo. Este rectángulo debe ser relativo al área de cliente de la ventana. Si esto se hace (el valor predeterminado es pintar siempre toda la ventana), hay un área que rodea el vídeo; es decir, el borde. El color del borde se puede establecer a través de la función miembro [**CBaseControlWindow::p ut \_ BorderColor.**](cbasecontrolwindow-put-bordercolor.md) Esta propiedad afecta al color del borde. Use esta función miembro en lugar de [**CBaseControlWindow::get \_ BorderColor**](cbasecontrolwindow-get-bordercolor.md), a menos que llame a esto externamente a través del método [**IVideoWindow::get \_ BorderColor.**](/windows/desktop/api/Control/nf-control-ivideowindow-get_bordercolor)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




