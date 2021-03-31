---
description: Representa un espacio de nombres WMI.
ms.assetid: d5f0abc7-32cf-4d85-b5cd-5d60c991bcbc
ms.tgt_platform: multiple
title: __Namespace (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- __Namespace
- All
api_type:
- Schema
api_location:
- All
ms.openlocfilehash: 9f396b588f372f26a808e97593ffcc30eac9b3ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103912754"
---
# <a name="__namespace-class"></a><span data-ttu-id="51c06-103">\_\_Namespace (clase)</span><span class="sxs-lookup"><span data-stu-id="51c06-103">\_\_Namespace class</span></span>

<span data-ttu-id="51c06-104">La clase de sistema de **\_ \_ espacio de nombres** representa un espacio de nombres WMI.</span><span class="sxs-lookup"><span data-stu-id="51c06-104">The **\_\_Namespace** system class represents a WMI namespace.</span></span>

<span data-ttu-id="51c06-105">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="51c06-105">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="51c06-106">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="51c06-106">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="51c06-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="51c06-107">Syntax</span></span>

``` syntax
class __Namespace : __SystemClass
{
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="51c06-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="51c06-108">Members</span></span>

<span data-ttu-id="51c06-109">La clase de **\_ \_ espacio de nombres** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="51c06-109">The **\_\_Namespace** class has these types of members:</span></span>

-   [<span data-ttu-id="51c06-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="51c06-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="51c06-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="51c06-111">Properties</span></span>

<span data-ttu-id="51c06-112">La clase de **\_ \_ espacio de nombres** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="51c06-112">The **\_\_Namespace** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="51c06-113">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="51c06-113">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="51c06-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="51c06-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="51c06-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="51c06-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="51c06-116">Calificadores: [ **clave**](standard-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="51c06-116">Qualifiers: [**Key**](standard-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="51c06-117">Nombre del espacio de nombres.</span><span class="sxs-lookup"><span data-stu-id="51c06-117">Namespace name.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="51c06-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="51c06-118">Remarks</span></span>

<span data-ttu-id="51c06-119">La clase de **\_ \_ espacio de nombres** se deriva de [**\_ \_ SystemClass**](--systemclass.md), que no tiene propiedades.</span><span class="sxs-lookup"><span data-stu-id="51c06-119">The **\_\_Namespace** class is derived from [**\_\_SystemClass**](--systemclass.md), which has no properties.</span></span>

<span data-ttu-id="51c06-120">Puede usar el **\_ \_ espacio de nombres** para identificar, crear y eliminar espacios de nombres secundarios en el espacio de nombres de trabajo actual para el que tiene un objeto [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) .</span><span class="sxs-lookup"><span data-stu-id="51c06-120">You can use **\_\_Namespace** to identify, create, and delete child namespaces within the current working namespace for which you have an [**IWbemServices**](/windows/desktop/api/WbemCli/nn-wbemcli-iwbemservices) object.</span></span> <span data-ttu-id="51c06-121">Al crear una nueva instancia del **\_ \_ espacio** de nombres en cualquier espacio de nombres de trabajo, se crea un espacio de nombres secundario en el espacio de nombres de trabajo.</span><span class="sxs-lookup"><span data-stu-id="51c06-121">Creating a new instance of **\_\_Namespace** within any working namespace creates a child namespace within the working namespace.</span></span> <span data-ttu-id="51c06-122">A la inversa, al eliminar una instancia del **\_ \_ espacio de nombres** se quita el espacio de nombres secundario del espacio de nombres de trabajo.</span><span class="sxs-lookup"><span data-stu-id="51c06-122">Conversely, deleting an instance of **\_\_Namespace** removes the child namespace from the working namespace.</span></span> <span data-ttu-id="51c06-123">Tenga en cuenta que al eliminar un espacio de nombres secundario también se eliminan todas sus clases e instancias.</span><span class="sxs-lookup"><span data-stu-id="51c06-123">Note that deleting a child namespace also deletes all of its classes and instances.</span></span>

<span data-ttu-id="51c06-124">La enumeración de instancias de esta clase en cualquier espacio de nombres de trabajo proporciona los espacios de nombres secundarios disponibles.</span><span class="sxs-lookup"><span data-stu-id="51c06-124">Enumerating instances of this class within any working namespace gives the available child namespaces.</span></span>

<span data-ttu-id="51c06-125">Por ejemplo, en el \\ espacio de nombres raíz hay dos instancias de **\_ \_ espacio de nombres**.</span><span class="sxs-lookup"><span data-stu-id="51c06-125">For example, within the \\root namespace are two instances of **\_\_Namespace**.</span></span> <span data-ttu-id="51c06-126">Uno tiene la propiedad **Name** establecida en "default", el otro tiene el **nombre** establecido en "Cimv2".</span><span class="sxs-lookup"><span data-stu-id="51c06-126">One has its **Name** property set to "Default," the other has **Name** set to "Cimv2."</span></span> <span data-ttu-id="51c06-127">Estas instancias representan el \\ \\ valor predeterminado raíz y los \\ espacios de nombres raíz de \\ cimv2, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="51c06-127">These instances represent the \\root\\default, and \\root\\cimv2 namespaces, respectively.</span></span>

## <a name="examples"></a><span data-ttu-id="51c06-128">Ejemplos</span><span class="sxs-lookup"><span data-stu-id="51c06-128">Examples</span></span>

<span data-ttu-id="51c06-129">En el ejemplo de VBScript de [lista de todos los espacios de nombres de WMI](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) de la galería de TechNet se usa una llamada recursiva para mostrar todas las instancias de la clase de espacio de \_ \_ nombres en un sistema.</span><span class="sxs-lookup"><span data-stu-id="51c06-129">The [List All WMI Namespaces](https://Gallery.TechNet.Microsoft.Com/4a8e84f1-4b52-452c-ae4f-e4e00e266257) VBScript example on the TechNet Gallery uses a recursive call to list all instances of the \_\_Namespace class on a system.</span></span>

<span data-ttu-id="51c06-130">En el ejemplo de código siguiente se recuperan todos los espacios de nombres en PowerShell.</span><span class="sxs-lookup"><span data-stu-id="51c06-130">The following code sample retrieves all namespaces in PowerShell.</span></span>


```PowerShell
get-wmiobject __namespace -namespace 'root' -list -recurse | format-table __namespace
```



<span data-ttu-id="51c06-131">En el ejemplo de código siguiente se mejora el ejemplo anterior y se agrega información adicional.</span><span class="sxs-lookup"><span data-stu-id="51c06-131">The following code sample improves on the previous sample, and adds in additional information.</span></span>


```PowerShell
# Set computer name 
$comp = "." 
 
# Get the name spaces on the local computer, and the local computer name 
$Namespace = get-wmiobject __namespace -namespace 'root' -list -recurse -computer $comp  
$hotsname = hostname 
 
# Display number of and names of the namespaces 
"{0} Namespaces on: {1}" -f $namespace.count, $hostname 
$NameSpace| sort __namespace  | Format-Table @{Expression = "__Namespace"; Label = "Namespace"}
```



## <a name="requirements"></a><span data-ttu-id="51c06-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51c06-132">Requirements</span></span>



| <span data-ttu-id="51c06-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="51c06-133">Requirement</span></span> | <span data-ttu-id="51c06-134">Value</span><span class="sxs-lookup"><span data-stu-id="51c06-134">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="51c06-135">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51c06-135">Minimum supported client</span></span><br/> | <span data-ttu-id="51c06-136">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51c06-136">Windows Vista</span></span><br/>       |
| <span data-ttu-id="51c06-137">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="51c06-137">Minimum supported server</span></span><br/> | <span data-ttu-id="51c06-138">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51c06-138">Windows Server 2008</span></span><br/> |
| <span data-ttu-id="51c06-139">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="51c06-139">Namespace</span></span><br/>                | <span data-ttu-id="51c06-140">Todos los espacios de nombres WMI</span><span class="sxs-lookup"><span data-stu-id="51c06-140">All WMI namespaces</span></span><br/>  |



## <a name="see-also"></a><span data-ttu-id="51c06-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="51c06-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51c06-142">**\_\_SystemClass**</span><span class="sxs-lookup"><span data-stu-id="51c06-142">**\_\_SystemClass**</span></span>](--systemclass.md)
</dt> <dt>

[<span data-ttu-id="51c06-143">Clases del sistema WMI</span><span class="sxs-lookup"><span data-stu-id="51c06-143">WMI System Classes</span></span>](wmi-system-classes.md)
</dt> </dl>

 

 




