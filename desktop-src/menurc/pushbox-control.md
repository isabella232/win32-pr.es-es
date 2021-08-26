---
title: Control PUSHBOX
description: Define un control de cuadro de inserción, que es idéntico a pushBUTTON, salvo que no muestra una cara o marco de botón; solo aparece el texto.
ms.assetid: b4e9d3f5-fcc4-40e1-90af-53d14e4638bf
keywords:
- Menús de control PUSHBOX y otros recursos
topic_type:
- apiref
api_name:
- PUSHBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06135aad813141e15bede8364a71e8fbc3016c7cb79afe0085bb6bc7bbcb2d8f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952375"
---
# <a name="pushbox-control"></a>Control PUSHBOX

Define un control de cuadro de inserción, que es idéntico a [**un PUSHBUTTON**](pushbutton-control.md), salvo que no muestra una cara de botón o marco; solo aparece el texto.

``` syntax
PUSHBOX text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos para el cuadro de inserción, que puede ser una combinación del estilo **\_ BS PUSHBOX** y los estilos siguientes: **WS \_ TABSTOP,** **WS \_ DISABLED** y **WS \_ GROUP**.

Si no especifica un estilo, el estilo predeterminado es `BS_PUSHBOX | WS_TABSTOP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [Parámetros de control comunes](common-control-parameters.md).

## <a name="see-also"></a>Vea también

<dl> <dt>

[Botones](https://www.bing.com/search?q=Push+Buttons)
</dt> <dt>

[**Pulsador**](pushbutton-control.md)
</dt> </dl>

 

 




