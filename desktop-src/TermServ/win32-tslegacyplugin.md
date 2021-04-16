---
title: Win32_TSLegacyPlugin (clase)
description: Representa un servidor de Escritorio remoto al que los complementos de servicio Administración de conexiones de RemoteApp y Escritorio integrados consultarán los programas RemoteApp.
ms.assetid: 99bec477-ae9d-4bc9-bf9d-11a4e439306b
ms.tgt_platform: multiple
keywords:
- Win32_TSLegacyPlugin clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSLegacyPlugin de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSLegacyPlugin
- Win32_TSLegacyPlugin.Caption
- Win32_TSLegacyPlugin.Description
- Win32_TSLegacyPlugin.InstallDate
- Win32_TSLegacyPlugin.Name
- Win32_TSLegacyPlugin.Status
- Win32_TSLegacyPlugin.Type
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 548eadac272f6f87daf1c43020cb65485e434aec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685864"
---
# <a name="win32_tslegacyplugin-class"></a><span data-ttu-id="98efc-105">\_Clase Win32 TSLegacyPlugin</span><span class="sxs-lookup"><span data-stu-id="98efc-105">Win32\_TSLegacyPlugin class</span></span>

<span data-ttu-id="98efc-106">Representa un servidor de Escritorio remoto al que los complementos de servicio Administración de conexiones de RemoteApp y Escritorio integrados consultarán los programas RemoteApp.</span><span class="sxs-lookup"><span data-stu-id="98efc-106">Represents a Remote Desktop server that the built-in RemoteApp and Desktop Connection Management Service plug-ins will query for RemoteApp programs.</span></span>

<span data-ttu-id="98efc-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="98efc-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

<span data-ttu-id="98efc-108">Esta clase está en desuso a partir de Windows Server 2012.</span><span class="sxs-lookup"><span data-stu-id="98efc-108">This class is deprecated beginning with Windows Server 2012.</span></span>

## <a name="syntax"></a><span data-ttu-id="98efc-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="98efc-109">Syntax</span></span>

``` syntax
[DEPRECATED, dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_TSLegacyPlugin : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  sint32   Type;
};
```

## <a name="members"></a><span data-ttu-id="98efc-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="98efc-110">Members</span></span>

<span data-ttu-id="98efc-111">La **clase \_ TSLegacyPlugin de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="98efc-111">The **Win32\_TSLegacyPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="98efc-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="98efc-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="98efc-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="98efc-113">Properties</span></span>

<span data-ttu-id="98efc-114">La **clase \_ TSLegacyPlugin de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="98efc-114">The **Win32\_TSLegacyPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="98efc-115">**Caption**</span><span class="sxs-lookup"><span data-stu-id="98efc-115">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98efc-116">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="98efc-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98efc-117">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98efc-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98efc-118">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="98efc-118">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="98efc-119">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="98efc-119">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="98efc-120">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="98efc-120">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="98efc-121">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="98efc-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98efc-122">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="98efc-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98efc-123">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98efc-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98efc-124">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="98efc-124">Description of the object.</span></span>

<span data-ttu-id="98efc-125">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="98efc-125">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="98efc-126">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="98efc-126">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98efc-127">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="98efc-127">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="98efc-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98efc-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98efc-129">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="98efc-129">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="98efc-130">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="98efc-130">The date the object was installed.</span></span> <span data-ttu-id="98efc-131">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="98efc-131">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="98efc-132">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="98efc-132">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="98efc-133">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="98efc-133">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98efc-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="98efc-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98efc-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98efc-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="98efc-136">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="98efc-136">The name of the object.</span></span>

<span data-ttu-id="98efc-137">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="98efc-137">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="98efc-138">**Estado**</span><span class="sxs-lookup"><span data-stu-id="98efc-138">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98efc-139">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="98efc-139">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="98efc-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="98efc-140">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="98efc-141">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="98efc-141">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="98efc-142">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="98efc-142">Current status of the object.</span></span> <span data-ttu-id="98efc-143">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="98efc-143">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="98efc-144">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="98efc-144">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="98efc-145">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="98efc-145">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="98efc-146">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="98efc-146">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="98efc-147">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="98efc-147">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="98efc-148">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="98efc-148">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="98efc-149">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="98efc-149">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="98efc-150">("Error")</span><span class="sxs-lookup"><span data-stu-id="98efc-150">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="98efc-151">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="98efc-151">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="98efc-152">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="98efc-152">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="98efc-153">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="98efc-153">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="98efc-154">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="98efc-154">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="98efc-155">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="98efc-155">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="98efc-156">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="98efc-156">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="98efc-157">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="98efc-157">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="98efc-158">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="98efc-158">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="98efc-159">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="98efc-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="98efc-160">Tipo del servidor de Servicios de Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="98efc-160">The type of the Remote Desktop Services server.</span></span>

<dt>

<span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>

<span data-ttu-id="98efc-161"><span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>**Terminal Server (0)** (0)</span><span class="sxs-lookup"><span data-stu-id="98efc-161"><span id="Terminal_Server_0_"></span><span id="terminal_server_0_"></span><span id="TERMINAL_SERVER_0_"></span>**Terminal Server(0)** (0)</span></span>


</dt> <dd>

<span data-ttu-id="98efc-162">Escritorio remoto Server.</span><span class="sxs-lookup"><span data-stu-id="98efc-162">Remote Desktop server.</span></span>

</dd> <dt>

<span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>

<span data-ttu-id="98efc-163"><span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>**Terminal Server ficticios para la granja de servidores de VM (1)** (1)</span><span class="sxs-lookup"><span data-stu-id="98efc-163"><span id="Dummy_Terminal_Server_for_VM_Farm_1_"></span><span id="dummy_terminal_server_for_vm_farm_1_"></span><span id="DUMMY_TERMINAL_SERVER_FOR_VM_FARM_1_"></span>**Dummy Terminal Server for VM Farm(1)** (1)</span></span>


</dt> <dd>

<span data-ttu-id="98efc-164">Servidor de Escritorio remoto artificial para una granja de máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="98efc-164">Artificial Remote Desktop server for a VM farm.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="98efc-165">Requisitos</span><span class="sxs-lookup"><span data-stu-id="98efc-165">Requirements</span></span>



| <span data-ttu-id="98efc-166">Requisito</span><span class="sxs-lookup"><span data-stu-id="98efc-166">Requirement</span></span> | <span data-ttu-id="98efc-167">Value</span><span class="sxs-lookup"><span data-stu-id="98efc-167">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="98efc-168">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98efc-168">Minimum supported client</span></span><br/> | <span data-ttu-id="98efc-169">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="98efc-169">None supported</span></span><br/>                                                                |
| <span data-ttu-id="98efc-170">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="98efc-170">Minimum supported server</span></span><br/> | <span data-ttu-id="98efc-171">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="98efc-171">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="98efc-172">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="98efc-172">Namespace</span></span><br/>                | <span data-ttu-id="98efc-173">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="98efc-173">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="98efc-174">MOF</span><span class="sxs-lookup"><span data-stu-id="98efc-174">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98efc-175"><dt>TscPub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="98efc-175"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="98efc-176">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="98efc-176">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98efc-177"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98efc-177"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

