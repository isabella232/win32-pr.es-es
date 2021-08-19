---
title: Control LTEXT
description: Define un control de texto alineado a la izquierda.
ms.assetid: ef6d7d06-3614-4b54-8a23-684d7ef65115
keywords:
- Menús de control LTEXT y otros recursos
topic_type:
- apiref
api_name:
- LTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cdaafe752d547466267e8494743e8f0c99ccef0d0fb05b77db5dab2fa358f158
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117870279"
---
# <a name="ltext-control"></a>Control LTEXT

Define un control de texto alineado a la izquierda. El control es un rectángulo simple que muestra el texto especificado alineado a la izquierda en el rectángulo. El texto tiene formato antes de mostrarse. Las palabras que se extenderían más allá del final de una línea se encapsulan automáticamente al principio de la línea siguiente. Las palabras que son más largas que el ancho del control se truncan.

La **instrucción LTEXT,** que solo se puede usar en una instrucción [**DIALOGEX,**](dialogex-resource.md) define el texto, el identificador, las dimensiones y los atributos del control.

``` syntax
LTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos de control. Este valor puede ser cualquier combinación del estilo **\_ BS RADIOBUTTON** y los estilos siguientes: **SS \_ LEFT,** **WS \_ TABSTOP** y **WS \_ GROUP**.

Si no especifica un estilo, el estilo predeterminado es `SS_LEFT | WS_GROUP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [Parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En este ejemplo se define un control de texto alineado a la izquierda con la etiqueta Filename:

``` syntax
LTEXT "Filename", 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[Editar controles](../controls/about-edit-controls.md)
</dt> <dt>

[**Rtext**](rtext-control.md)
</dt> </dl>

 

 