---
title: MDM_Policy_Result01_Bluetooth02 (clase)
description: La \_ clase MDM Policy \_ Result01 \_ Bluetooth02 representa las directivas de administración de Bluetooth disponibles.
ms.assetid: 629f2323-f6f6-4d4f-8558-9553f4dbe871
keywords:
- MDM_Policy_Result01_Bluetooth02 (clase)
- MDM_Policy_Result01_Bluetooth02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Bluetooth02
- MDM_Policy_Result01_Bluetooth02.InstanceID
- MDM_Policy_Result01_Bluetooth02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe3ceb0a3b7a3d2440f9769fde72c01ce4d68c34
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079740"
---
# <a name="mdm_policy_result01_bluetooth02-class"></a><span data-ttu-id="32124-105">\_ \_ Clase Bluetooth02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="32124-105">MDM\_Policy\_Result01\_Bluetooth02 class</span></span>

<span data-ttu-id="32124-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="32124-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="32124-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="32124-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="32124-108">La clase **MDM \_ Policy \_ Result01 \_ Bluetooth02** representa las directivas de administración de Bluetooth disponibles.</span><span class="sxs-lookup"><span data-stu-id="32124-108">The **MDM\_Policy\_Result01\_Bluetooth02** class represents the Bluetooth management policies available.</span></span>

<span data-ttu-id="32124-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="32124-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="32124-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="32124-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Bluetooth02
{
  string InstanceID;
  string ParentID;
  sint32 AllowDiscoverableMode;
  string LocalDeviceName;
  sint32 AllowAdvertising;
  string ServicesAllowedList;
  sint32 AllowPrepairing;
};
```

## <a name="members"></a><span data-ttu-id="32124-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="32124-111">Members</span></span>

<span data-ttu-id="32124-112">La clase Result01 de la **\_ Directiva MDM \_ \_ Bluetooth02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="32124-112">The **MDM\_Policy\_Result01\_Bluetooth02** class has these types of members:</span></span>

-   [<span data-ttu-id="32124-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32124-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="32124-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="32124-114">Properties</span></span>

<span data-ttu-id="32124-115">La **clase \_ \_ Result01 de \_ Bluetooth02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="32124-115">The **MDM\_Policy\_Result01\_Bluetooth02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="32124-116">AllowAdvertising</span><span class="sxs-lookup"><span data-stu-id="32124-116">AllowAdvertising</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowadvertising)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32124-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="32124-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="32124-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32124-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32124-119">AllowDiscoverableMode</span><span class="sxs-lookup"><span data-stu-id="32124-119">AllowDiscoverableMode</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowdiscoverablemode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32124-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="32124-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="32124-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32124-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="32124-122">AllowPrepairing</span><span class="sxs-lookup"><span data-stu-id="32124-122">AllowPrepairing</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-allowprepairing)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32124-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="32124-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="32124-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32124-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="32124-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="32124-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32124-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="32124-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32124-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="32124-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32124-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="32124-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="32124-129">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="32124-129">Identifies the name of the parent node.</span></span> <span data-ttu-id="32124-130">Para esta clase, la cadena es "Bluetooth".</span><span class="sxs-lookup"><span data-stu-id="32124-130">For this class, the string is "Bluetooth".</span></span>

</dd> <dt>

[<span data-ttu-id="32124-131">LocalDeviceName</span><span class="sxs-lookup"><span data-stu-id="32124-131">LocalDeviceName</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-localdevicename)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32124-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="32124-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32124-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32124-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="32124-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="32124-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="32124-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="32124-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32124-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="32124-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="32124-137">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="32124-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="32124-138">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="32124-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="32124-139">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="32124-139">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="32124-140">ServicesAllowedList</span><span class="sxs-lookup"><span data-stu-id="32124-140">ServicesAllowedList</span></span>](/windows/client-management/mdm/policy-csp-bluetooth#bluetooth-servicesallowedlist)
</dt> <dd> <dl> <dt>

<span data-ttu-id="32124-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="32124-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="32124-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="32124-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="32124-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32124-143">Requirements</span></span>



| <span data-ttu-id="32124-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="32124-144">Requirement</span></span> | <span data-ttu-id="32124-145">Value</span><span class="sxs-lookup"><span data-stu-id="32124-145">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32124-146">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32124-146">Minimum supported client</span></span><br/> | <span data-ttu-id="32124-147">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="32124-147">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="32124-148">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="32124-148">Minimum supported server</span></span><br/> | <span data-ttu-id="32124-149">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="32124-149">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="32124-150">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="32124-150">Namespace</span></span><br/>                | <span data-ttu-id="32124-151">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="32124-151">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="32124-152">MOF</span><span class="sxs-lookup"><span data-stu-id="32124-152">MOF</span></span><br/>                      | <dl> <span data-ttu-id="32124-153"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="32124-153"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="32124-154">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="32124-154">DLL</span></span><br/>                      | <dl> <span data-ttu-id="32124-155"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="32124-155"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32124-156">Vea también</span><span class="sxs-lookup"><span data-stu-id="32124-156">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32124-157">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="32124-157">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

