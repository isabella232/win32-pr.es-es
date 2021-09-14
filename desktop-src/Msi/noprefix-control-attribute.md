---
description: Si este bit se establece en un control de texto, la aparición del carácter &\# 0034;&&0034; en una cadena de texto se muestra como sí \# misma. Si no se establece este bit, el carácter siguiente &\# 0034;&&0034; en la cadena de texto se muestra como un carácter de \# subrayado.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: Atributo de control NoPrefix
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1a0c6da65605efca1aacc4582b34a8f673d2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260999"
---
# <a name="noprefix-control-attribute"></a>Atributo de control NoPrefix

Si este bit se establece en un control de texto, la aparición del carácter "&" en una cadena de texto se muestra como sí misma. Si no se establece este bit, el carácter que sigue a "&" en la cadena de texto se muestra como un carácter de subrayado.

## <a name="valid-controls"></a>Controles válidos

[Texto](text-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                           |
|---------|-------------|------------------------------------|
| 131 072  | 0x20000     | **msidbControlAttributesNoPrefix** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit NoPrefix en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Controles y atributos](control-attributes.md) de [control.](controls.md)

 

 



