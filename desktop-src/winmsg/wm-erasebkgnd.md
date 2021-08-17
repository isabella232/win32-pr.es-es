---
description: Se envía cuando se debe borrar el fondo de la ventana (por ejemplo, cuando se cambia el tamaño de una ventana). El mensaje se envía para preparar una parte invalidada de una ventana para pintar.
ms.assetid: 3bdc37da-227c-4be1-bf0b-99704b8acbe1
title: WM_ERASEBKGND mensaje (Winuser.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c74c3b0d1dd2e31e88715d0668f53676759c27cb986b6549fe9e001ab394579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119931785"
---
# <a name="wm_erasebkgnd-message"></a>Mensaje \_ ERASEBND de WM

Se envía cuando se debe borrar el fondo de la ventana (por ejemplo, cuando se cambia el tamaño de una ventana). El mensaje se envía para preparar una parte invalidada de una ventana para pintar.


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

## <a name="remarks"></a>Comentarios

La [**función DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) borra el fondo mediante el pincel de fondo de clase especificado por el **miembro hbrBackground** de la [**estructura WNDCLASS.**](/windows/win32/api/winuser/ns-winuser-wndclassa) Si **hbrBackground** es **NULL,** la aplicación debe procesar el **mensaje \_ ERASEB RGPDND de WM** y borrar el fondo.

Una aplicación debe devolver un valor distinto de cero en respuesta a **WM \_ ERASEBLONGND** si procesa el mensaje y borra el fondo; esto indica que no se requiere ningún borrado adicional. Si la aplicación devuelve cero, la ventana permanecerá marcada para borrarse. (Normalmente, esto indica que el **miembro fErase** de la [**estructura PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct) será **TRUE).**

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

[**WNDCLASS**](/windows/win32/api/winuser/ns-winuser-wndclassa)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Iconos](../menurc/icons.md)
</dt> <dt>

**Otros recursos**
</dt> <dt>

[**BeginPaint**](/windows/win32/api/winuser/nf-winuser-beginpaint)
</dt> <dt>

[**PAINTSTRUCT**](/windows/win32/api/winuser/ns-winuser-paintstruct)
</dt> </dl>

 

 
