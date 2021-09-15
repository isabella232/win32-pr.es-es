---
description: Una clase de vista de asociación permite usar consultas ASSOCIATORS OF en clases que residen en espacios de nombres diferentes.
ms.assetid: 4af4fe1b-2b19-472e-8261-798b374ae57e
ms.tgt_platform: multiple
title: Asociación de instancias entre espacios de nombres
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8347d3a35f06f72d3344f5c12606d82709a1370
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127568081"
---
# <a name="associating-instances-between-namespaces"></a>Asociación de instancias entre espacios de nombres

Una clase de vista de asociación permite usar [consultas ASSOCIATORS OF](associators-of-statement.md) en clases que residen en espacios de nombres diferentes.

En el procedimiento siguiente se describe cómo asociar instancias entre espacios de nombres.

**Para asociar instancias entre espacios de nombres**

1.  Comience la definición de clase con el [**calificador de cadena Association.**](meta-qualifiers.md)

    Los **calificadores JoinOn,** [**Association**](meta-qualifiers.md)y **Union** son mutuamente excluyentes.

2.  Cree las consultas que definen las instancias de origen usadas en la clase de vista con el [**calificador ViewSources.**](viewsources-qualifier.md)
3.  Defina los nombres y la ubicación de los espacios de nombres en los que se encuentran las instancias de origen con el [**calificador ViewSpaces.**](viewspaces-qualifier.md)
4.  Defina las propiedades que desee en la clase de vista de asociación con el [**calificador PropertySources.**](propertysources-qualifier.md)

    Si es necesario, puede etiquetar cualquiera de las propiedades como pertenecientes a una clase de origen mediante el [**calificador HiddenDefault.**](qualifiers-specific-to-the-view-provider.md)

5.  Etiquete las propiedades pertinentes con el **calificador Directo.**

    El **calificador Directo** impide que el proveedor de vistas a mapping la referencia de asociación etiquetada a una referencia de vista.

En los ejemplos de código siguientes se muestra cómo crear clases de vista de asociación.

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

 

 



