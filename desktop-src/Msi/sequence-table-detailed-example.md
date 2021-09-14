---
description: Este es un ejemplo de una tabla de secuencia.
ms.assetid: 25b3667a-1478-48c4-9c41-4defd25a0103
title: Ejemplo detallado de tabla de secuencias
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4698d5270f2f246fe6e676799ea239e47a950c7
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127260927"
---
# <a name="sequence-table-detailed-example"></a>Ejemplo detallado de tabla de secuencias

Este es un ejemplo de una tabla de secuencia.



| Acción                                          | Condición                                                       | Secuencia |
|-------------------------------------------------|-----------------------------------------------------------------|----------|
| [LaunchConditions](launchconditions-action.md) |                                                                 |          |
| [AppSearch](appsearch-action.md)               |                                                                 | 200      |
| [CCPSearch](ccpsearch-action.md)               | PRUEBA \_ DE CCP                                                       | 300      |
| CCPDialog                                       | NOT \_ CCP \_ SUCCESS                                               | 400      |
| MyCustomConfig                                  | NO [ **instalado**](installed.md)                              | 500      |
| [CostInitialize](costinitialize-action.md)     |                                                                 | 600      |
| [FileCost](filecost-action.md)                 |                                                                 | 700      |
| [CostFinalize](costfinalize-action.md)         |                                                                 | 800      |
| InstallDialog                                   | NO [ **instalado**](installed.md)                              | 900      |
| MaintenanceDialog                               | [**Instalado**](installed.md) AND NOT [ **Resume**](resume.md) | 1000     |
| ActionDialog                                    |                                                                 | 1100     |
| [RegisterProduct](registerproduct-action.md)   |                                                                 | 1200     |
| [InstallValidate](installvalidate-action.md)   |                                                                 | 1300     |
| [InstallFiles](installfiles-action.md)         |                                                                 | 1400     |
| MyCustomAction                                  | $MyComponent > 2                                             | 1.500     |
| [InstallFinalize](installfinalize-action.md)   |                                                                 | 1600     |



 

El instalador define las siguientes acciones de esta tabla de secuencias y son ejemplos de acciones estándar:

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

El autor de la tabla definió las siguientes [](custom-actions.md) acciones y son ejemplos de acciones personalizadas y deben aparecer en la [tabla CustomAction](customaction-table.md):

MyCustomConfig

 

MyCustomAction

Las entradas restantes del campo Acción son claves externas en la tabla [Dialog](dialog-table.md). Especifican los nombres de los cuadros de diálogo que se mostrarán si el campo de condición se evalúa como True.

CCPDialog

 

InstallDialog

 

MaintenanceDialog

 

ActionDialog

La columna Condición hace que el instalador omita la acción si la propiedad o expresión de este campo es False. Las [**propiedades Installed**](installed.md) y [**RESUME**](resume.md) son ejemplos de propiedades establecidas por el instalador. La [**propiedad Installed**](installed.md) se establece en true si el producto ya está instalado y la propiedad [**RESUME**](resume.md) se establece si se reanuda una instalación suspendida. Las propiedades CCP TEST y NOT CCP SUCCESS son ejemplos de propiedades que el usuario que instala la aplicación puede establecer en la línea \_ \_ de \_ comandos.

Todas las acciones se ejecutan en secuencia con los siguientes pasos condicionales:

-   CPPSearch solo se ejecuta si se establece CCP \_ TEST.
-   CCPDialog solo se ejecuta si se establece NOT \_ CCP \_ SUCCESS.
-   MaintenanceDialog solo se ejecuta si este producto ya está instalado y si no se trata de una instalación que se está reanudando después de suspenderse.
-   MyCustomAction solo se ejecuta si la expresión de la columna Condición es True. La expresión $MyComponent > 2 hace referencia al estado de acción del componente denominado MyComponent. Esta condición indica que MyCustomAction solo se debe ejecutar si MyComponent está establecido para instalarse. Para obtener más información sobre los estados de acción y los estados de selección, vea la propiedad [**FeatureRequestState,**](session-featurerequeststate.md) [la tabla Feature](feature-table.md)y la acción [InstallFiles](installfiles-action.md).

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Utilizar propiedades](using-properties.md)
</dt> <dt>

[Sintaxis de instrucciones condicionales](conditional-statement-syntax.md)
</dt> </dl>

 

 



