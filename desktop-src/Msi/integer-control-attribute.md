---
description: Si este bit se establece en un control, la propiedad asociada especificada en la columna de propiedades de la tabla de control es un entero. Si no se establece este bit, la propiedad es un valor de cadena.
ms.assetid: 58db9451-d152-439b-b7cf-39ddea84bcc9
title: Atributo de control de entero
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6310f6348a533874ce4dc176043a489b595c28b8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686572"
---
# <a name="integer-control-attribute"></a>Atributo de control de entero

Si este bit se establece en un control, la propiedad asociada especificada en la columna de propiedades de la [tabla de control](control-table.md) es un entero. Si no se establece este bit, la propiedad es un valor de cadena.

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



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit entero en la columna Attributes del registro del control en la [tabla de control](control-table.md).

Vea [controles y](controls.md) [atributos de control](control-attributes.md) .

 

 



