---
description: La \_ clase CIM AllocatedResource representa una asociación entre dispositivos lógicos y recursos del sistema e indica que el recurso está asignado al dispositivo.
ms.assetid: e1702635-32f5-4280-8c02-3940fd858106
ms.tgt_platform: multiple
title: CIM_AllocatedResource (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AllocatedResource
- CIM_AllocatedResource.Dependent
- CIM_AllocatedResource.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: e4191315b76553a8c23b94c04d9649cceb131855
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153296"
---
# <a name="cim_allocatedresource-class"></a><span data-ttu-id="123ac-103">\_Clase AllocatedResource de CIM</span><span class="sxs-lookup"><span data-stu-id="123ac-103">CIM\_AllocatedResource class</span></span>

<span data-ttu-id="123ac-104">La clase **CIM \_ AllocatedResource** representa una asociación entre dispositivos lógicos y recursos del sistema e indica que el recurso está asignado al dispositivo.</span><span class="sxs-lookup"><span data-stu-id="123ac-104">The **CIM\_AllocatedResource** class represents an association between logical devices and system resources and indicates that the resource is assigned to the device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="123ac-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="123ac-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="123ac-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="123ac-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="123ac-107">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="123ac-107">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="123ac-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="123ac-108">Syntax</span></span>

``` syntax
[Abstract, UUID("{8502C579-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class CIM_AllocatedResource : CIM_Dependency
{
  CIM_LogicalDevice  REF Dependent;
  CIM_SystemResource REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="123ac-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="123ac-109">Members</span></span>

<span data-ttu-id="123ac-110">La clase **CIM \_ AllocatedResource** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="123ac-110">The **CIM\_AllocatedResource** class has these types of members:</span></span>

-   [<span data-ttu-id="123ac-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="123ac-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="123ac-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="123ac-112">Properties</span></span>

<span data-ttu-id="123ac-113">La clase **CIM \_ AllocatedResource** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="123ac-113">The **CIM\_AllocatedResource** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="123ac-114">**Antecedente**</span><span class="sxs-lookup"><span data-stu-id="123ac-114">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123ac-115">Tipo de datos: **CIM \_ SystemResource**</span><span class="sxs-lookup"><span data-stu-id="123ac-115">Data type: **CIM\_SystemResource**</span></span>
</dt> <dt>

<span data-ttu-id="123ac-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="123ac-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123ac-117">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("antecedente")</span><span class="sxs-lookup"><span data-stu-id="123ac-117">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="123ac-118">Un [**\_ SystemResource de CIM**](cim-systemresource.md) que describe el recurso.</span><span class="sxs-lookup"><span data-stu-id="123ac-118">A [**CIM\_SystemResource**](cim-systemresource.md) that describes the resource.</span></span>

</dd> <dt>

<span data-ttu-id="123ac-119">**Dependientes**</span><span class="sxs-lookup"><span data-stu-id="123ac-119">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="123ac-120">Tipo de datos **: \_ LogicalDevice de CIM**</span><span class="sxs-lookup"><span data-stu-id="123ac-120">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="123ac-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="123ac-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="123ac-122">Calificadores: [**invalidación**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependiente")</span><span class="sxs-lookup"><span data-stu-id="123ac-122">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="123ac-123">Un [**\_ LogicalDevice de CIM**](cim-logicaldevice.md) que contiene el dispositivo lógico al que se asigna el recurso.</span><span class="sxs-lookup"><span data-stu-id="123ac-123">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that contains the logical device to which the resource is assigned.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="123ac-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="123ac-124">Remarks</span></span>

<span data-ttu-id="123ac-125">La clase **CIM \_ AllocatedResource** se deriva de [**la \_ dependencia CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="123ac-125">The **CIM\_AllocatedResource** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="123ac-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="123ac-126">WMI does not implement this class.</span></span> <span data-ttu-id="123ac-127">Para obtener más información sobre las clases derivadas de **CIM \_ AllocatedResource**, vea [Win32 classes](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="123ac-127">For more information about classes derived from **CIM\_AllocatedResource**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="123ac-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="123ac-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="123ac-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="123ac-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="123ac-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="123ac-130">Requirements</span></span>



| <span data-ttu-id="123ac-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="123ac-131">Requirement</span></span> | <span data-ttu-id="123ac-132">Value</span><span class="sxs-lookup"><span data-stu-id="123ac-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="123ac-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="123ac-133">Minimum supported client</span></span><br/> | <span data-ttu-id="123ac-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="123ac-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="123ac-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="123ac-135">Minimum supported server</span></span><br/> | <span data-ttu-id="123ac-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="123ac-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="123ac-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="123ac-137">Namespace</span></span><br/>                | <span data-ttu-id="123ac-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="123ac-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="123ac-139">MOF</span><span class="sxs-lookup"><span data-stu-id="123ac-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="123ac-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="123ac-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="123ac-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="123ac-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="123ac-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="123ac-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="123ac-143">Vea también</span><span class="sxs-lookup"><span data-stu-id="123ac-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="123ac-144">**Dependencia de CIM \_**</span><span class="sxs-lookup"><span data-stu-id="123ac-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

