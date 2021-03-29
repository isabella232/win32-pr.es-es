---
title: MDM_Policy_Config01_Kerberos02 (clase)
description: La \_ clase Config01 de Kerberos02 de directivas MDM \_ \_ configura las directivas de Kerberos.
ms.assetid: d34ccc8a-0c0c-4b7a-88c2-35360ebd0b8e
keywords:
- MDM_Policy_Config01_Kerberos02 (clase)
- MDM_Policy_Config01_Kerberos02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Kerberos02
- MDM_Policy_Config01_Kerberos02.InstanceID
- MDM_Policy_Config01_Kerberos02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c173c892985487ed1ac061ea720e3485ecb355ef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905235"
---
# <a name="mdm_policy_config01_kerberos02-class"></a><span data-ttu-id="e15f8-105">\_ \_ Clase Kerberos02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="e15f8-105">MDM\_Policy\_Config01\_Kerberos02 class</span></span>

<span data-ttu-id="e15f8-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="e15f8-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e15f8-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="e15f8-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e15f8-108">La \_ clase Config01 de Kerberos02 de directivas MDM \_ \_ configura las directivas de Kerberos.</span><span class="sxs-lookup"><span data-stu-id="e15f8-108">The MDM\_Policy\_Config01\_Kerberos02 class configures the Kerberos policies.</span></span>

<span data-ttu-id="e15f8-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e15f8-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e15f8-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e15f8-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Kerberos02
{
  string InstanceID;
  string ParentID;
  string AllowForestSearchOrder;
  string KerberosClientSupportsClaimsCompoundArmor;
  string RequireKerberosArmoring;
  string RequireStrictKDCValidation;
  string SetMaximumContextTokenSize;
};
```

## <a name="members"></a><span data-ttu-id="e15f8-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e15f8-111">Members</span></span>

<span data-ttu-id="e15f8-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Kerberos02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e15f8-112">The **MDM\_Policy\_Config01\_Kerberos02** class has these types of members:</span></span>

-   [<span data-ttu-id="e15f8-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e15f8-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e15f8-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e15f8-114">Properties</span></span>

<span data-ttu-id="e15f8-115">La **clase \_ \_ Config01 de \_ Kerberos02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e15f8-115">The **MDM\_Policy\_Config01\_Kerberos02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e15f8-116">AllowForestSearchOrder</span><span class="sxs-lookup"><span data-stu-id="e15f8-116">AllowForestSearchOrder</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-allowforestsearchorder)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e15f8-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e15f8-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e15f8-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e15f8-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e15f8-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e15f8-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e15f8-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e15f8-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e15f8-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e15f8-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e15f8-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e15f8-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e15f8-123">KerberosClientSupportsClaimsCompoundArmor</span><span class="sxs-lookup"><span data-stu-id="e15f8-123">KerberosClientSupportsClaimsCompoundArmor</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-kerberosclientsupportsclaimscompoundarmor)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e15f8-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e15f8-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e15f8-125">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e15f8-125">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e15f8-126">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e15f8-126">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e15f8-127">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e15f8-127">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e15f8-128">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e15f8-128">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e15f8-129">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e15f8-129">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e15f8-130">RequireKerberosArmoring</span><span class="sxs-lookup"><span data-stu-id="e15f8-130">RequireKerberosArmoring</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirekerberosarmoring)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e15f8-131">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e15f8-131">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e15f8-132">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e15f8-132">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e15f8-133">RequireStrictKDCValidation</span><span class="sxs-lookup"><span data-stu-id="e15f8-133">RequireStrictKDCValidation</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-requirestrictkdcvalidation)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e15f8-134">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e15f8-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e15f8-135">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e15f8-135">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="e15f8-136">SetMaximumContextTokenSize</span><span class="sxs-lookup"><span data-stu-id="e15f8-136">SetMaximumContextTokenSize</span></span>](/windows/client-management/mdm/policy-csp-kerberos#kerberos-setmaximumcontexttokensize)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e15f8-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e15f8-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e15f8-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e15f8-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e15f8-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e15f8-139">Requirements</span></span>



| <span data-ttu-id="e15f8-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="e15f8-140">Requirement</span></span> | <span data-ttu-id="e15f8-141">Value</span><span class="sxs-lookup"><span data-stu-id="e15f8-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e15f8-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e15f8-142">Minimum supported client</span></span><br/> | <span data-ttu-id="e15f8-143">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="e15f8-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e15f8-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e15f8-144">Minimum supported server</span></span><br/> | <span data-ttu-id="e15f8-145">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e15f8-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e15f8-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e15f8-146">Namespace</span></span><br/>                | <span data-ttu-id="e15f8-147">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="e15f8-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e15f8-148">MOF</span><span class="sxs-lookup"><span data-stu-id="e15f8-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e15f8-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e15f8-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e15f8-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e15f8-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e15f8-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e15f8-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

