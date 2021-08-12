---
description: El método IsAutoShowEnabled recupera información sobre si la ventana de vídeo aparece automáticamente cuando el filtro de representación se detiene o se ejecuta.
ms.assetid: 769e3023-a515-4b80-a979-2e4fa9612e65
title: Método CBaseControlWindow.IsAutoShowEnabled (Ctlutil.h)
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
ms.openlocfilehash: 81f5190d3b0634c763703a3e13aa711f097641285f49c469dab6bad6ce0d9055
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660234"
---
# <a name="cbasecontrolwindowisautoshowenabled-method"></a>Método CBaseControlWindow.IsAutoShowEnabled

El método recupera información sobre si la ventana de vídeo aparece automáticamente cuando el filtro de representación `IsAutoShowEnabled` se pausa o se ejecuta.

## <a name="syntax"></a>Sintaxis


```C++
BOOL IsAutoShowEnabled();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE** si el **miembro m \_ bAutoShow** está establecido en 1 o **FALSE** si está establecido en 0.

## <a name="remarks"></a>Observaciones

Si el **miembro m \_ bAutoShow** está establecido en 1 en una ventana de vídeo que está oculta, la ventana se vuelve visible cuando el filtro se pausa o se ejecuta. Si este miembro se establece en 0, la ventana solo aparecerá si usa la función miembro [**CBaseControlWindow::p ut \_ Visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p ut \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con los parámetros adecuados.

Esta función miembro recupera la configuración de **miembro m \_ bAutoShow** y tiene el mismo resultado que el uso del método [**IVideoWindow::get \_ AutoShow.**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




