---
title: MDM_Policy_Result01_WindowsLogon02 (clase)
description: La \_ \_ \_ clase Result01 de WINDOWSLOGON02 de directivas MDM obtiene la configuración de la pantalla de bloqueo y la interfaz de usuario de red en el inicio de sesión.
ms.assetid: 4c710e3d-e7d5-4e6e-ad99-b3c7d1813599
keywords:
- MDM_Policy_Result01_WindowsLogon02 (clase)
- MDM_Policy_Result01_WindowsLogon02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_WindowsLogon02
- MDM_Policy_Result01_WindowsLogon02.InstanceID
- MDM_Policy_Result01_WindowsLogon02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: de8e9c0e2ebc2e82d5daef174ce9322b5b4b5ec7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104149937"
---
# <a name="mdm_policy_result01_windowslogon02-class"></a><span data-ttu-id="7bdd4-105">\_ \_ Clase WindowsLogon02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="7bdd4-105">MDM\_Policy\_Result01\_WindowsLogon02 class</span></span>

<span data-ttu-id="7bdd4-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="7bdd4-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7bdd4-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="7bdd4-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7bdd4-108">La \_ \_ \_ clase Result01 de WINDOWSLOGON02 de directivas MDM obtiene la configuración de la pantalla de bloqueo y la interfaz de usuario de red en el inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="7bdd4-108">The MDM\_Policy\_Result01\_WindowsLogon02 class gets the settings of the lock screen and network user interface at logon.</span></span>

<span data-ttu-id="7bdd4-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7bdd4-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bdd4-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7bdd4-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_WindowsLogon02
{
  string InstanceID;
  string ParentID;
  string DontDisplayNetworkSelectionUI;
  string DisableLockScreenAppNotifications;
  sint32 HideFastUserSwitching;
};
```

## <a name="members"></a><span data-ttu-id="7bdd4-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="7bdd4-111">Members</span></span>

<span data-ttu-id="7bdd4-112">La clase Result01 de la **\_ Directiva MDM \_ \_ WindowsLogon02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7bdd4-112">The **MDM\_Policy\_Result01\_WindowsLogon02** class has these types of members:</span></span>

-   [<span data-ttu-id="7bdd4-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7bdd4-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7bdd4-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7bdd4-114">Properties</span></span>

<span data-ttu-id="7bdd4-115">La **clase \_ \_ Result01 de \_ WindowsLogon02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7bdd4-115">The **MDM\_Policy\_Result01\_WindowsLogon02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7bdd4-116">DisableLockScreenAppNotifications</span><span class="sxs-lookup"><span data-stu-id="7bdd4-116">DisableLockScreenAppNotifications</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-disablelockscreenappnotifications)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bdd4-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7bdd4-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bdd4-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7bdd4-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7bdd4-119">DontDisplayNetworkSelectionUI</span><span class="sxs-lookup"><span data-stu-id="7bdd4-119">DontDisplayNetworkSelectionUI</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-dontdisplaynetworkselectionui)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bdd4-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7bdd4-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bdd4-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7bdd4-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7bdd4-122">HideFastUserSwitching</span><span class="sxs-lookup"><span data-stu-id="7bdd4-122">HideFastUserSwitching</span></span>](/windows/client-management/mdm/policy-csp-windowslogon#windowslogon-hidefastuserswitching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bdd4-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7bdd4-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7bdd4-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7bdd4-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7bdd4-125">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7bdd4-125">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bdd4-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7bdd4-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bdd4-127">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7bdd4-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bdd4-128">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7bdd4-128">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7bdd4-129">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7bdd4-129">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7bdd4-130">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7bdd4-130">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7bdd4-131">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7bdd4-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7bdd4-132">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7bdd4-132">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7bdd4-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bdd4-133">Requirements</span></span>



| <span data-ttu-id="7bdd4-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bdd4-134">Requirement</span></span> | <span data-ttu-id="7bdd4-135">Value</span><span class="sxs-lookup"><span data-stu-id="7bdd4-135">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7bdd4-136">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bdd4-136">Minimum supported client</span></span><br/> | <span data-ttu-id="7bdd4-137">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="7bdd4-137">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7bdd4-138">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bdd4-138">Minimum supported server</span></span><br/> | <span data-ttu-id="7bdd4-139">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7bdd4-139">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="7bdd4-140">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7bdd4-140">Namespace</span></span><br/>                | <span data-ttu-id="7bdd4-141">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="7bdd4-141">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="7bdd4-142">MOF</span><span class="sxs-lookup"><span data-stu-id="7bdd4-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7bdd4-143"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7bdd4-143"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7bdd4-144">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7bdd4-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7bdd4-145"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7bdd4-145"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

