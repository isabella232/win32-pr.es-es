---
title: Control CTEXT
description: Define un control de texto centrado.
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- Menús de control de CTEXT y otros recursos
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c12b6c1da5d5bd5c8ce59a01e21b05baf77503
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149230"
---
# <a name="ctext-control"></a>Control CTEXT

Define un control de texto centrado. El control es un rectángulo simple que muestra el texto especificado centrado en el rectángulo. Se aplica formato al texto antes de que se muestre. Las palabras que se extienden más allá del final de una línea se ajustan automáticamente al principio de la línea siguiente. Las palabras que superan el ancho del control se truncan.

La instrucción [**LTEXT**](ltext-control.md) , que solo se puede usar en una instrucción REP, define el texto, el identificador, las dimensiones y los atributos del control.

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*negrita*
</dt> <dd>

Texto que se va a centrar en el área rectangular del control.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Estilos de control. Este valor puede ser cualquier combinación de los siguientes estilos: **SS \_ Center**, **WS \_ TABSTOP** y **WS \_ Group**.

Si no especifica un estilo, el estilo predeterminado es `SS_CENTER | WS_GROUP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En este ejemplo se define un control de texto centrado con la etiqueta nombre de archivo:

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[Controles de edición](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> <dt>

[**RTEXT**](rtext-control.md)
</dt> </dl>

 

 