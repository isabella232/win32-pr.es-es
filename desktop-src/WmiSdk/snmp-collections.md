---
description: Una colección SNMP se asigna a una clase CIM y los elementos de una colección se asignan a las propiedades de una clase CIM. Todas las definiciones de clases CIM generadas deben derivarse de la clase SnmpObjectType.
ms.assetid: e6f82fd6-e3d8-48c5-8c7b-a30a2d502f41
ms.tgt_platform: multiple
title: Colecciones SNMP
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: a85473a394ce715ff9759e974a47824e5621509f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715752"
---
# <a name="snmp-collections"></a><span data-ttu-id="7d3f4-104">Colecciones SNMP</span><span class="sxs-lookup"><span data-stu-id="7d3f4-104">SNMP Collections</span></span>

<span data-ttu-id="7d3f4-105">Una colección SNMP se asigna a una clase CIM y los elementos de una colección se asignan a las propiedades de una clase CIM.</span><span class="sxs-lookup"><span data-stu-id="7d3f4-105">An SNMP collection maps to a CIM class and the elements of a collection map to the properties of a CIM class.</span></span> <span data-ttu-id="7d3f4-106">Todas las definiciones de clases CIM generadas deben derivarse de la clase **SnmpObjectType** .</span><span class="sxs-lookup"><span data-stu-id="7d3f4-106">All generated CIM class definitions must be derived from the **SnmpObjectType** class.</span></span>

> [!Note]  
> <span data-ttu-id="7d3f4-107">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="7d3f4-107">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="7d3f4-108">Las siguientes definiciones de clase primarias todas las definiciones de clase generadas:</span><span class="sxs-lookup"><span data-stu-id="7d3f4-108">The following class definitions parent all generated class definitions:</span></span>

``` syntax
[abstract]
class SnmpMacro
{
};

[abstract]
class SnmpObjectType:SnmpMacro
{
};
```

## <a name="remarks"></a><span data-ttu-id="7d3f4-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7d3f4-109">Remarks</span></span>

<span data-ttu-id="7d3f4-110">Las siguientes reglas se aplican al asignar colecciones SNMP a clases CIM.</span><span class="sxs-lookup"><span data-stu-id="7d3f4-110">The following rules apply when mapping SNMP collections to CIM classes.</span></span> <span data-ttu-id="7d3f4-111">A menos que se especifique lo contrario, estas reglas se aplican a las colecciones escalares y de tabla:</span><span class="sxs-lookup"><span data-stu-id="7d3f4-111">Unless otherwise specified, these rules apply to both scalar and table collections:</span></span>

-   <span data-ttu-id="7d3f4-112">El proceso de asignación genera nombres de clase CIM mediante la concatenación de "SNMP \_ ", el nombre de identidad del módulo MIB, " \_ " y el descriptor de objeto de la colección.</span><span class="sxs-lookup"><span data-stu-id="7d3f4-112">The mapping process generates CIM class names by concatenating "SNMP\_", the MIB module identity name, "\_", and the collection's object descriptor.</span></span>

    <span data-ttu-id="7d3f4-113">Por ejemplo: **sistema** se traduce al **\_ \_ \_ sistema MIB SNMP RFC1213**, mientras que **ifTable** se traduce en **SNMP \_ RFC1213 \_ MIB \_ ifTable**.</span><span class="sxs-lookup"><span data-stu-id="7d3f4-113">For example: **system** translates to **SNMP\_RFC1213\_MIB\_system**, while **ifTable** translates to **SNMP\_RFC1213\_MIB\_ifTable**.</span></span>

-   <span data-ttu-id="7d3f4-114">En todos los casos, los guiones (-) de los identificadores SNMP MIB se asignan a los guiones bajos ( \_ ) en los nombres de clase CIM.</span><span class="sxs-lookup"><span data-stu-id="7d3f4-114">In all cases, hyphens (-) in SNMP MIB identifiers map to underscores (\_) in CIM class names.</span></span>
-   <span data-ttu-id="7d3f4-115">Pueden producirse conflictos de nomenclatura debido a que el nombre de CIM no distingue mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="7d3f4-115">Naming conflicts can occur due to CIM name case-insensitivity.</span></span> <span data-ttu-id="7d3f4-116">Si se produce un conflicto de nomenclatura, el proveedor elige una de las definiciones de grupo en conflicto y omite las definiciones restantes.</span><span class="sxs-lookup"><span data-stu-id="7d3f4-116">If a naming conflict occurs, the provider chooses one of the conflicting group definitions and ignores the remaining definitions.</span></span>
-   <span data-ttu-id="7d3f4-117">El nombre de identidad del módulo MIB que contiene la colección se asigna al **\_ nombre del módulo** calificador de clase CIM.</span><span class="sxs-lookup"><span data-stu-id="7d3f4-117">The identity name of the MIB module that contains the collection maps to the CIM class qualifier **Module\_Name**.</span></span>
-   <span data-ttu-id="7d3f4-118">El identificador de objeto de la colección fabricada se asigna al **grupo \_** de calificador de clase CIM.</span><span class="sxs-lookup"><span data-stu-id="7d3f4-118">The object identifier of the fabricated collection maps to the CIM class qualifier **Group\_Objectid**.</span></span>
-   <span data-ttu-id="7d3f4-119">La lista de importaciones de módulos MIB (obtenida de la definición de macro **de identidad de módulo** ) se asigna a las **\_ importaciones del módulo** calificador de clase CIM.</span><span class="sxs-lookup"><span data-stu-id="7d3f4-119">The MIB module imports list (obtained from the **MODULE-IDENTITY** macro definition) maps to the CIM class qualifier **module\_imports**.</span></span> <span data-ttu-id="7d3f4-120">Este calificador contiene una lista separada por comas de nombres de módulos.</span><span class="sxs-lookup"><span data-stu-id="7d3f4-120">This qualifier contains a comma-separated list of module names.</span></span>

 

 



