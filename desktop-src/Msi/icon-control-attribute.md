---
description: Si se establece este bit, el texto se reemplaza por una imagen de icono y la columna Texto de la tabla Control es una clave externa en la tabla Binaria.
ms.assetid: 5eefdfcb-89a5-4885-bab0-6409ef3ce349
title: Icono Atributo de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2caeb407b86b888a5dd3b1c08f16d0893233f82cec29b92519c267b286ea121
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119315125"
---
# <a name="icon-control-attribute"></a>Icono Atributo de control

Si se establece este bit, el texto se reemplaza por una imagen de icono y la columna Texto de la tabla [Control](control-table.md) es una clave externa en la [tabla binaria](binary-table.md).

Si no se establece este bit, el texto del control se especifica en la columna Texto de la [tabla Control](control-table.md).

## <a name="valid-controls"></a>Controles válidos

[CheckBox](checkbox-control.md)

[Pulsador](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                       |
|---------|-------------|--------------------------------|
| 5242288 | 0x00080000  | **msidbControlAttributesIcon** |



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control , incluya los bits de icono en la columna Atributos del registro del control en la [tabla Control](control-table.md).

La columna Text de la tabla Control se usa como clave externa para la tabla [Binary,](binary-table.md)por lo que el control no puede contener una imagen de icono y texto.

No establezca los bits Icono y [Mapa de](bitmap-control-attribute.md) bits.

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



