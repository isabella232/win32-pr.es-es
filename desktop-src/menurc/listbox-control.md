---
title: LISTBOX (control) (menús y otros recursos)
description: Define controles de uso frecuente para un cuadro de diálogo o una ventana. El control es un rectángulo que contiene una lista de cadenas (como nombres de archivo) desde las que el usuario puede seleccionar.
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
ms.openlocfilehash: f9f062387463917438a988c3b023ca656beef722
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149257"
---
# <a name="listbox-control"></a>LISTBOX (control)

Define controles de uso frecuente para un cuadro de diálogo o una ventana. El control es un rectángulo que contiene una lista de cadenas (como nombres de archivo) desde las que el usuario puede seleccionar.

La instrucción **ListBox** , que solo se puede utilizar en una instrucción [**DIALOGEX**](dialogex-resource.md) o **Window** , define el identificador, las dimensiones y los atributos de una ventana de control.

``` syntax
LISTBOX id, x, y, width, height [, style [, extended-style]]
```

<dl> <dt>

<span id="style"></span><span id="STYLE"></span>*aplicar*
</dt> <dd>

Estilos de control. Este valor puede ser una combinación de los estilos de clase de cuadro de lista y cualquiera de los siguientes estilos: **WS \_ Border** y **WS \_ VSCROLL**.

Si no especifica un estilo, el estilo predeterminado es `LBS_NOTIFY | WS_BORDER` .

</dd> </dl>

Para obtener más información sobre la sintaxis general de una instrucción de control, vea [parámetros de control comunes](common-control-parameters.md).

## <a name="examples"></a>Ejemplos

En este ejemplo se define un control de cuadro de lista cuyo identificador es 101:

``` syntax
LISTBOX 101, 10, 10, 100, 100
```

## <a name="see-also"></a>Vea también

<dl> <dt>

[**COMBOBOX**](combobox-control.md)
</dt> <dt>

[Cuadros de lista](../controls/about-list-boxes.md)
</dt> </dl>

 

 