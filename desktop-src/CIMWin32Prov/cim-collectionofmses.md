---
description: El \_ objeto CIM CollectionOfMSEs permite la agrupación de \_ objetos MANAGEDSYSTEMELEMENT de CIM con el fin de asociar configuraciones y configuraciones. Es abstracto requerir más definición y perfeccionamiento semántico en las subclases.
ms.assetid: 9448a7a1-defc-4bac-9ce6-29ec2406d573
ms.tgt_platform: multiple
title: CIM_CollectionOfMSEs (clase) (proveedores WMI de CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfMSEs
- CIM_CollectionOfMSEs.Caption
- CIM_CollectionOfMSEs.CollectionID
- CIM_CollectionOfMSEs.Description
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 57942dd6e00d819e4375ddd316e5e15126621b97
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153242"
---
# <a name="cim_collectionofmses-class-cimwin32-wmi-providers"></a><span data-ttu-id="6716f-104">CIM_CollectionOfMSEs (clase) (proveedores WMI de CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="6716f-104">CIM_CollectionOfMSEs class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="6716f-105">El objeto **CIM \_ CollectionOfMSEs** permite la agrupación de objetos [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md) con el fin de asociar configuraciones y configuraciones.</span><span class="sxs-lookup"><span data-stu-id="6716f-105">The **CIM\_CollectionOfMSEs** object allows the grouping of [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) objects for the purpose of associating settings and configurations.</span></span> <span data-ttu-id="6716f-106">Es abstracto requerir más definición y perfeccionamiento semántico en las subclases.</span><span class="sxs-lookup"><span data-stu-id="6716f-106">It is abstract to require further definition and semantic refinement in subclasses.</span></span>

<span data-ttu-id="6716f-107">El objeto **CIM \_ CollectionOfMSEs** no tiene ningún Estado o información de estado, pero solo representa una agrupación de elementos.</span><span class="sxs-lookup"><span data-stu-id="6716f-107">The **CIM\_CollectionOfMSEs** object does not carry any state or status information, but only represents a grouping of elements.</span></span> <span data-ttu-id="6716f-108">Por esta razón, es incorrecto que los grupos de subclases que tienen el estado/estado de **CIM \_ CollectionOfMSEs**, un ejemplo es [**CIM \_ RedundancyGroup**](cim-redundancygroup.md) (que se subclase correctamente de [**CIM \_ LogicalElement**](cim-logicalelement.md)).</span><span class="sxs-lookup"><span data-stu-id="6716f-108">For this reason, it is incorrect to subclass groups that have state/status from **CIM\_CollectionOfMSEs**, An example is [**CIM\_RedundancyGroup**](cim-redundancygroup.md) (which is correctly subclassed from [**CIM\_LogicalElement**](cim-logicalelement.md)).</span></span> <span data-ttu-id="6716f-109">Las colecciones suelen agregar objetos ' like ' y representan una optimización.</span><span class="sxs-lookup"><span data-stu-id="6716f-109">Collections typically aggregate 'like' objects, and represent an optimization.</span></span> <span data-ttu-id="6716f-110">Sin las colecciones, se fuerza la definición de las asociaciones de [**\_ ElementSetting**](cim-elementsetting.md) CIM y [**\_ ElementConfiguration CIM**](cim-elementconfiguration.md) individuales, para vincular los objetos de configuración y de configuración a los [**\_ ManagedSystemElements de CIM**](cim-managedsystemelement.md)individuales.</span><span class="sxs-lookup"><span data-stu-id="6716f-110">Without collections, one is forced to define individual [**CIM\_ElementSetting**](cim-elementsetting.md) and [**CIM\_ElementConfiguration**](cim-elementconfiguration.md) associations, to tie settings and configuration objects to individual [**CIM\_ManagedSystemElements**](cim-managedsystemelement.md).</span></span> <span data-ttu-id="6716f-111">Puede haber mucha duplicación en la asignación de la misma configuración a varios objetos.</span><span class="sxs-lookup"><span data-stu-id="6716f-111">There may be much duplication in assigning the same setting to multiple objects.</span></span> <span data-ttu-id="6716f-112">Además, el uso del objeto Collection permite determinar que las asociaciones de configuración y configuración son realmente iguales para los miembros de la colección.</span><span class="sxs-lookup"><span data-stu-id="6716f-112">In addition, using the collection object allows the determination that the setting and configuration associations are indeed the same for the collection's members.</span></span> <span data-ttu-id="6716f-113">De lo contrario, esta información se obtenería definiendo la colección de forma propietaria y, a continuación, consultando las asociaciones **CIM \_ ElementSetting** y **CIM \_ ElementConfiguration** para determinar si el conjunto de recopilación está totalmente incluido.</span><span class="sxs-lookup"><span data-stu-id="6716f-113">This information would otherwise be obtained by defining the collection in a proprietary manner, and then querying the **CIM\_ElementSetting** and **CIM\_ElementConfiguration** associations to determine if the collection set is completely covered.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6716f-114">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="6716f-114">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="6716f-115">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="6716f-115">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="6716f-116">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6716f-116">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="6716f-117">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="6716f-117">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="6716f-118">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6716f-118">Syntax</span></span>

``` syntax
class CIM_CollectionOfMSEs
{
  string Caption;
  string CollectionID;
  string Description;
};
```

## <a name="members"></a><span data-ttu-id="6716f-119">Miembros</span><span class="sxs-lookup"><span data-stu-id="6716f-119">Members</span></span>

<span data-ttu-id="6716f-120">La clase **CIM \_ CollectionOfMSEs** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6716f-120">The **CIM\_CollectionOfMSEs** class has these types of members:</span></span>

-   [<span data-ttu-id="6716f-121">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6716f-121">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6716f-122">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6716f-122">Properties</span></span>

<span data-ttu-id="6716f-123">La clase **CIM \_ CollectionOfMSEs** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6716f-123">The **CIM\_CollectionOfMSEs** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6716f-124">**Caption**</span><span class="sxs-lookup"><span data-stu-id="6716f-124">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6716f-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6716f-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6716f-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6716f-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6716f-127">Descripción textual breve del objeto CollectionOfMSEs.</span><span class="sxs-lookup"><span data-stu-id="6716f-127">Short textual description of the CollectionOfMSEs object.</span></span>

</dd> <dt>

<span data-ttu-id="6716f-128">**Recopilación**</span><span class="sxs-lookup"><span data-stu-id="6716f-128">**CollectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6716f-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6716f-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6716f-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6716f-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6716f-131">Identificación del objeto de colección.</span><span class="sxs-lookup"><span data-stu-id="6716f-131">Identification of the Collection object.</span></span> <span data-ttu-id="6716f-132">Cuando se subclasen, la propiedad CollectionID se puede invalidar para ser una propiedad de clave.</span><span class="sxs-lookup"><span data-stu-id="6716f-132">When subclassed, the CollectionID property can be overridden to be a Key property.</span></span>

</dd> <dt>

<span data-ttu-id="6716f-133">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="6716f-133">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6716f-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6716f-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6716f-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6716f-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="6716f-136">Descripción textual del objeto CollectionOfMSEs.</span><span class="sxs-lookup"><span data-stu-id="6716f-136">Textual description of the CollectionOfMSEs object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6716f-137">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6716f-137">Remarks</span></span>

<span data-ttu-id="6716f-138">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="6716f-138">WMI does not implement this class.</span></span> <span data-ttu-id="6716f-139">Vea [clases Win32](win32-provider.md) para clases WMI derivadas de **CIM \_ CollectionOfMSEs**.</span><span class="sxs-lookup"><span data-stu-id="6716f-139">See [Win32 Classes](win32-provider.md) for WMI classes derived from **CIM\_CollectionOfMSEs**.</span></span>

<span data-ttu-id="6716f-140">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="6716f-140">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="6716f-141">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="6716f-141">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="6716f-142">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6716f-142">Requirements</span></span>



| <span data-ttu-id="6716f-143">Requisito</span><span class="sxs-lookup"><span data-stu-id="6716f-143">Requirement</span></span> | <span data-ttu-id="6716f-144">Value</span><span class="sxs-lookup"><span data-stu-id="6716f-144">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6716f-145">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6716f-145">Minimum supported client</span></span><br/> | <span data-ttu-id="6716f-146">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="6716f-146">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="6716f-147">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6716f-147">Minimum supported server</span></span><br/> | <span data-ttu-id="6716f-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="6716f-148">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="6716f-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6716f-149">Namespace</span></span><br/>                | <span data-ttu-id="6716f-150">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="6716f-150">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="6716f-151">MOF</span><span class="sxs-lookup"><span data-stu-id="6716f-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6716f-152"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6716f-152"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="6716f-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6716f-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6716f-154"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6716f-154"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

 




