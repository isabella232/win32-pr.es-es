---
description: Si este bit se establece en un control , la propiedad asociada especificada en la columna Propiedad de la tabla Control es un entero. Si no se establece este bit, la propiedad es un valor de cadena.
ms.assetid: 58db9451-d152-439b-b7cf-39ddea84bcc9
title: Atributo de control integer
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6310f6348a533874ce4dc176043a489b595c28b8
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127072020"
---
# <a name="integer-control-attribute"></a>Atributo de control integer

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



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control , incluya el bit Entero en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Controles y atributos](control-attributes.md) de [control.](controls.md)

 

 



