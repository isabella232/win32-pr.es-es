---
description: ICE68 comprueba que todos los tipos de acción personalizados necesarios para una instalación sean válidos.
ms.assetid: a37d6d6c-3005-425b-883a-6fe074b9d708
title: ICE68
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1392db6ec05085c672ed70c8f035ea8eed3015e7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669809"
---
# <a name="ice68"></a>ICE68

ICE68 comprueba que todos los tipos de acción personalizados necesarios para una instalación sean válidos. Si no se corrige el error detectado por ICE68, se produce un error en una instalación que intenta ejecutar la acción. ICE68 emite una advertencia si se establece el atributo **msidbCustomActionTypeNoImpersonate** sin establecer también el atributo **msidbCustomActionTypeInScript** .

## <a name="result"></a>Resultado

ICE68 devuelve un error si un tipo de acción necesario para una instalación de no es válido.

## <a name="example"></a>Ejemplo

ICE68 envía la siguiente advertencia si una acción personalizada tiene el bit **msidbCustomActionTypeNoImpersonate** establecido en el campo Type de la tabla CustomAction sin la **msidbCustomActionTypeInScript** establecida también.

``` syntax
Even though custom action '[2]' is marked to be elevated (with 
attribute msidbCustomActionTypeNoImpersonate), it will not be run with elevated 
privileges because it's not deferred (with attribute msidbCustomActionTypeInScript).
```

Para corregir esta advertencia, incluya **msidbCustomActionTypeInScript** (0x400) si la acción personalizada incluye **msidbCustomActionTypeNoImpersonate** (0x800). En caso contrario, el instalador omite el atributo **msidbCustomActionTypeNoImpersonate** . Para obtener más información, vea [Custom Action In-Script Execution Options](custom-action-in-script-execution-options.md).

ICE68 notifica el siguiente error para el ejemplo mostrado:

``` syntax
Invalid custom action type for action 'Action1'.
```

1027 no es un tipo de acción válido.

Para corregir este error, elija un tipo de acción personalizado válido.

[Tabla CustomAction](customaction-table.md) (parcial)



| Acción  | Tipo | Source   | Destino     |
|---------|------|----------|------------|
| Action1 | 1027 | Argumento | Component1 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



