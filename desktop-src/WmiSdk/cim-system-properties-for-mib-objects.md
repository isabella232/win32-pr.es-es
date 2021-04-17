---
description: WMI define un conjunto de propiedades del sistema que están asociadas a todas las clases e instancias de clases, además de a las propiedades específicas de la clase.
ms.assetid: ea8ca4e4-9969-48fc-9b9f-5a5c8442006d
ms.tgt_platform: multiple
title: Propiedades del sistema CIM para objetos MIB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0425afecc399c3cd1399e8bf565908b1c7c5d2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105716206"
---
# <a name="cim-system-properties-for-mib-objects"></a><span data-ttu-id="32b9b-103">Propiedades del sistema CIM para objetos MIB</span><span class="sxs-lookup"><span data-stu-id="32b9b-103">CIM System Properties for MIB Objects</span></span>

<span data-ttu-id="32b9b-104">WMI define un conjunto de propiedades del sistema que están asociadas a todas las clases e instancias de clases, además de a las propiedades específicas de la clase.</span><span class="sxs-lookup"><span data-stu-id="32b9b-104">WMI defines a set of system properties that are associated with all classes and instances of classes in addition to class-specific properties.</span></span>

> [!Note]  
> <span data-ttu-id="32b9b-105">Para obtener más información acerca de cómo instalar el proveedor, consulte [configuración del entorno WMI SNMP](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="32b9b-105">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="32b9b-106">El proveedor SNMP utiliza las siguientes propiedades del sistema CIM al asignar definiciones de objeto MIB a definiciones de clase CIM.</span><span class="sxs-lookup"><span data-stu-id="32b9b-106">The SNMP Provider uses the following CIM system properties when mapping MIB object definitions to CIM class definitions.</span></span> <span data-ttu-id="32b9b-107">Deben existir propiedades obligatorias para que el proveedor SNMP resuelva por completo un objeto de grupo.</span><span class="sxs-lookup"><span data-stu-id="32b9b-107">Mandatory properties must be present for the SNMP Provider to fully resolve a group object.</span></span> <span data-ttu-id="32b9b-108">Si no se define una propiedad obligatoria, se devuelve un error.</span><span class="sxs-lookup"><span data-stu-id="32b9b-108">Failure to define a mandatory property returns an error.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="32b9b-109">Propiedad</span><span class="sxs-lookup"><span data-stu-id="32b9b-109">Property</span></span></th>
<th><span data-ttu-id="32b9b-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="32b9b-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="32b9b-111"><strong>__CLASS</strong></span><span class="sxs-lookup"><span data-stu-id="32b9b-111"><strong>__CLASS</strong></span></span></td>
<td><span data-ttu-id="32b9b-112"><strong>cadena</strong> Obligación</span><span class="sxs-lookup"><span data-stu-id="32b9b-112"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="32b9b-113">En el caso de las instancias, la clase a la que pertenece el objeto.</span><span class="sxs-lookup"><span data-stu-id="32b9b-113">For instances, the class to which the object belongs.</span></span> <span data-ttu-id="32b9b-114">En el caso de las clases, es el nombre de clase.</span><span class="sxs-lookup"><span data-stu-id="32b9b-114">For classes, this is the class name.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32b9b-115"><strong>__DYNASTY</strong></span><span class="sxs-lookup"><span data-stu-id="32b9b-115"><strong>__DYNASTY</strong></span></span></td>
<td><span data-ttu-id="32b9b-116"><strong>cadena</strong> Opta</span><span class="sxs-lookup"><span data-stu-id="32b9b-116"><strong>string</strong>Optional</span></span><br/> <span data-ttu-id="32b9b-117">Nombre de la clase que es la clase base Ultimate del objeto actual (no su clase primaria inmediata).</span><span class="sxs-lookup"><span data-stu-id="32b9b-117">Name of the class that is the ultimate base class for the current object (not its immediate parent class).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32b9b-118"><strong>__GENUS</strong></span><span class="sxs-lookup"><span data-stu-id="32b9b-118"><strong>__GENUS</strong></span></span></td>
<td><span data-ttu-id="32b9b-119"><strong>UInt32</strong> Obligación</span><span class="sxs-lookup"><span data-stu-id="32b9b-119"><strong>uint32</strong>Mandatory</span></span><br/> <span data-ttu-id="32b9b-120">Tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="32b9b-120">Type of object.</span></span> <span data-ttu-id="32b9b-121">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="32b9b-121">Values are:</span></span><br/> <dl> <span data-ttu-id="32b9b-122">1 = clase</span><span class="sxs-lookup"><span data-stu-id="32b9b-122">1 = class</span></span><br />
<span data-ttu-id="32b9b-123">2 = instancia</span><span class="sxs-lookup"><span data-stu-id="32b9b-123">2 = instance</span></span><br />
</dl></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32b9b-124"><strong>__NAMESPACE</strong></span><span class="sxs-lookup"><span data-stu-id="32b9b-124"><strong>__NAMESPACE</strong></span></span></td>
<td><span data-ttu-id="32b9b-125"><strong>cadena</strong> Obligación</span><span class="sxs-lookup"><span data-stu-id="32b9b-125"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="32b9b-126">Espacio de nombres donde se encuentra el objeto.</span><span class="sxs-lookup"><span data-stu-id="32b9b-126">Namespace where the object is located.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32b9b-127"><strong>__PATH</strong></span><span class="sxs-lookup"><span data-stu-id="32b9b-127"><strong>__PATH</strong></span></span></td>
<td><span data-ttu-id="32b9b-128"><strong>cadena</strong> Obligación</span><span class="sxs-lookup"><span data-stu-id="32b9b-128"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="32b9b-129">Ruta de acceso absoluta al objeto.</span><span class="sxs-lookup"><span data-stu-id="32b9b-129">Absolute path to the object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32b9b-130"><strong>__PROPERTYCOUNT</strong></span><span class="sxs-lookup"><span data-stu-id="32b9b-130"><strong>__PROPERTYCOUNT</strong></span></span></td>
<td><span data-ttu-id="32b9b-131"><strong>UInt32</strong> Obligación</span><span class="sxs-lookup"><span data-stu-id="32b9b-131"><strong>uint32</strong>Mandatory</span></span><br/> <span data-ttu-id="32b9b-132">Número de propiedades que no son del sistema definidas para el objeto.</span><span class="sxs-lookup"><span data-stu-id="32b9b-132">Number of non-system properties defined for the object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32b9b-133"><strong>__RELPATH</strong></span><span class="sxs-lookup"><span data-stu-id="32b9b-133"><strong>__RELPATH</strong></span></span></td>
<td><span data-ttu-id="32b9b-134"><strong>cadena</strong> Obligación</span><span class="sxs-lookup"><span data-stu-id="32b9b-134"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="32b9b-135">Ruta de acceso relativa al objeto.</span><span class="sxs-lookup"><span data-stu-id="32b9b-135">Relative path to the object.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="32b9b-136"><strong>__SERVER</strong></span><span class="sxs-lookup"><span data-stu-id="32b9b-136"><strong>__SERVER</strong></span></span></td>
<td><span data-ttu-id="32b9b-137"><strong>cadena</strong> Obligación</span><span class="sxs-lookup"><span data-stu-id="32b9b-137"><strong>string</strong>Mandatory</span></span><br/> <span data-ttu-id="32b9b-138">Servidor que proporciona el objeto.</span><span class="sxs-lookup"><span data-stu-id="32b9b-138">Server supplying the object.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="32b9b-139"><strong>__SUPERCLASS</strong></span><span class="sxs-lookup"><span data-stu-id="32b9b-139"><strong>__SUPERCLASS</strong></span></span></td>
<td><span data-ttu-id="32b9b-140"><strong>cadena</strong> Opta</span><span class="sxs-lookup"><span data-stu-id="32b9b-140"><strong>string</strong>Optional</span></span><br/> <span data-ttu-id="32b9b-141">Clase primaria inmediata del objeto.</span><span class="sxs-lookup"><span data-stu-id="32b9b-141">Immediate parent class of the object.</span></span><br/></td>
</tr>
</tbody>
</table>



 

 

 




