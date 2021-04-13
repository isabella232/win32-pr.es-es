---
title: Control COMBOBOX (menús y otros recursos)
description: Define un control de cuadro combinado (un cuadro combinado).
ms.assetid: 0a0fcfa8-b65c-44c1-89d8-f5020af10f0f
keywords:
- Menús de control COMBOBOX y otros recursos
topic_type:
- apiref
api_name:
- COMBOBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 311cb45282b949a166add8d3aececc0698803fe5
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104420606"
---
# <a name="combobox-control"></a>COMBOBOX (control)

Define un control de cuadro combinado (un cuadro combinado). Un cuadro combinado consta de un cuadro de texto estático o un cuadro de edición combinado con un cuadro de lista. El cuadro de lista se puede mostrar en todo momento o extraerlo el usuario. Si el cuadro combinado contiene un cuadro de texto estático, el cuadro de texto muestra siempre la selección (si existe) en la parte del cuadro de lista del cuadro combinado. Si usa un cuadro de edición, el usuario puede escribir la selección deseada; el cuadro de lista resalta el primer elemento (si existe) que coincida con lo que el usuario ha escrito en el cuadro de edición. A continuación, el usuario puede seleccionar el elemento resaltado en el cuadro de lista para completar la selección. Además, el cuadro combinado puede estar dibujado por el propietario y tener un alto fijo o variable.

``` syntax
COMBOBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Estilos de control. Este valor puede ser una combinación de los estilos de clase COMBOBOX y cualquiera de los siguientes estilos **: \_ WS TABSTOP**, **WS \_ Group**, **WS \_ VSCROLL** y **WS \_ deshabilitados**.

Si no especifica un estilo, el estilo predeterminado es `CBS_SIMPLE | WS_TABSTOP` .

</dd> </dl>

El parámetro *height* se aplica al alto de un cuadro combinado con una lista desplegable totalmente expandida.

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En este ejemplo se define un control de cuadro combinado con una barra de desplazamiento vertical:

``` syntax
COMBOBOX 777, 10, 10, 50, 54, CBS_SIMPLE | WS_VSCROLL | WS_TABSTOP 
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[Cuadros combinados](../controls/about-combo-boxes.md)
</dt> </dl>

 

 