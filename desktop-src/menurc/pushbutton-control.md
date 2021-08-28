---
title: Control PUSHBUTTON (menús y otros recursos)
description: Define un control de botón de inserción. El control es un rectángulo de esquinas redondeadas que contiene el texto especificado. El texto se centra en el control . El control envía un mensaje a su elemento primario cada vez que el usuario elige el control.
ms.assetid: c5fbcfb7-1b7d-4199-acac-d11bfd899298
keywords:
- Menús de control PUSHBUTTON y otros recursos
topic_type:
- apiref
api_name:
- PUSHBUTTON
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 24db89c986f3f6d466f1710bc18420f9da9eec3348eada10e95582a882fe25e9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119777005"
---
# <a name="pushbutton-control"></a>Control PUSHBUTTON

Define un control de botón de inserción. El control es un rectángulo de esquinas redondeadas que contiene el texto especificado. El texto se centra en el control . El control envía un mensaje a su elemento primario cada vez que el usuario elige el control.

``` syntax
PUSHBUTTON text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos para el botón de inserción, que puede ser una combinación del estilo **\_ PUSHBUTTON** de BS y los estilos siguientes: **WS \_ TABSTOP,** **WS \_ DISABLED** y **WS \_ GROUP**.

Si no especifica un estilo, el estilo predeterminado es `BS_PUSHBUTTON | WS_TABSTOP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [Parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de la **instrucción PUSHBUTTON:**

``` syntax
PUSHBUTTON "ON", 7, 10, 10, 20, 10
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[Botones](https://www.bing.com/search?q=Push+Buttons)
</dt> </dl>

 

 