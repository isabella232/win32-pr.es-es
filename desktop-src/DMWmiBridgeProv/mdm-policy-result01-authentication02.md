---
title: MDM_Policy_Result01_Authentication02 (clase)
description: La \_ clase Result01 de Authentication02 de directivas MDM \_ \_ representa las directivas de administración de autenticación disponibles.
ms.assetid: a67275dc-5f4d-4672-9a6e-84fa65cde3ad
keywords:
- MDM_Policy_Result01_Authentication02 (clase)
- MDM_Policy_Result01_Authentication02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Authentication02
- MDM_Policy_Result01_Authentication02.InstanceID
- MDM_Policy_Result01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d80979fe7b025ea7b0677436036c8760d4b0ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151104"
---
# <a name="mdm_policy_result01_authentication02-class"></a><span data-ttu-id="4178d-105">\_ \_ Clase Authentication02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="4178d-105">MDM\_Policy\_Result01\_Authentication02 class</span></span>

<span data-ttu-id="4178d-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="4178d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="4178d-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="4178d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="4178d-108">La **clase \_ \_ Result01 de \_ Authentication02 de directivas MDM** representa las directivas de administración de autenticación disponibles.</span><span class="sxs-lookup"><span data-stu-id="4178d-108">The **MDM\_Policy\_Result01\_Authentication02** class represents the authentication management policies available.</span></span>

<span data-ttu-id="4178d-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="4178d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="4178d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="4178d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowAadPasswordReset;
  sint32 AllowFastReconnect;
  sint32 AllowFidoDeviceSignon;
  sint32 AllowSecondaryAuthenticationDevice;
};
```

## <a name="members"></a><span data-ttu-id="4178d-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="4178d-111">Members</span></span>

<span data-ttu-id="4178d-112">La clase Result01 de la **\_ Directiva MDM \_ \_ Authentication02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="4178d-112">The **MDM\_Policy\_Result01\_Authentication02** class has these types of members:</span></span>

-   [<span data-ttu-id="4178d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4178d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="4178d-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="4178d-114">Properties</span></span>

<span data-ttu-id="4178d-115">La **clase \_ \_ Result01 de \_ Authentication02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="4178d-115">The **MDM\_Policy\_Result01\_Authentication02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="4178d-116">AllowAadPasswordReset</span><span class="sxs-lookup"><span data-stu-id="4178d-116">AllowAadPasswordReset</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowaadpasswordreset)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4178d-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4178d-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4178d-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4178d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4178d-119">AllowFastReconnect</span><span class="sxs-lookup"><span data-stu-id="4178d-119">AllowFastReconnect</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfastreconnect)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4178d-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4178d-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4178d-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4178d-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4178d-122">AllowFidoDeviceSignon</span><span class="sxs-lookup"><span data-stu-id="4178d-122">AllowFidoDeviceSignon</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowfidodevicesignon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4178d-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4178d-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4178d-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4178d-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="4178d-125">AllowSecondaryAuthenticationDevice</span><span class="sxs-lookup"><span data-stu-id="4178d-125">AllowSecondaryAuthenticationDevice</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-allowsecondaryauthenticationdevice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="4178d-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="4178d-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="4178d-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="4178d-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="4178d-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="4178d-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4178d-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4178d-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4178d-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4178d-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4178d-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4178d-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4178d-132">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="4178d-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="4178d-133">Para esta clase, la cadena es "Authentication".</span><span class="sxs-lookup"><span data-stu-id="4178d-133">For this class, the string is "Authentication".</span></span>

</dd> <dt>

<span data-ttu-id="4178d-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="4178d-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4178d-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="4178d-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="4178d-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="4178d-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="4178d-137">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="4178d-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="4178d-138">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="4178d-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="4178d-139">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="4178d-139">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4178d-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4178d-140">Requirements</span></span>



| <span data-ttu-id="4178d-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="4178d-141">Requirement</span></span> | <span data-ttu-id="4178d-142">Value</span><span class="sxs-lookup"><span data-stu-id="4178d-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4178d-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4178d-143">Minimum supported client</span></span><br/> | <span data-ttu-id="4178d-144">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="4178d-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="4178d-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="4178d-145">Minimum supported server</span></span><br/> | <span data-ttu-id="4178d-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="4178d-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="4178d-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="4178d-147">Namespace</span></span><br/>                | <span data-ttu-id="4178d-148">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="4178d-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="4178d-149">MOF</span><span class="sxs-lookup"><span data-stu-id="4178d-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4178d-150"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="4178d-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4178d-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="4178d-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4178d-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4178d-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4178d-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="4178d-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4178d-154">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="4178d-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

