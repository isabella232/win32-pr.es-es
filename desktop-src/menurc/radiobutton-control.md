---
title: RADIOBUTTON (control)
description: Define un control de botón de radio.
ms.assetid: c427080f-0408-42b4-8888-7333f3eb985d
keywords:
- Menús de controles RADIOBUTTON y otros recursos
topic_type:
- apiref
api_name:
- RADIOBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 67dd559c2d61ca8b2735d393170c177a65735b4b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077751"
---
# <a name="radiobutton-control"></a>RADIOBUTTON (control)

Define un control de botón de radio. El control es un círculo pequeño que tiene el texto especificado que se muestra junto a él, normalmente a su derecha. El control resalta el círculo y envía un mensaje a su ventana primaria cuando el usuario selecciona el botón. El control quita el resaltado y envía un mensaje cuando se selecciona el botón siguiente.

``` syntax
RADIOBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Estilos del botón de radio, que puede ser una combinación de estilos de clase de botón y los siguientes estilos: **WS \_ TABSTOP**, **WS \_ Disabled** y **WS \_ Group**.

Si no especifica un estilo, el estilo predeterminado es `BS_RADIOBUTTON | WS_TABSTOP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de la instrucción **RADIOBUTTON** :

``` syntax
RADIOBUTTON "Italic", 100, 10, 10, 40, 10
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Botones de radio](https://www.bing.com/search?q=Radio+Buttons)
</dt> </dl>

 

 