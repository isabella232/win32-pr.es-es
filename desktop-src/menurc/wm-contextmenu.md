---
title: WM_CONTEXTMENU mensaje (Winuser.h)
description: Notifica a una ventana que el usuario hizo clic con el botón derecho del mouse (clic con el botón derecho) en la ventana.
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
ms.openlocfilehash: 0c036bf0711f208bae25657d572102a7f4d82525076ee1d0b6f4ebd6598e8197
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118472510"
---
# <a name="wm_contextmenu-message"></a>Mensaje \_ CONTEXTMENU de WM

Notifica a una ventana que el usuario desea que aparezca un menú contextual.  Es posible que el usuario haya hecho clic con el botón derecho del mouse (clic con el botón derecho) en la ventana, presionado Mayús+F10 o presionado la tecla de aplicaciones (tecla de menú contextual) disponible en algunos teclados.


```C++
#define WM_CONTEXTMENU                  0x007B
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Identificador de la ventana en la que el usuario hizo clic con el botón derecho en el mouse. Puede ser una ventana secundaria de la ventana que recibe el mensaje. Para obtener más información sobre el procesamiento de este mensaje, vea la sección Comentarios.

</dd> <dt>

*lParam* 
</dt> <dd>

La palabra de orden bajo especifica la posición horizontal del cursor, en coordenadas de pantalla, en el momento del clic del mouse.

La palabra de orden superior especifica la posición vertical del cursor, en coordenadas de pantalla, en el momento del clic del mouse.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

No de devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Una ventana puede procesar este mensaje mostrando un menú contextual mediante las funciones [**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu) o [**TrackPopupMenuEx.**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex) Para obtener las posiciones horizontales y verticales, use el código siguiente.


```
xPos = GET_X_LPARAM(lParam); 
yPos = GET_Y_LPARAM(lParam); 
```



Si una ventana no muestra un menú contextual, debe pasar este mensaje a la [**función DefWindowProc.**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) Si una ventana es una ventana secundaria, **DefWindowProc** envía el mensaje al elemento primario. De lo contrario, **DefWindowProc muestra** un menú contextual predeterminado si la posición especificada está en el título de la ventana.

[**DefWindowProc genera**](/windows/desktop/api/winuser/nf-winuser-defwindowproca) el mensaje **\_ CONTEXTMENU** de WM cuando procesa el mensaje [**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup) o [**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup) o cuando el usuario tipos MAYÚS+F10. El **mensaje \_ CONTEXTMENU de WM** también se genera cuando el usuario presiona y suelta la tecla [**VK \_ APPS.**](/windows/desktop/inputdev/virtual-key-codes)

Si el menú contextual se genera desde el teclado, por ejemplo, si el usuario tipos MAYÚS+F10, las coordenadas x e y son -1 y la aplicación debe mostrar el menú contextual en la ubicación de la selección actual en lugar de en (xPos, yPos).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Professional<br/>                                               |
| Servidor mínimo compatible<br/> | \[Solo aplicaciones de escritorio\] de Windows 2000 Server<br/>                                                     |
| Encabezado<br/>                   | <dl> <dt>Winuser.h (incluir Windows.h)</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

**Referencia**
</dt> <dt>

[**DefWindowProc**](/windows/desktop/api/winuser/nf-winuser-defwindowproca)
</dt> <dt>

[**GET \_ X \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_x_lparam)
</dt> <dt>

[**GET \_ Y \_ LPARAM**](/windows/desktop/api/windowsx/nf-windowsx-get_y_lparam)
</dt> <dt>

[**TrackPopupMenu**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenu)
</dt> <dt>

[**TrackPopupMenuEx**](/windows/desktop/api/Winuser/nf-winuser-trackpopupmenuex)
</dt> <dt>

[**WM \_ NCRBUTTONUP**](/windows/desktop/inputdev/wm-ncrbuttonup)
</dt> <dt>

[**WM \_ RBUTTONUP**](/windows/desktop/inputdev/wm-rbuttonup)
</dt> <dt>

**Conceptual**
</dt> <dt>

[Menús](menus.md)
</dt> </dl>

 

