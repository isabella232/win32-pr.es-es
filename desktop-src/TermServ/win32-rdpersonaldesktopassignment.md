---
title: Win32_RDPersonalDesktopAssignment (clase)
description: Lista de asignaciones de escritorio personal.
ms.assetid: 3abf773d-8dc3-44ae-8887-1a1f38e29fbb
ms.tgt_platform: multiple
keywords:
- Win32_RDPersonalDesktopAssignment clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDPersonalDesktopAssignment de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDPersonalDesktopAssignment
- Win32_RDPersonalDesktopAssignment.Caption
- Win32_RDPersonalDesktopAssignment.Description
- Win32_RDPersonalDesktopAssignment.InstallDate
- Win32_RDPersonalDesktopAssignment.Name
- Win32_RDPersonalDesktopAssignment.Status
- Win32_RDPersonalDesktopAssignment.UserName
- Win32_RDPersonalDesktopAssignment.DomainName
- Win32_RDPersonalDesktopAssignment.FarmAlias
- Win32_RDPersonalDesktopAssignment.VMName
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 088e7be5da0a62a0f5b7ed72f8a439661cc41c80
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685896"
---
# <a name="win32_rdpersonaldesktopassignment-class"></a><span data-ttu-id="b7d91-105">\_Clase Win32 RDPersonalDesktopAssignment</span><span class="sxs-lookup"><span data-stu-id="b7d91-105">Win32\_RDPersonalDesktopAssignment class</span></span>

<span data-ttu-id="b7d91-106">Lista de asignaciones de escritorio personal.</span><span class="sxs-lookup"><span data-stu-id="b7d91-106">The list of personal desktop assignments.</span></span>

<span data-ttu-id="b7d91-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="b7d91-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7d91-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b7d91-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDPersonalDesktopAssignment : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   UserName;
  string   DomainName;
  string   FarmAlias;
  string   VMName;
};
```

## <a name="members"></a><span data-ttu-id="b7d91-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="b7d91-109">Members</span></span>

<span data-ttu-id="b7d91-110">La **clase \_ RDPersonalDesktopAssignment de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="b7d91-110">The **Win32\_RDPersonalDesktopAssignment** class has these types of members:</span></span>

-   [<span data-ttu-id="b7d91-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b7d91-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b7d91-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="b7d91-112">Properties</span></span>

<span data-ttu-id="b7d91-113">La **clase \_ RDPersonalDesktopAssignment de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="b7d91-113">The **Win32\_RDPersonalDesktopAssignment** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b7d91-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="b7d91-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d91-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7d91-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7d91-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7d91-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7d91-117">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="b7d91-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="b7d91-118">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="b7d91-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="b7d91-119">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7d91-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7d91-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="b7d91-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d91-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7d91-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7d91-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7d91-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7d91-123">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="b7d91-123">Description of the object.</span></span>

<span data-ttu-id="b7d91-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7d91-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7d91-125">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="b7d91-125">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d91-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7d91-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7d91-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b7d91-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b7d91-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b7d91-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b7d91-129">Nombre de dominio del usuario.</span><span class="sxs-lookup"><span data-stu-id="b7d91-129">Domain name of the user.</span></span>

</dd> <dt>

<span data-ttu-id="b7d91-130">**FarmAlias**</span><span class="sxs-lookup"><span data-stu-id="b7d91-130">**FarmAlias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d91-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7d91-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7d91-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b7d91-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b7d91-133">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b7d91-133">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b7d91-134">Granja en la que se ha asignado el escritorio personal.</span><span class="sxs-lookup"><span data-stu-id="b7d91-134">Farm in which personal desktop has been assigned.</span></span>

</dd> <dt>

<span data-ttu-id="b7d91-135">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="b7d91-135">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d91-136">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="b7d91-136">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="b7d91-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7d91-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7d91-138">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="b7d91-138">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="b7d91-139">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="b7d91-139">The date the object was installed.</span></span> <span data-ttu-id="b7d91-140">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="b7d91-140">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="b7d91-141">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7d91-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7d91-142">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="b7d91-142">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d91-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7d91-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7d91-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7d91-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="b7d91-145">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="b7d91-145">The name of the object.</span></span>

<span data-ttu-id="b7d91-146">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7d91-146">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7d91-147">**Estado**</span><span class="sxs-lookup"><span data-stu-id="b7d91-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d91-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7d91-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7d91-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="b7d91-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b7d91-150">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="b7d91-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="b7d91-151">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="b7d91-151">Current status of the object.</span></span> <span data-ttu-id="b7d91-152">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="b7d91-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="b7d91-153">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="b7d91-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="b7d91-154">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="b7d91-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="b7d91-155">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="b7d91-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="b7d91-156">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="b7d91-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="b7d91-157">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="b7d91-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="b7d91-158">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="b7d91-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b7d91-159">("Error")</span><span class="sxs-lookup"><span data-stu-id="b7d91-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b7d91-160">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="b7d91-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b7d91-161">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="b7d91-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b7d91-162">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="b7d91-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b7d91-163">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="b7d91-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b7d91-164">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="b7d91-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="b7d91-165">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="b7d91-165">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="b7d91-166">**UserName**</span><span class="sxs-lookup"><span data-stu-id="b7d91-166">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d91-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7d91-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7d91-168">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b7d91-168">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="b7d91-169">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="b7d91-169">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="b7d91-170">Nombre de usuario al que se ha asignado el escritorio personal.</span><span class="sxs-lookup"><span data-stu-id="b7d91-170">User name to whom personal desktop has been assigned.</span></span>

</dd> <dt>

<span data-ttu-id="b7d91-171">**VMName**</span><span class="sxs-lookup"><span data-stu-id="b7d91-171">**VMName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b7d91-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="b7d91-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="b7d91-173">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="b7d91-173">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="b7d91-174">Nombre de máquina virtual asignado.</span><span class="sxs-lookup"><span data-stu-id="b7d91-174">Assigned VM name.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b7d91-175">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b7d91-175">Requirements</span></span>



| <span data-ttu-id="b7d91-176">Requisito</span><span class="sxs-lookup"><span data-stu-id="b7d91-176">Requirement</span></span> | <span data-ttu-id="b7d91-177">Value</span><span class="sxs-lookup"><span data-stu-id="b7d91-177">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b7d91-178">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7d91-178">Minimum supported client</span></span><br/> | <span data-ttu-id="b7d91-179">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="b7d91-179">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b7d91-180">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b7d91-180">Minimum supported server</span></span><br/> | <span data-ttu-id="b7d91-181">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b7d91-181">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="b7d91-182">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="b7d91-182">Namespace</span></span><br/>                | <span data-ttu-id="b7d91-183">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b7d91-183">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b7d91-184">MOF</span><span class="sxs-lookup"><span data-stu-id="b7d91-184">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b7d91-185"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b7d91-185"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="b7d91-186">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b7d91-186">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b7d91-187"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b7d91-187"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

