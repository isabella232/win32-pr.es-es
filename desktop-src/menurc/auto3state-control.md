---
title: Control AUTO3STATE
description: Define una casilla de tres Estados automática.
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- Menús de control de AUTO3STATE y otros recursos
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de184a639de7beee7ac05bdf63609ae29a0f034b
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149232"
---
# <a name="auto3state-control"></a>Control AUTO3STATE

Define una casilla de tres Estados automática. El control es un cuadro abierto con el texto especificado situado a la derecha del cuadro. Cuando se elige, el cuadro avanza automáticamente entre tres Estados: activado, desactivado y deshabilitado (atenuado). El control envía un mensaje a su elemento primario cada vez que el usuario elige el control.

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Estilos para el control, que puede ser una combinación del estilo **BS \_ AUTO3STATE** y los siguientes estilos: **WS \_ TABSTOP**, **WS \_ Disabled** y **WS \_ Group**.

Si no especifica un estilo, el estilo predeterminado es `BS_AUTO3STATE | WS_TABSTOP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Autocheckbox**](autocheckbox-control.md)
</dt> <dt>

[Casillas](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**CASILLA**](checkbox-control.md)
</dt> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> <dt>

[Estilos de ventana](/windows/desktop/winmsg/window-styles)
</dt> </dl>

 

 