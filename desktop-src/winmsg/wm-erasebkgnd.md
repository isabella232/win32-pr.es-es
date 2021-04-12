---
description: Se envía cuando se debe borrar el fondo de la ventana (por ejemplo, cuando se cambia el tamaño de una ventana). El mensaje se envía para preparar una parte invalidada de una ventana para su dibujo.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: Mensaje de WM_ERASEBKGND (Winuser. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7dccde6ab4efa8a6589fe7d422dd9e1c04e425f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277765"
---
# <a name="wm_erasebkgnd-message"></a>Mensaje de ERASEBKGND de WM \_

Se envía cuando se debe borrar el fondo de la ventana (por ejemplo, cuando se cambia el tamaño de una ventana). El mensaje se envía para preparar una parte invalidada de una ventana para su dibujo.


```C++
#define WM_ERASEBKGND                   0x0014
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador del contexto del dispositivo.

</dd> <dt>

*lParam* 
</dt> <dd>

Este parámetro no se utiliza.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Tipo: **LRESULT**

Una aplicación debe devolver un valor distinto de cero si borra el fondo; de lo contrario, debe devolver cero.

## <a name="remarks"></a>Observaciones

La función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) borra el fondo mediante el pincel de fondo de clase especificado por el miembro **hbrBackground** de la estructura [**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa) . Si **hbrBackground** es **null**, la aplicación debe procesar el mensaje de **\_ ERASEBKGND de WM** y borrar el fondo.

Una aplicación debe devolver un valor distinto de cero en respuesta a **WM \_ ERASEBKGND** si procesa el mensaje y borra el fondo; esto indica que no es necesario borrar más. Si la aplicación devuelve cero, la ventana permanecerá marcada para borrarse. (Normalmente, esto indica que el miembro **fErase** de la estructura [**paintstruct (**](/windows/win32/api/winuser/ns-winuser-paintstruct) será **true**).

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

[**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)
</dt> <dt>

**Vista**
</dt> <dt>

[Iconos](../menurc/icons.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[**PAINTSTRUCT (**](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
