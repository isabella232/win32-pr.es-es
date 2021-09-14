---
title: Control CTEXT
description: Define un control de texto centrado.
ms.assetid: 11f42d25-8fe1-4a8b-a5c5-c8cb47cc8c73
keywords:
- Menús de control CTEXT y otros recursos
topic_type:
- apiref
api_name:
- CTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41c12b6c1da5d5bd5c8ce59a01e21b05baf77503
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127248474"
---
# <a name="ctext-control"></a>Control CTEXT

Define un control de texto centrado. El control es un rectángulo simple que muestra el texto dado centrado en el rectángulo. El texto tiene formato antes de que se muestre. Las palabras que se extenderían más allá del final de una línea se encapsulan automáticamente al principio de la línea siguiente. Las palabras que son más largas que el ancho del control se truncan.

La [**instrucción LTEXT,**](ltext-control.md) que solo se puede usar en una instrucción rep, define el texto, el identificador, las dimensiones y los atributos del control.

``` syntax
CTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="text"></span><span id="TEXT"></span>*Texto*
</dt> <dd>

Texto que se va a centrar en el área rectangular del control.

</dd> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos de control. Este valor puede ser cualquier combinación de los estilos **\_ siguientes:** **SS \_ CENTER,** **WS \_ TABSTOP** y WS GROUP .

Si no especifica un estilo, el estilo predeterminado es `SS_CENTER | WS_GROUP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [Parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En este ejemplo se define un control de texto centrado con la etiqueta Filename:

``` syntax
CTEXT "Filename", 101, 10, 10, 100, 100 
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[Editar controles](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> <dt>

[**RTEXT**](rtext-control.md)
</dt> </dl>

 

 