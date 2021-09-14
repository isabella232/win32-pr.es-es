---
description: Si este bit se establece, el texto del control se muestra en una sola línea. Si el texto se extiende más allá de los márgenes del control, se trunca y se truncan los puntos suspensivos (&\# 0034;...&\# 0034;). se inserta al final para indicar el truncamiento. Si no se establece este bit, el texto se ajusta.
ms.assetid: 0dec3d25-0da7-4054-8d5c-55e81be16489
title: Atributo de control NoWrap
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 51ee40b52fbec1c8add841f7055a7f42667eca94
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074339"
---
# <a name="nowrap-control-attribute"></a>Atributo de control NoWrap

Si este bit se establece, el texto del control se muestra en una sola línea. Si el texto se extiende más allá de los márgenes del control, se trunca y se insertan puntos suspensivos ("...") al final para indicar el truncamiento. Si no se establece este bit, el texto se ajusta.

## <a name="valid-controls"></a>Controles válidos

[Texto](text-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                         |
|---------|-------------|----------------------------------|
| 262 144  | 0x00040000  | **msidbControlAttributesNoWrap** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit NoWrap en la columna Attributes del registro del control en la [tabla Control](control-table.md).

Vea [Controles y atributos](control-attributes.md) de [control.](controls.md)

 

 



