---
description: ICEM02 comprueba que todas las dependencias del módulo y las exclusiones están relacionadas con el módulo actual.
ms.assetid: c7d77cb6-0ee6-4857-a749-7908e1c5fcda
title: ICEM02
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a9a976132dbfad42e95f4141bc00adb48a544c1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104275760"
---
# <a name="icem02"></a>ICEM02

ICEM02 comprueba que todas las dependencias del módulo y las exclusiones están relacionadas con el módulo actual.

El módulo de combinación ICEs se almacena en un archivo. Cub de módulo de combinación denominado Mergemod. Cub y no en el archivo. Cub que contiene el ICEs usado para la validación del paquete.

## <a name="result"></a>Resultado

ICEM02 envía mensajes de error si la base de datos del módulo intenta especificar dependencias o exclusiones que no se relacionan con el módulo actual. ICEM02 envía un mensaje de error si la base de datos del módulo intenta especificar el módulo actual como dependiente o como excluido por sí mismo.

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

[ModuleSignature (tabla)](modulesignature-table.md)



| ModuleID         | Idioma | Versión |
|------------------|----------|---------|
| MyModule. *GUID1* | 3082     | 1,0     |



 

[Tabla ModuleDependency](moduledependency-table.md)



| ModuleID            | ModuleLanguage | RequiredID          | RequiredLanguage | RequiredVersion |
|---------------------|----------------|---------------------|------------------|-----------------|
| OtherModule. *GUID2* | 3082           | OtherModule. *GUID3* | 0                | 1.0             |
| MyModule. *GUID1*    | 3082           | MyModule. *GUID1*    | 3082             | 1.2             |



 

[Tabla ModuleExclusion](moduleexclusion-table.md) (parcial)



| ModuleID            | ModuleLanguage | ExcludedID          | ExcludedLanguage |
|---------------------|----------------|---------------------|------------------|
| OtherModule. *GUID2* | 3082           | OtherModule. *GUID3* | 0                |
| MyModule. *GUID1*    | 3082           | MyModule. *GUID1*    | 3082             |



 

El módulo de combinación ICE envía el primer error porque el de la primera fila de la tabla ModuleDependency, que no especifica una dependencia necesaria para el módulo actual especificado en la tabla ModuleSignature. Las dependencias de un módulo solo se pueden especificar en su propia tabla ModuleDependency. Si OtherModule. El módulo actual requiere *GUID3* , reemplace las dos primeras columnas de la fila por los datos de la tabla ModuleSignature. Si OtherModule. *GUID3* no es necesario para este módulo, elimine esta fila.

El módulo de combinación ICE envía el segundo error porque un módulo no puede especificar una dependencia en sí mismo.

El módulo de combinación ICE envía el tercer error debido a la primera fila de la tabla ModuleExclusion, que no especifica una exclusión necesaria para el módulo actual especificado en la tabla ModuleSignature. Las exclusiones de un módulo solo se pueden especificar en su propia tabla ModuleExclusion. Si el módulo actual excluye OtherModule. *GUID3*, reemplace las dos primeras columnas de la fila por los datos de la tabla ModuleSignature. Si el módulo actual no excluye OtherModule. *GUID3*, elimine esta fila.

El módulo de combinación ICE envía el cuarto error porque un módulo no puede especificar que se excluya a sí mismo.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de módulo de combinación ICE](merge-module-ice-reference.md)
</dt> </dl>

 

 



