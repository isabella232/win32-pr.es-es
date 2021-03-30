---
description: Todas las clases de vista deben tener un calificador de matriz de cadenas denominado ViewSources.
ms.assetid: aefa8cda-962f-4f6c-92a0-a8825d48db60
ms.tgt_platform: multiple
title: Calificador ViewSources
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ViewSources
api_type:
- NA
api_location: ''
ms.openlocfilehash: 1f39146f8065401052c352472b28c4946cca6b98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815371"
---
# <a name="viewsources-qualifier"></a><span data-ttu-id="3e6f2-103">Calificador ViewSources</span><span class="sxs-lookup"><span data-stu-id="3e6f2-103">ViewSources Qualifier</span></span>

<span data-ttu-id="3e6f2-104">Todas las clases de vista deben tener un calificador de matriz de cadenas denominado **ViewSources**.</span><span class="sxs-lookup"><span data-stu-id="3e6f2-104">All view classes must have a string array qualifier called **ViewSources**.</span></span> <span data-ttu-id="3e6f2-105">El calificador **ViewSources** contiene las consultas de origen que definen las instancias de origen usadas en la clase de vista.</span><span class="sxs-lookup"><span data-stu-id="3e6f2-105">The **ViewSources** qualifier contains the source queries that define the source instances used in the view class.</span></span> <span data-ttu-id="3e6f2-106">El valor del calificador **ViewSources** es una matriz de cadenas que contiene consultas [*lenguaje de consulta de WMI (WQL)*](gloss-w.md) .</span><span class="sxs-lookup"><span data-stu-id="3e6f2-106">The value of the **ViewSources** qualifier is a string array containing [*WMI Query Language (WQL)*](gloss-w.md) queries.</span></span> <span data-ttu-id="3e6f2-107">Puede definir clases de origen y restringir las instancias de origen que utiliza la clase de vista con la cláusula de [consulta con WQL](querying-with-wql.md)[Where](where-clause.md) para crear una vista filtrada.</span><span class="sxs-lookup"><span data-stu-id="3e6f2-107">You can define source classes and restrict the source instances your view class uses with the [Querying with WQL](querying-with-wql.md)[WHERE Clause](where-clause.md) to create a filtered view.</span></span>

<span data-ttu-id="3e6f2-108">El [proveedor de vistas](view-provider.md) hace coincidir las consultas de origen del calificador **ViewSources** con los espacios de nombres enumerados en el [calificador ViewSpaces](viewspaces-qualifier.md) en el orden en que se muestran las consultas y los espacios de nombres.</span><span class="sxs-lookup"><span data-stu-id="3e6f2-108">The [View Provider](view-provider.md) matches the source queries in the **ViewSources** qualifier to the namespaces listed in the [ViewSpaces qualifier](viewspaces-qualifier.md) in the order the queries and namespaces are listed.</span></span> <span data-ttu-id="3e6f2-109">El número de consultas de origen debe coincidir con el número de espacios de nombres enumerados en el calificador ViewSpaces.</span><span class="sxs-lookup"><span data-stu-id="3e6f2-109">The number of source queries must match the number of namespaces listed in the ViewSpaces qualifier.</span></span> <span data-ttu-id="3e6f2-110">El orden en que se enumeran las consultas de origen determina los espacios de nombres desde los que se dibujan las instancias de origen.</span><span class="sxs-lookup"><span data-stu-id="3e6f2-110">The order in which you list the source queries determines the namespaces from which the source instances are drawn.</span></span>

<span data-ttu-id="3e6f2-111">En el ejemplo siguiente se seleccionan solo las instancias de la clase **LocalDisk** en las que el valor de la propiedad **FILESYSTEM** es "NTFS" y las instancias de la clase **RemoteDisk** en las que el valor de la propiedad **FreeSpace** es mayor que 45 megabytes:</span><span class="sxs-lookup"><span data-stu-id="3e6f2-111">The following example selects only instances of the **LocalDisk** class where the value of the **FileSystem** property is "NTFS" and instances of the **RemoteDisk** class where the value of the **FreeSpace** property is greater than 45 megabytes:</span></span>


```sql
ViewSources{
"SELECT __Namespace, 
   Description, 
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM LocalDisk 
 WHERE FileSystem = \"NTFS\"", 
   "SELECT __Namespace, 
   Description,
   DeviceID, 
   FileSystem, 
   FreeSpace, 
   VolumeName FROM RemoteDisk 
 WHERE FreeSpace > 45000000"}
```



> [!Note]  
> <span data-ttu-id="3e6f2-112">El número de consultas de origen que se pueden definir para las clases de vista de combinación depende del número de instancias devueltas por estas consultas y de cuántas formas se pueden combinar con estas instancias.</span><span class="sxs-lookup"><span data-stu-id="3e6f2-112">The number of source queries you can define for join view classes depends on the number of instances these queries return and how many ways these instances can be joined.</span></span> <span data-ttu-id="3e6f2-113">El número de combinaciones posibles de instancias de origen para las clases de vista crece exponencialmente, por lo que las consultas de código fuente para las clases de vista de combinación son lo más sencillas posible.</span><span class="sxs-lookup"><span data-stu-id="3e6f2-113">The number of possible combinations of source instances for view classes grows exponentially, so keep source queries for join view classes as simple as possible.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3e6f2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e6f2-114">Requirements</span></span>



| <span data-ttu-id="3e6f2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e6f2-115">Requirement</span></span> | <span data-ttu-id="3e6f2-116">Value</span><span class="sxs-lookup"><span data-stu-id="3e6f2-116">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3e6f2-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e6f2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3e6f2-118">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3e6f2-118">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3e6f2-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3e6f2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3e6f2-120">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3e6f2-120">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3e6f2-121">Vea también</span><span class="sxs-lookup"><span data-stu-id="3e6f2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e6f2-122">**Calificadores específicos del proveedor de vistas**</span><span class="sxs-lookup"><span data-stu-id="3e6f2-122">**Qualifiers Specific to the View Provider**</span></span>](qualifiers-specific-to-the-view-provider.md)
</dt> </dl>

 

 




