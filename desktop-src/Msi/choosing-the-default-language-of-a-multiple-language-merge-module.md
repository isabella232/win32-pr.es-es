---
description: El idioma predeterminado para un módulo de combinación es el idioma que se muestra en la tabla ModuleSignature del módulo antes de que se apliquen las transformaciones de lenguaje. Este también es el primer idioma que se muestra en la propiedad Resumen de plantilla.
ms.assetid: 4d795727-684c-4dc1-8b46-d72b69c455c3
title: Elegir el idioma predeterminado de un módulo de combinación de varios idiomas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7c174a3917538b1562626819f8ba2bf07864c9169c27e717a078cca8d64992ef
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118145661"
---
# <a name="choosing-the-default-language-of-a-multiple-language-merge-module"></a>Elegir el idioma predeterminado de un módulo de combinación de varios idiomas

El idioma predeterminado para un módulo de combinación es el idioma que se muestra en la tabla [ModuleSignature](modulesignature-table.md) del módulo antes de que se apliquen las transformaciones de lenguaje. Este también es el primer idioma que se muestra en la [**propiedad Resumen de**](template-summary.md) plantilla.

El idioma predeterminado del módulo debe ser uno de los idiomas más específicos que admita, ya que el idioma predeterminado siempre se comprueba primero y, si satisface el idioma solicitado, se usa incluso si otro idioma coincide mejor. Por ejemplo, si un módulo admite 1033 y 0, 1033 debe ser el idioma predeterminado. Si 0 fuera el idioma predeterminado, siempre satisfaría cualquier solicitud y la transformación 1033 nunca se usaría, aunque 1033 sea el idioma exacto solicitado.

 

 



