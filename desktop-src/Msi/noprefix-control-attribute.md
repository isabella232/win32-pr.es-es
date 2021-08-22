---
description: Si este bit se establece en un control de texto, la aparición del carácter &\# 0034;&&0034; en una cadena de texto se muestra \# como sí misma. Si no se establece este bit, el carácter siguiente &\# 0034;&&0034; en la cadena de texto se muestra como un carácter de \# subrayado.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: Atributo de control NoPrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15345bb56ad85ec654cffe7a0bf2173973e032ac33aca633105d3a220647cf93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119065885"
---
# <a name="noprefix-control-attribute"></a>Atributo de control NoPrefix

Si este bit se establece en un control de texto, la aparición del carácter "&" en una cadena de texto se muestra como sí misma. Si no se establece este bit, el carácter siguiente a "&" en la cadena de texto se muestra como un carácter de subrayado.

## <a name="valid-controls"></a>Controles válidos

[Texto](text-control.md)

## <a name="value"></a>Valor



| Decimal | Hexadecimal | Constante                           |
|---------|-------------|------------------------------------|
| 131 072  | 0x20000     | **msidbControlAttributesNoPrefix** |



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control , incluya el bit NoPrefix en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Controles y atributos](control-attributes.md) de [control.](controls.md)

 

 



