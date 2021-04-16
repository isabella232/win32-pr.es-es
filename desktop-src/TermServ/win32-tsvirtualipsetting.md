---
title: Win32_TSVirtualIPSetting (clase)
description: Representa la asociación entre una clase de elemento de Win32 \_ TerminalService y una \_ clase de configuración TSVirtualIP de Win32.
ms.assetid: 06a78b4d-973a-4912-b7e6-bc490197c4a6
ms.tgt_platform: multiple
keywords:
- Win32_TSVirtualIPSetting clase Servicios de Escritorio remoto
- Servicios de Escritorio remoto de Win32_TSVirtualIPSetting de clase, se describe
topic_type:
- apiref
api_name:
- Win32_TSVirtualIPSetting
- Win32_TSVirtualIPSetting.Caption
- Win32_TSVirtualIPSetting.Description
- Win32_TSVirtualIPSetting.InstallDate
- Win32_TSVirtualIPSetting.Name
- Win32_TSVirtualIPSetting.Status
- Win32_TSVirtualIPSetting.Element
- Win32_TSVirtualIPSetting.Setting
api_location:
- TSCfgWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7368b3b2e932f45d047d4ca4db724030b2dd82ad
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685862"
---
# <a name="win32_tsvirtualipsetting-class"></a><span data-ttu-id="38e19-105">\_Clase Win32 TSVirtualIPSetting</span><span class="sxs-lookup"><span data-stu-id="38e19-105">Win32\_TSVirtualIPSetting class</span></span>

<span data-ttu-id="38e19-106">Representa la asociación entre una clase de elemento de [**Win32 \_ TerminalService**](win32-terminalservice.md) y una clase de configuración [**\_ TSVirtualIP de Win32**](win32-tsvirtualip.md) .</span><span class="sxs-lookup"><span data-stu-id="38e19-106">Represents the association between a [**Win32\_TerminalService**](win32-terminalservice.md) element class and a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) setting class.</span></span>

<span data-ttu-id="38e19-107">La siguiente sintaxis se simplifica desde el código de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="38e19-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="38e19-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38e19-108">Syntax</span></span>

``` syntax
[Dynamic, Provider("Win32_WIN32_TSVIRTUALIPSETTING_Prov"), ClassContext("local|hkey_local_machine\\SYSTEM\\CurrentControlSet\\Control\\TerminalServer\\TSAppSrv\\VirtualIP"), AMENDMENT]
class Win32_TSVirtualIPSetting : CIM_ElementSetting
{
  string                    Caption;
  string                    Description;
  datetime                  InstallDate;
  string                    Name;
  string                    Status;
  Win32_TerminalService REF Element;
  Win32_TSVirtualIP     REF Setting;
};
```

## <a name="members"></a><span data-ttu-id="38e19-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="38e19-109">Members</span></span>

<span data-ttu-id="38e19-110">La **clase \_ TSVirtualIPSetting de Win32** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="38e19-110">The **Win32\_TSVirtualIPSetting** class has these types of members:</span></span>

-   [<span data-ttu-id="38e19-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="38e19-111">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="38e19-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="38e19-112">Properties</span></span>

<span data-ttu-id="38e19-113">La **clase \_ TSVirtualIPSetting de Win32** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="38e19-113">The **Win32\_TSVirtualIPSetting** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="38e19-114">**Caption**</span><span class="sxs-lookup"><span data-stu-id="38e19-114">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e19-115">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="38e19-115">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38e19-116">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e19-116">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38e19-117">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="38e19-117">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="38e19-118">Descripción breve (cadena de una línea) del objeto.</span><span class="sxs-lookup"><span data-stu-id="38e19-118">Short description (one-line string) of the object.</span></span>

<span data-ttu-id="38e19-119">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="38e19-119">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="38e19-120">**Descripción**</span><span class="sxs-lookup"><span data-stu-id="38e19-120">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e19-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="38e19-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38e19-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e19-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38e19-123">Descripción del objeto.</span><span class="sxs-lookup"><span data-stu-id="38e19-123">Description of the object.</span></span>

<span data-ttu-id="38e19-124">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="38e19-124">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="38e19-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="38e19-125">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e19-126">Tipo de datos: **[ **Win32 \_ TerminalService**](win32-terminalservice.md)**</span><span class="sxs-lookup"><span data-stu-id="38e19-126">Data type: **[**Win32\_TerminalService**](win32-terminalservice.md)**</span></span>
</dt> <dt>

<span data-ttu-id="38e19-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e19-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38e19-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="38e19-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="38e19-129">Referencia a un objeto [**\_ TerminalService de Win32**](win32-terminalservice.md) que es la clase de elemento de la asociación.</span><span class="sxs-lookup"><span data-stu-id="38e19-129">A reference to a [**Win32\_TerminalService**](win32-terminalservice.md) object that is the element class for the association.</span></span>

</dd> <dt>

<span data-ttu-id="38e19-130">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="38e19-130">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e19-131">Tipo de datos: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="38e19-131">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="38e19-132">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e19-132">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38e19-133">Calificadores: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. DMTF \| ComponentID \| 001,5 ")</span><span class="sxs-lookup"><span data-stu-id="38e19-133">Qualifiers: [**Mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|ComponentID\|001.5")</span></span>
</dt> </dl>

<span data-ttu-id="38e19-134">Fecha en que se instaló el objeto.</span><span class="sxs-lookup"><span data-stu-id="38e19-134">The date the object was installed.</span></span> <span data-ttu-id="38e19-135">La falta de un valor no indica que el objeto no está instalado.</span><span class="sxs-lookup"><span data-stu-id="38e19-135">A lack of a value does not indicate that the object is not installed.</span></span>

<span data-ttu-id="38e19-136">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="38e19-136">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="38e19-137">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="38e19-137">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e19-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="38e19-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38e19-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e19-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="38e19-140">El nombre del objeto.</span><span class="sxs-lookup"><span data-stu-id="38e19-140">The name of the object.</span></span>

<span data-ttu-id="38e19-141">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="38e19-141">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="38e19-142">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="38e19-142">**Setting**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e19-143">Tipo de datos: **[ **Win32 \_ TSVirtualIP**](win32-tsvirtualip.md)**</span><span class="sxs-lookup"><span data-stu-id="38e19-143">Data type: **[**Win32\_TSVirtualIP**](win32-tsvirtualip.md)**</span></span>
</dt> <dt>

<span data-ttu-id="38e19-144">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e19-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38e19-145">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="38e19-145">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="38e19-146">Referencia a un objeto [**\_ TSVirtualIP de Win32**](win32-tsvirtualip.md) que es la clase de configuración para la asociación.</span><span class="sxs-lookup"><span data-stu-id="38e19-146">A reference to a [**Win32\_TSVirtualIP**](win32-tsvirtualip.md) object that is the setting class for the association.</span></span>

</dd> <dt>

<span data-ttu-id="38e19-147">**Estado**</span><span class="sxs-lookup"><span data-stu-id="38e19-147">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="38e19-148">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="38e19-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="38e19-149">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="38e19-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="38e19-150">Calificadores: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span><span class="sxs-lookup"><span data-stu-id="38e19-150">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (10)</span></span>
</dt> </dl>

<span data-ttu-id="38e19-151">Estado actual del objeto.</span><span class="sxs-lookup"><span data-stu-id="38e19-151">Current status of the object.</span></span> <span data-ttu-id="38e19-152">Se pueden definir varios Estados operativos y no operativos.</span><span class="sxs-lookup"><span data-stu-id="38e19-152">Various operational and nonoperational statuses can be defined.</span></span> <span data-ttu-id="38e19-153">Los Estados operativos incluyen: "correcto", "degradado" y "Pred FAIL" (un elemento, como una unidad de disco duro habilitada para SMART, puede estar funcionando correctamente pero prediciendo un error en un futuro próximo).</span><span class="sxs-lookup"><span data-stu-id="38e19-153">Operational statuses include: "OK", "Degraded", and "Pred Fail" (an element, such as a SMART-enabled hard disk drive, may be functioning properly but predicting a failure in the near future).</span></span> <span data-ttu-id="38e19-154">Los Estados no operativos incluyen: "error", "iniciando", "deteniendo" y "servicio".</span><span class="sxs-lookup"><span data-stu-id="38e19-154">Nonoperational statuses include: "Error", "Starting", "Stopping", and "Service".</span></span> <span data-ttu-id="38e19-155">El último, "servicio", se puede aplicar durante la resilverización del reflejo de un disco, la recarga de una lista de permisos de usuario u otro trabajo administrativo.</span><span class="sxs-lookup"><span data-stu-id="38e19-155">The latter, "Service", could apply during mirror-resilvering of a disk, reload of a user permissions list, or other administrative work.</span></span> <span data-ttu-id="38e19-156">No todo el trabajo está en línea, pero el elemento administrado no es "OK" ni está en uno de los otros Estados.</span><span class="sxs-lookup"><span data-stu-id="38e19-156">Not all such work is on-line, yet the managed element is neither "OK" nor in one of the other states.</span></span>

<span data-ttu-id="38e19-157">Esta propiedad se hereda del [**\_ ManagedSystemElement de CIM**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="38e19-157">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<dt>



 <span data-ttu-id="38e19-158">("Correcto")</span><span class="sxs-lookup"><span data-stu-id="38e19-158">("OK")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="38e19-159">("Error")</span><span class="sxs-lookup"><span data-stu-id="38e19-159">("Error")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="38e19-160">("Degradado")</span><span class="sxs-lookup"><span data-stu-id="38e19-160">("Degraded")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="38e19-161">("Desconocido")</span><span class="sxs-lookup"><span data-stu-id="38e19-161">("Unknown")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="38e19-162">("Pred FAIL")</span><span class="sxs-lookup"><span data-stu-id="38e19-162">("Pred Fail")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="38e19-163">("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="38e19-163">("Starting")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="38e19-164">("Deteniéndose")</span><span class="sxs-lookup"><span data-stu-id="38e19-164">("Stopping")</span></span>


</dt> <dd></dd> <dt>



 <span data-ttu-id="38e19-165">("Servicio")</span><span class="sxs-lookup"><span data-stu-id="38e19-165">("Service")</span></span>


<span data-ttu-id="38e19-166"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="38e19-166"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="38e19-167">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38e19-167">Requirements</span></span>



| <span data-ttu-id="38e19-168">Requisito</span><span class="sxs-lookup"><span data-stu-id="38e19-168">Requirement</span></span> | <span data-ttu-id="38e19-169">Value</span><span class="sxs-lookup"><span data-stu-id="38e19-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38e19-170">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38e19-170">Minimum supported client</span></span><br/> | <span data-ttu-id="38e19-171">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="38e19-171">None supported</span></span><br/>                                                               |
| <span data-ttu-id="38e19-172">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38e19-172">Minimum supported server</span></span><br/> | <span data-ttu-id="38e19-173">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="38e19-173">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="38e19-174">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="38e19-174">Namespace</span></span><br/>                | <span data-ttu-id="38e19-175">Raíz de \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="38e19-175">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="38e19-176">MOF</span><span class="sxs-lookup"><span data-stu-id="38e19-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="38e19-177"><dt>TSCfgWmi. mof</dt></span><span class="sxs-lookup"><span data-stu-id="38e19-177"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="38e19-178">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="38e19-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38e19-179"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38e19-179"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38e19-180">Vea también</span><span class="sxs-lookup"><span data-stu-id="38e19-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38e19-181">**\_ELEMENTSETTING CIM**</span><span class="sxs-lookup"><span data-stu-id="38e19-181">**CIM\_ElementSetting**</span></span>](cim-elementsetting.md)
</dt> <dt>

[<span data-ttu-id="38e19-182">**Win32 \_ TerminalService**</span><span class="sxs-lookup"><span data-stu-id="38e19-182">**Win32\_TerminalService**</span></span>](win32-terminalservice.md)
</dt> <dt>

[<span data-ttu-id="38e19-183">**Win32 \_ TSVirtualIP**</span><span class="sxs-lookup"><span data-stu-id="38e19-183">**Win32\_TSVirtualIP**</span></span>](win32-tsvirtualip.md)
</dt> </dl>

 

