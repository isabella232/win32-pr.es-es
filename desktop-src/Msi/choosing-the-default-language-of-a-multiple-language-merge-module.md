---
description: El idioma predeterminado de un módulo de combinación es el idioma que aparece en la tabla ModuleSignature del módulo antes de aplicar las transformaciones de lenguaje. También es el primer idioma que aparece en la propiedad Resumen de plantilla.
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: Elección del idioma predeterminado de un módulo de combinación de varios idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 758a3b47b7a41777652a11a1cdc1b7f380055cb7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158913"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a>Elección del idioma predeterminado de un módulo de combinación de varios idiomas

El idioma predeterminado de un módulo de combinación es el idioma que aparece en la tabla [ModuleSignature](modulesignature-table.md) del módulo antes de aplicar las transformaciones de lenguaje. También es el primer idioma que aparece en la [**propiedad Resumen de**](template-summary.md) plantilla.

El idioma predeterminado del módulo debe ser uno de los idiomas más específicos que admita, ya que el idioma predeterminado siempre se comprueba primero y, si satisface el idioma solicitado, se usa incluso si otro idioma coincide mejor. Por ejemplo, si un módulo admite 1033 y 0, 1033 debe ser el idioma predeterminado. Si 0 fuera el idioma predeterminado, siempre satisfaría cualquier solicitud y la transformación 1033 nunca se usaría, aunque 1033 sea el idioma exacto solicitado.

 

 



