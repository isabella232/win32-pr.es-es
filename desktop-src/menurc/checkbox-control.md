---
title: Control CHECKBOX (compilador de recursos)
description: Define un control de casilla.
ms.assetid: 24ee25e5-9de2-4843-a55e-96b897f6ae8e
keywords:
- Menús de control CHECKBOX y otros recursos
topic_type:
- apiref
api_name:
- CHECKBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab103291a919a166d63656718629a7781bdd5f3a4b3023283f2dd114decd966e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119461335"
---
# <a name="checkbox-control"></a>Control CHECKBOX

Define un control de casilla. El control es un rectángulo pequeño (casilla) que muestra el texto especificado junto a él (normalmente, a la derecha). Cuando el usuario selecciona el control, el control resalta el rectángulo y envía un mensaje a su ventana primaria.

La **instrucción CHECKBOX,** que solo se puede usar en una [**instrucción DIALOGEX,**](dialogex-resource.md) define el texto, el identificador, las dimensiones y los atributos del control.

``` syntax
CHECKBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Texto*
</dt> <dd>

Texto que se va a mostrar a la derecha del control.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos de control. Este valor puede ser una combinación del estilo de clase de botón **BS \_ CHECKBOX** y los estilos **\_ WS TABSTOP** y **WS \_ GROUP.**

Si no especifica un estilo, el estilo predeterminado es `BS_CHECKBOX | WS_TABSTOP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [Parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En este ejemplo se define un control de casilla con la etiqueta Cursiva:

``` syntax
CHECKBOX "Italic", 3, 10, 10, 40, 10
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**AUTOCHECKBOX**](autocheckbox-control.md)
</dt> <dt>

[**AUTO3STATE**](auto3state-control.md)
</dt> <dt>

[Casillas](https://www.bing.com/search?q=Check+Boxes)
</dt> <dt>

[**GetDialogBaseUnits**](/windows/win32/api/winuser/nf-winuser-getdialogbaseunits)
</dt> <dt>

[**STATE3**](state3-control.md)
</dt> </dl>

 

 