---
description: La \_ clase InstalledSoftwareElement de CIM asocia un equipo con un elemento de software instalado.
ms.assetid: b9a570ed-b4e0-4f73-82e3-6d2bd1708e16
ms.tgt_platform: multiple
title: CIM_InstalledSoftwareElement (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_InstalledSoftwareElement
- CIM_InstalledSoftwareElement.Software
- CIM_InstalledSoftwareElement.System
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: dd082477b2e2ba194163784b74883872b1edb6a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153167"
---
# <a name="cim_installedsoftwareelement-class"></a><span data-ttu-id="30927-103">\_Clase InstalledSoftwareElement de CIM</span><span class="sxs-lookup"><span data-stu-id="30927-103">CIM\_InstalledSoftwareElement class</span></span>

<span data-ttu-id="30927-104">La **clase \_ InstalledSoftwareElement de CIM** asocia un equipo con un elemento de software instalado.</span><span class="sxs-lookup"><span data-stu-id="30927-104">The **CIM\_InstalledSoftwareElement** class associates a computer system with an installed software element.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="30927-105">Las clases de CIM (Modelo de información común) de DMTF (Distributed Management Task Force) son las clases primarias en las que se compilan las clases de WMI.</span><span class="sxs-lookup"><span data-stu-id="30927-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="30927-106">WMI actualmente solo admite los [esquemas de la versión CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="30927-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="30927-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="30927-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="30927-108">Las propiedades se enumeran en orden alfabético, no en orden MOF.</span><span class="sxs-lookup"><span data-stu-id="30927-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="30927-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="30927-109">Syntax</span></span>

``` syntax
[UUID("{A7B05028-DB2A-11d2-85FC-0000F8102E5F}"), Association, Abstract, AMENDMENT]
class CIM_InstalledSoftwareElement
{
  CIM_SoftwareElement REF Software;
  CIM_ComputerSystem  REF System;
};
```

## <a name="members"></a><span data-ttu-id="30927-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="30927-110">Members</span></span>

<span data-ttu-id="30927-111">La clase **CIM \_ InstalledSoftwareElement** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="30927-111">The **CIM\_InstalledSoftwareElement** class has these types of members:</span></span>

-   [<span data-ttu-id="30927-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="30927-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="30927-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="30927-113">Properties</span></span>

<span data-ttu-id="30927-114">La clase **CIM \_ InstalledSoftwareElement** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="30927-114">The **CIM\_InstalledSoftwareElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="30927-115">**Software**</span><span class="sxs-lookup"><span data-stu-id="30927-115">**Software**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30927-116">Tipo de datos: **CIM \_ SoftwareElement**</span><span class="sxs-lookup"><span data-stu-id="30927-116">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="30927-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="30927-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30927-118">Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false)</span><span class="sxs-lookup"><span data-stu-id="30927-118">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE)</span></span>
</dt> </dl>

<span data-ttu-id="30927-119">Referencia al elemento de software que está instalado en el sistema del equipo.</span><span class="sxs-lookup"><span data-stu-id="30927-119">Reference to the software element that is installed on the computer system.</span></span>

</dd> <dt>

<span data-ttu-id="30927-120">**Sistema**</span><span class="sxs-lookup"><span data-stu-id="30927-120">**System**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="30927-121">Tipo de datos: **CIM \_ ComputerSystem**</span><span class="sxs-lookup"><span data-stu-id="30927-121">Data type: **CIM\_ComputerSystem**</span></span>
</dt> <dt>

<span data-ttu-id="30927-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="30927-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="30927-123">Calificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false)</span><span class="sxs-lookup"><span data-stu-id="30927-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE)</span></span>
</dt> </dl>

<span data-ttu-id="30927-124">Referencia al sistema del equipo que hospeda un elemento de software determinado.</span><span class="sxs-lookup"><span data-stu-id="30927-124">Reference to the computer system hosting a particular software element.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="30927-125">Observaciones</span><span class="sxs-lookup"><span data-stu-id="30927-125">Remarks</span></span>

<span data-ttu-id="30927-126">WMI no implementa esta clase.</span><span class="sxs-lookup"><span data-stu-id="30927-126">WMI does not implement this class.</span></span> <span data-ttu-id="30927-127">Para las clases derivadas de **CIM \_ InstalledSoftwareElement**, vea [clases Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="30927-127">For classes derived from **CIM\_InstalledSoftwareElement**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="30927-128">Esta documentación se deriva de las descripciones de clases CIM publicadas por DMTF.</span><span class="sxs-lookup"><span data-stu-id="30927-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="30927-129">Es posible que Microsoft haya realizado cambios para corregir los errores menores, cumplir los estándares de documentación del SDK de Microsoft o proporcionar más información.</span><span class="sxs-lookup"><span data-stu-id="30927-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="30927-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30927-130">Requirements</span></span>



| <span data-ttu-id="30927-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="30927-131">Requirement</span></span> | <span data-ttu-id="30927-132">Value</span><span class="sxs-lookup"><span data-stu-id="30927-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30927-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30927-133">Minimum supported client</span></span><br/> | <span data-ttu-id="30927-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="30927-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="30927-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="30927-135">Minimum supported server</span></span><br/> | <span data-ttu-id="30927-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="30927-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="30927-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="30927-137">Namespace</span></span><br/>                | <span data-ttu-id="30927-138">Origen de \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="30927-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="30927-139">MOF</span><span class="sxs-lookup"><span data-stu-id="30927-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30927-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="30927-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="30927-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="30927-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30927-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30927-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

