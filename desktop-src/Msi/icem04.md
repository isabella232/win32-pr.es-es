---
description: ICEM04 comprueba que las tablas vacías necesarias del módulo de combinación están vacías. Si no se corrige un error que informe ICEM04, puede producirse una combinación incorrecta del módulo de combinación.
ms.assetid: c6f64f5e-be65-485b-8831-e377535bd335
title: ICEM04
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8388cbccd576b89a70716dd7c2ca6c82ac49fb30c8c39776904753de00b68dba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050165"
---
# <a name="icem04"></a>ICEM04

ICEM04 comprueba que las tablas vacías necesarias del módulo de combinación están vacías. Si no se corrige un error que informe ICEM04, puede producirse una combinación incorrecta del módulo de combinación.

## <a name="result"></a>Resultado

ICEM04 publica un error cuando las tablas vacías necesarias del módulo de mezcla no están vacías.

## <a name="example"></a>Ejemplo

ICEM04 publica los siguientes mensajes de error para un módulo que contiene las entradas de base de datos mostradas.

``` syntax
An empty FeatureComponents table is required in a Merge Module.

The Merge Module contains the 'ModuleInstallExecuteSequence' table. It 
must therefore have an empty 'InstallExecuteSequence' table.

Action 'CostInitialize' found in the AdvtExecuteSequence table. This 
table must be empty in a Merge Module
```

En la tabla siguiente se muestra una tabla [advtExecuteSequence parcial.](advtexecutesequence-table.md)



| Acción         | Secuencia |
|----------------|----------|
| CostInitialize | 1        |



 

En la lista siguiente se muestra el contenido parcial de MergeModule:

-   ModuleInstallExecuteSequence
-   ModuleAdvtExecuteSequence
-   InstallUISequence

En el ejemplo siguiente se muestra otro posible error.

``` syntax
Feature-Component '[1].[2]' found in the FeatureComponents table. The 
FeatureComponents table must be empty in a Merge Module.
```

Si un módulo de combinación contiene una tabla de secuencias de módulos, debe contener la tabla de secuencia vacía correspondiente, independientemente de si la tabla de secuencia del módulo está vacía o no. Por ejemplo, si el módulo merge contiene [moduleAdminExecuteSequence Table](moduleadminexecutesequence-table.md), también debe contener una tabla AdminExecuteSequence vacía.

La [tabla FeatureComponents es](featurecomponents-table.md) necesaria en todos los módulos de combinación y debe estar vacía.

En el procedimiento siguiente se muestra cómo corregir errores.

**Para corregir errores**

1.  Agregue una tabla [FeatureComponents vacía](featurecomponents-table.md) al módulo de combinación.
2.  Agregue una tabla [InstallExecuteSequence vacía](installexecutesequence-table.md) al módulo merge.
3.  Quite la acción "CostInitialize" de [la tabla AdvtExecuteSequence](advtexecutesequence-table.md).
    > [!Note]  
    > Esta tabla debe estar vacía en un módulo de combinación. Las acciones solo deben aparecer en la tabla ModuleAdvtExecuteSequence.

     

## <a name="tables-used-during-execution"></a>Tablas usadas durante la ejecución

En la lista siguiente se identifican las tablas que se usan durante la ejecución:

-   [Tabla FeatureComponents](featurecomponents-table.md)
-   Tablas \* de secuencia de módulo y tablas de secuencia \* correspondientes.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Acerca de los módulos de combinación](about-merge-modules.md)
</dt> <dt>

[Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md)
</dt> </dl>

 

 



