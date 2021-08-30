---
description: Si este bit se establece en un control , la propiedad asociada especificada en la columna Propiedad de la tabla Control es un entero. Si no se establece este bit, la propiedad es un valor de cadena.
ms.assetid: 58db9451-d152-439b-b7cf-39ddea84bcc9
title: Atributo de control de entero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9311e0a665a8bb71c0cf672a7ca9b71ca0638c678eb5913cab51437f408a378
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119996505"
---
# <a name="integer-control-attribute"></a>Atributo de control de entero

Si este bit se establece en un control , la propiedad asociada especificada en la columna Propiedad de la [tabla Control](control-table.md) es un entero. Si no se establece este bit, la propiedad es un valor de cadena.

## <a name="valid-controls"></a>Controles válidos

[CheckBox](checkbox-control.md)

[ComboBox](combobox-control.md)

[Editar](edit-control.md)

[ListBox](listbox-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                          |
|---------|-------------|-----------------------------------|
| 16      | 0x00000010  | **msidbControlAttributesInteger** |



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control , incluya el bit Entero en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Controles y atributos](control-attributes.md) de [control.](controls.md)

 

 



