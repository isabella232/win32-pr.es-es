---
description: El método get AutoShow recupera la marca de estado \_ actual de AutoShow.
ms.assetid: b27651d1-3ac5-4a52-9549-b63bacda5dc8
title: CBaseControlWindow.get_AutoShow método (Ctlutil.h)
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126974039"
---
# <a name="cbasecontrolwindowget_autoshow-method"></a>CBaseControlWindow.get \_ AutoShow (método)

El `get_AutoShow` método recupera la marca de estado AutoShow actual.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_AutoShow(
   long *AutoShow
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Autoshow* 
</dt> <dd>

Puntero a una marca booleana de Automation (0 está desactivado, 1 está en).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

Esta función miembro implementa el [**método IVideoWindow::get \_ AutoShow.**](/windows/desktop/api/Control/nf-control-ivideowindow-get_autoshow) Esta propiedad simplifica el acceso de visualización de ventana para las aplicaciones. Si se establece en 1 (en), la ventana, que normalmente se oculta después de la conexión del filtro, se mostrará automáticamente cuando el filtro se detenga o se ejecute. Sin embargo, la ventana no debe ocultarse cuando se detiene el filtro. Si este parámetro se establece en 0 (desactivado), la ventana se hace visible solo cuando la aplicación llama [**a CBaseControlWindow::p ut \_ Visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p ut \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con los parámetros adecuados.

Esta función miembro está pensada para que la llamen objetos externos a través de la interfaz [**IVideoWindow**](/windows/desktop/api/Control/nn-control-ivideowindow) y, por tanto, bloquea la sección crítica para sincronizarse con el filtro asociado. Llame a la función miembro [**CBaseControlWindow::IsAutoShowEnabled**](cbasecontrolwindow-isautoshowenabled.md) para recuperar esta propiedad si no llama a desde un objeto externo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




