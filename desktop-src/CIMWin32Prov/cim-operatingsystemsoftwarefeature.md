---
description: La \_ clase CIM OperatingSystemSoftwareFeature representa las características de software que componen el sistema operativo.
ms.assetid: 9ffc709c-213e-4252-9662-76f01e1685e5
ms.tgt_platform: multiple
title: CIM_OperatingSystemSoftwareFeature (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_OperatingSystemSoftwareFeature
- CIM_OperatingSystemSoftwareFeature.PartComponent
- CIM_OperatingSystemSoftwareFeature.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: b9d74478f211b23e103854cedb09a1e0186618b8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659627"
---
# <a name="cim_operatingsystemsoftwarefeature-class"></a><span data-ttu-id="4f4a7-103">\_Clase OperatingSystemSoftwareFeature de CIM</span><span class="sxs-lookup"><span data-stu-id="4f4a7-103">CIM\_OperatingSystemSoftwareFeature class</span></span>

<span data-ttu-id="4f4a7-104">La clase **CIM \_ OperatingSystemSoftwareFeature** representa las características de software que componen el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4f4a7-104">The **CIM\_OperatingSystemSoftwareFeature** class represents the software features that make up the operating system.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4f4a7-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="4f4a7-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="4f4a7-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="4f4a7-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="4f4a7-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4f4a7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="4f4a7-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="4f4a7-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f4a7-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4f4a7-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{96B4C734-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_OperatingSystemSoftwareFeature : CIM_Component
{
  CIM_SoftwareFeature REF PartComponent;
  CIM_OperatingSystem REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="4f4a7-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="4f4a7-110">Members</span></span>

<span data-ttu-id="4f4a7-111">La clase **CIM \_ OperatingSystemSoftwareFeature** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4f4a7-111">The **CIM\_OperatingSystemSoftwareFeature** class has these types of members:</span></span>

-   [<span data-ttu-id="4f4a7-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4f4a7-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4f4a7-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4f4a7-113">Properties</span></span>

<span data-ttu-id="4f4a7-114">La clase **CIM \_ OperatingSystemSoftwareFeature** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4f4a7-114">The **CIM\_OperatingSystemSoftwareFeature** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="4f4a7-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="4f4a7-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4a7-116">Tipo de datos: **CIM \_ OperatingSystem**</span><span class="sxs-lookup"><span data-stu-id="4f4a7-116">Data type: **CIM\_OperatingSystem**</span></span>
</dt> <dt>

<span data-ttu-id="4f4a7-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4a7-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4a7-118">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="4f4a7-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4f4a7-119">Un [**\_ OperatingSystem de CIM**](cim-operatingsystem.md) que describe el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4f4a7-119">A [**CIM\_OperatingSystem**](cim-operatingsystem.md) describing the operating system.</span></span>

</dd> <dt>

<span data-ttu-id="4f4a7-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="4f4a7-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4f4a7-121">Tipo de datos: **CIM \_ SoftwareFeature**</span><span class="sxs-lookup"><span data-stu-id="4f4a7-121">Data type: **CIM\_SoftwareFeature**</span></span>
</dt> <dt>

<span data-ttu-id="4f4a7-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4f4a7-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4f4a7-123">Calificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="4f4a7-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="4f4a7-124">Un [**\_ SoftwareFeature de CIM**](cim-softwarefeature.md) que describe las características de software que componen el sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="4f4a7-124">A [**CIM\_SoftwareFeature**](cim-softwarefeature.md) describing the software features that make up the operating system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4f4a7-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4f4a7-125">Remarks</span></span>

<span data-ttu-id="4f4a7-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="4f4a7-126">WMI does not implement this class.</span></span>

<span data-ttu-id="4f4a7-127">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="4f4a7-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="4f4a7-128">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="4f4a7-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="4f4a7-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f4a7-129">Requirements</span></span>



| <span data-ttu-id="4f4a7-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f4a7-130">Requirement</span></span> | <span data-ttu-id="4f4a7-131">Value</span><span class="sxs-lookup"><span data-stu-id="4f4a7-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4f4a7-132">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f4a7-132">Minimum supported client</span></span><br/> | <span data-ttu-id="4f4a7-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="4f4a7-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="4f4a7-134">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4f4a7-134">Minimum supported server</span></span><br/> | <span data-ttu-id="4f4a7-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="4f4a7-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="4f4a7-136">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4f4a7-136">Namespace</span></span><br/>                | <span data-ttu-id="4f4a7-137">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="4f4a7-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="4f4a7-138">MOF</span><span class="sxs-lookup"><span data-stu-id="4f4a7-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4f4a7-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4f4a7-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="4f4a7-140">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4f4a7-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4f4a7-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4f4a7-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f4a7-142">Vea también</span><span class="sxs-lookup"><span data-stu-id="4f4a7-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f4a7-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="4f4a7-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

