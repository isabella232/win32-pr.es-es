---
title: MDM_Policy_Config01_Licensing02 (clase)
description: La \_ clase MDM Policy \_ Config01 \_ Licensing02 representa las directivas de licencias disponibles.
ms.assetid: 7ec186e9-626e-4361-88fd-665b947ca23d
keywords:
- MDM_Policy_Config01_Licensing02 (clase)
- MDM_Policy_Config01_Licensing02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Licensing02
- MDM_Policy_Config01_Licensing02.InstanceID
- MDM_Policy_Config01_Licensing02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d654facc7ec3ba08d1f5b0f31497545945cc73d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996374"
---
# <a name="mdm_policy_config01_licensing02-class"></a><span data-ttu-id="6711b-105">\_ \_ Clase Licensing02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="6711b-105">MDM\_Policy\_Config01\_Licensing02 class</span></span>

<span data-ttu-id="6711b-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="6711b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="6711b-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="6711b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="6711b-108">La clase **MDM \_ Policy \_ Config01 \_ Licensing02** representa las directivas de licencias disponibles.</span><span class="sxs-lookup"><span data-stu-id="6711b-108">The **MDM\_Policy\_Config01\_Licensing02** class represents the licensing policies available.</span></span>

<span data-ttu-id="6711b-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="6711b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="6711b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6711b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Licensing02
{
  string InstanceID;
  string ParentID;
  sint32 AllowWindowsEntitlementReactivation;
  sint32 DisallowKMSClientOnlineAVSValidation;
};
```

## <a name="members"></a><span data-ttu-id="6711b-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="6711b-111">Members</span></span>

<span data-ttu-id="6711b-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Licensing02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="6711b-112">The **MDM\_Policy\_Config01\_Licensing02** class has these types of members:</span></span>

-   [<span data-ttu-id="6711b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6711b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6711b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="6711b-114">Properties</span></span>

<span data-ttu-id="6711b-115">La **clase \_ \_ Config01 de \_ Licensing02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="6711b-115">The **MDM\_Policy\_Config01\_Licensing02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="6711b-116">AllowWindowsEntitlementReactivation</span><span class="sxs-lookup"><span data-stu-id="6711b-116">AllowWindowsEntitlementReactivation</span></span>](/windows/client-management/mdm/policy-csp-licensing#licensing-allowwindowsentitlementreactivation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6711b-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6711b-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6711b-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6711b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="6711b-119">DisallowKMSClientOnlineAVSValidation</span><span class="sxs-lookup"><span data-stu-id="6711b-119">DisallowKMSClientOnlineAVSValidation</span></span>](/windows/client-management/mdm/policy-csp-licensing#licensing-disallowkmsclientonlineavsvalidation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="6711b-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="6711b-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="6711b-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="6711b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="6711b-122">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="6711b-122">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6711b-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6711b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6711b-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6711b-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6711b-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6711b-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6711b-126">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="6711b-126">Identifies the name of the parent node.</span></span> <span data-ttu-id="6711b-127">Para esta clase, la cadena es "Licensing".</span><span class="sxs-lookup"><span data-stu-id="6711b-127">For this class, the string is "Licensing".</span></span>

</dd> <dt>

<span data-ttu-id="6711b-128">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="6711b-128">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6711b-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="6711b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="6711b-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="6711b-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6711b-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="6711b-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="6711b-132">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="6711b-132">Describes the full path to the parent node.</span></span> <span data-ttu-id="6711b-133">Para esta clase, la cadena es "./Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="6711b-133">For this class, the string is "./Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6711b-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6711b-134">Requirements</span></span>



| <span data-ttu-id="6711b-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="6711b-135">Requirement</span></span> | <span data-ttu-id="6711b-136">Value</span><span class="sxs-lookup"><span data-stu-id="6711b-136">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6711b-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6711b-137">Minimum supported client</span></span><br/> | <span data-ttu-id="6711b-138">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="6711b-138">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6711b-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6711b-139">Minimum supported server</span></span><br/> | <span data-ttu-id="6711b-140">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="6711b-140">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="6711b-141">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="6711b-141">Namespace</span></span><br/>                | <span data-ttu-id="6711b-142">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="6711b-142">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="6711b-143">MOF</span><span class="sxs-lookup"><span data-stu-id="6711b-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6711b-144"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6711b-144"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="6711b-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="6711b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6711b-146"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="6711b-146"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

