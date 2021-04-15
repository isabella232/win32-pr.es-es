---
description: Este es un ejemplo de una tabla de secuencia.
ms.assetid: 25b3667a-1478-48c4-9c41-4defd25a0103
title: Ejemplo detallado de tabla de secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4698d5270f2f246fe6e676799ea239e47a950c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669835"
---
# <a name="sequence-table-detailed-example"></a>Ejemplo detallado de tabla de secuencias

Este es un ejemplo de una tabla de secuencia.



| Acción                                          | Condición                                                       | Secuencia |
|-------------------------------------------------|-----------------------------------------------------------------|----------|
| [LaunchConditions](launchconditions-action.md) |                                                                 |          |
| [AppSearch](appsearch-action.md)               |                                                                 | 200      |
| [CCPSearch](ccpsearch-action.md)               | prueba de CCP \_                                                       | 300      |
| CCPDialog                                       | NO se ha \_ ejecutado el CCP \_                                               | 400      |
| MyCustomConfig                                  | NO [ **instalado**](installed.md)                              | 500      |
| [CostInitialize](costinitialize-action.md)     |                                                                 | 600      |
| [FileCost](filecost-action.md)                 |                                                                 | 700      |
| [CostFinalize](costfinalize-action.md)         |                                                                 | 800      |
| InstallDialog                                   | NO [ **instalado**](installed.md)                              | 900      |
| MaintenanceDialog                               | [**Instalado**](installed.md) Y no [ **reanudar**](resume.md) | 1000     |
| ActionDialog                                    |                                                                 | 1100     |
| [RegisterProduct](registerproduct-action.md)   |                                                                 | 1200     |
| [InstallValidate](installvalidate-action.md)   |                                                                 | 1300     |
| [InstallFiles](installfiles-action.md)         |                                                                 | 1400     |
| MyCustomAction                                  | $MyComponent > 2                                             | 1.500     |
| [InstallFinalize](installfinalize-action.md)   |                                                                 | 1600     |



 

Las siguientes acciones de esta tabla de secuencia las define el instalador y son ejemplos de acciones estándar:

[LaunchConditions](launchconditions-action.md)

 

[AppSearch](appsearch-action.md)

 

[CCPSearch](ccpsearch-action.md)

 

[CostInitialize](costinitialize-action.md)

 

[FileCost](filecost-action.md)

 

[CostFinalize](costfinalize-action.md)

 

[RegisterProduct](registerproduct-action.md)

 

[InstallFiles](installfiles-action.md)

 

[InstallFiles](installfiles-action.md)

 

[InstallValidate](installvalidate-action.md)

Las siguientes acciones fueron definidas por el autor de la tabla y son ejemplos de [acciones personalizadas](custom-actions.md) y deben aparecer en la [tabla CustomAction](customaction-table.md):

MyCustomConfig

 

MyCustomAction

Las entradas restantes en el campo acción son claves externas en la [tabla del cuadro de diálogo](dialog-table.md). Especifican los nombres de los cuadros de diálogo que se mostrarán si el campo condition se evalúa como true.

CCPDialog

 

InstallDialog

 

MaintenanceDialog

 

ActionDialog

La columna condición hace que el instalador omita la acción si la propiedad o expresión de este campo es false. La propiedad [**installed**](installed.md) y la propiedad [**resume**](resume.md) son ejemplos de propiedades que se establecen mediante el instalador. La propiedad [**installed**](installed.md) se establece en true si el producto ya está instalado y se establece la propiedad [**resume**](resume.md) si se reanuda una instalación suspendida. Las \_ propiedades CCP test y not \_ CCP \_ Success son ejemplos de propiedades que el usuario puede establecer en la línea de comandos mediante la instalación de la aplicación.

Todas las acciones se ejecutan en secuencia con los siguientes pasos condicionales:

-   CPPSearch se ejecuta solo si \_ se establece la prueba de CCP.
-   CCPDialog se ejecuta solo si \_ se ha \_ establecido no se ha realizado correctamente.
-   MaintenanceDialog se ejecuta solo si este producto ya está instalado y si no se trata de una instalación que se está reanudando después de suspenderse.
-   MyCustomAction se ejecuta solo si la expresión de la columna Condition es true. La expresión $MyComponent > 2 hace referencia al estado de acción del componente denominado mi componente. Esta condición indica que MyCustomAction solo debe ejecutarse si se ha establecido que el componente está instalado. Para obtener más información sobre los Estados de acción y los Estados de selección, vea la propiedad [**FeatureRequestState**](session-featurerequeststate.md) , la [tabla de características](feature-table.md)y la [acción InstallFiles](installfiles-action.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Utilizar propiedades](using-properties.md)
</dt> <dt>

[Sintaxis de la instrucción condicional](conditional-statement-syntax.md)
</dt> </dl>

 

 



