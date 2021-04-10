---
title: MDM_Policy_User_Result01_ApplicationManagement02 (clase)
description: La \_ clase Result01 de usuario de directiva de MDM \_ \_ \_ ApplicationManagement02 representa las directivas de inicio disponibles que se establecen por usuario.
ms.assetid: 62545af1-9c26-481e-9668-cd253cf592e7
keywords:
- MDM_Policy_User_Result01_ApplicationManagement02 (clase)
- MDM_Policy_User_Result01_ApplicationManagement02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_ApplicationManagement02
- MDM_Policy_User_Result01_ApplicationManagement02.InstanceID
- MDM_Policy_User_Result01_ApplicationManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18177046691e5c9fe5ca8cb61ee0518a41533c59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150345"
---
# <a name="mdm_policy_user_result01_applicationmanagement02-class"></a><span data-ttu-id="1e64d-105">\_Clase ApplicationManagement02 de usuario de directiva MDM \_ \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="1e64d-105">MDM\_Policy\_User\_Result01\_ApplicationManagement02 class</span></span>

<span data-ttu-id="1e64d-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="1e64d-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="1e64d-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="1e64d-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="1e64d-108">La **clase \_ Result01 de usuario de directiva de MDM \_ \_ \_ ApplicationManagement02** representa las directivas de inicio disponibles que se establecen por usuario.</span><span class="sxs-lookup"><span data-stu-id="1e64d-108">The **MDM\_Policy\_User\_Result01\_ApplicationManagement02** class represents the start policies available that are set on a per-user basis.</span></span>

<span data-ttu-id="1e64d-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="1e64d-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e64d-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1e64d-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_ApplicationManagement02
{
  string InstanceID;
  string ParentID;
  sint32 RequirePrivateStoreOnly;
};
```

## <a name="members"></a><span data-ttu-id="1e64d-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="1e64d-111">Members</span></span>

<span data-ttu-id="1e64d-112">La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ ApplicationManagement02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="1e64d-112">The **MDM\_Policy\_User\_Result01\_ApplicationManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="1e64d-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e64d-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="1e64d-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="1e64d-114">Properties</span></span>

<span data-ttu-id="1e64d-115">La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ ApplicationManagement02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="1e64d-115">The **MDM\_Policy\_User\_Result01\_ApplicationManagement02** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1e64d-116">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="1e64d-116">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e64d-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1e64d-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e64d-118">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1e64d-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e64d-119">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1e64d-119">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1e64d-120">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="1e64d-120">Identifies the name of the parent node.</span></span> <span data-ttu-id="1e64d-121">Para esta clase, la cadena es "ApplicationManagement".</span><span class="sxs-lookup"><span data-stu-id="1e64d-121">For this class, the string is "ApplicationManagement"</span></span>

</dd> <dt>

<span data-ttu-id="1e64d-122">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="1e64d-122">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e64d-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="1e64d-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1e64d-124">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="1e64d-124">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1e64d-125">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="1e64d-125">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="1e64d-126">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="1e64d-126">Describes the full path to the parent node.</span></span> <span data-ttu-id="1e64d-127">Para esta clase, la cadena es "./User/Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="1e64d-127">For this class, the string is "./User/Vendor/MSFT/Policy/Result"</span></span>

</dd> <dt>

[<span data-ttu-id="1e64d-128">RequirePrivateStoreOnly</span><span class="sxs-lookup"><span data-stu-id="1e64d-128">RequirePrivateStoreOnly</span></span>](/windows/client-management/mdm/policy-csp-applicationmanagement#applicationmanagement-requireprivatestoreonly)
</dt> <dd> <dl> <dt>

<span data-ttu-id="1e64d-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="1e64d-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="1e64d-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="1e64d-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="1e64d-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e64d-131">Requirements</span></span>



| <span data-ttu-id="1e64d-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e64d-132">Requirement</span></span> | <span data-ttu-id="1e64d-133">Value</span><span class="sxs-lookup"><span data-stu-id="1e64d-133">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1e64d-134">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e64d-134">Minimum supported client</span></span><br/> | <span data-ttu-id="1e64d-135">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="1e64d-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="1e64d-136">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1e64d-136">Minimum supported server</span></span><br/> | <span data-ttu-id="1e64d-137">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="1e64d-137">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="1e64d-138">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="1e64d-138">Namespace</span></span><br/>                | <span data-ttu-id="1e64d-139">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="1e64d-139">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="1e64d-140">MOF</span><span class="sxs-lookup"><span data-stu-id="1e64d-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1e64d-141"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1e64d-141"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="1e64d-142">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1e64d-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e64d-143"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e64d-143"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e64d-144">Vea también</span><span class="sxs-lookup"><span data-stu-id="1e64d-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e64d-145">Usar scripting de PowerShell con el proveedor de puente WMI</span><span class="sxs-lookup"><span data-stu-id="1e64d-145">Using PowerShell scripting with the WMI Bridge Provider</span></span>](/windows/client-management/mdm/using-powershell-scripting-with-the-wmi-bridge-provider)
</dt> </dl>

 

