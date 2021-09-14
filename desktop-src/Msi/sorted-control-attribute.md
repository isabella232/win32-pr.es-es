---
description: Si se establece este bit, los elementos enumerados en el control se muestran en un orden especificado. Si no se establece el bit, los elementos se muestran en orden alfabético.
ms.assetid: c55bf6bf-6625-47cb-867a-14b3ef8aea0a
title: Atributo de control ordenado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a84af4b0683e35c66e159602b9ed2fe1b3005d8f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127266108"
---
# <a name="sorted-control-attribute"></a>Atributo de control ordenado

Si se establece este bit, los elementos enumerados en el control se muestran en un orden especificado. Si no se establece el bit, los elementos se muestran en orden alfabético.

## <a name="valid-controls"></a>Controles válidos

[ComboBox](combobox-control.md)

 

[ListBox](listbox-control.md)

 

[Control ListView](listview-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesSorted** |



 

## <a name="remarks"></a>Observaciones

Para ordenar los elementos de un [ComboBox](combobox-control.md), incluya el bit Ordenado en la columna Atributos de la tabla [Control](control-table.md) y especifique el orden de los elementos en la columna Order de la [tabla ComboBox](combobox-table.md).

Para ordenar los elementos de [un Control ListBox](listbox-control.md), incluya el bit Ordenado en la columna Atributos de la [tabla Control](control-table.md) y especifique el orden de los elementos en la columna Order de la [tabla ComboBox](combobox-table.md).

Para ordenar los elementos de [un control ListView](listview-control.md), incluya el bit Ordenado en la columna Atributos de la tabla [Control](control-table.md) y especifique el orden de los elementos en la [tabla ComboBox](combobox-table.md).

Vea [Controles y atributos](control-attributes.md) de [control.](controls.md)

 

 



