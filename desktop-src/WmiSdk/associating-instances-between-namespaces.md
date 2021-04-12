---
description: Una clase de vista de asociación le permite usar ASOCIAdores de consultas en clases que residen en diferentes espacios de nombres.
ms.assetid: 4af4fe1b-2b19-472e-8261-798b374ae57e
ms.tgt_platform: multiple
title: Asociar instancias entre espacios de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8347d3a35f06f72d3344f5c12606d82709a1370
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104360844"
---
# <a name="associating-instances-between-namespaces"></a>Asociar instancias entre espacios de nombres

Una clase de vista de asociación le permite usar [asociadores de](associators-of-statement.md) consultas en clases que residen en diferentes espacios de nombres.

En el procedimiento siguiente se describe cómo asociar instancias entre espacios de nombres.

**Para asociar instancias entre espacios de nombres**

1.  Comience la definición de clase con el calificador de cadena de [**Asociación**](meta-qualifiers.md) .

    Los calificadores **joinon**, [**Association**](meta-qualifiers.md)y **Union** se excluyen mutuamente.

2.  Cree las consultas que definen las instancias de origen usadas en la clase de vista con el calificador [**ViewSources**](viewsources-qualifier.md) .
3.  Defina los nombres y la ubicación de los espacios de nombres en los que se encuentran las instancias de origen con el calificador [**ViewSpaces**](viewspaces-qualifier.md) .
4.  Defina las propiedades que desee en la clase de vista de asociación con el calificador [**PropertySources**](propertysources-qualifier.md) .

    Si es necesario, puede etiquetar cualquiera de las propiedades como perteneciente a una clase de origen mediante el calificador [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) .

5.  Etiquete cualquier propiedad pertinente con el calificador **Direct** .

    El calificador **directo** evita que el proveedor de vistas asigne la referencia de asociación etiquetada a una referencia de vista.

En los siguientes ejemplos de código se muestra cómo crear clases de vista de asociación.

``` syntax
[union,
ViewSources {"SELECT * FROM Win32_OperatingSystem"},
    ViewSpaces {"\\\\.\\root\\cimv2"},
    dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Union_OS_For_AssociationExample
{
    [key, PropertySources{"Name"}]
    string Name;

    [PropertySources{"Version"}]
    string Version;

    [PropertySources{"BuildNumber"}]
    string BuildNumber;
};

[
Association,
ViewSources {"SELECT * FROM Win32_SystemOperatingSystem"}, 
ViewSpaces {"\\\\.\\root\\cimv2"},
dynamic, provider("MS_VIEW_INSTANCE_PROVIDER")
]
class Association_SystemViewOperatingSystem
{
    [Direct, key, PropertySources{"GroupComponent"}]
    Win32_ComputerSystem ref Computer;
    
    [key, PropertySources{"PartComponent"}]
    Union_OS_For_AssociationExample ref OperatingSystem;
};
```

 

 



