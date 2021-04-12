---
title: Win32_RDCentralPublishedRemoteDesktop (clase)
description: Escritorio publicado en otro equipo, para su uso remoto a través de Terminal Services.
ms.assetid: 2b28a2d3-048f-446f-9ce0-eb684b393eaa
ms.tgt_platform: multiple
keywords:
- Win32_RDCentralPublishedRemoteDesktop clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_RDCentralPublishedRemoteDesktop de clase, se describe
topic_type:
- apiref
api_name:
- Win32_RDCentralPublishedRemoteDesktop
- Win32_RDCentralPublishedRemoteDesktop.Caption
- Win32_RDCentralPublishedRemoteDesktop.Description
- Win32_RDCentralPublishedRemoteDesktop.InstallDate
- Win32_RDCentralPublishedRemoteDesktop.Name
- Win32_RDCentralPublishedRemoteDesktop.Status
- Win32_RDCentralPublishedRemoteDesktop.PublishingFarm
- Win32_RDCentralPublishedRemoteDesktop.Alias
- Win32_RDCentralPublishedRemoteDesktop.IconContents
- Win32_RDCentralPublishedRemoteDesktop.ShowInPortal
- Win32_RDCentralPublishedRemoteDesktop.RDPFileContents
- Win32_RDCentralPublishedRemoteDesktop.Folders
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04696331b7027b7cc65d2202c29e6ce95bb3f4b8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490102"
---
# <a name="win32_rdcentralpublishedremotedesktop-class"></a><span data-ttu-id="a12ee-105">\_Clase Win32 RDCentralPublishedRemoteDesktop</span><span class="sxs-lookup"><span data-stu-id="a12ee-105">Win32\_RDCentralPublishedRemoteDesktop class</span></span>

<span data-ttu-id="a12ee-106">Escritorio publicado en otro equipo, para su uso remoto a través de Terminal Services</span><span class="sxs-lookup"><span data-stu-id="a12ee-106">Desktop published on another computer, for remote use through Terminal Services</span></span>

<span data-ttu-id="a12ee-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a12ee-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a12ee-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a12ee-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_RDCentralPublishedRemoteDesktop : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   PublishingFarm;
  string   Alias;
  uint8    IconContents[];
  boolean  ShowInPortal;
  string   RDPFileContents;
  string   Folders[];
};
```

## <a name="members"></a><span data-ttu-id="a12ee-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="a12ee-109">Members</span></span>

<span data-ttu-id="a12ee-110">La **clase \_ RDCentralPublishedRemoteDesktop de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a12ee-110">The **Win32\_RDCentralPublishedRemoteDesktop** class has these types of members:</span></span>

-   [<span data-ttu-id="a12ee-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a12ee-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a12ee-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a12ee-112">Properties</span></span>

<span data-ttu-id="a12ee-113">La **clase \_ RDCentralPublishedRemoteDesktop de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a12ee-113">The **Win32\_RDCentralPublishedRemoteDesktop** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a12ee-114">**Alias**</span><span class="sxs-lookup"><span data-stu-id="a12ee-114">**Alias**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a12ee-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a12ee-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-116">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a12ee-116">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-117">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a12ee-117">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a12ee-118">Alias del escritorio.</span><span class="sxs-lookup"><span data-stu-id="a12ee-118">Alias of the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="a12ee-119">**Caption**</span><span class="sxs-lookup"><span data-stu-id="a12ee-119">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a12ee-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a12ee-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a12ee-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-122">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="a12ee-122">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="a12ee-123">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="a12ee-123">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="a12ee-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a12ee-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a12ee-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="a12ee-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a12ee-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a12ee-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a12ee-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a12ee-128">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="a12ee-128">Description of the object.</span></span>

<span data-ttu-id="a12ee-129">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a12ee-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a12ee-130">**Carpetas**</span><span class="sxs-lookup"><span data-stu-id="a12ee-130">**Folders**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a12ee-131">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="a12ee-131">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a12ee-132">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a12ee-133">Lista de las carpetas en las que se debe mostrar este recurso.</span><span class="sxs-lookup"><span data-stu-id="a12ee-133">List of the folders where this resource should be displayed.</span></span>

</dd> <dt>

<span data-ttu-id="a12ee-134">**IconContents**</span><span class="sxs-lookup"><span data-stu-id="a12ee-134">**IconContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a12ee-135">Tipo de datos: **Uint8** array</span><span class="sxs-lookup"><span data-stu-id="a12ee-135">Data type: **uint8** array</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a12ee-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-137">Calificadores: [ **opcional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="a12ee-137">Qualifiers: [**optional**](/windows/desktop/WmiSdk/standard-wmi-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="a12ee-138">Contenido del icono correspondiente a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="a12ee-138">Contents of the icon corresponding to the application.</span></span>

</dd> <dt>

<span data-ttu-id="a12ee-139">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="a12ee-139">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a12ee-140">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="a12ee-140">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-141">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a12ee-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-142">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="a12ee-142">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="a12ee-143">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="a12ee-143">The date the object was installed.</span></span> <span data-ttu-id="a12ee-144">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="a12ee-144">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="a12ee-145">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a12ee-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a12ee-146">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="a12ee-146">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a12ee-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a12ee-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a12ee-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a12ee-149">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="a12ee-149">The name of the object.</span></span>

<span data-ttu-id="a12ee-150">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a12ee-150">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="a12ee-151">**PublishingFarm**</span><span class="sxs-lookup"><span data-stu-id="a12ee-151">**PublishingFarm**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a12ee-152">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a12ee-152">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-153">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a12ee-153">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-154">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a12ee-154">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="a12ee-155">Alias de la granja de servidores que publicó el escritorio.</span><span class="sxs-lookup"><span data-stu-id="a12ee-155">Alias of the farm that published the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="a12ee-156">**RDPFileContents**</span><span class="sxs-lookup"><span data-stu-id="a12ee-156">**RDPFileContents**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a12ee-157">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a12ee-157">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-158">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a12ee-158">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="a12ee-159">Contenido del archivo RDP correspondiente al escritorio.</span><span class="sxs-lookup"><span data-stu-id="a12ee-159">Contents of the RDP file corresponding to the desktop.</span></span>

</dd> <dt>

<span data-ttu-id="a12ee-160">**ShowInPortal**</span><span class="sxs-lookup"><span data-stu-id="a12ee-160">**ShowInPortal**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a12ee-161">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="a12ee-161">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-162">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a12ee-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="a12ee-163">**true** si esta aplicación debe mostrarse en el acceso web de TS; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="a12ee-163">**true** if this application should be shown in the TS Web Access; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="a12ee-164">**Estado**</span><span class="sxs-lookup"><span data-stu-id="a12ee-164">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a12ee-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a12ee-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a12ee-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a12ee-167">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="a12ee-167">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="a12ee-168">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="a12ee-168">Current status of the object.</span></span> <span data-ttu-id="a12ee-169">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="a12ee-169">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="a12ee-170">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="a12ee-170">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="a12ee-171">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="a12ee-171">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="a12ee-172">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="a12ee-172">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="a12ee-173">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="a12ee-173">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="a12ee-174">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="a12ee-174">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="a12ee-175">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="a12ee-175">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a12ee-176">("Error")</span><span class="sxs-lookup"><span data-stu-id="a12ee-176">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a12ee-177">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="a12ee-177">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a12ee-178">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="a12ee-178">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a12ee-179">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="a12ee-179">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a12ee-180">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="a12ee-180">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a12ee-181">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="a12ee-181">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="a12ee-182">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="a12ee-182">("Service")</span></span>


<span data-ttu-id="a12ee-183"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="a12ee-183"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="a12ee-184">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a12ee-184">Requirements</span></span>



| <span data-ttu-id="a12ee-185">Requisito</span><span class="sxs-lookup"><span data-stu-id="a12ee-185">Requirement</span></span> | <span data-ttu-id="a12ee-186">Value</span><span class="sxs-lookup"><span data-stu-id="a12ee-186">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="a12ee-187">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a12ee-187">Minimum supported client</span></span><br/> | <span data-ttu-id="a12ee-188">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a12ee-188">None supported</span></span><br/>                                                                |
| <span data-ttu-id="a12ee-189">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a12ee-189">Minimum supported server</span></span><br/> | <span data-ttu-id="a12ee-190">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="a12ee-190">Windows Server 2012</span></span><br/>                                                           |
| <span data-ttu-id="a12ee-191">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a12ee-191">Namespace</span></span><br/>                | <span data-ttu-id="a12ee-192">Raíz de \\ cimv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a12ee-192">Root\\cimv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="a12ee-193">MOF</span><span class="sxs-lookup"><span data-stu-id="a12ee-193">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a12ee-194"><dt>Tscpub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a12ee-194"><dt>Tscpub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="a12ee-195">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a12ee-195">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a12ee-196"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a12ee-196"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

