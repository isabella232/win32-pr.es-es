---
description: Si este bit se establece en un control de texto, la aparición del carácter &\# 0034; &&\# 0034; en una cadena de texto se muestra como sí mismo. Si no se establece este bit, el carácter que sigue a &\# 0034; &&\# 0034; en la cadena de texto se muestra como un carácter de subrayado.
ms.assetid: b958eecb-2f44-420f-8c93-7a4bd8b589da
title: Noprefix (atributo de control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae1e1a0c6da65605efca1aacc4582b34a8f673d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275924"
---
# <a name="noprefix-control-attribute"></a>Noprefix (atributo de control)

Si este bit se establece en un control de texto, la aparición del carácter "&" en una cadena de texto se muestra como sí mismo. Si no se establece este bit, el carácter que sigue a "&" en la cadena de texto se muestra como un carácter de subrayado.

## <a name="valid-controls"></a>Controles válidos

[Texto](text-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                           |
|---------|-------------|------------------------------------|
| 131 072  | 0x20000     | **msidbControlAttributesNoPrefix** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit noprefix en la columna Attributes del registro del control en la [tabla de control](control-table.md).

Vea [controles y](controls.md) [atributos de control](control-attributes.md) .

 

 



