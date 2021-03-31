---
title: Mensaje de TTM_ADJUSTRECT (commctrl. h)
description: Calcula el rectángulo de presentación del texto de un control ToolTip desde su rectángulo de ventana o el rectángulo de la ventana de información sobre herramientas necesario para mostrar un rectángulo de presentación de texto especificado.
ms.assetid: b848c16f-9f41-4ed2-918a-9c03aebe535c
keywords:
- TTM_ADJUSTRECT controles de mensajes de Windows
topic_type:
- apiref
api_name:
- TTM_ADJUSTRECT
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: af89374161d5e3f9d9ab6affc2b3b498a39cbf68
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996416"
---
# <a name="ttm_adjustrect-message"></a>TTM \_ ADJUSTRECT

Calcula el rectángulo de presentación del texto de un control ToolTip desde su rectángulo de ventana o el rectángulo de la ventana de información sobre herramientas necesario para mostrar un rectángulo de presentación de texto especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica la operación que se va a realizar. Si es **true**, *lParam* se usa para especificar un rectángulo de presentación de texto y recibe el rectángulo de ventana correspondiente. Si es **false**, *lParam* se usa para especificar un rectángulo de ventana y recibe el rectángulo de presentación de texto correspondiente.

</dd> <dt>

*lParam* 
</dt> <dd>

Estructura **Rect** para contener un rectángulo de la ventana de información sobre herramientas o un rectángulo de presentación de texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si el rectángulo se ajusta correctamente y devuelve cero si se produce un error.

## <a name="remarks"></a>Observaciones

Este mensaje es especialmente útil si desea utilizar un control de información sobre herramientas para mostrar el texto completo de una cadena que se suele truncar. Se suele usar con los controles ListView y TreeView. Normalmente envía este mensaje en respuesta a un [TTN \_ Mostrar](ttn-show.md) código de notificación para que pueda colocar el control de información sobre herramientas correctamente.

El rectángulo de la ventana de información sobre herramientas es algo más grande que el rectángulo de presentación de texto que delimita la cadena de información sobre herramientas. El origen de la ventana también está desplazado hacia arriba y a la izquierda desde el origen del rectángulo de presentación del texto. Para colocar el rectángulo de presentación de texto, debe calcular el rectángulo de ventana correspondiente y usar ese rectángulo para colocar la información sobre herramientas. **TTM \_ ADJUSTRECT** controla este cálculo.

Si establece *wParam* en **true**, **TTM \_ ADJUSTRECT** toma el tamaño y la posición del rectángulo de visualización del texto de información sobre herramientas deseado y devuelve el tamaño y la posición de la ventana de información sobre herramientas necesaria para mostrar el texto en la posición especificada. Si establece *wParam* en **false**, puede especificar un rectángulo de la ventana de información sobre herramientas y **TTM \_ ADJUSTRECT** devolverá el tamaño y la posición de su rectángulo de texto.

En el fragmento de código siguiente se muestra el uso del mensaje **TTM \_ ADJUSTRECT** para colocar un control ToolTip para que muestre el texto completo de la cadena de un control en lugar de una cadena truncada. La función **GetMyItemRect** definida por la aplicación devuelve el rectángulo de texto que será necesario para mostrar el texto de información sobre herramientas directamente sobre la cadena truncada. Los detalles de cómo se implementa esta función dependerán del control determinado. **TTM \_ ADJUSTRECT** se usa para enviar este rectángulo de texto al control ToolTip. Devuelve un rectángulo de ventana colocado y con el tamaño adecuado que se usa para colocar la ventana de información sobre herramientas.


```
case TTN_SHOW:

if (MyStringIsTruncated) {
    RECT rc;
    
    GetMyItemRect(&rc);
    SendMessage(hwndToolTip, TTM_ADJUSTRECT, TRUE, (LPARAM)&rc);
    SetWindowPos(hwndToolTip,
                 NULL,
                 rc.left, rc.top,
                 0, 0,
                 SWP_NOSIZE|SWP_NOZORDER|SWP_NOACTIVATE);
} 
```



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                        |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl. h</dt> </dl> |



 

 





