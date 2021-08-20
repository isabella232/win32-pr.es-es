---
title: Control RTEXT
description: Define un control de texto alineado a la derecha.
ms.assetid: 66b890db-598e-4255-9d65-a21647005f8e
keywords:
- Menús del control RTEXT y otros recursos
topic_type:
- apiref
api_name:
- RTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d0fa44cb1584195518ad39f27fbe7cd802cccc193086ebaf225ce18019b093d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117687068"
---
# <a name="rtext-control"></a>Control RTEXT

Define un control de texto alineado a la derecha. El control es un rectángulo simple que muestra el texto especificado alineado a la derecha en el rectángulo. El texto tiene formato antes de que se muestre. Las palabras que se extenderían más allá del final de una línea se encapsulan automáticamente al principio de la línea siguiente. Las palabras que son más largas que el ancho del control se truncan.

La **instrucción RTEXT,** que solo se puede usar en una [**instrucción DIALOGEX,**](dialogex-resource.md) define el texto, el identificador, las dimensiones y los atributos del control.

``` syntax
RTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos para el control de texto, que puede ser cualquier combinación de lo siguiente: **WS \_ TABSTOP** y **WS \_ GROUP**.

Si no especifica un estilo, el estilo predeterminado es `SS_RIGHT | WS_GROUP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [Parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de la **instrucción RTEXT:**

``` syntax
RTEXT "Number of Messages", 4, 30, 50, 100, 10
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Control**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[Editar controles](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> </dl>

 

 