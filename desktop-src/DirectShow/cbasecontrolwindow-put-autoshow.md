---
description: El \_ método put Autoshow establece la marca de estado de Automostrar.
ms.assetid: 857472b8-845b-46d3-8593-3fba9a9c8cdc
title: Método CBaseControlWindow.put_AutoShow (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.put_AutoShow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eda5c0c4055979537c5cc471053715e29a348f1a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105660467"
---
# <a name="cbasecontrolwindowput_autoshow-method"></a>CBaseControlWindow. put ( \_ método de Autoshow)

El `put_AutoShow` método establece la marca de estado de Automostrar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_AutoShow(
   long AutoShow
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*Automostrar* 
</dt> <dd>

Marca booleana de Automation (0 está desactivado, 1 en).

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta propiedad simplifica el acceso de visualización de la ventana para las aplicaciones. Si se establece en 1 (activado), la ventana, que normalmente se oculta después de que el filtro está conectado, se mostrará automáticamente cuando el filtro se ejecute en pausa o se ejecute. No obstante, no se debe ocultar la ventana cuando el filtro se detenga. Si se establece en 0 (desactivado), la ventana solo se hace visible cuando la aplicación llama a [**CBaseControlWindow::p UT \_ visible**](cbasecontrolwindow-put-visible.md) o [**CBaseControlWindow::p UT \_ WindowState**](cbasecontrolwindow-put-windowstate.md) con los parámetros adecuados.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




