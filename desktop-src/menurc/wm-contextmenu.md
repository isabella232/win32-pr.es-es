---
title: Mensaje de WM_CONTEXTMENU (Winuser. h)
description: Notifica a una ventana que el usuario hizo clic con el botón secundario del mouse en la ventana.
ms.assetid: e607a61a-0f9b-4d11-b8c0-b01a2e7fb35b
keywords:
- WM_CONTEXTMENU menús de mensajes y otros recursos
topic_type:
- apiref
api_name:
- WM_CONTEXTMENU
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ff7764926709bfc8ab6aa95be330a9d45d38bc48
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105714573"
---
# <a name="wm_contextmenu-message"></a>Mensaje de CONTEXTMENU de WM \_

Notifica a una ventana que el usuario desea que aparezca un menú contextual.  Es posible que el usuario haya hecho clic con el botón secundario del mouse en la ventana, presionó Mayús + F10 o presionó la tecla aplicaciones (tecla del menú contextual) disponible en algunos teclados.


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana en la que el usuario hizo clic con el botón secundario del mouse. Puede tratarse de una ventana secundaria de la ventana que recibe el mensaje. Para obtener más información sobre el procesamiento de este mensaje, consulte la sección Comentarios.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden inferior especifica la posición horizontal del cursor, en coordenadas de la pantalla, en el momento del clic del mouse.

La palabra de orden superior especifica la posición vertical del cursor, en coordenadas de pantalla, en el momento del clic del mouse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Una ventana puede procesar este mensaje mostrando un menú contextual mediante las funciones [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) o [**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) . Para obtener las posiciones horizontal y vertical, use el código siguiente.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Si una ventana no muestra un menú contextual, debe pasar este mensaje a la función [**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) . Si una ventana es una ventana secundaria, **DefWindowProc** envía el mensaje al elemento primario. De lo contrario, **DefWindowProc** muestra un menú contextual predeterminado si la posición especificada está en el título de la ventana.

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) genera el mensaje de **\_ CONTEXTMENU de WM** cuando procesa el mensaje de [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) o [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) o cuando el usuario escribe Mayús + F10. El mensaje de **\_ CONTEXTMENU de WM** también se genera cuando el usuario presiona y libera la clave de [**\_ aplicaciones VK**](/windows/desktop/inputdev/virtual-key-codes) .

Si el menú contextual se genera desde el teclado, por ejemplo, si el usuario escribe Mayús + F10, las coordenadas x e y son-1 y la aplicación debe mostrar el menú contextual en la ubicación de la selección actual en lugar de en (xPos, yPos).

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

[**OBTENER \_ X \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**OBTENER \_ \_ lParam**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[**NCRBUTTONUP de WM \_**](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[**RBUTTONUP de WM \_**](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

**Vista**
</dt> <dt>

[Menús](menus.md)
</dt> </dl>

 

