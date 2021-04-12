---
title: MDM_Policy_Config01_CredentialProviders02 (clase)
description: La \_ clase Config01 de CredentialProviders02 de directivas MDM \_ \_ configura las directivas de proveedor de credenciales disponibles.
ms.assetid: 84a44fef-1481-4d1d-9531-f2ff6f3b36e6
keywords:
- MDM_Policy_Config01_CredentialProviders02 (clase)
- MDM_Policy_Config01_CredentialProviders02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_CredentialProviders02
- MDM_Policy_Config01_CredentialProviders02.InstanceID
- MDM_Policy_Config01_CredentialProviders02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c22f77a4ec63a37c71353be43836dd307d5f5293
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489917"
---
# <a name="mdm_policy_config01_credentialproviders02-class"></a><span data-ttu-id="1fc92-105">\_ \_ Clase CredentialProviders02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="1fc92-105">MDM\_Policy\_Config01\_CredentialProviders02 class</span></span>

<span data-ttu-id="1fc92-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="1fc92-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1fc92-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="1fc92-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1fc92-108">La \_ clase Config01 de CredentialProviders02 de directivas MDM \_ \_ configura las directivas de proveedor de credenciales disponibles.</span><span class="sxs-lookup"><span data-stu-id="1fc92-108">The MDM\_Policy\_Config01\_CredentialProviders02 class configures the available credential provider policies.</span></span>

<span data-ttu-id="1fc92-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1fc92-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fc92-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1fc92-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_CredentialProviders02
{
  string InstanceID;
  string ParentID;
  string AllowPINLogon;
  string BlockPicturePassword;
  sint32 DisableAutomaticReDeploymentCredentials;
};
```

## <a name="members"></a><span data-ttu-id="1fc92-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="1fc92-111">Members</span></span>

<span data-ttu-id="1fc92-112">La clase Config01 de la **\_ Directiva MDM \_ \_ CredentialProviders02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1fc92-112">The **MDM\_Policy\_Config01\_CredentialProviders02** class has these types of members:</span></span>

-   [<span data-ttu-id="1fc92-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1fc92-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1fc92-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1fc92-114">Properties</span></span>

<span data-ttu-id="1fc92-115">La **clase \_ \_ Config01 de \_ CredentialProviders02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1fc92-115">The **MDM\_Policy\_Config01\_CredentialProviders02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="1fc92-116">AllowPINLogon</span><span class="sxs-lookup"><span data-stu-id="1fc92-116">AllowPINLogon</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-allowpinlogon)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc92-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1fc92-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fc92-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1fc92-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fc92-119">BlockPicturePassword</span><span class="sxs-lookup"><span data-stu-id="1fc92-119">BlockPicturePassword</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-blockpicturepassword)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc92-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1fc92-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fc92-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1fc92-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="1fc92-122">DisableAutomaticReDeploymentCredentials</span><span class="sxs-lookup"><span data-stu-id="1fc92-122">DisableAutomaticReDeploymentCredentials</span></span>](/windows/client-management/mdm/policy-csp-credentialproviders#credentialproviders-disableautomaticredeploymentcredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc92-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1fc92-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1fc92-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1fc92-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1fc92-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1fc92-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc92-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1fc92-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fc92-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1fc92-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc92-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1fc92-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="1fc92-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1fc92-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1fc92-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1fc92-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1fc92-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1fc92-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1fc92-132">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1fc92-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1fc92-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fc92-133">Requirements</span></span>



| <span data-ttu-id="1fc92-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fc92-134">Requirement</span></span> | <span data-ttu-id="1fc92-135">Value</span><span class="sxs-lookup"><span data-stu-id="1fc92-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1fc92-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fc92-136">Minimum supported client</span></span><br/> | <span data-ttu-id="1fc92-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="1fc92-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1fc92-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1fc92-138">Minimum supported server</span></span><br/> | <span data-ttu-id="1fc92-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1fc92-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1fc92-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1fc92-140">Namespace</span></span><br/>                | <span data-ttu-id="1fc92-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="1fc92-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1fc92-142">MOF</span><span class="sxs-lookup"><span data-stu-id="1fc92-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1fc92-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1fc92-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1fc92-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1fc92-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fc92-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fc92-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

