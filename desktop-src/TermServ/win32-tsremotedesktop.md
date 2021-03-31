---
title: Win32_TSRemoteDesktop (clase)
description: Describe una conexión a escritorio remoto que está disponible a través de Escritorio remoto acceso web (acceso web de escritorio remoto).
ms.assetid: 40c7d8f1-cc45-4f0a-8c07-8215342ca02e
ms.tgt_platform: multiple
keywords:
- Win32_TSRemoteDesktop clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSRemoteDesktop de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSRemoteDesktop
- Win32_TSRemoteDesktop.Caption
- Win32_TSRemoteDesktop.Description
- Win32_TSRemoteDesktop.InstallDate
- Win32_TSRemoteDesktop.Name
- Win32_TSRemoteDesktop.Status
- Win32_TSRemoteDesktop.Alias
- Win32_TSRemoteDesktop.SecurityDescriptor
- Win32_TSRemoteDesktop.IconPath
- Win32_TSRemoteDesktop.IconIndex
- Win32_TSRemoteDesktop.IconContents
- Win32_TSRemoteDesktop.ShowInPortal
- Win32_TSRemoteDesktop.RDPFileContents
- Win32_TSRemoteDesktop.IsVmFarm
- Win32_TSRemoteDesktop.VmFarmSettings
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b3a23e63d5c79313933b7ce6951265a85740bc8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149956"
---
# <a name="win32_tsremotedesktop-class"></a><span data-ttu-id="69a40-105">\_Clase Win32 TSRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="69a40-105">Win32\_TSRemoteDesktop class</span></span>

<span data-ttu-id="69a40-106">Describe una conexión a escritorio remoto que está disponible a través de Escritorio remoto acceso web (acceso web de escritorio remoto).</span><span class="sxs-lookup"><span data-stu-id="69a40-106">Describes a remote desktop connection that is available through Remote Desktop Web Access (RD Web Access).</span></span>

## <a name="syntax"></a><span data-ttu-id="69a40-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="69a40-107">Syntax</span></span>

``` syntax
class Win32_TSRemoteDesktop : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   Alias;
  string   SecurityDescriptor;
  string   IconPath;
  sint32   IconIndex;
  uint8    IconContents[];
  boolean  ShowInPortal;
  string   RDPFileContents;
  boolean  IsVmFarm;
  string   VmFarmSettings;
};
```

## <a name="members"></a><span data-ttu-id="69a40-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="69a40-108">Members</span></span>

<span data-ttu-id="69a40-109">La **clase \_ TSRemoteDesktop de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="69a40-109">The **Win32\_TSRemoteDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="69a40-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="69a40-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="69a40-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="69a40-111">Properties</span></span>

<span data-ttu-id="69a40-112">La **clase \_ TSRemoteDesktop de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="69a40-112">The **Win32\_TSRemoteDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="69a40-113">**Alias**</span><span class="sxs-lookup"><span data-stu-id="69a40-113">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69a40-114">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="69a40-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69a40-115">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="69a40-115">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="69a40-116">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="69a40-116">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="69a40-117">El alias de la conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="69a40-117">The alias of the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="69a40-118">**Caption**</span><span class="sxs-lookup"><span data-stu-id="69a40-118">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69a40-119">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="69a40-119">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69a40-120">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="69a40-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69a40-121">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="69a40-121">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="69a40-122">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="69a40-122">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="69a40-123">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="69a40-123">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="69a40-124">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="69a40-124">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69a40-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="69a40-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69a40-126">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="69a40-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69a40-127">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="69a40-127">Description of the object.</span></span>

<span data-ttu-id="69a40-128">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="69a40-128">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="69a40-129">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="69a40-129">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69a40-130">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="69a40-130">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="69a40-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="69a40-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69a40-132">El contenido de bytes del icono que corresponde a la conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="69a40-132">The byte contents of the icon that corresponds to the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="69a40-133">**IconIndex**</span><span class="sxs-lookup"><span data-stu-id="69a40-133">**IconIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69a40-134">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="69a40-134">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="69a40-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="69a40-135">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="69a40-136">Índice o identificador del icono de la conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="69a40-136">The index or ID of the icon for the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="69a40-137">**IconPath**</span><span class="sxs-lookup"><span data-stu-id="69a40-137">**IconPath**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69a40-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="69a40-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69a40-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="69a40-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="69a40-140">Ruta de acceso del icono de la conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="69a40-140">Path of the icon for the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="69a40-141">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="69a40-141">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69a40-142">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="69a40-142">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="69a40-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="69a40-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69a40-144">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="69a40-144">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="69a40-145">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="69a40-145">The date the object was installed.</span></span> <span data-ttu-id="69a40-146">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="69a40-146">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="69a40-147">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="69a40-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="69a40-148">**IsVmFarm**</span><span class="sxs-lookup"><span data-stu-id="69a40-148">**IsVmFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69a40-149">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="69a40-149">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="69a40-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="69a40-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="69a40-151">Indica si esta conexión a escritorio remoto forma parte de una granja de máquinas virtuales.</span><span class="sxs-lookup"><span data-stu-id="69a40-151">Indicates if this remote desktop connection is part of a virtual machine farm.</span></span>

</dd> <dt>

<span data-ttu-id="69a40-152">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="69a40-152">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69a40-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="69a40-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69a40-154">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="69a40-154">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="69a40-155">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="69a40-155">The name of the object.</span></span>

<span data-ttu-id="69a40-156">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="69a40-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="69a40-157">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="69a40-157">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69a40-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="69a40-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69a40-159">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="69a40-159">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="69a40-160">Contenido del archivo RDP que corresponde a la conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="69a40-160">Contents of the RDP file that correspond to the remote desktop connection.</span></span>

</dd> <dt>

<span data-ttu-id="69a40-161">**SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="69a40-161">**SecurityDescriptor**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69a40-162">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="69a40-162">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69a40-163">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="69a40-163">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="69a40-164">Un descriptor de seguridad que controla el acceso a la conexión a escritorio remoto, en formato SDDL.</span><span class="sxs-lookup"><span data-stu-id="69a40-164">A security descriptor that controls access to the remote desktop connection, in SDDL format.</span></span> <span data-ttu-id="69a40-165">Una cadena vacía implica permitir todo acceso.</span><span class="sxs-lookup"><span data-stu-id="69a40-165">An empty string implies allow all access.</span></span> <span data-ttu-id="69a40-166">Este descriptor de seguridad no admite ACE de denegación ni ACE que hagan referencia a usuarios o grupos que no son de dominio.</span><span class="sxs-lookup"><span data-stu-id="69a40-166">This security descriptor does not support DENY ACEs, or ACEs that refer to nondomain users or groups.</span></span>

</dd> <dt>

<span data-ttu-id="69a40-167">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="69a40-167">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69a40-168">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="69a40-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="69a40-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="69a40-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="69a40-170">Indica si se debe mostrar la conexión a escritorio remoto en acceso web de escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="69a40-170">Indicates whether the remote desktop connection should be shown in RD Web Access.</span></span>

</dd> <dt>

<span data-ttu-id="69a40-171">**Estado**</span><span class="sxs-lookup"><span data-stu-id="69a40-171">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69a40-172">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="69a40-172">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69a40-173">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="69a40-173">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="69a40-174">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="69a40-174">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="69a40-175">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="69a40-175">Current status of the object.</span></span> <span data-ttu-id="69a40-176">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="69a40-176">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="69a40-177">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="69a40-177">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="69a40-178">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="69a40-178">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="69a40-179">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="69a40-179">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="69a40-180">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="69a40-180">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="69a40-181">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="69a40-181">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="69a40-182">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="69a40-182">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="69a40-183">("Error")</span><span class="sxs-lookup"><span data-stu-id="69a40-183">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="69a40-184">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="69a40-184">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="69a40-185">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="69a40-185">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="69a40-186">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="69a40-186">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="69a40-187">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="69a40-187">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="69a40-188">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="69a40-188">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="69a40-189">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="69a40-189">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="69a40-190">**VmFarmSettings**</span><span class="sxs-lookup"><span data-stu-id="69a40-190">**VmFarmSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="69a40-191">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="69a40-191">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="69a40-192">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="69a40-192">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="69a40-193">Configuración de la granja de máquinas virtuales para la conexión a escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="69a40-193">Virtual machine farm settings for the remote desktop connection.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="69a40-194">Observaciones</span><span class="sxs-lookup"><span data-stu-id="69a40-194">Remarks</span></span>

<span data-ttu-id="69a40-195">Debe ser miembro del grupo administradores para establecer las propiedades utilizando esta clase.</span><span class="sxs-lookup"><span data-stu-id="69a40-195">You must be a member of the Administrators group to set properties by using this class.</span></span>

<span data-ttu-id="69a40-196">Para conectarse al \\ espacio de \\ nombres TerminalServices de cimv2 raíz \\ , el nivel de autenticación debe incluir privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="69a40-196">To connect to the \\root\\CIMV2\\TerminalServices namespace, the authentication level must include packet privacy.</span></span> <span data-ttu-id="69a40-197">En el caso de las llamadas de C/C++, se trata de un nivel de autenticación de **\_ \_ \_ \_ \_ privacidad de nivel** de autenticación de RPC C, que se puede establecer mediante la función com [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) .</span><span class="sxs-lookup"><span data-stu-id="69a40-197">For C/C++ calls, this is an authentication level of **RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**, which can be set by using the [**CoSetProxyBlanket**](/windows/win32/api/combaseapi/nf-combaseapi-cosetproxyblanket) COM function.</span></span> <span data-ttu-id="69a40-198">En el caso de las llamadas de Visual Basic y scripting, se trata de un nivel de autenticación de **WbemAuthenticationLevelPktPrivacy** o "pktPrivacy", con un valor de 6.</span><span class="sxs-lookup"><span data-stu-id="69a40-198">For Visual Basic and scripting calls, this is an authentication level of **WbemAuthenticationLevelPktPrivacy** or "pktPrivacy", with a value of 6.</span></span> <span data-ttu-id="69a40-199">En el siguiente ejemplo de Visual Basic Scripting Edition (VBScript) se muestra cómo conectarse a un equipo remoto con privacidad de paquetes.</span><span class="sxs-lookup"><span data-stu-id="69a40-199">The following Visual Basic Scripting Edition (VBScript) example shows how to connect to a remote computer with packet privacy.</span></span>


```VB
strComputer = "RemoteServer1" 
Set objServices = GetObject( _
    "winmgmts:{authenticationLevel=pktPrivacy}!Root/CIMv2/TerminalServices")
```



<span data-ttu-id="69a40-200">Los archivos Managed Object Format (MOF) contienen las definiciones de las clases de Instrumental de administración de Windows (WMI).</span><span class="sxs-lookup"><span data-stu-id="69a40-200">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="69a40-201">Los archivos MOF no se instalan como parte del kit de desarrollo de software (SDK) de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="69a40-201">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="69a40-202">Se instalan en el servidor cuando se agrega el rol asociado mediante el Administrador del servidor.</span><span class="sxs-lookup"><span data-stu-id="69a40-202">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="69a40-203">Para obtener más información acerca de los archivos MOF, consulte [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="69a40-203">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="69a40-204">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69a40-204">Requirements</span></span>



| <span data-ttu-id="69a40-205">Requisito</span><span class="sxs-lookup"><span data-stu-id="69a40-205">Requirement</span></span> | <span data-ttu-id="69a40-206">Value</span><span class="sxs-lookup"><span data-stu-id="69a40-206">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="69a40-207">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69a40-207">Minimum supported client</span></span><br/> | <span data-ttu-id="69a40-208">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="69a40-208">None supported</span></span><br/>                                                               |
| <span data-ttu-id="69a40-209">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="69a40-209">Minimum supported server</span></span><br/> | <span data-ttu-id="69a40-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="69a40-210">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="69a40-211">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="69a40-211">Namespace</span></span><br/>                | <span data-ttu-id="69a40-212">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="69a40-212">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="69a40-213">MOF</span><span class="sxs-lookup"><span data-stu-id="69a40-213">MOF</span></span><br/>                      | <dl> <span data-ttu-id="69a40-214"><dt>Tsallow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="69a40-214"><dt>Tsallow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="69a40-215">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="69a40-215">DLL</span></span><br/>                      | <dl> <span data-ttu-id="69a40-216"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="69a40-216"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

