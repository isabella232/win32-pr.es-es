---
title: Win32_TSSystemInfo (clase)
description: Representa el servicio de información del servidor de publicación centralizado.
ms.assetid: fd8155dc-63bf-4001-ab93-dc87a6c91284
ms.tgt_platform: multiple
keywords:
- Win32_TSSystemInfo clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSSystemInfo de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSSystemInfo
- Win32_TSSystemInfo.Caption
- Win32_TSSystemInfo.Description
- Win32_TSSystemInfo.InstallDate
- Win32_TSSystemInfo.Name
- Win32_TSSystemInfo.Status
- Win32_TSSystemInfo.RDUGroup
- Win32_TSSystemInfo.ProviderVersion
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 188761bd06a32e0c6f246dfe41f354adf1e06332
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490085"
---
# <a name="win32_tssysteminfo-class"></a><span data-ttu-id="0edae-105">\_Clase Win32 TSSystemInfo</span><span class="sxs-lookup"><span data-stu-id="0edae-105">Win32\_TSSystemInfo class</span></span>

<span data-ttu-id="0edae-106">Representa el servicio de información del servidor de publicación centralizado</span><span class="sxs-lookup"><span data-stu-id="0edae-106">Represents the Centralized Publishing Server Information Service</span></span>

<span data-ttu-id="0edae-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0edae-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0edae-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0edae-108">Syntax</span></span>

``` syntax
class Win32_TSSystemInfo : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   RDUGroup;
  uint32   ProviderVersion;
};
```

## <a name="members"></a><span data-ttu-id="0edae-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="0edae-109">Members</span></span>

<span data-ttu-id="0edae-110">La **clase \_ TSSystemInfo de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0edae-110">The **Win32\_TSSystemInfo** class has these types of members:</span></span>

-   [<span data-ttu-id="0edae-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0edae-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0edae-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0edae-112">Properties</span></span>

<span data-ttu-id="0edae-113">La **clase \_ TSSystemInfo de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0edae-113">The **Win32\_TSSystemInfo** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0edae-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="0edae-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0edae-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0edae-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0edae-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0edae-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0edae-117">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="0edae-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="0edae-118">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="0edae-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="0edae-119">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0edae-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0edae-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="0edae-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0edae-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0edae-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0edae-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0edae-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0edae-123">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="0edae-123">Description of the object.</span></span>

<span data-ttu-id="0edae-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0edae-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0edae-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="0edae-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0edae-126">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="0edae-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="0edae-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0edae-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0edae-128">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="0edae-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="0edae-129">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="0edae-129">The date the object was installed.</span></span> <span data-ttu-id="0edae-130">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="0edae-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="0edae-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0edae-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0edae-132">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="0edae-132">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0edae-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0edae-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0edae-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0edae-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0edae-135">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="0edae-135">The name of the object.</span></span>

<span data-ttu-id="0edae-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0edae-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="0edae-137">**ProviderVersion**</span><span class="sxs-lookup"><span data-stu-id="0edae-137">**ProviderVersion**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0edae-138">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0edae-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="0edae-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0edae-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0edae-140">Número de versión de este proveedor WMI.</span><span class="sxs-lookup"><span data-stu-id="0edae-140">The version number of this WMI Provider.</span></span>

</dd> <dt>

<span data-ttu-id="0edae-141">**RDUGroup**</span><span class="sxs-lookup"><span data-stu-id="0edae-141">**RDUGroup**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0edae-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0edae-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0edae-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0edae-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="0edae-144">El grupo usuarios de Escritorio remoto, en formato SDDL (lenguaje de definición de descriptores de seguridad).</span><span class="sxs-lookup"><span data-stu-id="0edae-144">The Remote Desktop Users group, in security descriptor definition language (SDDL) format.</span></span>

</dd> <dt>

<span data-ttu-id="0edae-145">**Estado**</span><span class="sxs-lookup"><span data-stu-id="0edae-145">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0edae-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0edae-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0edae-147">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0edae-147">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0edae-148">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="0edae-148">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="0edae-149">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="0edae-149">Current status of the object.</span></span> <span data-ttu-id="0edae-150">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="0edae-150">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="0edae-151">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="0edae-151">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="0edae-152">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="0edae-152">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="0edae-153">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="0edae-153">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="0edae-154">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="0edae-154">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="0edae-155">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="0edae-155">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="0edae-156">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="0edae-156">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0edae-157">("Error")</span><span class="sxs-lookup"><span data-stu-id="0edae-157">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0edae-158">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="0edae-158">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0edae-159">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="0edae-159">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0edae-160">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="0edae-160">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0edae-161">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="0edae-161">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0edae-162">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="0edae-162">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="0edae-163">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="0edae-163">("Service")</span></span>


<span data-ttu-id="0edae-164"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="0edae-164"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="0edae-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0edae-165">Requirements</span></span>



| <span data-ttu-id="0edae-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="0edae-166">Requirement</span></span> | <span data-ttu-id="0edae-167">Value</span><span class="sxs-lookup"><span data-stu-id="0edae-167">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0edae-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0edae-168">Minimum supported client</span></span><br/> | <span data-ttu-id="0edae-169">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0edae-169">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0edae-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0edae-170">Minimum supported server</span></span><br/> | <span data-ttu-id="0edae-171">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0edae-171">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="0edae-172">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0edae-172">Namespace</span></span><br/>                | <span data-ttu-id="0edae-173">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0edae-173">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0edae-174">MOF</span><span class="sxs-lookup"><span data-stu-id="0edae-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0edae-175"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0edae-175"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="0edae-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0edae-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0edae-177"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0edae-177"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

