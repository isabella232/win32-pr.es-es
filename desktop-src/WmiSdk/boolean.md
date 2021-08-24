---
title: boolean (WMI)
description: Es un parámetro VT BOOL que toma el valor de \_ VARIANT \_ TRUE (&\# 8211;1) o VARIANT \_ FALSE (0).
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50422990a45dd59c2bedc3ac90bddcf06f7796cd3308daf03a11db0dca38f0b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119051063"
---
# <a name="boolean-wmi"></a>boolean (WMI)

El tipo de datos booleano es un parámetro VT BOOL que toma el valor \_ de VARIANT \_ TRUE (–1) o VARIANT \_ FALSE (0). En la tabla siguiente se muestra la diferencia entre las representaciones mediante programación de **TRUE** lógico en C/C++ y el tipo automation.

| Lenguaje   | Valor         | Valor numérico |
|------------|---------------|-----------------|
| C/C++      | **TRUE**      | 1               |
| Automation | VARIANT \_ TRUE | –1              |

Ambos tipos son distintos de cero y, por tanto, **no FALSE,** pero tienen representaciones diferentes para **TRUE.**
