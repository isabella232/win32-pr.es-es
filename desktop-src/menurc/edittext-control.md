---
title: Control EDITTEXT
description: Define un control de edición que pertenece a la clase EDIT.
ms.assetid: 9dc4be90-9503-4c97-813d-db246869ba3c
keywords:
- Menús de control EDITTEXT y otros recursos
topic_type:
- apiref
api_name:
- EDITTEXT
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 511cff6791703b30ec975625e0cd5cb044f4f492
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127252422"
---
# <a name="edittext-control"></a>Control EDITTEXT

Define un control de edición que pertenece a la clase EDIT. Crea una región rectangular en la que el usuario puede escribir y editar texto. El control muestra un cursor cuando el usuario hace clic en el mouse en él. A continuación, el usuario puede usar el teclado para escribir texto o editar el texto existente. Las claves de edición incluyen las claves BACKSPACE y DELETE. El usuario también puede usar el mouse para seleccionar los caracteres que se eliminarán o para seleccionar el lugar donde se insertarán nuevos caracteres.

``` syntax
EDITTEXT id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos de control. Este valor puede ser una combinación de los estilos de clase de edición y los estilos siguientes: **WS \_ TABSTOP,** **WS \_ GROUP,** **WS \_ VSCROLL,** **WS \_ HSCROLL** y **WS \_ DISABLED.**

Si no especifica un estilo, el estilo predeterminado es `ES_LEFT | WS_BORDER | WS_TABSTOP` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [Parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En el ejemplo siguiente se muestra el uso de la **instrucción EDITTEXT:**

``` syntax
EDITTEXT  3, 10, 10, 100, 10
```

## <a name="see-also"></a>Consulte también

<dl> <dt>

[Editar controles](../controls/about-edit-controls.md)
</dt> </dl>

 

 