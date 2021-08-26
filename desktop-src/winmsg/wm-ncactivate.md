---
description: Se envía a una ventana cuando es necesario cambiar su área no cliente para indicar un estado activo o inactivo.
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: WM_NCACTIVATE mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 095f0cc7f555b4daf80a67a2394e29286f32a49dcba687780e8747f5d1b193fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120056005"
---
# <a name="wm_ncactivate-message"></a>Mensaje \_ WM NCACTIVATE

Se envía a una ventana cuando es necesario cambiar su área no cliente para indicar un estado activo o inactivo.

Una ventana recibe este mensaje a través de su [**función WindowProc.**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85))


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica cuándo es necesario cambiar una barra de título o un icono para indicar un estado activo o inactivo. Si se va a dibujar una barra de título o un icono activo, el *parámetro wParam* es **TRUE.** Si se va a dibujar una barra de título o un icono inactivos, *wParam* es **FALSE.**

</dd> <dt>

*lParam* 
</dt> <dd>

Cuando un [estilo visual](../controls/themes-overview.md) está activo para esta ventana, no se usa este parámetro.

Cuando un estilo visual no está activo para esta ventana, este parámetro es un identificador de una región de actualización opcional para el área no cliente de la ventana. Si este parámetro se establece en -1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) no vuelve a dibujar el área no cliente para reflejar el cambio de estado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Cuando el *parámetro wParam* es **FALSE,** una aplicación debe devolver **TRUE** para indicar que el sistema debe continuar con el procesamiento predeterminado o debe devolver **FALSE** para evitar el cambio. Cuando *wParam es* **TRUE,** se omite el valor devuelto.

## <a name="remarks"></a>Comentarios

No se recomienda procesar mensajes relacionados con el área no cliente de una ventana estándar, ya que la aplicación debe poder dibujar todas las partes necesarias del área no cliente para la ventana. Si una aplicación procesa este mensaje, debe devolver **TRUE** para dirigir al sistema a completar el cambio de ventana activa. Si la ventana se minimiza cuando se recibe este mensaje, la aplicación debe pasar el mensaje a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dibuja la barra de título o el título del icono en sus colores activos cuando el parámetro *wParam* es **TRUE** y en sus colores inactivos cuando *wParam* es **FALSE.**

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

**Conceptual**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
