---
title: MDM_Policy_Config01_Accounts02 (clase)
description: La \_ clase Config01 de Accounts02 de directivas MDM \_ \_ representa las directivas relacionadas con las cuentas.
ms.assetid: 628a0745-0ac5-4038-8ea8-04344098682d
keywords:
- MDM_Policy_Config01_Accounts02 (clase)
- MDM_Policy_Config01_Accounts02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Accounts02
- MDM_Policy_Config01_Accounts02.InstanceID
- MDM_Policy_Config01_Accounts02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8833f1477014f3c7c2200e07c242549f5235fbdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079185"
---
# <a name="mdm_policy_config01_accounts02-class"></a><span data-ttu-id="5a806-105">\_ \_ Clase Accounts02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="5a806-105">MDM\_Policy\_Config01\_Accounts02 class</span></span>

<span data-ttu-id="5a806-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="5a806-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5a806-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="5a806-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5a806-108">La **clase \_ \_ Config01 de \_ Accounts02 de directivas MDM** representa las directivas relacionadas con las cuentas.</span><span class="sxs-lookup"><span data-stu-id="5a806-108">The **MDM\_Policy\_Config01\_Accounts02** class represents policies related to accounts.</span></span>

<span data-ttu-id="5a806-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5a806-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a806-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a806-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Accounts02
{
  string InstanceID;
  string ParentID;
  sint32 AllowMicrosoftAccountConnection;
  sint32 AllowMicrosoftAccountSignInAssistant;
  sint32 AllowAddingNonMicrosoftAccountsManually;
  string DomainNamesForEmailSync;
};
```

## <a name="members"></a><span data-ttu-id="5a806-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="5a806-111">Members</span></span>

<span data-ttu-id="5a806-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Accounts02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5a806-112">The **MDM\_Policy\_Config01\_Accounts02** class has these types of members:</span></span>

-   [<span data-ttu-id="5a806-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5a806-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5a806-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5a806-114">Properties</span></span>

<span data-ttu-id="5a806-115">La **clase \_ \_ Config01 de \_ Accounts02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5a806-115">The **MDM\_Policy\_Config01\_Accounts02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5a806-116">AllowAddingNonMicrosoftAccountsManually</span><span class="sxs-lookup"><span data-stu-id="5a806-116">AllowAddingNonMicrosoftAccountsManually</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowaddingnonmicrosoftaccountsmanually)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a806-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5a806-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a806-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5a806-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5a806-119">AllowMicrosoftAccountConnection</span><span class="sxs-lookup"><span data-stu-id="5a806-119">AllowMicrosoftAccountConnection</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountconnection)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a806-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5a806-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a806-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5a806-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="5a806-122">AllowMicrosoftAccountSignInAssistant</span><span class="sxs-lookup"><span data-stu-id="5a806-122">AllowMicrosoftAccountSignInAssistant</span></span>](/windows/client-management/mdm/policy-csp-accounts#accounts-allowmicrosoftaccountsigninassistant)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a806-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="5a806-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="5a806-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5a806-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5a806-125">DomainNamesForEmailSync</span><span class="sxs-lookup"><span data-stu-id="5a806-125">DomainNamesForEmailSync</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a806-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a806-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a806-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5a806-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5a806-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5a806-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a806-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a806-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a806-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a806-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a806-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5a806-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5a806-132">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="5a806-132">Identifies the name of the parent node.</span></span> <span data-ttu-id="5a806-133">Para esta clase, la cadena es "Accounts".</span><span class="sxs-lookup"><span data-stu-id="5a806-133">For this class, the string is "Accounts".</span></span>

</dd> <dt>

<span data-ttu-id="5a806-134">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5a806-134">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a806-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a806-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a806-136">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a806-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a806-137">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5a806-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="5a806-138">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="5a806-138">Describes the full path to the parent node.</span></span> <span data-ttu-id="5a806-139">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="5a806-139">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a806-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a806-140">Requirements</span></span>



| <span data-ttu-id="5a806-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a806-141">Requirement</span></span> | <span data-ttu-id="5a806-142">Value</span><span class="sxs-lookup"><span data-stu-id="5a806-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a806-143">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a806-143">Minimum supported client</span></span><br/> | <span data-ttu-id="5a806-144">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a806-144">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5a806-145">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a806-145">Minimum supported server</span></span><br/> | <span data-ttu-id="5a806-146">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5a806-146">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5a806-147">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5a806-147">Namespace</span></span><br/>                | <span data-ttu-id="5a806-148">DMMap de MDM raíz de \\ CIMv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="5a806-148">Root\\CIMv2\\MDM\\DMMap</span></span><br/>                                                             |
| <span data-ttu-id="5a806-149">MOF</span><span class="sxs-lookup"><span data-stu-id="5a806-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a806-150"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a806-150"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a806-151">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5a806-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a806-152"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a806-152"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a806-153">Vea también</span><span class="sxs-lookup"><span data-stu-id="5a806-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a806-154">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="5a806-154">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

