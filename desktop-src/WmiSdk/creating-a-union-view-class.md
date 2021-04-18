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
# <a name="creating-a-union-view-class"></a><span data-ttu-id="81b77-104">Crear una clase de vista Union</span><span class="sxs-lookup"><span data-stu-id="81b77-104">Creating a Union View Class</span></span>

<span data-ttu-id="81b77-105">Una clase de vista Union es una Unión lógica de instancias de clase de origen.</span><span class="sxs-lookup"><span data-stu-id="81b77-105">A union view class is a logical union of source class instances.</span></span> <span data-ttu-id="81b77-106">Una clase de vista Union incluye todas las instancias de las clases de origen a menos que se limiten las instancias mediante la inclusión de una cláusula WHERE en la consulta de origen.</span><span class="sxs-lookup"><span data-stu-id="81b77-106">A union view class includes all the instances of the source classes unless you limit the instances by including a WHERE clause on the source query.</span></span>

<span data-ttu-id="81b77-107">Las clases de vista de Unión son útiles cuando desea ver instancias de clases similares o idénticas que se encuentran en diferentes espacios de nombres o en equipos diferentes.</span><span class="sxs-lookup"><span data-stu-id="81b77-107">Union view classes are useful when you want to see instances of similar or identical classes that are located in different namespaces or on different computers.</span></span> <span data-ttu-id="81b77-108">Por ejemplo, puede crear una clase de Unión que contenga instancias de distintas unidades de disco que se van a supervisar.</span><span class="sxs-lookup"><span data-stu-id="81b77-108">For example, you can create a union class that contains instances of different disk drives to monitor.</span></span>

<span data-ttu-id="81b77-109">También puede basar las propiedades de una clase de vista Union en las propiedades que no están presentes en todas las instancias de la clase de origen.</span><span class="sxs-lookup"><span data-stu-id="81b77-109">You can also base the properties of a union view class on properties not present in all of the source class instances.</span></span> <span data-ttu-id="81b77-110">Si las instancias de clase de origen no tienen la misma propiedad, las propiedades de las instancias de clase Union tienen un valor **null**.</span><span class="sxs-lookup"><span data-stu-id="81b77-110">If the source class instances do not have the same property, the properties of union class instances have a value of **NULL**.</span></span> <span data-ttu-id="81b77-111">Por ejemplo, si una unidad de disco duro tiene una propiedad de **temperatura** pero otra no, todavía puede crear una unión entre las dos.</span><span class="sxs-lookup"><span data-stu-id="81b77-111">For example, if one hard disk drive has a **temperature** property but another does not, you can still create a union between the two.</span></span>

<span data-ttu-id="81b77-112">En el procedimiento siguiente se describe cómo crear una clase de vista Union.</span><span class="sxs-lookup"><span data-stu-id="81b77-112">The following procedure describes how to create a union view class.</span></span>

<span data-ttu-id="81b77-113">**Para crear una clase de vista Union**</span><span class="sxs-lookup"><span data-stu-id="81b77-113">**To create a union view class**</span></span>

1.  <span data-ttu-id="81b77-114">Comience la definición de clase con el calificador de cadena [**Union**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="81b77-114">Begin your class definition with the [**Union**](qualifiers-specific-to-the-view-provider.md) string qualifier.</span></span>

    <span data-ttu-id="81b77-115">Los calificadores [**joinon**](qualifiers-specific-to-the-view-provider.md), **Association** y **Union** se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="81b77-115">The [**JoinOn**](qualifiers-specific-to-the-view-provider.md), **Association**, and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="81b77-116">Cree las consultas que definen las clases de origen usadas en la clase de vista con el calificador [**ViewSources**](viewsources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="81b77-116">Create the queries that define source classes used in the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
3.  <span data-ttu-id="81b77-117">Defina los nombres y la ubicación de los espacios de nombres en los que se encuentran las clases de origen con el calificador [**ViewSpaces**](viewspaces-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="81b77-117">Define the names and location of the namespaces in which the source classes are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="81b77-118">Defina las propiedades que se asignan a las propiedades de las clases de origen con el calificador [**PropertySources**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="81b77-118">Define the properties that map to the properties in the source classes with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="81b77-119">Si es necesario, puede etiquetar cualquiera de las propiedades como perteneciente a una clase de origen mediante el calificador [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="81b77-119">If necessary, you can tag any of the properties as belonging to a source class by using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

5.  <span data-ttu-id="81b77-120">Defina las propiedades clave de las clases de origen de la clase de vista Union.</span><span class="sxs-lookup"><span data-stu-id="81b77-120">Define the key properties of the source classes of your union view class.</span></span>

    <span data-ttu-id="81b77-121">Cada clase de origen debe tener el mismo número de propiedades de clave que coincidan con [**CIMType**](swbemproperty-cimtype.md).</span><span class="sxs-lookup"><span data-stu-id="81b77-121">Each source class must have the same number of key properties matched by [**CIMType**](swbemproperty-cimtype.md).</span></span> <span data-ttu-id="81b77-122">Además, las claves de la clase de vista Union deben identificar de forma exclusiva todas las instancias de origen.</span><span class="sxs-lookup"><span data-stu-id="81b77-122">Also, the keys of your union view class must uniquely identify all source instances.</span></span> <span data-ttu-id="81b77-123">En algunos casos, es posible que tenga que especificar propiedades del sistema para asegurarse de que las instancias son únicas.</span><span class="sxs-lookup"><span data-stu-id="81b77-123">In some cases, you might need to specify system properties to ensure that instances are unique.</span></span> <span data-ttu-id="81b77-124">Por ejemplo, si crea una vista a partir de la Unión de dos clases idénticas en dos espacios de nombres diferentes, podría incluir la propiedad [**\_ \_ espacio de nombres**](--namespace.md) como una clave en la clase de vista para diferenciar entre las dos instancias.</span><span class="sxs-lookup"><span data-stu-id="81b77-124">For example, if you create a view from the union of two identical classes in two different namespaces, you could include the [**\_\_Namespace**](--namespace.md) property as a key in the view class to differentiate between the two instances.</span></span> <span data-ttu-id="81b77-125">Si usa dos clases similares del mismo espacio de nombres para crear una vista, puede usar la propiedad de **\_ \_ clase** para distinguir entre los dos.</span><span class="sxs-lookup"><span data-stu-id="81b77-125">If you use two similar classes from the same namespace to create a view, you could use the **\_\_Class** property to distinguish between the two.</span></span> <span data-ttu-id="81b77-126">Cambie el nombre de las propiedades del sistema en la vista para evitar un conflicto con las propiedades del sistema de la clase de vista.</span><span class="sxs-lookup"><span data-stu-id="81b77-126">Rename any system properties in the view so you can avoid a conflict with the system properties of the view class.</span></span>

6.  <span data-ttu-id="81b77-127">Defina los métodos que desee mediante el calificador [**MethodSource**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="81b77-127">Define any methods you want using the [**MethodSource**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

    <span data-ttu-id="81b77-128">A diferencia de otras clases de vista, puede crear métodos para modificar una vista de Unión.</span><span class="sxs-lookup"><span data-stu-id="81b77-128">Unlike other view classes, you can create methods to modify a union view.</span></span>

<span data-ttu-id="81b77-129">En el ejemplo de código siguiente se describe una clase de vista Union.</span><span class="sxs-lookup"><span data-stu-id="81b77-129">The following code example describes a union view class.</span></span>

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

 

 



