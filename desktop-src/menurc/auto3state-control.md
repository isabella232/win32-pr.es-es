---
title: Auto3STATE (control)
description: Define una casilla automática de tres estados.
ms.assetid: 8b27367c-30d0-4591-93d0-756c65255b26
keywords:
- Menús de control AUTO3STATE y otros recursos
topic_type:
- apiref
api_name:
- AUTO3STATE
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de184a639de7beee7ac05bdf63609ae29a0f034b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127468573"
---
# <a name="auto3state-control"></a>Auto3STATE (control)

Define una casilla automática de tres estados. El control es un cuadro abierto con el texto especificado situado a la derecha del cuadro. Cuando se elige, el cuadro avanza automáticamente entre tres estados: activado, desactivado y deshabilitado (atenuado). El control envía un mensaje a su elemento primario cada vez que el usuario elige el control.

``` syntax
AUTO3STATE text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos para el control , que puede ser una combinación del estilo **\_ AUTO3STATE** de BS y los estilos siguientes: **WS \_ TABSTOP,** **WS \_ DISABLED** y **WS \_ GROUP**.

Si no especifica un estilo, el estilo predeterminado es `BS_AUTO3STATE | WS_TABSTOP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [Parámetros de control comunes](common-control-parameters.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**AUTOCHECKBOX**](autocheckbox-control.md)
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

 

 