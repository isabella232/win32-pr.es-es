---
title: Win32_TSDeploymentLicensing (clase)
description: Configuración de licencias para la implementación de Escritorio remoto Virtualization (RDV).
ms.assetid: 78e95629-6580-4aa1-bcbd-a79af44ddb54
ms.tgt_platform: multiple
keywords:
- Win32_TSDeploymentLicensing clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSDeploymentLicensing de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSDeploymentLicensing
- Win32_TSDeploymentLicensing.Caption
- Win32_TSDeploymentLicensing.Description
- Win32_TSDeploymentLicensing.InstallDate
- Win32_TSDeploymentLicensing.Name
- Win32_TSDeploymentLicensing.Status
- Win32_TSDeploymentLicensing.UseCentralLicensingSettings
- Win32_TSDeploymentLicensing.LicenseServers
- Win32_TSDeploymentLicensing.LicensingType
api_location:
- TsPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 952f58daa8a809e158265aac71b0094c0cd46fd6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676918"
---
# <a name="win32_tsdeploymentlicensing-class"></a><span data-ttu-id="512d7-105">\_Clase Win32 TSDeploymentLicensing</span><span class="sxs-lookup"><span data-stu-id="512d7-105">Win32\_TSDeploymentLicensing class</span></span>

<span data-ttu-id="512d7-106">Configuración de licencias para la implementación de Escritorio remoto Virtualization (RDV).</span><span class="sxs-lookup"><span data-stu-id="512d7-106">Licensing Settings for the Remote Desktop Virtualization (RDV) deployment.</span></span>

<span data-ttu-id="512d7-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="512d7-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="512d7-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="512d7-108">Syntax</span></span>

``` syntax
class Win32_TSDeploymentLicensing : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  boolean  UseCentralLicensingSettings;
  String   LicenseServers[];
  uint32   LicensingType;
};
```

## <a name="members"></a><span data-ttu-id="512d7-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="512d7-109">Members</span></span>

<span data-ttu-id="512d7-110">La **clase \_ TSDeploymentLicensing de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="512d7-110">The **Win32\_TSDeploymentLicensing** class has these types of members:</span></span>

-   [<span data-ttu-id="512d7-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="512d7-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="512d7-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="512d7-112">Properties</span></span>

<span data-ttu-id="512d7-113">La **clase \_ TSDeploymentLicensing de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="512d7-113">The **Win32\_TSDeploymentLicensing** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="512d7-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="512d7-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="512d7-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="512d7-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="512d7-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="512d7-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="512d7-117">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="512d7-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="512d7-118">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="512d7-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="512d7-119">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="512d7-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="512d7-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="512d7-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="512d7-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="512d7-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="512d7-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="512d7-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="512d7-123">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="512d7-123">Description of the object.</span></span>

<span data-ttu-id="512d7-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="512d7-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="512d7-125">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="512d7-125">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="512d7-126">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="512d7-126">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="512d7-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="512d7-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="512d7-128">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="512d7-128">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="512d7-129">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="512d7-129">The date the object was installed.</span></span> <span data-ttu-id="512d7-130">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="512d7-130">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="512d7-131">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="512d7-131">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="512d7-132">**LicenseServers**</span><span class="sxs-lookup"><span data-stu-id="512d7-132">**LicenseServers**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="512d7-133">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="512d7-133">Data type: **String** array</span></span>
</dt> <dt>

<span data-ttu-id="512d7-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="512d7-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="512d7-135">Especifica los servidores de licencias que se usarán.</span><span class="sxs-lookup"><span data-stu-id="512d7-135">Specifies the license servers to use.</span></span>

</dd> <dt>

<span data-ttu-id="512d7-136">**LicensingType**</span><span class="sxs-lookup"><span data-stu-id="512d7-136">**LicensingType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="512d7-137">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="512d7-137">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="512d7-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="512d7-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="512d7-139">Modo de licencia</span><span class="sxs-lookup"><span data-stu-id="512d7-139">Licensing Mode</span></span>

<dt>

<span id="Per_Device"></span><span id="per_device"></span><span id="PER_DEVICE"></span>

<span data-ttu-id="512d7-140">**Por dispositivo** (2)</span><span class="sxs-lookup"><span data-stu-id="512d7-140">**Per Device** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Per_User"></span><span id="per_user"></span><span id="PER_USER"></span>

<span data-ttu-id="512d7-141">**Por usuario** (4)</span><span class="sxs-lookup"><span data-stu-id="512d7-141">**Per User** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Yet_Configured"></span><span id="not_yet_configured"></span><span id="NOT_YET_CONFIGURED"></span>

<span data-ttu-id="512d7-142">**Todavía no se ha configurado** (5)</span><span class="sxs-lookup"><span data-stu-id="512d7-142">**Not Yet Configured** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="512d7-143">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="512d7-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="512d7-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="512d7-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="512d7-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="512d7-145">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="512d7-146">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="512d7-146">The name of the object.</span></span>

<span data-ttu-id="512d7-147">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="512d7-147">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="512d7-148">**Estado**</span><span class="sxs-lookup"><span data-stu-id="512d7-148">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="512d7-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="512d7-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="512d7-150">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="512d7-150">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="512d7-151">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="512d7-151">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="512d7-152">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="512d7-152">Current status of the object.</span></span> <span data-ttu-id="512d7-153">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="512d7-153">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="512d7-154">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="512d7-154">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="512d7-155">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="512d7-155">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="512d7-156">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="512d7-156">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="512d7-157">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="512d7-157">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="512d7-158">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="512d7-158">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="512d7-159">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="512d7-159">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="512d7-160">("Error")</span><span class="sxs-lookup"><span data-stu-id="512d7-160">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="512d7-161">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="512d7-161">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="512d7-162">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="512d7-162">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="512d7-163">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="512d7-163">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="512d7-164">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="512d7-164">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="512d7-165">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="512d7-165">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="512d7-166">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="512d7-166">("Service")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="512d7-167">**UseCentralLicensingSettings**</span><span class="sxs-lookup"><span data-stu-id="512d7-167">**UseCentralLicensingSettings**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="512d7-168">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="512d7-168">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="512d7-169">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="512d7-169">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="512d7-170">Especifica si se va a usar la configuración de licencias en todo el nivel de implementación.</span><span class="sxs-lookup"><span data-stu-id="512d7-170">Specifies whether to use deployment-wide licensing settings.</span></span> <span data-ttu-id="512d7-171">**True** para usar esta configuración para todos los servidores de esta implementación.</span><span class="sxs-lookup"><span data-stu-id="512d7-171">**True** to use these settings for all servers in this deployment.</span></span> <span data-ttu-id="512d7-172">**false** para establecerlos por servidor.</span><span class="sxs-lookup"><span data-stu-id="512d7-172">**false** to set them per-server.</span></span> <span data-ttu-id="512d7-173">Si se establece en **false**, se omiten todas las demás opciones de configuración de licencias.</span><span class="sxs-lookup"><span data-stu-id="512d7-173">If this is set to **false**, all other licensing settings are ignored.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="512d7-174">Requisitos</span><span class="sxs-lookup"><span data-stu-id="512d7-174">Requirements</span></span>



| <span data-ttu-id="512d7-175">Requisito</span><span class="sxs-lookup"><span data-stu-id="512d7-175">Requirement</span></span> | <span data-ttu-id="512d7-176">Value</span><span class="sxs-lookup"><span data-stu-id="512d7-176">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="512d7-177">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="512d7-177">Minimum supported client</span></span><br/> | <span data-ttu-id="512d7-178">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="512d7-178">None supported</span></span><br/>                                                               |
| <span data-ttu-id="512d7-179">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="512d7-179">Minimum supported server</span></span><br/> | <span data-ttu-id="512d7-180">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="512d7-180">Windows Server 2012</span></span><br/>                                                          |
| <span data-ttu-id="512d7-181">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="512d7-181">Namespace</span></span><br/>                | <span data-ttu-id="512d7-182">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="512d7-182">Root\\cimv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="512d7-183">MOF</span><span class="sxs-lookup"><span data-stu-id="512d7-183">MOF</span></span><br/>                      | <dl> <span data-ttu-id="512d7-184"><dt>TsAllow. mof</dt></span><span class="sxs-lookup"><span data-stu-id="512d7-184"><dt>TsAllow.mof</dt></span></span> </dl>  |
| <span data-ttu-id="512d7-185">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="512d7-185">DLL</span></span><br/>                      | <dl> <span data-ttu-id="512d7-186"><dt>TsPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="512d7-186"><dt>TsPubWmi.dll</dt></span></span> </dl> |



 

