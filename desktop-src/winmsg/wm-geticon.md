---
description: Se envía a una ventana para recuperar un identificador al icono grande o pequeño asociado a una ventana. El sistema muestra el icono grande en el cuadro de diálogo ALT+TAB y el icono pequeño en el título de la ventana.
ms.assetid: d3101a9b-9658-4a21-b1f6-2920b723926c
title: WM_GETICON mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2df8922fa09cf425594a07768f0d7c9ae0ac09222647f181f45331c2b0d47fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587425"
---
# <a name="wm_geticon-message"></a>Mensaje \_ GETICON de WM

Se envía a una ventana para recuperar un identificador al icono grande o pequeño asociado a una ventana. El sistema muestra el icono grande en el cuadro de diálogo ALT+TAB y el icono pequeño en el título de la ventana.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_GETICON                      0x007F
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Tipo de icono que se va a recuperar. Este parámetro puede ser uno de los valores siguientes.



| Valor                                                                                                                                                                                                          | Significado                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="ICON_BIG"></span><span id="icon_big"></span><dl> <dt>**ICONO \_ BIG**</dt> <dt>1</dt> </dl>          | Recupere el icono grande de la ventana.<br/>                                                                                                                   |
| <span id="ICON_SMALL"></span><span id="icon_small"></span><dl> <dt>**ICONO \_ SMALL**</dt> <dt>0</dt> </dl>    | Recupere el icono pequeño de la ventana.<br/>                                                                                                                   |
| <span id="ICON_SMALL2"></span><span id="icon_small2"></span><dl> <dt>**ICONO \_ SMALL2**</dt> <dt>2</dt> </dl> | Recupera el icono pequeño proporcionado por la aplicación. Si la aplicación no proporciona una, el sistema usa el icono generado por el sistema para esa ventana.<br/> |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ppp del icono que se va a recuperar. Se puede usar para proporcionar iconos diferentes en función del tamaño del icono.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **HICON**

El valor devuelto es un identificador para el icono grande o pequeño, dependiendo del valor de *wParam*. Cuando una aplicación recibe este mensaje, puede devolver un identificador a un icono grande o pequeño, o pasar el mensaje a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

## <a name="remarks"></a>Comentarios

Cuando una aplicación recibe este mensaje, puede devolver un identificador a un icono grande o pequeño, o pasar el mensaje a [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca).

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devuelve un identificador al icono grande o pequeño asociado a la ventana, en función del valor de *wParam*.

Una ventana que no tiene ningún icono establecido explícitamente (con WM SETICON) usa el icono para la clase de ventana registrada y, en este [**caso, DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) devolverá 0 para un mensaje **WM \_ GETICON.** **\_** Si el envío **de un mensaje WM \_ GETICON** a una ventana devuelve 0, intente llamar a la función [**GetClassLongPtr**](/windows/win32/api/winuser/nf-winuser-getclasslongptra) para la ventana. Si devuelve 0, pruebe la [**función LoadIcon.**](/windows/win32/api/winuser/nf-winuser-loadicona)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**WM \_ SETICON**](wm-seticon.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
