---
description: Si se establece este bit, el texto del control se muestra en una sola línea. Si el texto se extiende más allá de los márgenes del control, se trunca y un botón de puntos suspensivos (&\# 0034;... &\# 0034;) se inserta al final para indicar el truncamiento. Si no se establece este bit, el texto se ajusta.
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: NoWrap (atributo de control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ee40b52fbec1c8add841f7055a7f42667eca94
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105677997"
---
# <a name="nowrap-control-attribute"></a>NoWrap (atributo de control)

Si se establece este bit, el texto del control se muestra en una sola línea. Si el texto se extiende más allá de los márgenes del control, se trunca y se inserta un botón de puntos suspensivos ("...") al final para indicar el truncamiento. Si no se establece este bit, el texto se ajusta.

## <a name="valid-controls"></a>Controles válidos

[Texto](text-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 262 144  | 0x00040000  | **msidbControlAttributesNoWrap** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit NoWrap en la columna Attributes del registro del control en la [tabla de control](control-table.md).

Vea [controles y](controls.md) [atributos de control](control-attributes.md) .

 

 



