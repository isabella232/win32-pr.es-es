---
description: Si se establece este bit, el control se muestra con un aspecto hundido de tres dimensiones.
ms.assetid: 00052b01-f2f0-4749-8826-084e5ebb300a
title: Atributo de control hundido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c6852a2f32880a427016e41ce9f68314a4a4ea6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104155120"
---
# <a name="sunken-control-attribute"></a>Atributo de control hundido

Si se establece este bit, el control se muestra con un aspecto hundido de tres dimensiones. El efecto de este bit de estilo es diferente en los distintos controles y versiones de Windows. En algunos controles no tiene ningún efecto visible. Si el sistema no admite el atributo de control hundido, el control se muestra en el estilo visual predeterminado. Si no se establece este bit, el control se muestra con el estilo visual predeterminado.

## <a name="valid-controls"></a>Controles válidos

Todos los controles.

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 4       | 0x00000004  | **msidbControlAttributesSunken** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit hundido en la columna Attributes del registro del control en la [tabla de control](control-table.md).

Vea [controles y](controls.md) [atributos de control](control-attributes.md) .

 

 



