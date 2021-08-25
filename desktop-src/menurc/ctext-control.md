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
ms.openlocfilehash: a6b220448fcaa6cbbbb6b01c605a9b5fd6e03f8dc6a60a0e409f6f275d9b74b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119826005"
---
# <a name="ctext-control"></a>Control CTEXT

Define un control de texto centrado. El control es un rectángulo simple que muestra el texto dado centrado en el rectángulo. El texto tiene formato antes de mostrarse. Las palabras que se extenderían más allá del final de una línea se encapsulan automáticamente al principio de la línea siguiente. Las palabras que son más largas que el ancho del control se truncan.

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

Estilos de control. Este valor puede ser cualquier combinación de los estilos siguientes: **SS \_ CENTER**, **WS \_ TABSTOP** y **WS \_ GROUP**.

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

[**Control**](control-control.md)
</dt> <dt>

[Editar controles](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> <dt>

[**Rtext**](rtext-control.md)
</dt> </dl>

 

 