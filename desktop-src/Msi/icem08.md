---
description: ICEM08 garantiza que un módulo no excluya otro módulo del que dependa.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a9767c6748f5a21d83bddb3b5fe93a0a8d7ea67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277749"
---
# <a name="icem08"></a>ICEM08

ICEM08 garantiza que un módulo no excluya otro módulo del que dependa.

## <a name="result"></a>Resultado

ICEM08 expone un error cuando un módulo excluye otro módulo del que depende.

## <a name="example"></a>Ejemplo

ICEM08 envía el siguiente mensaje de error para un módulo que contiene las entradas de base de datos que se muestran en el ejemplo.

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[Tabla ModuleDependency](moduledependency-table.md)



| ModuleID             | ModuleLanguage | RequiredID           | RequiredLanguage | RequiredVersion |
|----------------------|----------------|----------------------|------------------|-----------------|
| Móduloa.<GUID> | 3082           | ModuleB.<GUID> | 3082             | 1,0             |



 

[Tabla ModuleExclusion](moduleexclusion-table.md)



| ModuleID             | ModuleLanguage | ExcludedID           | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| Móduloa.<GUID> | 3082           | ModuleB.<GUID> | 3082             |                    | 1,0                |



 

Para corregir el error, quite la dependencia o la exclusión. Si ModuleB es una dependencia (RequiredID) de Modulea, no se puede excluir (como se muestra en la columna ExludedID de la tabla ModuleExclusion). Si debe excluir ModuleB, debe quitar la dependencia del Móduloa en él.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de módulo de combinación ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



