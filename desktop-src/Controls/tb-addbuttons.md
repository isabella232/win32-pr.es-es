---
title: Mensaje de TB_ADDBUTTONS (commctrl. h)
description: Agrega uno o más botones a una barra de herramientas.
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- TB_ADDBUTTONS controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TB_ADDBUTTONS
- TB_ADDBUTTONSA
- TB_ADDBUTTONSW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f954e9a133f78a9415358d1c7f61d68008cd3d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997178"
---
# <a name="tb_addbuttons-message"></a>\_Mensaje ADDBUTTONS TB

Agrega uno o más botones a una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de botones que se van a agregar.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de estructuras [**TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que contienen información sobre los botones que se van a agregar. Debe haber el mismo número de elementos en la matriz que los botones especificados por *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **true** si es correcto, o **false** en caso contrario.

## <a name="remarks"></a>Observaciones

Si la barra de herramientas se creó mediante la función [**CreateWindowEx**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) , debe enviar el mensaje de [**TB \_ BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) a la barra de herramientas antes de enviar **TB \_ ADDBUTTONS**.

Vea [**TB \_ SETIMAGELIST**](tb-setimagelist.md) para obtener una explicación de cómo asignar mapas de bits a los botones de la barra de herramientas de una o varias listas de imágenes.

## <a name="examples"></a>Ejemplos

En el ejemplo de código siguiente se agregan tres botones a una barra de herramientas, utilizando el mapa de bits estándar del sistema para botones de vista. El mensaje [**TB \_ ADDBITMAP**](tb-addbitmap.md) devuelve el índice de la primera imagen de botón en la lista de imágenes. Las imágenes individuales se identifican por sus desplazamientos a partir de ese valor.


```C++
TBADDBITMAP tbAddBitmap;
tbAddBitmap.hInst = HINST_COMMCTRL;
tbAddBitmap.nID = IDB_VIEW_SMALL_COLOR;

// There are 12 items in IDB_VIEW_SMALL_COLOR.  However, because this is a standard
// system-defined bitmap, the wParam (nButtons) is ignored.
//
// hWndToolbar is the handle of the toolbar window.
//
// Do not forget to send TB_BUTTONSTRUCTSIZE if the toolbar was created
// by using CreateWindowEx.
//
int stdidx = SendMessage(hWndToolbar, TB_ADDBITMAP, 0, (LPARAM)&tbAddBitmap);

// Define the buttons. 
// IDM_SETLARGEICONVIEW and so on are application-defined command IDs.

const int numButtons = 3;
TBBUTTON tbButtonsAdd[numButtons] = 
{
    {stdidx + VIEW_LARGEICONS, IDM_SETLARGEICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_SMALLICONS, IDM_SETSMALLICONVIEW, TBSTATE_ENABLED, BTNS_BUTTON},
    {stdidx + VIEW_DETAILS, IDM_SETDETAILSVIEW, TBSTATE_ENABLED, BTNS_BUTTON}
}; 

// Add the view buttons.
SendMessage(hWndToolbar, TB_ADDBUTTONS, numButtons, (LPARAM)tbButtonsAdd);
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TB \_ ADDBUTTONSW** (Unicode) y **TB \_ ADDBUTTONSA** (ANSI)<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Valores de índice de imagen de botón estándar de la barra de herramientas**](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

