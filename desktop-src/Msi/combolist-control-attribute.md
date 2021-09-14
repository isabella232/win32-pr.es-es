---
description: Si el bit Control ComboList está establecido en un cuadro combinado, el campo de edición se reemplaza por un campo de texto estático. Esto impide que un usuario escriba un nuevo valor y requiere que el usuario elija solo uno de los valores predefinidos.
ms.assetid: 79af4bb0-1e0f-4df3-ae25-d2798842adb6
title: Atributo de control ComboList
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2dcb1c51e8eccaba03c3b4d905b0501e8a3f97a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158878"
---
# <a name="combolist-control-attribute"></a>Atributo de control ComboList

Si el bit Control ComboList está establecido en un cuadro combinado, el campo de edición se reemplaza por un campo de texto estático. Esto impide que un usuario escriba un nuevo valor y requiere que el usuario elija solo uno de los valores predefinidos.

Si no se establece este bit, el cuadro combinado tiene un campo de edición.

## <a name="valid-controls"></a>Controles válidos

[ComboBox](combobox-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Descripción                     |
|---------|-------------|---------------------------------|
| 131 072  | 0x00020000  | msidbControlAttributesComboList |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control , incluya el bit ComboList en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



