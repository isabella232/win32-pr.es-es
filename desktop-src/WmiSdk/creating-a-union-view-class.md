---
description: Una clase de vista de unión es una unión lógica de instancias de clase de origen. Una clase de vista de unión incluye todas las instancias de las clases de origen a menos que se limiten las instancias mediante la inclusión de una cláusula WHERE en la consulta de origen.
ms.assetid: 54a9804d-644d-4ab6-a3d5-c9c4f7761967
ms.tgt_platform: multiple
title: Crear una clase de vista union
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 3408e3aaec9ee809711b3f400c77ffab5ab2b376eaace3311bd0367f61937c30
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119612395"
---
# <a name="creating-a-union-view-class"></a>Crear una clase de vista union

Una clase de vista de unión es una unión lógica de instancias de clase de origen. Una clase de vista de unión incluye todas las instancias de las clases de origen a menos que se limiten las instancias mediante la inclusión de una cláusula WHERE en la consulta de origen.

Las clases de vista de unión son útiles cuando se quieren ver instancias de clases similares o idénticas que se encuentran en espacios de nombres diferentes o en equipos diferentes. Por ejemplo, puede crear una clase de unión que contenga instancias de diferentes unidades de disco para supervisar.

También puede basar las propiedades de una clase de vista de unión en propiedades que no están presentes en todas las instancias de clase de origen. Si las instancias de clase de origen no tienen la misma propiedad, las propiedades de las instancias de clase de unión tienen un valor **null.** Por ejemplo, si una unidad de disco duro tiene una propiedad **temperature** pero otra no, puede crear una unión entre los dos.

En el procedimiento siguiente se describe cómo crear una clase de vista de unión.

**Para crear una clase de vista de unión**

1.  Comience la definición de clase con el [**calificador de**](qualifiers-specific-to-the-view-provider.md) cadena Union.

    Los [**calificadores JoinOn,**](qualifiers-specific-to-the-view-provider.md) **Association** y **Union** son mutuamente excluyentes.

2.  Cree las consultas que definen las clases de origen usadas en la clase de vista con el [**calificador ViewSources.**](viewsources-qualifier.md)
3.  Defina los nombres y la ubicación de los espacios de nombres en los que se encuentran las clases de origen con el [**calificador ViewSpaces.**](viewspaces-qualifier.md)
4.  Defina las propiedades que se asignan a las propiedades de las clases de origen con el [**calificador PropertySources.**](propertysources-qualifier.md)

    Si es necesario, puede etiquetar cualquiera de las propiedades como pertenecientes a una clase de origen mediante el [**calificador HiddenDefault.**](qualifiers-specific-to-the-view-provider.md)

5.  Defina las propiedades clave de las clases de origen de la clase de vista de unión.

    Cada clase de origen debe tener el mismo número de propiedades de clave coincidentes con [**CIMType**](swbemproperty-cimtype.md). Además, las claves de la clase de vista de unión deben identificar de forma única todas las instancias de origen. En algunos casos, es posible que deba especificar las propiedades del sistema para asegurarse de que las instancias son únicas. Por ejemplo, si crea una vista a partir de la unión de dos clases idénticas en dos espacios de nombres diferentes, podría incluir la propiedad [**\_ \_ Namespace**](--namespace.md) como clave en la clase de vista para diferenciar entre las dos instancias. Si usa dos clases similares del mismo espacio de nombres para crear una vista, podría usar la **\_ \_ propiedad Class** para distinguir entre las dos. Cambie el nombre de las propiedades del sistema de la vista para evitar conflictos con las propiedades del sistema de la clase de vista.

6.  Defina los métodos que desee mediante el [**calificador MethodSource.**](qualifiers-specific-to-the-view-provider.md)

    A diferencia de otras clases de vista, puede crear métodos para modificar una vista de unión.

En el ejemplo de código siguiente se describe una clase de vista de unión.

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

 

 



