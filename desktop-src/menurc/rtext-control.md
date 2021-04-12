---
title: Control RTEXT
description: Define un control de texto alineado a la derecha.
ms.assetid: 66b890db-598e-4255-9d65-a21647005f8e
keywords:
- Menús de control de RTEXT y otros recursos
topic_type:
- apiref
api_name:
- RTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2bc56a870df7ebf5d2696e70573ae320220e803c
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104487710"
---
# <a name="rtext-control"></a>Control RTEXT

Define un control de texto alineado a la derecha. El control es un rectángulo simple que muestra el texto especificado alineado a la derecha en el rectángulo. Se aplica formato al texto antes de que se muestre. Las palabras que se extienden más allá del final de una línea se ajustan automáticamente al principio de la línea siguiente. Las palabras que superan el ancho del control se truncan.

La instrucción **RText** , que solo se puede usar en una instrucción [**DIALOGEX**](dialogex-resource.md) , define el texto, el identificador, las dimensiones y los atributos del control.

``` syntax
RTEXT text, id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Estilos para el control de texto, que puede ser cualquier combinación de los siguientes: **WS \_ TABSTOP** y **WS \_ Group**.

Si no especifica un estilo, el estilo predeterminado es `SS_RIGHT | WS_GROUP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de la instrucción **RText** :

``` syntax
RTEXT "Number of Messages", 4, 30, 50, 100, 10
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**CONTROL**](control-control.md)
</dt> <dt>

[**CTEXT**](ctext-control.md)
</dt> <dt>

[Controles de edición](../controls/about-edit-controls.md)
</dt> <dt>

[**LTEXT**](ltext-control.md)
</dt> </dl>

 

 