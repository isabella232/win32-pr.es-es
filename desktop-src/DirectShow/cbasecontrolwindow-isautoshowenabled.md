---
description: El método IsAutoShowEnabled recupera información sobre si la ventana de vídeo aparece automáticamente cuando el filtro de representación se detiene o se ejecuta.
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: Método CBaseControlWindow. IsAutoShowEnabled (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.IsAutoShowEnabled
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2c4b4a894593cb3be26a1034098cd2a0cdacf926
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660737"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a>CBaseControlWindow. IsAutoShowEnabled, método

El `IsAutoShowEnabled` método recupera información sobre si la ventana de vídeo aparece automáticamente cuando el filtro de representación se detiene o se ejecuta.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si el miembro **m \_ bAutoShow** se establece en 1 o **false** si se establece en 0.

## <a name="remarks"></a>Observaciones

Si el miembro **m \_ bAutoShow** se establece en 1 en una ventana de vídeo que está oculta, la ventana se vuelve visible cuando el filtro se pausa o se ejecuta. Si este miembro se establece en 0, la ventana solo aparecerá si se usa la función miembro [**CBaseControlWindow::p UT \_ visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con los parámetros adecuados.

Esta función miembro recupera la configuración del miembro **m \_ bAutoShow** y tiene el mismo resultado que usar el método [**IVideoWindow:: get \_ Autoshow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




