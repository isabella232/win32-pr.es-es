---
title: boolean (WMI)
description: Es un parámetro VT BOOL que toma el valor \_ de VARIANT \_ TRUE (&\# 8211;1) o VARIANT \_ FALSE (0).
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569f7ce633bfb70fdba5e7055a80ad73ebd0fb6c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127073065"
---
# <a name="boolean-wmi"></a>boolean (WMI)

El tipo de datos booleano es un parámetro VT BOOL que toma el valor \_ de VARIANT \_ TRUE (–1) o VARIANT \_ FALSE (0). En la tabla siguiente se muestra la diferencia entre las representaciones mediante programación de **TRUE** lógico en C/C++ y el tipo automation.

| Idioma   | Value         | Valor numérico |
|------------|---------------|-----------------|
| C/C++      | **TRUE**      | 1               |
| Automation | VARIANT \_ TRUE | –1              |

Ambos tipos son distintos de cero y, por tanto, **no FALSE,** pero tienen representaciones diferentes para **TRUE.**
