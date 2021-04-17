---
description: Representa un servicio de dispositivo virtual de la plataforma Hyper-V de Microsoft Windows.
ms.assetid: 865D83E1-0FC6-4F96-94BB-AA5116890127
title: Msvm_VirtualSystemResourceComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemResourceComponent
- Msvm_VirtualSystemResourceComponent.Name
- Msvm_VirtualSystemResourceComponent.CLSID
- Msvm_VirtualSystemResourceComponent.Context
- Msvm_VirtualSystemResourceComponent.Enabled
- Msvm_VirtualSystemResourceComponent.AdditionalClassNames
- Msvm_VirtualSystemResourceComponent.Type
- Msvm_VirtualSystemResourceComponent.HotAdd
- Msvm_VirtualSystemResourceComponent.HotRemove
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 81c2d31a6497325ac77003ded266333518de890a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666325"
---
# <a name="msvm_virtualsystemresourcecomponent-class"></a><span data-ttu-id="f6e7d-103">MSVM \_ VirtualSystemResourceComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="f6e7d-103">Msvm\_VirtualSystemResourceComponent class</span></span>

<span data-ttu-id="f6e7d-104">Representa un servicio de dispositivo virtual de la plataforma Hyper-V de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-104">Represents a virtual device service of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="f6e7d-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF) e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6e7d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6e7d-106">Syntax</span></span>

``` syntax
class Msvm_VirtualSystemResourceComponent : Msvm_VirtualizationComponent
{
  string  Name;
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  AdditionalClassNames[];
  uint16  Type = 1;
  boolean HotAdd = False;
  boolean HotRemove = False;
};
```

## <a name="members"></a><span data-ttu-id="f6e7d-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="f6e7d-107">Members</span></span>

<span data-ttu-id="f6e7d-108">La clase **MSVM \_ VirtualSystemResourceComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f6e7d-108">The **Msvm\_VirtualSystemResourceComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="f6e7d-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6e7d-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6e7d-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6e7d-110">Properties</span></span>

<span data-ttu-id="f6e7d-111">La clase **MSVM \_ VirtualSystemResourceComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-111">The **Msvm\_VirtualSystemResourceComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f6e7d-112">**AdditionalClassNames**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-112">**AdditionalClassNames**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6e7d-113">Tipo de datos: matriz de **cadenas**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-113">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f6e7d-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6e7d-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6e7d-115">Matriz de cadenas que contiene las clases no asociadas adicionales expuestas por esta instancia de **\_ VirtualSystemResourceComponent de MSVM** .</span><span class="sxs-lookup"><span data-stu-id="f6e7d-115">An array of strings containing additional non-association classes surfaced by this **Msvm\_VirtualSystemResourceComponent** instance.</span></span> <span data-ttu-id="f6e7d-116">Estas clases deben derivarse de no tener ningún [**\_ desResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata) [**CIM \_**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) ni de CIM.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-116">These classes must derive from neither [**CIM\_LogicalDevice**](/windows/desktop/CIMWin32Prov/cim-logicaldevice) nor [**CIM\_ResourceAllocationSettingData**](/previous-versions/windows/desktop/clushyperv/cim-resourceallocationsettingdata).</span></span>

</dd> <dt>

<span data-ttu-id="f6e7d-117">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-117">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6e7d-118">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-118">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6e7d-119">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6e7d-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6e7d-120">GUID que representa el identificador de clase del objeto COM del servicio.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-120">A GUID that represents the class identifier of the service's COM object.</span></span> <span data-ttu-id="f6e7d-121">Esta propiedad se hereda de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="f6e7d-121">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6e7d-122">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-122">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6e7d-123">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-123">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="f6e7d-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6e7d-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6e7d-125">Contexto en el que se ejecutará el objeto recién creado.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-125">The context in which the newly created object will run.</span></span> <span data-ttu-id="f6e7d-126">Este valor se pasa en el parámetro *dwClsContext* a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="f6e7d-126">This value is passed in the *dwClsContext* parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="f6e7d-127">Esta propiedad se hereda de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)y siempre está establecida en 1.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-127">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="f6e7d-128">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-128">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6e7d-129">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-129">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6e7d-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6e7d-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6e7d-131">**True** si esta instancia está habilitada y se puede usar para completar las solicitudes de cliente; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-131">**True** if this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="f6e7d-132">Esta propiedad se hereda de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md)y siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-132">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md), and it is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="f6e7d-133">**HotAdd**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-133">**HotAdd**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6e7d-134">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-134">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6e7d-135">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6e7d-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6e7d-136">**True** si esta instancia se puede Agregar en caliente a una máquina virtual; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-136">**True** if this instance can be hot-added to a virtual machine; otherwise, **False**.</span></span> <span data-ttu-id="f6e7d-137">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-137">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="f6e7d-138">**HotRemove**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-138">**HotRemove**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6e7d-139">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-139">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="f6e7d-140">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6e7d-140">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6e7d-141">**True** si esta instancia se puede quitar en caliente de una máquina virtual; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-141">**True** if this instance can be hot-removed from a virtual machine; otherwise, **False**.</span></span> <span data-ttu-id="f6e7d-142">El valor predeterminado es **False**.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-142">The default is **False**.</span></span>

</dd> <dt>

<span data-ttu-id="f6e7d-143">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-143">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6e7d-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6e7d-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6e7d-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6e7d-146">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-146">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="f6e7d-147">Cadena independiente del lenguaje que identifica de forma única el servicio.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-147">A language-neutral string that uniquely identifies the service.</span></span> <span data-ttu-id="f6e7d-148">Se sugiere el siguiente formato para evitar conflictos de nomenclatura: " \| versión del componente del proveedor \| ".</span><span class="sxs-lookup"><span data-stu-id="f6e7d-148">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="f6e7d-149">Por ejemplo, este nombre representa la versión 1,0 del componente de puerto de red emulado de Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| v 1.0".</span><span class="sxs-lookup"><span data-stu-id="f6e7d-149">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span> <span data-ttu-id="f6e7d-150">Esta propiedad se hereda de [**MSVM \_ VirtualizationComponent**](msvm-virtualizationcomponent.md).</span><span class="sxs-lookup"><span data-stu-id="f6e7d-150">This property is inherited from [**Msvm\_VirtualizationComponent**](msvm-virtualizationcomponent.md).</span></span>

</dd> <dt>

<span data-ttu-id="f6e7d-151">**Tipo**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-151">**Type**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6e7d-152">Tipo de datos: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-152">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="f6e7d-153">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6e7d-153">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f6e7d-154">La relación del objeto WMI que se describe aquí con el dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-154">The relationship of the WMI object that is described here with the virtual device.</span></span>



| <span data-ttu-id="f6e7d-155">Value</span><span class="sxs-lookup"><span data-stu-id="f6e7d-155">Value</span></span>                                                                                                                                                                                                                                                           | <span data-ttu-id="f6e7d-156">Significado</span><span class="sxs-lookup"><span data-stu-id="f6e7d-156">Meaning</span></span>                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="_Not_Changeable_"></span><span id="_not_changeable_"></span><span id="_NOT_CHANGEABLE_"></span><dl> <span data-ttu-id="f6e7d-157"><dt>**"No modificable"**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f6e7d-157"><dt>**"Not Changeable"**</dt> <dt>0</dt></span></span> </dl> |                                                                                                                                                                                                                |
| <span id="_Singleton_"></span><span id="_singleton_"></span><span id="_SINGLETON_"></span><dl> <span data-ttu-id="f6e7d-158"><dt>**"Singleton"**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f6e7d-158"><dt>**"Singleton"**</dt> <dt>1</dt></span></span> </dl>                     | <span data-ttu-id="f6e7d-159">Singleton es un objeto WMI de nivel superior que está vinculado a 1:1 con un dispositivo virtual y solo puede existir una vez por cada máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-159">Singleton is a top level WMI object that is tied 1:1 with a Virtual Device and can only exist once per virtual machine.</span></span> <span data-ttu-id="f6e7d-160">Este es el valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-160">This is the default value.</span></span><br/>                                                  |
| <span id="_MultiInstance_"></span><span id="_multiinstance_"></span><span id="_MULTIINSTANCE_"></span><dl> <span data-ttu-id="f6e7d-161"><dt>**"Multiinstancia"**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f6e7d-161"><dt>**"MultiInstance"**</dt> <dt>2</dt></span></span> </dl>     | <span data-ttu-id="f6e7d-162">Multiinstancia es un objeto WMI de nivel superior que puede existir varias veces por máquina virtual y que está vinculado a 1:1 con un dispositivo virtual.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-162">MultiInstance is a top level WMI object that can exist multiple times per virtual machine and is tied 1:1 with a Virtual Device.</span></span><br/>                                                                    |
| <span id="_Subdevice_"></span><span id="_subdevice_"></span><span id="_SUBDEVICE_"></span><dl> <span data-ttu-id="f6e7d-163"><dt>**"Subdispositivo"**</dt> <dt>3</dt></span><span class="sxs-lookup"><span data-stu-id="f6e7d-163"><dt>**"Subdevice"**</dt> <dt>3</dt></span></span> </dl>                     | <span data-ttu-id="f6e7d-164">El subdispositivo es un objeto WMI que no tiene referencia primaria pero que solo está controlado por un único dispositivo virtual que solo puede existir una vez por cada máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-164">Subdevice is a WMI object that has not parent reference but is controlled by only one Virtual Device that can exist only once per virtual machine.</span></span> <span data-ttu-id="f6e7d-165">Aunque el objeto WMI puede existir varias veces.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-165">The WMI object though can exist multiples times.</span></span><br/> |



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f6e7d-166">Observaciones</span><span class="sxs-lookup"><span data-stu-id="f6e7d-166">Remarks</span></span>

<span data-ttu-id="f6e7d-167">El acceso a la clase **MSVM \_ VirtualSystemResourceComponent** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="f6e7d-167">Access to the **Msvm\_VirtualSystemResourceComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f6e7d-168">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f6e7d-168">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f6e7d-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6e7d-169">Requirements</span></span>



| <span data-ttu-id="f6e7d-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6e7d-170">Requirement</span></span> | <span data-ttu-id="f6e7d-171">Value</span><span class="sxs-lookup"><span data-stu-id="f6e7d-171">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6e7d-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6e7d-172">Minimum supported client</span></span><br/> | <span data-ttu-id="f6e7d-173">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6e7d-173">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f6e7d-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6e7d-174">Minimum supported server</span></span><br/> | <span data-ttu-id="f6e7d-175">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6e7d-175">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6e7d-176">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="f6e7d-176">End of client support</span></span><br/>    | <span data-ttu-id="f6e7d-177">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f6e7d-177">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="f6e7d-178">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="f6e7d-178">End of server support</span></span><br/>    | <span data-ttu-id="f6e7d-179">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f6e7d-179">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="f6e7d-180">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f6e7d-180">Namespace</span></span><br/>                | <span data-ttu-id="f6e7d-181">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="f6e7d-181">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f6e7d-182">MOF</span><span class="sxs-lookup"><span data-stu-id="f6e7d-182">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6e7d-183"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6e7d-183"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6e7d-184">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6e7d-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6e7d-185"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f6e7d-185"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f6e7d-186">Vea también</span><span class="sxs-lookup"><span data-stu-id="f6e7d-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f6e7d-187">**MSVM \_ VirtualizationComponent**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-187">**Msvm\_VirtualizationComponent**</span></span>](/windows/desktop/HyperV_v2/msvm-virtualizationcomponent)
</dt> <dt>

[<span data-ttu-id="f6e7d-188">**MSVM \_ VirtualizationComponent**</span><span class="sxs-lookup"><span data-stu-id="f6e7d-188">**Msvm\_VirtualizationComponent**</span></span>](msvm-virtualizationcomponent.md)
</dt> </dl>

 

