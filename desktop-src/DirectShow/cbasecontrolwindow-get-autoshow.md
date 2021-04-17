---
description: El \_ método get Autoshow recupera la marca de estado de Automostrar actual.
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: Método CBaseControlWindow.get_AutoShow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f45679b9d036f1c5386cd2c1d18a31fa3d6bd64f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105670542"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a>CBaseControlWindow. get ( \_ método de Autoshow)

El `get_AutoShow` método recupera la marca de estado de Automostrar actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Automostrar* 
</dt> <dd>

Puntero a una marca booleana de Automation (0 es OFF, 1 es ON).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el método [**IVideoWindow:: get \_ Autoshow**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) . Esta propiedad simplifica el acceso de visualización de la ventana para las aplicaciones. Si se establece en 1 (activado), la ventana, que normalmente se oculta después de la conexión del filtro, se mostrará automáticamente cuando el filtro se ejecute en pausa o se ejecute. No obstante, no se debe ocultar la ventana cuando el filtro se detenga. Si este parámetro se establece en 0 (desactivado), la ventana solo se hace visible cuando la aplicación llama a [**CBaseControlWindow::p UT \_ visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con los parámetros adecuados.

Esta función miembro está pensada para que la llamen los objetos externos a través de la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) y, por tanto, bloquea la sección crítica para sincronizar con el filtro asociado. Llame a la función miembro [**CBaseControlWindow:: IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) para recuperar esta propiedad si no está llamando a desde un objeto externo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




