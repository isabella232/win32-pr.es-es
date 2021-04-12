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
# <a name="associating-instances-between-namespaces"></a><span data-ttu-id="19bdc-103">Asociar instancias entre espacios de nombres</span><span class="sxs-lookup"><span data-stu-id="19bdc-103">Associating Instances Between Namespaces</span></span>

<span data-ttu-id="19bdc-104">Una clase de vista de asociación le permite usar [asociadores de](associators-of-statement.md) consultas en clases que residen en diferentes espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="19bdc-104">An association view class allows you to use [ASSOCIATORS OF](associators-of-statement.md) queries on classes that reside in different namespaces.</span></span>

<span data-ttu-id="19bdc-105">En el procedimiento siguiente se describe cómo asociar instancias entre espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="19bdc-105">The following procedure describes how to associate instances between namespaces.</span></span>

<span data-ttu-id="19bdc-106">**Para asociar instancias entre espacios de nombres**</span><span class="sxs-lookup"><span data-stu-id="19bdc-106">**To associate instances between namespaces**</span></span>

1.  <span data-ttu-id="19bdc-107">Comience la definición de clase con el calificador de cadena de [**Asociación**](meta-qualifiers.md) .</span><span class="sxs-lookup"><span data-stu-id="19bdc-107">Begin your class definition with the [**Association**](meta-qualifiers.md) string qualifier.</span></span>

    <span data-ttu-id="19bdc-108">Los calificadores **joinon**, [**Association**](meta-qualifiers.md)y **Union** se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="19bdc-108">The **JoinOn**, [**Association**](meta-qualifiers.md), and **Union** qualifiers are mutually exclusive.</span></span>

2.  <span data-ttu-id="19bdc-109">Cree las consultas que definen las instancias de origen usadas en la clase de vista con el calificador [**ViewSources**](viewsources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="19bdc-109">Create the queries that define source instances used in the view class with the [**ViewSources**](viewsources-qualifier.md) qualifier.</span></span>
3.  <span data-ttu-id="19bdc-110">Defina los nombres y la ubicación de los espacios de nombres en los que se encuentran las instancias de origen con el calificador [**ViewSpaces**](viewspaces-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="19bdc-110">Define the names and location of the namespaces in which the source instances are located with the [**ViewSpaces**](viewspaces-qualifier.md) qualifier.</span></span>
4.  <span data-ttu-id="19bdc-111">Defina las propiedades que desee en la clase de vista de asociación con el calificador [**PropertySources**](propertysources-qualifier.md) .</span><span class="sxs-lookup"><span data-stu-id="19bdc-111">Define the properties you want in your association view class with the [**PropertySources**](propertysources-qualifier.md) qualifier.</span></span>

    <span data-ttu-id="19bdc-112">Si es necesario, puede etiquetar cualquiera de las propiedades como perteneciente a una clase de origen mediante el calificador [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) .</span><span class="sxs-lookup"><span data-stu-id="19bdc-112">If necessary, you can tag any of the properties as belonging to a source class by using the [**HiddenDefault**](qualifiers-specific-to-the-view-provider.md) qualifier.</span></span>

5.  <span data-ttu-id="19bdc-113">Etiquete cualquier propiedad pertinente con el calificador **Direct** .</span><span class="sxs-lookup"><span data-stu-id="19bdc-113">Tag any relevant properties with the **Direct** qualifier.</span></span>

    <span data-ttu-id="19bdc-114">El calificador **directo** evita que el proveedor de vistas asigne la referencia de asociación etiquetada a una referencia de vista.</span><span class="sxs-lookup"><span data-stu-id="19bdc-114">The **Direct** qualifier prevents the View Provider from mapping the tagged association reference to a view reference.</span></span>

<span data-ttu-id="19bdc-115">En los siguientes ejemplos de código se muestra cómo crear clases de vista de asociación.</span><span class="sxs-lookup"><span data-stu-id="19bdc-115">The following code examples show how to create association view classes.</span></span>

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

 

 



