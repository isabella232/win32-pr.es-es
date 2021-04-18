---
description: Una clase de vista Union es una Unión lógica de instancias de clase de origen. Una clase de vista Union incluye todas las instancias de las clases de origen a menos que se limiten las instancias mediante la inclusión de una cláusula WHERE en la consulta de origen.
ms.assetid: 54a9804d-644d-4ab6-a3d5-c9c4f7761967
ms.tgt_platform: multiple
title: Crear una clase de vista Union
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2ff9327645828c3db78a82811831f058cc27f202
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707098"
---
# <a name="creating-a-union-view-class"></a>Crear una clase de vista Union

Una clase de vista Union es una Unión lógica de instancias de clase de origen. Una clase de vista Union incluye todas las instancias de las clases de origen a menos que se limiten las instancias mediante la inclusión de una cláusula WHERE en la consulta de origen.

Las clases de vista de Unión son útiles cuando desea ver instancias de clases similares o idénticas que se encuentran en diferentes espacios de nombres o en equipos diferentes. Por ejemplo, puede crear una clase de Unión que contenga instancias de distintas unidades de disco que se van a supervisar.

También puede basar las propiedades de una clase de vista Union en las propiedades que no están presentes en todas las instancias de la clase de origen. Si las instancias de clase de origen no tienen la misma propiedad, las propiedades de las instancias de clase Union tienen un valor **null**. Por ejemplo, si una unidad de disco duro tiene una propiedad de **temperatura** pero otra no, todavía puede crear una unión entre las dos.

En el procedimiento siguiente se describe cómo crear una clase de vista Union.

**Para crear una clase de vista Union**

1.  Comience la definición de clase con el calificador de cadena [**Union**](qualifiers-specific-to-the-view-provider.md) .

    Los calificadores [**joinon**](qualifiers-specific-to-the-view-provider.md), **Association** y **Union** se excluyen mutuamente.

2.  Cree las consultas que definen las clases de origen usadas en la clase de vista con el calificador [**ViewSources**](viewsources-qualifier.md) .
3.  Defina los nombres y la ubicación de los espacios de nombres en los que se encuentran las clases de origen con el calificador [**ViewSpaces**](viewspaces-qualifier.md) .
4.  Defina las propiedades que se asignan a las propiedades de las clases de origen con el calificador [**PropertySources**](propertysources-qualifier.md) .

    Si es necesario, puede etiquetar cualquiera de las propiedades como perteneciente a una clase de origen mediante el calificador [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) .

5.  Defina las propiedades clave de las clases de origen de la clase de vista Union.

    Cada clase de origen debe tener el mismo número de propiedades de clave que coincidan con [**CIMType**](swbemproperty-cimtype.md). Además, las claves de la clase de vista Union deben identificar de forma exclusiva todas las instancias de origen. En algunos casos, es posible que tenga que especificar propiedades del sistema para asegurarse de que las instancias son únicas. Por ejemplo, si crea una vista a partir de la Unión de dos clases idénticas en dos espacios de nombres diferentes, podría incluir la propiedad [**\_ \_ espacio de nombres**](--namespace.md) como una clave en la clase de vista para diferenciar entre las dos instancias. Si usa dos clases similares del mismo espacio de nombres para crear una vista, puede usar la propiedad de **\_ \_ clase** para distinguir entre los dos. Cambie el nombre de las propiedades del sistema en la vista para evitar un conflicto con las propiedades del sistema de la clase de vista.

6.  Defina los métodos que desee mediante el calificador [**MethodSource**](qualifiers-specific-to-the-view-provider.md) .

    A diferencia de otras clases de vista, puede crear métodos para modificar una vista de Unión.

En el ejemplo de código siguiente se describe una clase de vista Union.

``` syntax
[Union, ViewSources{"SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM LocalDisk", 
    "SELECT Description, DeviceID, __Namespace, FileSystem, FreeSpace, VolumeName FROM RemoteDisk"}, 
    ViewSpaces{"\\\\.\\Root\\LocalNamespace","\\\\.\\Root\\RemoteNamespace"}, 
    dynamic: ToInstance, provider("MS_VIEW_INSTANCE_PROVIDER")]

class UnionOfDrives

{
    [PropertySources{"Description", "Description"}] string des;
    [PropertySources{"DeviceID", "DeviceID"}, key] String did;
    [PropertySources{"__Namespace", "__Namespace"}, key] String KEYID;
    [PropertySources{"FileSystem", "FileSystem"}] String fsystem ;
    [PropertySources{"FreeSpace", "FreeSpace"}] uint64 fspace;
    [PropertySources{"VolumeName", "VolumeName"}] String vname;
};
```

 

 



