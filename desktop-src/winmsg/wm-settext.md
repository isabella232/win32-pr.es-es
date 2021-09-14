---
description: Establece el texto de una ventana.
ms.assetid: 1b48c309-6903-4139-bf42-e8526963e681
title: WM_SETTEXT mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c3284855d817d5207b0d7572a41774e961c0113f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127251655"
---
# <a name="wm_settext-message"></a>Mensaje \_ SETTEXT de WM

Establece el texto de una ventana.


```C++
#define WM_SETTEXT                      0x000C
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una cadena terminada en NULL que es el texto de la ventana.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

El valor devuelto es **TRUE** si se establece el texto. Es **FALSE** (para un control de edición), **LB \_ ERRSPACE** (para un cuadro de lista) o **CB \_ ERRSPACE** (para un cuadro combinado) si no hay suficiente espacio disponible para establecer el texto en el control de edición. Es CB **\_ ERR si** este mensaje se envía a un cuadro combinado sin un control de edición.

## <a name="remarks"></a>Observaciones

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) establece y muestra el texto de la ventana. Para un control de edición, el texto es el contenido del control de edición. Para un cuadro combinado, el texto es el contenido de la parte de control de edición del cuadro combinado. Para un botón, el texto es el nombre del botón. Para otras ventanas, el texto es el título de la ventana.

Este mensaje no cambia la selección actual en el cuadro de lista de un cuadro combinado. Una aplicación debe usar el mensaje [**\_ SELECTSTRING de CB**](../controls/cb-selectstring.md) para seleccionar el elemento en un cuadro de lista que coincida con el texto del control de edición.

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

[**WM \_ GETTEXT**](wm-gettext.md)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**CB \_ SELECTSTRING**](../controls/cb-selectstring.md)
</dt> </dl>

 

 
