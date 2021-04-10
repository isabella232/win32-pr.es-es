---
title: MDM_Policy_Result01_Cryptography02 (clase)
description: La \_ clase Result01 de Cryptography02 de directivas MDM \_ \_ representa las directivas relacionadas con la criptografía.
ms.assetid: 3ab41bb4-920d-4647-8f05-f6938f51c409
keywords:
- MDM_Policy_Result01_Cryptography02 (clase)
- MDM_Policy_Result01_Cryptography02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Cryptography02
- MDM_Policy_Result01_Cryptography02.InstanceID
- MDM_Policy_Result01_Cryptography02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6beb62d7d9fdba320220c9bb4de5074fce416ac2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150716"
---
# <a name="mdm_policy_result01_cryptography02-class"></a><span data-ttu-id="e100d-105">\_ \_ Clase Cryptography02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="e100d-105">MDM\_Policy\_Result01\_Cryptography02 class</span></span>

<span data-ttu-id="e100d-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="e100d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e100d-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="e100d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e100d-108">La **clase \_ \_ Result01 de \_ Cryptography02 de directivas MDM** representa las directivas relacionadas con la criptografía.</span><span class="sxs-lookup"><span data-stu-id="e100d-108">The **MDM\_Policy\_Result01\_Cryptography02** class represents policies related to cryptography.</span></span>

<span data-ttu-id="e100d-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e100d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e100d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e100d-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Cryptography02
{
  string InstanceID;
  string ParentID;
  sint32 AllowFipsAlgorithmPolicy;
  string TLSCipherSuites;
};
```

## <a name="members"></a><span data-ttu-id="e100d-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e100d-111">Members</span></span>

<span data-ttu-id="e100d-112">La clase Result01 de la **\_ Directiva MDM \_ \_ Cryptography02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e100d-112">The **MDM\_Policy\_Result01\_Cryptography02** class has these types of members:</span></span>

-   [<span data-ttu-id="e100d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e100d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e100d-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e100d-114">Properties</span></span>

<span data-ttu-id="e100d-115">La **clase \_ \_ Result01 de \_ Cryptography02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e100d-115">The **MDM\_Policy\_Result01\_Cryptography02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e100d-116">AllowFipsAlgorithmPolicy</span><span class="sxs-lookup"><span data-stu-id="e100d-116">AllowFipsAlgorithmPolicy</span></span>](/windows/client-management/mdm/policy-csp-cryptography#cryptography-allowfipsalgorithmpolicy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e100d-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e100d-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e100d-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e100d-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e100d-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e100d-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e100d-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e100d-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e100d-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e100d-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e100d-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e100d-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e100d-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="e100d-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="e100d-124">Para esta clase, la cadena es "Cryptography"</span><span class="sxs-lookup"><span data-stu-id="e100d-124">For this class, the string is "Cryptography"</span></span>

</dd> <dt>

<span data-ttu-id="e100d-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e100d-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e100d-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e100d-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e100d-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e100d-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e100d-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e100d-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e100d-129">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="e100d-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="e100d-130">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="e100d-130">For this class, the string is "./Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="e100d-131">TLSCipherSuites</span><span class="sxs-lookup"><span data-stu-id="e100d-131">TLSCipherSuites</span></span>](/windows/client-management/mdm/policy-csp-cryptography#cryptography-tlsciphersuites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e100d-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e100d-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e100d-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e100d-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e100d-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e100d-134">Requirements</span></span>



| <span data-ttu-id="e100d-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="e100d-135">Requirement</span></span> | <span data-ttu-id="e100d-136">Value</span><span class="sxs-lookup"><span data-stu-id="e100d-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e100d-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e100d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="e100d-138">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="e100d-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e100d-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e100d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="e100d-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e100d-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e100d-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e100d-141">Namespace</span></span><br/>                | <span data-ttu-id="e100d-142">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="e100d-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e100d-143">MOF</span><span class="sxs-lookup"><span data-stu-id="e100d-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e100d-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e100d-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e100d-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e100d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e100d-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e100d-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e100d-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="e100d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e100d-148">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="e100d-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

