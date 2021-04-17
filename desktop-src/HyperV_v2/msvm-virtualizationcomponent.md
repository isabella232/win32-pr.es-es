---
description: Representa un servicio de la plataforma Hyper-V de Microsoft Windows.
ms.assetid: 309EFE4C-EEA4-454C-943D-CBF99D64FE15
title: Msvm_VirtualizationComponent (clase)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualizationComponent
- Msvm_VirtualizationComponent.CLSID
- Msvm_VirtualizationComponent.Context
- Msvm_VirtualizationComponent.Enabled
- Msvm_VirtualizationComponent.Name
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 19811b224a4e93e85420539248b7d010491335aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686601"
---
# <a name="msvm_virtualizationcomponent-class"></a><span data-ttu-id="78a39-103">MSVM \_ VirtualizationComponent (clase)</span><span class="sxs-lookup"><span data-stu-id="78a39-103">Msvm\_VirtualizationComponent class</span></span>

<span data-ttu-id="78a39-104">Representa un servicio de la plataforma Hyper-V de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="78a39-104">Represents a service of the Microsoft Windows Hyper-V platform.</span></span>

<span data-ttu-id="78a39-105">La siguiente sintaxis es código simplificado de Managed Object Format (MOF).</span><span class="sxs-lookup"><span data-stu-id="78a39-105">The following syntax is simplified Managed Object Format (MOF) code.</span></span>

## <a name="syntax"></a><span data-ttu-id="78a39-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="78a39-106">Syntax</span></span>

``` syntax
[Abstract]
class Msvm_VirtualizationComponent
{
  string  CLSID;
  uint32  Context = 1;
  boolean Enabled = True;
  string  Name;
};
```

## <a name="members"></a><span data-ttu-id="78a39-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="78a39-107">Members</span></span>

<span data-ttu-id="78a39-108">La clase **MSVM \_ VirtualizationComponent** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="78a39-108">The **Msvm\_VirtualizationComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="78a39-109">Propiedades</span><span class="sxs-lookup"><span data-stu-id="78a39-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="78a39-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="78a39-110">Properties</span></span>

<span data-ttu-id="78a39-111">La clase **MSVM \_ VirtualizationComponent** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="78a39-111">The **Msvm\_VirtualizationComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="78a39-112">**CLSID**</span><span class="sxs-lookup"><span data-stu-id="78a39-112">**CLSID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78a39-113">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78a39-113">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78a39-114">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78a39-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78a39-115">**GUID** que representa el identificador de clase del objeto com del servicio.</span><span class="sxs-lookup"><span data-stu-id="78a39-115">A **GUID** that represents the class identifier of the service's COM object.</span></span>

</dd> <dt>

<span data-ttu-id="78a39-116">**Contexto**</span><span class="sxs-lookup"><span data-stu-id="78a39-116">**Context**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78a39-117">Tipo de datos: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="78a39-117">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="78a39-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78a39-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78a39-119">Calificadores: **experimental**</span><span class="sxs-lookup"><span data-stu-id="78a39-119">Qualifiers: **Experimental**</span></span>
</dt> </dl>

<span data-ttu-id="78a39-120">Contexto en el que se ejecutará el objeto recién creado.</span><span class="sxs-lookup"><span data-stu-id="78a39-120">The context in which the newly created object will run.</span></span> <span data-ttu-id="78a39-121">Este valor se pasa en el parámetro *dwClsContext* a [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="78a39-121">This value is passed in the *dwClsContext* parameter to [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="78a39-122">Esta propiedad siempre se establece en 1.</span><span class="sxs-lookup"><span data-stu-id="78a39-122">This property is always set to 1.</span></span>

</dd> <dt>

<span data-ttu-id="78a39-123">**Enabled**</span><span class="sxs-lookup"><span data-stu-id="78a39-123">**Enabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78a39-124">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="78a39-124">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="78a39-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78a39-125">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="78a39-126">**True** si esta instancia está habilitada y se puede usar para completar las solicitudes de cliente; en caso contrario, **false**.</span><span class="sxs-lookup"><span data-stu-id="78a39-126">**True** is this instance is enabled and can be used to complete client requests; otherwise, **False**.</span></span> <span data-ttu-id="78a39-127">Esta propiedad siempre se establece en **true**.</span><span class="sxs-lookup"><span data-stu-id="78a39-127">This property is always set to **True**.</span></span>

</dd> <dt>

<span data-ttu-id="78a39-128">**Nombre**</span><span class="sxs-lookup"><span data-stu-id="78a39-128">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="78a39-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="78a39-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="78a39-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="78a39-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="78a39-131">Calificadores: **clave**</span><span class="sxs-lookup"><span data-stu-id="78a39-131">Qualifiers: **Key**</span></span>
</dt> </dl>

<span data-ttu-id="78a39-132">Cadena independiente del lenguaje que identifica de forma única el servicio.</span><span class="sxs-lookup"><span data-stu-id="78a39-132">A language-neutral string that uniquely identifies the service.</span></span> <span data-ttu-id="78a39-133">Se sugiere el siguiente formato para evitar conflictos de nomenclatura: " \| versión del componente del proveedor \| ".</span><span class="sxs-lookup"><span data-stu-id="78a39-133">The following format is suggested to prevent naming conflicts: "vendor\|component\|version".</span></span> <span data-ttu-id="78a39-134">Por ejemplo, este nombre representa la versión 1,0 del componente de puerto de red emulado de Microsoft: "Microsoft \| EmulatedNetworkPortComponent \| v 1.0".</span><span class="sxs-lookup"><span data-stu-id="78a39-134">For example, this name represents version 1.0 of the Microsoft Emulated Network Port Component: "Microsoft\|EmulatedNetworkPortComponent\|V1.0".</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="78a39-135">Observaciones</span><span class="sxs-lookup"><span data-stu-id="78a39-135">Remarks</span></span>

<span data-ttu-id="78a39-136">El acceso a la clase **MSVM \_ VirtualizationComponent** puede estar restringido por el filtrado de UAC.</span><span class="sxs-lookup"><span data-stu-id="78a39-136">Access to the **Msvm\_VirtualizationComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="78a39-137">Para obtener más información, vea [control de cuentas de usuario y WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="78a39-137">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="78a39-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="78a39-138">Requirements</span></span>



| <span data-ttu-id="78a39-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="78a39-139">Requirement</span></span> | <span data-ttu-id="78a39-140">Value</span><span class="sxs-lookup"><span data-stu-id="78a39-140">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="78a39-141">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78a39-141">Minimum supported client</span></span><br/> | <span data-ttu-id="78a39-142">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="78a39-142">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="78a39-143">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="78a39-143">Minimum supported server</span></span><br/> | <span data-ttu-id="78a39-144">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="78a39-144">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="78a39-145">Fin de compatibilidad de cliente</span><span class="sxs-lookup"><span data-stu-id="78a39-145">End of client support</span></span><br/>    | <span data-ttu-id="78a39-146">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="78a39-146">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="78a39-147">Fin de compatibilidad de servidor</span><span class="sxs-lookup"><span data-stu-id="78a39-147">End of server support</span></span><br/>    | <span data-ttu-id="78a39-148">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="78a39-148">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="78a39-149">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="78a39-149">Namespace</span></span><br/>                | <span data-ttu-id="78a39-150">\\Virtualización de raíz \\ V2</span><span class="sxs-lookup"><span data-stu-id="78a39-150">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="78a39-151">MOF</span><span class="sxs-lookup"><span data-stu-id="78a39-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="78a39-152"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="78a39-152"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="78a39-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="78a39-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="78a39-154"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="78a39-154"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

