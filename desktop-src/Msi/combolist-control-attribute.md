---
description: Si el bit Control ComboList está establecido en un cuadro combinado, el campo de edición se reemplaza por un campo de texto estático. Esto impide que un usuario escriba un nuevo valor y requiere que el usuario elija solo uno de los valores predefinidos.
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: Atributo de control ComboList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71e0a53357d91c5c5a016f65e8e1e0fb341b15cae1ea2c6cf480e536fa109067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145384"
---
# <a name="combolist-control-attribute"></a>Atributo de control ComboList

Si el bit Control ComboList está establecido en un cuadro combinado, el campo de edición se reemplaza por un campo de texto estático. Esto impide que un usuario escriba un nuevo valor y requiere que el usuario elija solo uno de los valores predefinidos.

Si no se establece este bit, el cuadro combinado tiene un campo de edición.

## <a name="valid-controls"></a>Controles válidos

[ComboBox](combobox-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Descripción                     |
|---------|-------------|---------------------------------|
| 131 072  | 0x00020000  | msidbControlAttributesComboList |



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control , incluya el bit ComboList en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



