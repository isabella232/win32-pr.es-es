---
description: ICEM08 garantiza que un módulo no excluya otro módulo del que depende.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43f5d0076de382889e5fd3df8a03dddb51c6a73eb5a4f825068f6cd66ad24d07
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119811015"
---
# <a name="icem08"></a>ICEM08

ICEM08 garantiza que un módulo no excluya otro módulo del que depende.

## <a name="result"></a>Resultado

ICEM08 publica un error cuando un módulo excluye otro módulo del que depende.

## <a name="example"></a>Ejemplo

ICEM08 publica el siguiente mensaje de error para un módulo que contiene las entradas de base de datos que se muestran en el ejemplo.

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[ModuleDependency Table](moduledependency-table.md)



| ModuleID             | ModuleLanguage | RequiredID           | RequiredLanguage | RequiredVersion |
|----------------------|----------------|----------------------|------------------|-----------------|
| ModuleA.<GUID> | 3082           | ModuleB.<GUID> | 3082             | 1.0             |



 

[ModuleExclusion Table](moduleexclusion-table.md)



| ModuleID             | ModuleLanguage | ExcludedID           | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| ModuleA.<GUID> | 3082           | ModuleB.<GUID> | 3082             |                    | 1.0                |



 

Para corregir el error, quite la dependencia o la exclusión. Si ModuleB es una dependencia (RequiredID) de ModuleA, no se puede excluir (como se muestra en la columna ExludedID de la tabla ModuleExclusion). Si debe excluir ModuleB, debe quitar la dependencia de ModuleA en él.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md)
</dt> </dl>

 

 



