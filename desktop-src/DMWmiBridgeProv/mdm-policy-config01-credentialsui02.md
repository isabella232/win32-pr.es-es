---
title: MDM_Policy_Config01_CredentialsUI02 (clase)
description: La \_ clase Config01 de CredentialsUI02 de directivas MDM \_ \_ configura las directivas de proveedor de credenciales disponibles.
ms.assetid: 508b8dc8-cc89-4260-9346-30deeac606fd
keywords:
- MDM_Policy_Config01_CredentialsUI02 (clase)
- MDM_Policy_Config01_CredentialsUI02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_CredentialsUI02
- MDM_Policy_Config01_CredentialsUI02.InstanceID
- MDM_Policy_Config01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d5e0fcb9b736adfabbf2b3de12d576ef76652e17
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079177"
---
# <a name="mdm_policy_config01_credentialsui02-class"></a><span data-ttu-id="a8fde-105">\_ \_ Clase CredentialsUI02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="a8fde-105">MDM\_Policy\_Config01\_CredentialsUI02 class</span></span>

<span data-ttu-id="a8fde-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="a8fde-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="a8fde-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="a8fde-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="a8fde-108">La \_ clase Config01 de CredentialsUI02 de directivas MDM \_ \_ configura las directivas de proveedor de credenciales disponibles.</span><span class="sxs-lookup"><span data-stu-id="a8fde-108">The MDM\_Policy\_Config01\_CredentialsUI02 class configures the available credential provider policies.</span></span>

<span data-ttu-id="a8fde-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="a8fde-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="a8fde-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a8fde-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
  string EnumerateAdministrators;
};
```

## <a name="members"></a><span data-ttu-id="a8fde-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="a8fde-111">Members</span></span>

<span data-ttu-id="a8fde-112">La clase Config01 de la **\_ Directiva MDM \_ \_ CredentialsUI02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="a8fde-112">The **MDM\_Policy\_Config01\_CredentialsUI02** class has these types of members:</span></span>

-   [<span data-ttu-id="a8fde-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a8fde-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a8fde-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="a8fde-114">Properties</span></span>

<span data-ttu-id="a8fde-115">La **clase \_ \_ Config01 de \_ CredentialsUI02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="a8fde-115">The **MDM\_Policy\_Config01\_CredentialsUI02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="a8fde-116">DisablePasswordReveal</span><span class="sxs-lookup"><span data-stu-id="a8fde-116">DisablePasswordReveal</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8fde-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a8fde-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8fde-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a8fde-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="a8fde-119">EnumerateAdministrators</span><span class="sxs-lookup"><span data-stu-id="a8fde-119">EnumerateAdministrators</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-enumerateadministrators)
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8fde-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a8fde-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8fde-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="a8fde-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a8fde-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="a8fde-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8fde-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a8fde-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8fde-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a8fde-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8fde-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a8fde-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="a8fde-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="a8fde-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a8fde-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="a8fde-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="a8fde-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="a8fde-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a8fde-129">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="a8fde-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a8fde-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a8fde-130">Requirements</span></span>



| <span data-ttu-id="a8fde-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a8fde-131">Requirement</span></span> | <span data-ttu-id="a8fde-132">Value</span><span class="sxs-lookup"><span data-stu-id="a8fde-132">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a8fde-133">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8fde-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a8fde-134">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="a8fde-134">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="a8fde-135">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a8fde-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a8fde-136">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="a8fde-136">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="a8fde-137">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="a8fde-137">Namespace</span></span><br/>                | <span data-ttu-id="a8fde-138">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="a8fde-138">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="a8fde-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a8fde-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a8fde-140"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a8fde-140"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="a8fde-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a8fde-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a8fde-142"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a8fde-142"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

