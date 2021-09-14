---
description: ICE25 valida que un archivo .msi cumple todas sus dependencias y exclusiones internas del módulo de combinación.
ms.assetid: e6e3ea44-a1d4-451a-b326-e8fb7ed4adeb
title: ICE25
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0d966c4c374d6e61e30b44a41ad88bed8bf907f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074638"
---
# <a name="ice25"></a>ICE25

ICE25 valida que un archivo .msi cumpla todas [](merge-modules.md) sus dependencias y exclusiones internas del módulo de combinación. ICE valida lo siguiente:

-   Que todas las dependencias del módulo de combinación indicadas en la tabla [ModuleDependency](moduledependency-table.md) del archivo .msi se satisfacen mediante al menos un módulo de combinación enumerado en la [tabla ModuleSignature](modulesignature-table.md).
-   Que ninguno de los módulos de combinación excluidos de la [tabla ModuleExclusion](moduleexclusion-table.md) es incompatible con los módulos de combinación enumerados en [la tabla ModuleSignature](modulesignature-table.md).

## <a name="result"></a>Resultado

ICE25 envía un mensaje de error si .msi archivo se ha combinado previamente con un módulo de combinación incompatible o si no se ha combinado con un módulo de combinación necesario.

## <a name="example"></a>Ejemplo

ICE25 publica los siguientes errores para el ejemplo mostrado.

``` syntax
Dependency failure: Need ModuleX@0 v2.0 
Module ModuleB@1033 v1.0 is excluded.
```

[ModuleSignature Table](modulesignature-table.md)



| ModuleID | Idioma | Versión |
|----------|----------|---------|
| ModuleA  | 0        | 1.0     |
| ModuleB  | 3082     | 1.0     |



 

[ModuleDependency Table](moduledependency-table.md)



| ModuleID | ModuleLanguage | RequiredID | RequiredLanguage | RequiredVersion |
|----------|----------------|------------|------------------|-----------------|
| ModuleA  | 0              | ModuleX    | 0                | 2.0             |



 

[ModuleExclusion Table](moduleexclusion-table.md)



| ModuleID | ModuleLanguage | ExcludedID | ExcludedLanguage | ExcludedMinVersion | ExcludedMaxVersion |
|----------|----------------|------------|------------------|--------------------|--------------------|
| ModuleA  | 0              | ModuleB    | 3082             |                    |                    |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE](ice-reference.md)
</dt> </dl>

 

 



