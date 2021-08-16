---
description: El método GetOwnerWindow recupera el identificador de ventana propietario, m \_ hwndOwner.
ms.assetid: fa576b42-b4a7-4374-8ba4-7d21e86d9d61
title: Método CBaseControlWindow.GetOwnerWindow (Ctlutil.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseControlWindow.GetOwnerWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0cdb3073d1dd8055986b905d6e8f50967a304e5f294b0ffcaeddcd50d8c0ee33
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119432515"
---
# <a name="cbasecontrolwindowgetownerwindow-method"></a>Método CBaseControlWindow.GetOwnerWindow

El `GetOwnerWindow` método recupera el identificador de ventana propietario, m **\_ hwndOwner**.

## <a name="syntax"></a>Sintaxis


```C++
HWND GetOwnerWindow();
```



## <a name="parameters"></a>Parámetros

Este método no tiene parámetros.

## <a name="return-value"></a>Valor devuelto

Devuelve la ventana de propietario.

## <a name="remarks"></a>Comentarios

Recupera la ventana propietaria sin llamar al método de interfaz. Use esta función miembro en lugar de [**CBaseControlWindow::get \_ Owner**](cbasecontrolwindow-get-owner.md), a menos que llame a esto externamente a través del método [**IVideoWindow::get \_ Owner.**](/windows/desktop/api/Control/nf-control-ivideowindow-get_owner)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Encabezado<br/>  | <dl> <dt>Ctlutil.h (incluir Secuencias.h)</dt> </dl>                                                                                   |
| Biblioteca<br/> | <dl> <dt>Strmbase.lib (compilaciones comerciales); </dt> <dt>Strmbasd.lib (compilaciones de depuración)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**CBaseControlWindow (clase)**](cbasecontrolwindow.md)
</dt> </dl>

 

 




