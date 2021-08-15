---
title: Control LISTBOX (menús y otros recursos)
description: Define los controles usados habitualmente para un cuadro de diálogo o ventana. El control es un rectángulo que contiene una lista de cadenas (por ejemplo, nombres de archivo) desde las que el usuario puede seleccionar.
ms.assetid: 78f6d36e-5079-4f04-87e4-ca55a1161a51
keywords:
- Menús de control LISTBOX y otros recursos
topic_type:
- apiref
api_name:
- LISTBOX
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 676ea07f7d66a0d84997f0b2b22b9973c326db0fb603caedcc631caeffffaf98
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119226355"
---
# <a name="listbox-control"></a>Control LISTBOX

Define los controles usados habitualmente para un cuadro de diálogo o ventana. El control es un rectángulo que contiene una lista de cadenas (por ejemplo, nombres de archivo) desde las que el usuario puede seleccionar.

La **instrucción LISTBOX,** que solo se puede usar en una [**instrucción DIALOGEX**](dialogex-resource.md) o **WINDOW,** define el identificador, las dimensiones y los atributos de una ventana de control.

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*Estilo*
</dt> <dd>

Estilos de control. Este valor puede ser una combinación de los estilos de clase de cuadro de lista y cualquiera de los estilos siguientes: **WS \_ BORDER** y **WS \_ VSCROLL**.

Si no especifica un estilo, el estilo predeterminado es `LBS_NOTIFY | WS_BORDER` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [Parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En este ejemplo se define un control de cuadro de lista cuyo identificador es 101:

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Combobox**](combobox-control.md)
</dt> <dt>

[Cuadros de lista](../controls/about-list-boxes.md)
</dt> </dl>

 

 