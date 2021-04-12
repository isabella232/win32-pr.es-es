---
title: MDM_Policy_Config01_Cryptography02 (clase)
description: La \_ clase Config01 de Cryptography02 de directivas MDM \_ \_ representa las directivas relacionadas con la criptografía.
ms.assetid: e1e06dbd-507e-4da5-bcd5-4d551bd99302
keywords:
- MDM_Policy_Config01_Cryptography02 (clase)
- MDM_Policy_Config01_Cryptography02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Cryptography02
- MDM_Policy_Config01_Cryptography02.InstanceID
- MDM_Policy_Config01_Cryptography02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 92f13a5a04e3d312d8ba262359847719652ecc4b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489911"
---
# <a name="mdm_policy_config01_cryptography02-class"></a><span data-ttu-id="0b636-105">\_ \_ Clase Cryptography02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="0b636-105">MDM\_Policy\_Config01\_Cryptography02 class</span></span>

<span data-ttu-id="0b636-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="0b636-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="0b636-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="0b636-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="0b636-108">La **clase \_ \_ Config01 de \_ Cryptography02 de directivas MDM** representa las directivas relacionadas con la criptografía.</span><span class="sxs-lookup"><span data-stu-id="0b636-108">The **MDM\_Policy\_Config01\_Cryptography02** class represents policies related to cryptography.</span></span>

<span data-ttu-id="0b636-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="0b636-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b636-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0b636-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Cryptography02
{
  string InstanceID;
  string ParentID;
  sint32 AllowFipsAlgorithmPolicy;
  string TLSCipherSuites;
};
```

## <a name="members"></a><span data-ttu-id="0b636-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="0b636-111">Members</span></span>

<span data-ttu-id="0b636-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Cryptography02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="0b636-112">The **MDM\_Policy\_Config01\_Cryptography02** class has these types of members:</span></span>

-   [<span data-ttu-id="0b636-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b636-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0b636-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="0b636-114">Properties</span></span>

<span data-ttu-id="0b636-115">La **clase \_ \_ Config01 de \_ Cryptography02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="0b636-115">The **MDM\_Policy\_Config01\_Cryptography02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="0b636-116">AllowFipsAlgorithmPolicy</span><span class="sxs-lookup"><span data-stu-id="0b636-116">AllowFipsAlgorithmPolicy</span></span>](/windows/client-management/mdm/policy-csp-cryptography#cryptography-allowfipsalgorithmpolicy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b636-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="0b636-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="0b636-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b636-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="0b636-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="0b636-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b636-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b636-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b636-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b636-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b636-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b636-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0b636-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="0b636-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="0b636-124">Para esta clase, la cadena es "Cryptography"</span><span class="sxs-lookup"><span data-stu-id="0b636-124">For this class, the string is "Cryptography"</span></span>

</dd> <dt>

<span data-ttu-id="0b636-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="0b636-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b636-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b636-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b636-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="0b636-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0b636-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="0b636-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="0b636-129">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="0b636-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="0b636-130">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="0b636-130">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> <dt>

[<span data-ttu-id="0b636-131">TLSCipherSuites</span><span class="sxs-lookup"><span data-stu-id="0b636-131">TLSCipherSuites</span></span>](/windows/client-management/mdm/policy-csp-cryptography#cryptography-tlsciphersuites)
</dt> <dd> <dl> <dt>

<span data-ttu-id="0b636-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="0b636-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="0b636-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="0b636-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b636-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b636-134">Requirements</span></span>



| <span data-ttu-id="0b636-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b636-135">Requirement</span></span> | <span data-ttu-id="0b636-136">Value</span><span class="sxs-lookup"><span data-stu-id="0b636-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b636-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b636-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0b636-138">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="0b636-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0b636-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0b636-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0b636-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="0b636-140">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="0b636-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="0b636-141">Namespace</span></span><br/>                | <span data-ttu-id="0b636-142">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="0b636-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="0b636-143">MOF</span><span class="sxs-lookup"><span data-stu-id="0b636-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0b636-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0b636-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="0b636-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0b636-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0b636-146"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0b636-146"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b636-147">Vea también</span><span class="sxs-lookup"><span data-stu-id="0b636-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b636-148">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="0b636-148">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

