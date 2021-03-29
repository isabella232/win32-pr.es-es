---
title: Win32_TSCPubPlugin (clase)
description: Representa un complemento que está configurado para usarse a través del servicio de Administración de conexiones de RemoteApp y Escritorio.
ms.assetid: 0eebdeea-4bfb-4032-a28b-870df7103473
ms.tgt_platform: multiple
keywords:
- Win32_TSCPubPlugin clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSCPubPlugin de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSCPubPlugin
- Win32_TSCPubPlugin.Caption
- Win32_TSCPubPlugin.Description
- Win32_TSCPubPlugin.InstallDate
- Win32_TSCPubPlugin.Name
- Win32_TSCPubPlugin.Status
- Win32_TSCPubPlugin.CLSID
- Win32_TSCPubPlugin.IsEnabled
api_location:
- TscPubWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c0b4fcff8cadae32d59fe45c61c506e768782d5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905190"
---
# <a name="win32_tscpubplugin-class"></a><span data-ttu-id="715fd-105">\_Clase Win32 TSCPubPlugin</span><span class="sxs-lookup"><span data-stu-id="715fd-105">Win32\_TSCPubPlugin class</span></span>

<span data-ttu-id="715fd-106">Representa un complemento que está configurado para usarse a través del servicio de Administración de conexiones de RemoteApp y Escritorio.</span><span class="sxs-lookup"><span data-stu-id="715fd-106">Represents a plug-in that is configured to be used through the RemoteApp and Desktop Connection Management Service.</span></span>

<span data-ttu-id="715fd-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="715fd-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="715fd-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="715fd-108">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_TSCentralPublisher_Prov")]
class Win32_TSCPubPlugin : CIM_LogicalElement
{
  string   Caption;
  string   Description;
  datetime InstallDate;
  string   Name;
  string   Status;
  string   CLSID;
  boolean  IsEnabled;
};
```

## <a name="members"></a><span data-ttu-id="715fd-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="715fd-109">Members</span></span>

<span data-ttu-id="715fd-110">La **clase \_ TSCPubPlugin de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="715fd-110">The **Win32\_TSCPubPlugin** class has these types of members:</span></span>

-   [<span data-ttu-id="715fd-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="715fd-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="715fd-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="715fd-112">Properties</span></span>

<span data-ttu-id="715fd-113">La **clase \_ TSCPubPlugin de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="715fd-113">The **Win32\_TSCPubPlugin** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="715fd-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="715fd-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="715fd-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="715fd-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="715fd-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="715fd-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="715fd-117">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="715fd-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="715fd-118">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="715fd-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="715fd-119">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="715fd-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="715fd-120">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="715fd-120">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="715fd-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="715fd-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="715fd-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="715fd-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="715fd-123">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="715fd-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="715fd-124">CLSID del complemento.</span><span class="sxs-lookup"><span data-stu-id="715fd-124">The CLSID of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="715fd-125">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="715fd-125">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="715fd-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="715fd-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="715fd-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="715fd-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="715fd-128">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="715fd-128">Description of the object.</span></span>

<span data-ttu-id="715fd-129">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="715fd-129">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="715fd-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="715fd-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="715fd-131">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="715fd-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="715fd-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="715fd-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="715fd-133">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="715fd-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="715fd-134">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="715fd-134">The date the object was installed.</span></span> <span data-ttu-id="715fd-135">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="715fd-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="715fd-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="715fd-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="715fd-137">**IsEnabled**</span><span class="sxs-lookup"><span data-stu-id="715fd-137">**IsEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="715fd-138">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="715fd-138">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="715fd-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="715fd-139">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="715fd-140">Especifica si está habilitado el complemento.</span><span class="sxs-lookup"><span data-stu-id="715fd-140">Specifies whether the plug-in is enabled.</span></span>

</dd> <dt>

<span data-ttu-id="715fd-141">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="715fd-141">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="715fd-142">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="715fd-142">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="715fd-143">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="715fd-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="715fd-144">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="715fd-144">The name of the object.</span></span>

<span data-ttu-id="715fd-145">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="715fd-145">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="715fd-146">**Estado**</span><span class="sxs-lookup"><span data-stu-id="715fd-146">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="715fd-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="715fd-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="715fd-148">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="715fd-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="715fd-149">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="715fd-149">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="715fd-150">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="715fd-150">Current status of the object.</span></span> <span data-ttu-id="715fd-151">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="715fd-151">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="715fd-152">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="715fd-152">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="715fd-153">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="715fd-153">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="715fd-154">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="715fd-154">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="715fd-155">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="715fd-155">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="715fd-156">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="715fd-156">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="715fd-157">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="715fd-157">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="715fd-158">("Error")</span><span class="sxs-lookup"><span data-stu-id="715fd-158">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="715fd-159">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="715fd-159">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="715fd-160">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="715fd-160">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="715fd-161">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="715fd-161">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="715fd-162">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="715fd-162">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="715fd-163">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="715fd-163">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="715fd-164">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="715fd-164">("Service")</span></span>


<span data-ttu-id="715fd-165"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="715fd-165"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="715fd-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="715fd-166">Requirements</span></span>



| <span data-ttu-id="715fd-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="715fd-167">Requirement</span></span> | <span data-ttu-id="715fd-168">Value</span><span class="sxs-lookup"><span data-stu-id="715fd-168">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="715fd-169">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="715fd-169">Minimum supported client</span></span><br/> | <span data-ttu-id="715fd-170">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="715fd-170">None supported</span></span><br/>                                                                |
| <span data-ttu-id="715fd-171">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="715fd-171">Minimum supported server</span></span><br/> | <span data-ttu-id="715fd-172">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="715fd-172">Windows Server 2008 R2</span></span><br/>                                                        |
| <span data-ttu-id="715fd-173">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="715fd-173">Namespace</span></span><br/>                | <span data-ttu-id="715fd-174">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="715fd-174">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="715fd-175">MOF</span><span class="sxs-lookup"><span data-stu-id="715fd-175">MOF</span></span><br/>                      | <dl> <span data-ttu-id="715fd-176"><dt>TscPub. mof</dt></span><span class="sxs-lookup"><span data-stu-id="715fd-176"><dt>TscPub.mof</dt></span></span> </dl>    |
| <span data-ttu-id="715fd-177">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="715fd-177">DLL</span></span><br/>                      | <dl> <span data-ttu-id="715fd-178"><dt>TscPubWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="715fd-178"><dt>TscPubWmi.dll</dt></span></span> </dl> |



 

