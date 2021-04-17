---
description: ICEM04 comprueba que las tablas vacías necesarias del módulo de combinación están vacías. Error al corregir un error que indica que los informes de ICEM04 pueden producir una combinación incorrecta del módulo de combinación.
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ef993690ae690e0651db1538196998c4dd28c7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652493"
---
# <a name="icem04"></a>ICEM04

ICEM04 comprueba que las tablas vacías necesarias del módulo de combinación están vacías. Error al corregir un error que indica que los informes de ICEM04 pueden producir una combinación incorrecta del módulo de combinación.

## <a name="result"></a>Resultado

ICEM04 expone un error cuando las tablas vacías requeridas del módulo de combinación no están vacías.

## <a name="example"></a>Ejemplo

ICEM04 expone los siguientes mensajes de error para un módulo que contiene las entradas de base de datos que se muestran.

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

En la tabla siguiente se muestra una [tabla AdvtExecuteSequence](advtexecutesequence-table.md)parcial.



| Acción         | Secuencia |
|----------------|----------|
| CostInitialize | 1        |



 

La lista siguiente muestra el contenido parcial de módulo CRT:

-   ModuleInstallExecuteSequence
-   ModuleAdvtExecuteSequence
-   InstallUISequence

En el ejemplo siguiente se muestra otro posible error.

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

Si un módulo de combinación contiene una tabla de secuencia de módulo, debe contener la tabla de secuencia vacía correspondiente, tanto si la tabla de secuencia de módulo está vacía como si no. Por ejemplo, si el módulo de combinación contiene la [tabla ModuleAdminExecuteSequence](moduleadminexecutesequence-table.md), también debe contener una tabla AdminExecuteSequence vacía.

La [tabla FeatureComponents](featurecomponents-table.md) es necesaria en todos los módulos de combinación y debe estar vacía.

En el procedimiento siguiente se muestra cómo corregir los errores.

**Para corregir errores**

1.  Agregue una [tabla FeatureComponents](featurecomponents-table.md) vacía al módulo Merge.
2.  Agregue una [tabla InstallExecuteSequence](installexecutesequence-table.md) vacía al módulo Merge.
3.  Quite la acción ' CostInitialize ' de la [tabla AdvtExecuteSequence](advtexecutesequence-table.md).
    > [!Note]  
    > Esta tabla debe estar vacía en un módulo de combinación. Las acciones solo deben aparecer en la tabla ModuleAdvtExecuteSequence.

     

## <a name="tables-used-during-execution"></a>Tablas usadas durante la ejecución

En la lista siguiente se identifican las tablas que se usan durante la ejecución:

-   [Tabla FeatureComponents](featurecomponents-table.md)
-   \*Tablas de secuencia de módulo y \* tablas de secuencia correspondientes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los módulos de combinación](about-merge-modules.md)
</dt> <dt>

[Referencia de módulo de combinación ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



