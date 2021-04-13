---
title: Control PUSHBUTTON (menús y otros recursos)
description: Define un control de botón de reenvío. El control es un rectángulo de esquinas redondas que contiene el texto especificado. El texto se centra en el control. El control envía un mensaje a su elemento primario cada vez que el usuario elige el control.
ms.assetid: c5fbcfb7-1b7d-4199-acac-d11bfd899298
keywords:
- Menús de control de PULSAdores y otros recursos
topic_type:
- apiref
api_name:
- PUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9a303121b7c0eee7ac57fc369164547bd3ae6b9
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358972"
---
# <a name="pushbutton-control"></a>Control PUSHBUTTON

Define un control de botón de reenvío. El control es un rectángulo de esquinas redondas que contiene el texto especificado. El texto se centra en el control. El control envía un mensaje a su elemento primario cada vez que el usuario elige el control.

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Estilos para el Pushbutton, que puede ser una combinación del estilo **de \_ pulsador de BS** y los siguientes estilos: **WS \_ TABSTOP**, **WS \_ Disabled** y **WS \_ Group**.

Si no especifica un estilo, el estilo predeterminado es `BS_PUSHBUTTON | WS_TABSTOP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En el siguiente ejemplo se muestra el uso de la instrucción **PUSHBUTTON** :

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Botones de reenvío](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 