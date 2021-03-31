---
title: MDM_Policy_User_Config01_CredentialsUI02 (clase)
description: La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ CredentialsUI02 representa las directivas de credenciales disponibles.
ms.assetid: b0a45070-c25b-4a4d-9fbc-cd107fd0fa2f
keywords:
- MDM_Policy_User_Config01_CredentialsUI02 (clase)
- MDM_Policy_User_Config01_CredentialsUI02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_CredentialsUI02
- MDM_Policy_User_Config01_CredentialsUI02.InstanceID
- MDM_Policy_User_Config01_CredentialsUI02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230d0286ac36540b4d0b8506a72a9b4389d37e6e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079592"
---
# <a name="mdm_policy_user_config01_credentialsui02-class"></a><span data-ttu-id="5a50f-105">\_Clase CredentialsUI02 de usuario de directiva MDM \_ \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="5a50f-105">MDM\_Policy\_User\_Config01\_CredentialsUI02 class</span></span>

<span data-ttu-id="5a50f-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="5a50f-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="5a50f-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="5a50f-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="5a50f-108">La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ CredentialsUI02 representa las directivas de credenciales disponibles.</span><span class="sxs-lookup"><span data-stu-id="5a50f-108">The MDM\_Policy\_User\_Config01\_CredentialsUI02 class represents the available credentials policies.</span></span>

<span data-ttu-id="5a50f-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="5a50f-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a50f-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="5a50f-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_CredentialsUI02
{
  string InstanceID;
  string ParentID;
  string DisablePasswordReveal;
};
```

## <a name="members"></a><span data-ttu-id="5a50f-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="5a50f-111">Members</span></span>

<span data-ttu-id="5a50f-112">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ CredentialsUI02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="5a50f-112">The **MDM\_Policy\_User\_Config01\_CredentialsUI02** class has these types of members:</span></span>

-   [<span data-ttu-id="5a50f-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5a50f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="5a50f-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="5a50f-114">Properties</span></span>

<span data-ttu-id="5a50f-115">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ CredentialsUI02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="5a50f-115">The **MDM\_Policy\_User\_Config01\_CredentialsUI02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="5a50f-116">DisablePasswordReveal</span><span class="sxs-lookup"><span data-stu-id="5a50f-116">DisablePasswordReveal</span></span>](/windows/client-management/mdm/policy-csp-credentialsui#credentialsui-disablepasswordreveal)
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a50f-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a50f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a50f-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="5a50f-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5a50f-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="5a50f-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a50f-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a50f-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a50f-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a50f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a50f-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5a50f-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="5a50f-123">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="5a50f-123">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="5a50f-124">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="5a50f-124">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="5a50f-125">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="5a50f-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="5a50f-126">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="5a50f-126">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5a50f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a50f-127">Requirements</span></span>



| <span data-ttu-id="5a50f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a50f-128">Requirement</span></span> | <span data-ttu-id="5a50f-129">Value</span><span class="sxs-lookup"><span data-stu-id="5a50f-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a50f-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a50f-130">Minimum supported client</span></span><br/> | <span data-ttu-id="5a50f-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="5a50f-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="5a50f-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="5a50f-132">Minimum supported server</span></span><br/> | <span data-ttu-id="5a50f-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="5a50f-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="5a50f-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="5a50f-134">Namespace</span></span><br/>                | <span data-ttu-id="5a50f-135">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="5a50f-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="5a50f-136">MOF</span><span class="sxs-lookup"><span data-stu-id="5a50f-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5a50f-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="5a50f-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="5a50f-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="5a50f-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5a50f-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5a50f-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

