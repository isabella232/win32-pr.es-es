---
title: MDM_Policy_User_Result01_Authentication02 (clase)
description: La \_ clase Result01 de usuario de directiva de MDM \_ \_ \_ Authentication02 representa las directivas de administración de autenticación disponibles.
ms.assetid: 57da7a17-9955-445d-998e-369b101cda3c
keywords:
- MDM_Policy_User_Result01_Authentication02 (clase)
- MDM_Policy_User_Result01_Authentication02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Authentication02
- MDM_Policy_User_Result01_Authentication02.InstanceID
- MDM_Policy_User_Result01_Authentication02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba1630cc4df9062627a5a2e7ea3b6e9516908ca
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490781"
---
# <a name="mdm_policy_user_result01_authentication02-class"></a><span data-ttu-id="e102e-105">\_Clase Authentication02 de usuario de directiva MDM \_ \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="e102e-105">MDM\_Policy\_User\_Result01\_Authentication02 class</span></span>

<span data-ttu-id="e102e-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="e102e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="e102e-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="e102e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="e102e-108">La **clase \_ Result01 de usuario de directiva de MDM \_ \_ \_ Authentication02** representa las directivas de administración de autenticación disponibles.</span><span class="sxs-lookup"><span data-stu-id="e102e-108">The **MDM\_Policy\_User\_Result01\_Authentication02** class represents the authentication management policies available.</span></span>

<span data-ttu-id="e102e-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="e102e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="e102e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="e102e-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Authentication02
{
  string InstanceID;
  string ParentID;
  sint32 AllowEAPCertSSO;
};
```

## <a name="members"></a><span data-ttu-id="e102e-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="e102e-111">Members</span></span>

<span data-ttu-id="e102e-112">La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ Authentication02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e102e-112">The **MDM\_Policy\_User\_Result01\_Authentication02** class has these types of members:</span></span>

-   [<span data-ttu-id="e102e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e102e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e102e-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e102e-114">Properties</span></span>

<span data-ttu-id="e102e-115">La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ Authentication02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e102e-115">The **MDM\_Policy\_User\_Result01\_Authentication02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="e102e-116">AllowEAPCertSSO</span><span class="sxs-lookup"><span data-stu-id="e102e-116">AllowEAPCertSSO</span></span>](/windows/client-management/mdm/policy-csp-authentication#authentication-alloweapcertsso)
</dt> <dd> <dl> <dt>

<span data-ttu-id="e102e-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="e102e-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="e102e-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="e102e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="e102e-119">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="e102e-119">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e102e-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e102e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e102e-121">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e102e-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e102e-122">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e102e-122">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e102e-123">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="e102e-123">Identifies the name of the parent node.</span></span> <span data-ttu-id="e102e-124">Para esta clase, la cadena es "Authentication".</span><span class="sxs-lookup"><span data-stu-id="e102e-124">For this class, the string is "Authentication".</span></span>

</dd> <dt>

<span data-ttu-id="e102e-125">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="e102e-125">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e102e-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="e102e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e102e-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="e102e-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e102e-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="e102e-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="e102e-129">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="e102e-129">Describes the full path to the parent node.</span></span> <span data-ttu-id="e102e-130">Para esta clase, la cadena es "./User/Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="e102e-130">For this class, the string is "./User/Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e102e-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e102e-131">Requirements</span></span>



| <span data-ttu-id="e102e-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e102e-132">Requirement</span></span> | <span data-ttu-id="e102e-133">Value</span><span class="sxs-lookup"><span data-stu-id="e102e-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e102e-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e102e-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e102e-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="e102e-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="e102e-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e102e-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e102e-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="e102e-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="e102e-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="e102e-138">Namespace</span></span><br/>                | <span data-ttu-id="e102e-139">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="e102e-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="e102e-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e102e-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e102e-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e102e-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e102e-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e102e-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e102e-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e102e-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e102e-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="e102e-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e102e-145">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="e102e-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

