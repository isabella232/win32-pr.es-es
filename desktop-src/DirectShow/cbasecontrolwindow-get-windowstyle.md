---
description: El \_ método get WindowStyle recupera los estilos de ventana estándar.
ms.assetid: 5c204814-5c7c-47e2-95dd-86455ed77cc7
title: Método CBaseControlWindow.get_WindowStyle (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.get_WindowStyle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 91e04efac3a67c262b4eeb85948f846dbb06086a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105661203"
---
# <a name="cbasecontrolwindowget_windowstyle-method"></a>CBaseControlWindow. Get \_ estiloVentana (método)

El `get_WindowStyle` método recupera los estilos de ventana estándar.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_WindowStyle(
   long *pWindowStyle
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pWindowStyle* 
</dt> <dd>

Puntero a los estilos de ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor **HRESULT** .

## <a name="remarks"></a>Observaciones

Esta función miembro devuelve los estilos de ventana estándar, como WS \_ Child y WS \_ visible. Llama a la función miembro [**CBaseControlWindow::D ogetwindowstyle**](cbasecontrolwindow-dogetwindowstyle.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil. h (incluir streams. h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase. lib (compilaciones comerciales); </dt> <dt>Strmbasd. lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Clase CBaseControlWindow**](cbasecontrolwindow.md)
</dt> </dl>

 

 




