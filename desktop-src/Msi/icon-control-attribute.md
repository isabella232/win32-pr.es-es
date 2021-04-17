---
description: Si se establece este bit, el texto se reemplaza por una imagen de icono y la columna de texto de la tabla de control es una clave externa de la tabla binaria.
ms.assetid: 5eefdfcb-89a5-4885-bab0-6409ef3ce349
title: Atributo de control de icono
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e60c19674ac26f108109fad04e0836ed8dfeba6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652509"
---
# <a name="icon-control-attribute"></a>Atributo de control de icono

Si se establece este bit, el texto se reemplaza por una imagen de icono y la columna de texto de la [tabla de control](control-table.md) es una clave externa de la [tabla binaria](binary-table.md).

Si no se establece este bit, el texto del control se especifica en la columna de texto de la [tabla de control](control-table.md).

## <a name="valid-controls"></a>Controles válidos

[CheckBox](checkbox-control.md)

[Botones](pushbutton-control.md)

[RadioButtonGroup](radiobuttongroup-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                       |
|---------|-------------|--------------------------------|
| 5242288 | 0x00080000  | **msidbControlAttributesIcon** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya los bits de icono en la columna Attributes del registro del control en la [tabla de control](control-table.md).

La columna de texto de la tabla de control se usa como clave externa de la [tabla binaria](binary-table.md), por lo que el control no puede contener una imagen de icono y texto.

No establezca los bits de icono y de [mapa](bitmap-control-attribute.md) de bits.

Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).

 

 



