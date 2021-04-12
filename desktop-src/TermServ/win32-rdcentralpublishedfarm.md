---
title: Win32_RDCentralPublishedFarm (clase)
description: La lista de granjas de servidores desde la que se publicaron los equipos de escritorio o las aplicaciones.
ms.assetid: 8fead659-42b4-4a10-892a-a6b616c47255
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedFarm clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDCentralPublishedFarm de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedFarm
- Win32_RDCentralPublishedFarm.Caption
- Win32_RDCentralPublishedFarm.Description
- Win32_RDCentralPublishedFarm.InstallDate
- Win32_RDCentralPublishedFarm.Name
- Win32_RDCentralPublishedFarm.Status
- Win32_RDCentralPublishedFarm.Alias
- Win32_RDCentralPublishedFarm.FarmType
- Win32_RDCentralPublishedFarm.IsUserAdmin
- Win32_RDCentralPublishedFarm.RollbackEnabled
- Win32_RDCentralPublishedFarm.SecurityDescriptor
- Win32_RDCentralPublishedFarm.VmFarmSettings
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9377053906168d4228e3b2cb8ae4f24cbb571634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490103"
---
# <a name="win32_rdcentralpublishedfarm-class"></a><span data-ttu-id="c0a59-105">\_Clase Win32 RDCentralPublishedFarm</span><span class="sxs-lookup"><span data-stu-id="c0a59-105">Win32\_RDCentralPublishedFarm class</span></span>

<span data-ttu-id="c0a59-106">La lista de granjas de servidores desde la que se publicaron los equipos de escritorio o las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c0a59-106">The list of farms from which desktops or applications have been published.</span></span>

<span data-ttu-id="c0a59-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c0a59-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0a59-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c0a59-108">Syntax</span></span>

``` syntax
[provider("Win32_TSCentralPublisher_Prov"), dynamic]
class Win32_RDCentralPublishedFarm : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  uint32   FarmType;
  boolean  IsUserAdmin;
  boolean  RollbackEnabled;
  string   SecurityDescriptor;
  string   VmFarmSettings;
};
```

## <a name="members"></a><span data-ttu-id="c0a59-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="c0a59-109">Members</span></span>

<span data-ttu-id="c0a59-110">La **clase \_ RDCentralPublishedFarm de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c0a59-110">The **Win32\_RDCentralPublishedFarm** class has these types of members:</span></span>

-   [<span data-ttu-id="c0a59-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c0a59-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c0a59-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c0a59-112">Properties</span></span>

<span data-ttu-id="c0a59-113">La **clase \_ RDCentralPublishedFarm de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c0a59-113">The **Win32\_RDCentralPublishedFarm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c0a59-114">**Alias**</span><span class="sxs-lookup"><span data-stu-id="c0a59-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0a59-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0a59-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c0a59-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-117">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c0a59-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="c0a59-118">El nombre de la granja desde la que se publicaron los equipos de escritorio o las aplicaciones.</span><span class="sxs-lookup"><span data-stu-id="c0a59-118">The name of the farm from which desktops or applications have been published.</span></span>

</dd> <dt>

<span data-ttu-id="c0a59-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="c0a59-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0a59-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0a59-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0a59-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-122">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="c0a59-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="c0a59-123">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="c0a59-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="c0a59-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0a59-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0a59-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="c0a59-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0a59-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0a59-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0a59-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0a59-128">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="c0a59-128">Description of the object.</span></span>

<span data-ttu-id="c0a59-129">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0a59-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0a59-130">**FarmType**</span><span class="sxs-lookup"><span data-stu-id="c0a59-130">**FarmType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0a59-131">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="c0a59-131">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c0a59-132">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-133">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c0a59-133">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c0a59-134">El tipo de granja:</span><span class="sxs-lookup"><span data-stu-id="c0a59-134">The kind of farm:</span></span>

<dt>

<span id="RDSH"></span><span id="rdsh"></span>

<span data-ttu-id="c0a59-135">**RDSH** (0)</span><span class="sxs-lookup"><span data-stu-id="c0a59-135">**RDSH** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="TempVM"></span><span id="tempvm"></span><span id="TEMPVM"></span>

<span data-ttu-id="c0a59-136">**TempVM** (1)</span><span class="sxs-lookup"><span data-stu-id="c0a59-136">**TempVM** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="ManualPersonalVM"></span><span id="manualpersonalvm"></span><span id="MANUALPERSONALVM"></span>

<span data-ttu-id="c0a59-137">**ManualPersonalVM** (2)</span><span class="sxs-lookup"><span data-stu-id="c0a59-137">**ManualPersonalVM** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="AutoPersonalVM"></span><span id="autopersonalvm"></span><span id="AUTOPERSONALVM"></span>

<span data-ttu-id="c0a59-138">**AutoPersonalVM** (3)</span><span class="sxs-lookup"><span data-stu-id="c0a59-138">**AutoPersonalVM** (3)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0a59-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="c0a59-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0a59-140">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="c0a59-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0a59-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-142">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="c0a59-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="c0a59-143">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="c0a59-143">The date the object was installed.</span></span> <span data-ttu-id="c0a59-144">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="c0a59-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="c0a59-145">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0a59-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0a59-146">**IsUserAdmin**</span><span class="sxs-lookup"><span data-stu-id="c0a59-146">**IsUserAdmin**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0a59-147">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c0a59-147">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c0a59-148">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-149">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c0a59-149">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c0a59-150">**true** si es necesario agregar un usuario al grupo de administradores locales tras la conexión; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="c0a59-150">**true** if a user needs to be added to local administrator group upon connection; otherwise, **false**.</span></span> <span data-ttu-id="c0a59-151">Solo se aplica a los tipos de granja de ManualPersonalVm y AutoPersonalVM.</span><span class="sxs-lookup"><span data-stu-id="c0a59-151">Applicable only to ManualPersonalVm and AutoPersonalVM farm types.</span></span>

</dd> <dt>

<span data-ttu-id="c0a59-152">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="c0a59-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0a59-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0a59-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0a59-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="c0a59-155">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="c0a59-155">The name of the object.</span></span>

<span data-ttu-id="c0a59-156">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0a59-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="c0a59-157">**RollbackEnabled**</span><span class="sxs-lookup"><span data-stu-id="c0a59-157">**RollbackEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0a59-158">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="c0a59-158">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-159">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c0a59-159">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-160">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c0a59-160">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c0a59-161">**true** para revertir automáticamente la máquina virtual a una instantánea después de cerrar la sesión del usuario; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="c0a59-161">**true** to auto rollback VM to a snapshot after user logoff; otherwise, **false**.</span></span> <span data-ttu-id="c0a59-162">Solo se aplica a los tipos de granja de TempVm.</span><span class="sxs-lookup"><span data-stu-id="c0a59-162">Applicable only to TempVm farm types.</span></span>

</dd> <dt>

<span data-ttu-id="c0a59-163">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="c0a59-163">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0a59-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0a59-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c0a59-165">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-166">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c0a59-166">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c0a59-167">Nombre del descriptor de seguridad que controla el acceso a la aplicación, en formato SDDL.</span><span class="sxs-lookup"><span data-stu-id="c0a59-167">The name of the security descriptor controlling access to the application, in SDDL Format.</span></span> <span data-ttu-id="c0a59-168">El uso de una cadena vacía implica permitir todo acceso.</span><span class="sxs-lookup"><span data-stu-id="c0a59-168">Using an empty string implies allow all access.</span></span>

</dd> <dt>

<span data-ttu-id="c0a59-169">**Estado**</span><span class="sxs-lookup"><span data-stu-id="c0a59-169">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0a59-170">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0a59-170">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-171">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c0a59-171">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-172">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="c0a59-172">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="c0a59-173">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="c0a59-173">Current status of the object.</span></span> <span data-ttu-id="c0a59-174">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="c0a59-174">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="c0a59-175">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="c0a59-175">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="c0a59-176">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="c0a59-176">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="c0a59-177">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="c0a59-177">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="c0a59-178">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="c0a59-178">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="c0a59-179">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="c0a59-179">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="c0a59-180">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="c0a59-180">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c0a59-181">("Error")</span><span class="sxs-lookup"><span data-stu-id="c0a59-181">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c0a59-182">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="c0a59-182">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c0a59-183">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="c0a59-183">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c0a59-184">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="c0a59-184">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c0a59-185">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="c0a59-185">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c0a59-186">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="c0a59-186">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="c0a59-187">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="c0a59-187">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="c0a59-188">**VmFarmSettings**</span><span class="sxs-lookup"><span data-stu-id="c0a59-188">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c0a59-189">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c0a59-189">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-190">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c0a59-190">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="c0a59-191">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="c0a59-191">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="c0a59-192">La configuración de la granja de máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="c0a59-192">The virtual machine farm settings.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c0a59-193">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c0a59-193">Requirements</span></span>



| <span data-ttu-id="c0a59-194">Requisito</span><span class="sxs-lookup"><span data-stu-id="c0a59-194">Requirement</span></span> | <span data-ttu-id="c0a59-195">Value</span><span class="sxs-lookup"><span data-stu-id="c0a59-195">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c0a59-196">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0a59-196">Minimum supported client</span></span><br/> | <span data-ttu-id="c0a59-197">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c0a59-197">None supported</span></span><br/>                                                                |
| <span data-ttu-id="c0a59-198">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c0a59-198">Minimum supported server</span></span><br/> | <span data-ttu-id="c0a59-199">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="c0a59-199">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="c0a59-200">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c0a59-200">Namespace</span></span><br/>                | <span data-ttu-id="c0a59-201">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c0a59-201">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="c0a59-202">MOF</span><span class="sxs-lookup"><span data-stu-id="c0a59-202">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c0a59-203"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c0a59-203"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="c0a59-204">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c0a59-204">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c0a59-205"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c0a59-205"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

