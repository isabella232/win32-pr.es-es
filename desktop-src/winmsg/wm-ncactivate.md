---
description: Se envía a una ventana cuando se debe cambiar su área no cliente para indicar un estado activo o inactivo.
ms.assetid: d25732b9-b9ab-4754-a4cf-002d32e3945e
title: Mensaje de WM_NCACTIVATE (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6a23cc5e0495d6679efea805eab80290b209906d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677917"
---
# <a name="wm_ncactivate-message"></a>Mensaje de NCACTIVATE de WM \_

Se envía a una ventana cuando se debe cambiar su área no cliente para indicar un estado activo o inactivo.

Una ventana recibe este mensaje a través de su función [**WindowProc**](/previous-versions/windows/desktop/legacy/ms633573(v=vs.85)) .


```C++
#define WM_NCACTIVATE                   0x0086
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Indica cuándo es necesario cambiar una barra de título o un icono para indicar un estado activo o inactivo. Si se va a dibujar una barra de título o un icono activo, el parámetro *wParam* es **true**. Si se va a dibujar una barra de título o un icono inactivo, *wParam* es **false**.

</dd> <dt>

*lParam* 
</dt> <dd>

Cuando hay un [estilo visual](../controls/themes-overview.md) activo para esta ventana, no se utiliza este parámetro.

Cuando no hay ningún estilo visual activo para esta ventana, este parámetro es un identificador de una región de actualización opcional para el área no cliente de la ventana. Si este parámetro se establece en-1, [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) no vuelve a dibujar el área no cliente para reflejar el cambio de estado.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Cuando el parámetro *wParam* es **false**, una aplicación debe devolver **true** para indicar que el sistema debe continuar con el procesamiento predeterminado, o bien debe devolver **false** para evitar el cambio. Cuando *wParam* es **true**, se omite el valor devuelto.

## <a name="remarks"></a>Observaciones

No se recomienda el procesamiento de mensajes relacionados con el área no cliente de una ventana estándar, ya que la aplicación debe ser capaz de dibujar todas las partes necesarias del área no cliente de la ventana. Si una aplicación procesa este mensaje, debe devolver **true** para indicar al sistema que complete el cambio de la ventana activa. Si se minimiza la ventana cuando se recibe este mensaje, la aplicación debe pasar el mensaje a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) .

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) dibuja el título de la barra de título o el icono en sus colores activos cuando el parámetro *wParam* es **true** y en sus colores inactivos cuando *wParam* es **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser. h (incluir Windows. h)</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

**Vista**
</dt> <dt>

[Windows](windows.md)
</dt> </dl>

 

 
