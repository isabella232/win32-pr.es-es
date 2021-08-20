---
title: TB_ADDBUTTONS mensaje (Commctrl.h)
description: Agrega uno o varios botones a una barra de herramientas.
ms.assetid: 65294dfc-b04b-475d-b38e-9d84c0fb000b
keywords:
- TB_ADDBUTTONS controles de Windows mensaje
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
ms.openlocfilehash: 4bd3a5a15ac1983d93ca161dae20876159e5f633cf580d485686d67889276747
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118168528"
---
# <a name="tb_addbuttons-message"></a>Mensaje \_ ADDBUTTONS de TB

Agrega uno o varios botones a una barra de herramientas.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Número de botones que se agregarán.

</dd> <dt>

*lParam* 
</dt> <dd>

Puntero a una matriz de [**estructuras TBBUTTON**](/windows/desktop/api/Commctrl/ns-commctrl-tbbutton) que contienen información sobre los botones que se agregarán. Debe haber el mismo número de elementos de la matriz que los botones especificados por *wParam*.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **TRUE si** se realiza correctamente o **FALSE** de lo contrario.

## <a name="remarks"></a>Comentarios

Si la barra de herramientas se creó mediante la función [**CreateWindowEx,**](/windows/desktop/api/winuser/nf-winuser-createwindowexa) debe enviar el mensaje [**\_ TB BUTTONSTRUCTSIZE**](tb-buttonstructsize.md) a la barra de herramientas antes de enviar **TB \_ ADDBUTTONS**.

Consulte [**TB \_ SETIMAGELIST para**](tb-setimagelist.md) obtener una explicación sobre cómo asignar mapas de bits a botones de la barra de herramientas de una o varias listas de imágenes.

## <a name="examples"></a>Ejemplos

El código de ejemplo siguiente agrega tres botones a una barra de herramientas, usando el mapa de bits del sistema estándar para los botones de vista. El [**mensaje \_ ADDBITMAP de TB**](tb-addbitmap.md) devuelve el índice de la primera imagen de botón dentro de la lista de imágenes. Las imágenes individuales se identifican por sus desplazamientos de ese valor.


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



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |
| Nombres Unicode y ANSI<br/>   | **TB \_ ADDBUTTONSW** (Unicode) y **TB \_ ADDBUTTONSA** (ANSI)<br/>               |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Valores de índice de imagen del botón Estándar de la barra de herramientas**](toolbar-standard-button-image-index-values.md)
</dt> </dl>

 

