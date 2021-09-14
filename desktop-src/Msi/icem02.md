---
description: ICEM02 comprueba que todas las dependencias y exclusiones del módulo están relacionadas con el módulo actual.
ms.assetid: c7d77cb6-0ee6-4857-a749-7908e1c5fcda
title: ICEM02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a976132dbfad42e95f4141bc00adb48a544c1b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074490"
---
# <a name="icem02"></a>ICEM02

ICEM02 comprueba que todas las dependencias y exclusiones del módulo están relacionadas con el módulo actual.

Los ICE del módulo de mezcla se almacenan en un archivo .cub del módulo de mezcla denominado Mergemod.pack y no en el archivo .pack que contiene los ICE usados para la validación del paquete.

## <a name="result"></a>Resultado

ICEM02 publica mensajes de error si la base de datos del módulo intenta especificar dependencias o exclusiones que no están relacionadas con el módulo actual. ICEM02 envía un mensaje de error si la base de datos del módulo intenta especificar el módulo actual como dependiente o como excluido por sí mismo.

## <a name="example"></a>Ejemplo

ICEM02 publicaría los siguientes mensajes de error para un módulo que contiene las entradas de base de datos que se muestran a continuación.

``` syntax
The dependency OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleDependency table creates a dependency for an unrelated module. A 
module can only define dependencies for itself

This module is listed as depending on itself!

The exclusion OtherModule.GUID2.1033.OtherModule.GUID3.0 in the 
ModuleExclusion table creates an excluded module for an unrelated 
module. A module can only define exclusions for itself.

This module excludes itself from the target database!
```

[ModuleSignature Table](modulesignature-table.md)



| ModuleID         | Idioma | Versión |
|------------------|----------|---------|
| Mimodulo. *GUID1* | 3082     | 1.0     |



 

[ModuleDependency (tabla)](moduledependency-table.md)



| ModuleID            | ModuleLanguage | RequiredID          | RequiredLanguage | RequiredVersion |
|---------------------|----------------|---------------------|------------------|-----------------|
| OtherModule. *GUID2* | 3082           | OtherModule. *GUID3* | 0                | 1.0             |
| Mimodulo. *GUID1*    | 3082           | Mimodulo. *GUID1*    | 3082             | 1.2             |



 

[Tabla ModuleExclusion](moduleexclusion-table.md) (parcial)



| ModuleID            | ModuleLanguage | ExcludedID          | ExcludedLanguage |
|---------------------|----------------|---------------------|------------------|
| OtherModule. *GUID2* | 3082           | OtherModule. *GUID3* | 0                |
| Mimodulo. *GUID1*    | 3082           | Mimodulo. *GUID1*    | 3082             |



 

El módulo de mezcla ICE publica el primer error porque el de la primera fila de la tabla ModuleDependency, que no especifica una dependencia necesaria para el módulo actual especificado en la tabla ModuleSignature. Las dependencias de un módulo solo se pueden especificar en su propia tabla ModuleDependency. Si Es OtherModule. El módulo actual requiere *GUID3,* reemplace las dos primeras columnas de la fila por los datos de la tabla ModuleSignature. Si Es OtherModule. *Guid3* no es necesario para este módulo, elimine esta fila.

El ICE del módulo de mezcla publica el segundo error porque un módulo no puede especificar una dependencia en sí mismo.

El módulo de mezcla ICE publica el tercer error debido a la primera fila de la tabla ModuleExclusion, que no especifica una exclusión necesaria para el módulo actual especificado en la tabla ModuleSignature. Las exclusiones de un módulo solo se pueden especificar en su propia tabla ModuleExclusion. Si el módulo actual excluye OtherModule. *GUID3*, reemplace las dos primeras columnas de la fila por los datos de la tabla ModuleSignature. Si el módulo actual no excluye OtherModule. *GUID3,* elimine esta fila.

El ICE del módulo de mezcla publica el cuarto error porque un módulo no puede especificar que se excluya a sí mismo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de ICE del módulo de mezcla](merge-module-ice-reference.md)
</dt> </dl>

 

 



