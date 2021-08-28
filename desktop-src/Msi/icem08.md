---
description: ICEM08 garantiza que un módulo no excluya otro módulo del que dependa.
ms.assetid: 56d115b4-7410-4db2-a9af-bc6716f3358d
title: ICEM08
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c953c40d29458613b0fc2027dd691adb672eb15
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/26/2021
ms.locfileid: "122884214"
---
# <a name="icem08"></a>ICEM08

ICEM08 garantiza que un módulo no excluya otro módulo del que dependa.

## <a name="result"></a>Resultado

ICEM08 publica un error cuando un módulo excluye otro módulo del que depende.

## <a name="example"></a>Ejemplo

ICEM08 publica el siguiente mensaje de error para un módulo que contiene las entradas de base de datos que se muestran en el ejemplo.

``` syntax
Error: This module requires module ModuleB.<GUID> (1033v1.0) but also 
lists it as an exclusion.
```

[ModuleDependency (tabla)](moduledependency-table.md)



| ModuleID             | ModuleLanguage | RequiredID           | RequiredLanguage | RequiredVersion |
|----------------------|----------------|----------------------|------------------|-----------------|
| ModuleA. &lt; GUID&gt; | 3082           | ModuleB. &lt; GUID&gt; | 3082             | 1,0             |



 

[ModuleExclusion Table](moduleexclusion-table.md)



| ModuleID             | ModuleLanguage | ExcludedID           | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------------------|----------------|----------------------|------------------|--------------------|--------------------|
| ModuleA. &lt; GUID&gt; | 3082           | ModuleB. &lt; GUID&gt; | 3082             |                    | 1,0                |



 

Para corregir el error, quite la dependencia o la exclusión. Si ModuleB es una dependencia (RequiredID) de ModuleA, no se puede excluir (como se muestra en la columna ExludedID de la tabla ModuleExclusion). Si debe excluir ModuleB, debe quitar la dependencia de ModuleA en él.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md)
</dt> </dl>

 

 



