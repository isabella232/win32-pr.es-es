---
title: TTM_ADJUSTRECT mensaje (Commctrl.h)
description: Calcula el rectángulo de presentación de texto de un control de información sobre herramientas a partir de su rectángulo de ventana o el rectángulo de ventana de información sobre herramientas necesario para mostrar un rectángulo de presentación de texto especificado.
ms.assetid: b848c16f-9f41-4ed2-918a-9c03aebe535c
keywords:
- TTM_ADJUSTRECT controles de Windows mensaje
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165945"
---
# <a name="ttm_adjustrect-message"></a>Mensaje \_ ADJUSTRECT de TTM

Calcula el rectángulo de presentación de texto de un control de información sobre herramientas a partir de su rectángulo de ventana o el rectángulo de ventana de información sobre herramientas necesario para mostrar un rectángulo de presentación de texto especificado.

## <a name="parameters"></a>Parámetros

<dl> <dt>

*wParam* 
</dt> <dd>

Valor que especifica la operación que se va a realizar. Si **es TRUE,** *lParam* se usa para especificar un rectángulo de presentación de texto y recibe el rectángulo de ventana correspondiente. Si **es FALSE,** *lParam* se usa para especificar un rectángulo de ventana y recibe el rectángulo de presentación de texto correspondiente.

</dd> <dt>

*lParam* 
</dt> <dd>

**Estructura RECT** para contener un rectángulo de ventana de información sobre herramientas o un rectángulo de presentación de texto.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve un valor distinto de cero si el rectángulo se ajusta correctamente y devuelve cero si se produce un error.

## <a name="remarks"></a>Observaciones

Este mensaje es especialmente útil cuando se desea usar un control de información sobre herramientas para mostrar el texto completo de una cadena que normalmente se trunca. Se usa normalmente con controles listview y treeview. Normalmente, este mensaje se envía en respuesta a un código de notificación SHOW de [TTN \_ ](ttn-show.md) para que pueda colocar correctamente el control de información sobre herramientas.

El rectángulo de ventana de información sobre herramientas es algo mayor que el rectángulo de presentación de texto que delimita la cadena de información sobre herramientas. El origen de la ventana también se desplaza hacia arriba y hacia la izquierda desde el origen del rectángulo de presentación de texto. Para colocar el rectángulo de presentación de texto, debe calcular el rectángulo de ventana correspondiente y usarlo para colocar la información sobre herramientas. **TTM \_ ADJUSTRECT controla** este cálculo automáticamente.

Si establece *wParam* en **TRUE,** **TTM \_ ADJUSTRECT** toma el tamaño y la posición del rectángulo de presentación de texto de información sobre herramientas deseado y pasa de nuevo el tamaño y la posición de la ventana de información sobre herramientas necesaria para mostrar el texto en la posición especificada. Si establece *wParam* en **FALSE,** puede especificar un rectángulo de ventana de información sobre herramientas y **TTM \_ ADJUSTRECT** devolverá el tamaño y la posición de su rectángulo de texto.

En el fragmento de código siguiente se muestra el uso del mensaje **DE \_ AJUSTERECT DE LA PROPIEDAD PARA COLOCAR** UN CONTROL DE INFORMACIÓN SOBRE HERRAMIENTAS para mostrar el texto completo de la cadena de un control en lugar de una cadena truncada. La función **GetMyItemRect** definida por la aplicación devuelve el rectángulo de texto que será necesario para mostrar el texto de la información sobre herramientas directamente sobre la cadena truncada. Los detalles de cómo se implementa esta función dependerán del control determinado. **TTM \_ ADJUSTRECT se** usa para enviar este rectángulo de texto al control de información sobre herramientas. Devuelve un rectángulo de ventana con el tamaño y la posición adecuados que se usa para colocar la ventana de información sobre herramientas.


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
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                        |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Commctrl.h</dt> </dl> |



 

 





