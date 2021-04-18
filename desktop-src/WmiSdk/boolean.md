---
title: booleano (WMI)
description: Es un \_ parámetro de VT bool que toma el valor de Variant \_ TRUE (&\# 8211; 1) o Variant \_ false (0).
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569f7ce633bfb70fdba5e7055a80ad73ebd0fb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105706933"
---
# <a name="boolean-wmi"></a>booleano (WMI)

El tipo de datos Boolean es un \_ parámetro VT bool que toma el valor de Variant \_ true (– 1) o Variant \_ false (0). En la tabla siguiente se muestra la diferencia entre las representaciones mediante programación de **true** lógico en C/C++ y el tipo de automatización.

| Idioma   | Value         | Valor numérico |
|------------|---------------|-----------------|
| C/C++      | **TRUE**      | 1               |
| Automatización | VARIANTE \_ true | –1              |

Ambos tipos son distintos de cero y, por lo tanto, no son **false**, pero tienen representaciones diferentes para **true**.
