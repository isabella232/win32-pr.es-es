---
title: MDM_Policy_User_Result01_Desktop02 (clase)
description: La \_ clase Result01 de usuario de directiva de MDM \_ \_ \_ Desktop02 representa las directivas de Perfil de carpeta disponibles.
ms.assetid: dab89ac4-b857-474e-8fe5-6822fe06ac91
keywords:
- MDM_Policy_User_Result01_Desktop02 (clase)
- MDM_Policy_User_Result01_Desktop02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Desktop02
- MDM_Policy_User_Result01_Desktop02.InstanceID
- MDM_Policy_User_Result01_Desktop02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da6504176140b9e775c7b7f83e0f9835ce25b42c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079416"
---
# <a name="mdm_policy_user_result01_desktop02-class"></a><span data-ttu-id="9af45-105">\_Clase Desktop02 de usuario de directiva MDM \_ \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="9af45-105">MDM\_Policy\_User\_Result01\_Desktop02 class</span></span>

<span data-ttu-id="9af45-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="9af45-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9af45-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="9af45-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9af45-108">La \_ clase Result01 de usuario de directiva de MDM \_ \_ \_ Desktop02 representa las directivas de Perfil de carpeta disponibles.</span><span class="sxs-lookup"><span data-stu-id="9af45-108">The MDM\_Policy\_User\_Result01\_Desktop02 class represents the available folder profile policies.</span></span>

<span data-ttu-id="9af45-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9af45-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9af45-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9af45-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Desktop02
{
  string InstanceID;
  string ParentID;
  string PreventUserRedirectionOfProfileFolders;
};
```

## <a name="members"></a><span data-ttu-id="9af45-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="9af45-111">Members</span></span>

<span data-ttu-id="9af45-112">La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ Desktop02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9af45-112">The **MDM\_Policy\_User\_Result01\_Desktop02** class has these types of members:</span></span>

-   [<span data-ttu-id="9af45-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9af45-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9af45-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9af45-114">Properties</span></span>

<span data-ttu-id="9af45-115">La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ Desktop02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9af45-115">The **MDM\_Policy\_User\_Result01\_Desktop02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9af45-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9af45-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af45-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9af45-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af45-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9af45-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af45-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9af45-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9af45-120">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9af45-120">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af45-121">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9af45-121">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af45-122">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9af45-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9af45-123">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9af45-123">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9af45-124">PreventUserRedirectionOfProfileFolders</span><span class="sxs-lookup"><span data-stu-id="9af45-124">PreventUserRedirectionOfProfileFolders</span></span>](/windows/client-management/mdm/policy-csp-desktop#desktop-preventuserredirectionofprofilefolders)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9af45-125">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9af45-125">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9af45-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9af45-126">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9af45-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9af45-127">Requirements</span></span>



| <span data-ttu-id="9af45-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="9af45-128">Requirement</span></span> | <span data-ttu-id="9af45-129">Value</span><span class="sxs-lookup"><span data-stu-id="9af45-129">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9af45-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9af45-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9af45-131">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="9af45-131">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9af45-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9af45-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9af45-133">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9af45-133">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9af45-134">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9af45-134">Namespace</span></span><br/>                | <span data-ttu-id="9af45-135">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="9af45-135">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9af45-136">MOF</span><span class="sxs-lookup"><span data-stu-id="9af45-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9af45-137"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9af45-137"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9af45-138">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9af45-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9af45-139"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9af45-139"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

