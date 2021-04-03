---
title: Autocheckbox (control)
description: Define un control de casilla automática.
ms.assetid: 086f5dd3-267f-4ec6-be37-4e9402f7aede
keywords:
- Menús de control autocheckbox y otros recursos
topic_type:
- apiref
api_name:
- AUTOCHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 842bb3ede2b1f96f3e5b343e351e047d112a8403
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790318"
---
# <a name="autocheckbox-control"></a>Autocheckbox (control)

Define un control de casilla automática. El control es un rectángulo pequeño (casilla) con el texto especificado que aparece junto a él (normalmente, a la derecha). Cuando el usuario elige el control, el control resalta el rectángulo y envía un mensaje a su ventana primaria.

La instrucción **autocheckbox** solo se puede usar en el cuerpo de un [**cuadro de diálogo**](dialog-resource.md) o una instrucción [**DIALOGEX**](dialogex-resource.md) .

``` syntax
AUTOCHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Estilos del control. Este valor puede ser una combinación del estilo de clase de botón **BS \_ autocheckbox** y los estilos **WS \_ TABSTOP** y **WS \_ Group** .

Si no especifica un estilo, el estilo predeterminado es `BS_AUTOCHECKBOX | WS_TABSTOP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[**AUTO3STATE**](auto3state-control.md)
</dt> <dt>

[Estilos de botón](../controls/button-styles.md)
</dt> <dt>

[**CASILLA**](checkbox-control.md)
</dt> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> </dl>

 

 