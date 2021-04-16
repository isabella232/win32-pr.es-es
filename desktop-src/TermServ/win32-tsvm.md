---
title: Win32_TSVm (clase)
description: Representa una máquina virtual Escritorio remoto.
ms.assetid: 9e076963-1c02-4419-b4d5-9863a2bbb23b
ms.tgt_platform: multiple
keywords:
- Win32_TSVm clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSVm de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSVm
- Win32_TSVm.Caption
- Win32_TSVm.Description
- Win32_TSVm.InstallDate
- Win32_TSVm.Name
- Win32_TSVm.Status
- Win32_TSVm.VmName
- Win32_TSVm.EnlightmentSettings
api_location:
- TSVmHostWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25f419a888adef946d2a7b281919a9a9293eeca5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676575"
---
# <a name="win32_tsvm-class"></a><span data-ttu-id="48309-105">\_Clase Win32 TSVm</span><span class="sxs-lookup"><span data-stu-id="48309-105">Win32\_TSVm class</span></span>

<span data-ttu-id="48309-106">Representa una máquina virtual Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="48309-106">Represents a Remote Desktop virtual machine.</span></span>

<span data-ttu-id="48309-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="48309-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="48309-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48309-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSVmHost_Prov"), AMENDMENT]
class Win32_TSVm : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   VmName;
  string   EnlightmentSettings;
};
```

## <a name="members"></a><span data-ttu-id="48309-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="48309-109">Members</span></span>

<span data-ttu-id="48309-110">La **clase \_ TSVm de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="48309-110">The **Win32\_TSVm** class has these types of members:</span></span>

-   [<span data-ttu-id="48309-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="48309-111">Methods</span></span>](#methods)
-   [<span data-ttu-id="48309-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48309-112">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="48309-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="48309-113">Methods</span></span>

<span data-ttu-id="48309-114">La clase **Win32 \_ TSVm** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="48309-114">The **Win32\_TSVm** class has these methods.</span></span>



| <span data-ttu-id="48309-115">Método</span><span class="sxs-lookup"><span data-stu-id="48309-115">Method</span></span>                                                                | <span data-ttu-id="48309-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="48309-116">Description</span></span>                                              |
|:----------------------------------------------------------------------|:---------------------------------------------------------|
| [<span data-ttu-id="48309-117">**DumpVmInfo**</span><span class="sxs-lookup"><span data-stu-id="48309-117">**DumpVmInfo**</span></span>](dumpvminfo-win32-tsvm.md)                           | <span data-ttu-id="48309-118">Solo con fines de prueba.</span><span class="sxs-lookup"><span data-stu-id="48309-118">For test purposes only.</span></span><br/>                       |
| [<span data-ttu-id="48309-119">**Exportación**</span><span class="sxs-lookup"><span data-stu-id="48309-119">**Export**</span></span>](export-win32-tsvm.md)                                   | <span data-ttu-id="48309-120">Obtiene información de supervisión de sesión de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="48309-120">Gets Session Monitoring Information of the VM</span></span><br/> |
| [<span data-ttu-id="48309-121">**QueryOfflineInformation**</span><span class="sxs-lookup"><span data-stu-id="48309-121">**QueryOfflineInformation**</span></span>](queryofflineinformation-win32-tsvm.md) | <span data-ttu-id="48309-122">Solo consulta las propiedades cuando está sin conexión.</span><span class="sxs-lookup"><span data-stu-id="48309-122">Queries properties only when it is offline.</span></span><br/>   |



 

### <a name="properties"></a><span data-ttu-id="48309-123">Propiedades</span><span class="sxs-lookup"><span data-stu-id="48309-123">Properties</span></span>

<span data-ttu-id="48309-124">La **clase \_ TSVm de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="48309-124">The **Win32\_TSVm** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="48309-125">**Caption**</span><span class="sxs-lookup"><span data-stu-id="48309-125">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48309-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48309-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48309-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48309-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48309-128">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="48309-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="48309-129">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="48309-129">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="48309-130">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="48309-130">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="48309-131">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="48309-131">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48309-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48309-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48309-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48309-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48309-134">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="48309-134">Description of the object.</span></span>

<span data-ttu-id="48309-135">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="48309-135">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="48309-136">**EnlightmentSettings**</span><span class="sxs-lookup"><span data-stu-id="48309-136">**EnlightmentSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48309-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48309-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48309-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="48309-138">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="48309-139">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="48309-139">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="48309-140">Un BLOB XML que contiene la configuración de la habilitación de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="48309-140">An XML BLOB that contains the enlightenment settings for the virtual machine.</span></span>

</dd> <dt>

<span data-ttu-id="48309-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="48309-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48309-142">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="48309-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="48309-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48309-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48309-144">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="48309-144">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="48309-145">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="48309-145">The date the object was installed.</span></span> <span data-ttu-id="48309-146">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="48309-146">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="48309-147">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="48309-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="48309-148">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="48309-148">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48309-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48309-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48309-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48309-150">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="48309-151">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="48309-151">The name of the object.</span></span>

<span data-ttu-id="48309-152">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="48309-152">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="48309-153">**Estado**</span><span class="sxs-lookup"><span data-stu-id="48309-153">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48309-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48309-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48309-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48309-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48309-156">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="48309-156">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="48309-157">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="48309-157">Current status of the object.</span></span> <span data-ttu-id="48309-158">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="48309-158">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="48309-159">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="48309-159">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="48309-160">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="48309-160">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="48309-161">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="48309-161">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="48309-162">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="48309-162">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="48309-163">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="48309-163">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="48309-164">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="48309-164">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="48309-165">("Error")</span><span class="sxs-lookup"><span data-stu-id="48309-165">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="48309-166">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="48309-166">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="48309-167">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="48309-167">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="48309-168">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="48309-168">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="48309-169">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="48309-169">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="48309-170">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="48309-170">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="48309-171">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="48309-171">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="48309-172">**VmName**</span><span class="sxs-lookup"><span data-stu-id="48309-172">**VmName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="48309-173">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="48309-173">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="48309-174">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="48309-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="48309-175">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="48309-175">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="48309-176">El nombre de la máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="48309-176">The name of the virtual machine.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="48309-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48309-177">Requirements</span></span>



| <span data-ttu-id="48309-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="48309-178">Requirement</span></span> | <span data-ttu-id="48309-179">Value</span><span class="sxs-lookup"><span data-stu-id="48309-179">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="48309-180">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48309-180">Minimum supported client</span></span><br/> | <span data-ttu-id="48309-181">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="48309-181">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="48309-182">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="48309-182">Minimum supported server</span></span><br/> | <span data-ttu-id="48309-183">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="48309-183">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="48309-184">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="48309-184">Namespace</span></span><br/>                | <span data-ttu-id="48309-185">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="48309-185">Root\\CIMV2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="48309-186">MOF</span><span class="sxs-lookup"><span data-stu-id="48309-186">MOF</span></span><br/>                      | <dl> <span data-ttu-id="48309-187"><dt>TSVmHost. mof</dt></span><span class="sxs-lookup"><span data-stu-id="48309-187"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="48309-188">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="48309-188">DLL</span></span><br/>                      | <dl> <span data-ttu-id="48309-189"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="48309-189"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



 

