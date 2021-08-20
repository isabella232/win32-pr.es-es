---
description: ICE68 comprueba que todos los tipos de acción personalizados necesarios para una instalación son válidos.
ms.assetid: a37d6d6c-3005-425b-883a-6fe074b9d708
title: ICE68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 577844dcbc4e7a2f5582eca40839b6e30cff37c200cf073f1b5d0f9b4387b46f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117991110"
---
# <a name="ice68"></a>ICE68

ICE68 comprueba que todos los tipos de acción personalizados necesarios para una instalación son válidos. Si no se corrige el error notificado por ICE68, se produce un error en una instalación que intenta ejecutar la acción. ICE68 emite una advertencia si se establece el atributo **msidbCustomActionTypeNoImpersonate** sin establecer también el atributo **msidbCustomActionTypeInScript.**

## <a name="result"></a>Resultado

ICE68 devuelve un error si un tipo de acción necesario para una instalación no es válido.

## <a name="example"></a>Ejemplo

ICE68 envía la siguiente advertencia si una acción personalizada tiene el bit **msidbCustomActionTypeNoImpersonate** establecido en el campo Tipo de la tabla CustomAction sin **msidbCustomActionTypeInScript** también establecido.

``` syntax
Even though custom action '[2]' is marked to be elevated (with 
attribute msidbCustomActionTypeNoImpersonate), it will not be run with elevated 
privileges because it's not deferred (with attribute msidbCustomActionTypeInScript).
```

Para corregir esta advertencia, incluya **msidbCustomActionTypeInScript** (0x400) si la acción personalizada incluye **msidbCustomActionTypeNoImpersonate** (0x800). De lo contrario, el instalador omite **el atributo msidbCustomActionTypeNoImpersonate.** Para obtener más información, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

ICE68 notifica el siguiente error para el ejemplo que se muestra:

``` syntax
Invalid custom action type for action 'Action1'.
```

1027 no es un tipo de acción válido.

Para corregir este error, elija un tipo de acción personalizado válido.

[Tabla CustomAction](customaction-table.md) (parcial)



| Acción  | Tipo | Source   | Destino     |
|---------|------|----------|------------|
| Action1 | 1027 | Argumento | Componente1 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



