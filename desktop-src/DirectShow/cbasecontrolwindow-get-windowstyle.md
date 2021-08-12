---
description: El método get \_ WindowStyle recupera los estilos de ventana estándar.
ms.assetid: 5c204814-5c7c-47e2-95dd-86455ed77cc7
title: CBaseControlWindow.get_WindowStyle método (Ctlutil.h)
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
ms.openlocfilehash: e9356b449adbb4ee760ec70990c4db0b6703c16e9d0970f2756bac23907b1bfb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118660264"
---
# <a name="cbasecontrolwindowget_windowstyle-method"></a>CBaseControlWindow.get \_ (método WindowStyle)

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

Puntero a estilos de ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un **valor HRESULT.**

## <a name="remarks"></a>Observaciones

Esta función miembro devuelve los estilos de ventana estándar, como WS \_ CHILD y WS \_ VISIBLE. Llama a la [**función miembro CBaseControlWindow::D oGetWindowStyle.**](cbasecontrolwindow-dogetwindowstyle.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




