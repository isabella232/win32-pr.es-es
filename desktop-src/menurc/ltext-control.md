---
title: Control LTEXT
description: Define un control de texto alineado a la izquierda.
ms.assetid: ef6d7d06-3614-4b54-8a23-684d7ef65115
keywords:
- Menús de control de LTEXT y otros recursos
topic_type:
- apiref
api_name:
- LTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f253c55238a36f7f6dd43f578c5ea5862a516869
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105656355"
---
# <a name="ltext-control"></a>Control LTEXT

Define un control de texto alineado a la izquierda. El control es un rectángulo simple que muestra el texto especificado alineado a la izquierda en el rectángulo. Se aplica formato al texto antes de que se muestre. Las palabras que se extienden más allá del final de una línea se ajustan automáticamente al principio de la línea siguiente. Las palabras que superan el ancho del control se truncan.

La instrucción **LTEXT** , que solo se puede usar en una instrucción [**DIALOGEX**](dialogex-resource.md) , define el texto, el identificador, las dimensiones y los atributos del control.

``` syntax
LTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Estilos de control. Este valor puede ser cualquier combinación del estilo **de \_ RADIOBUTTON de BS** y los siguientes estilos **: SS \_ left**, **WS \_ TABSTOP** y **WS \_ Group**.

Si no especifica un estilo, el estilo predeterminado es `SS_LEFT | WS_GROUP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En este ejemplo se define un control de texto alineado a la izquierda que tiene la etiqueta nombre de archivo:

``` syntax
LTEXT "Filename", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[Controles de edición](../controls/about-edit-controls.md)
</dt> <dt>

[**RTEXT**](rtext-control.md)
</dt> </dl>

 

 