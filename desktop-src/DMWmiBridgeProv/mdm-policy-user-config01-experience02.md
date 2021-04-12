---
title: MDM_Policy_User_Config01_Experience02 (clase)
description: La \_ clase Config01 de usuario de directiva de MDM \_ \_ \_ Experience02 representa las directivas de experiencia disponibles.
ms.assetid: 61a5f093-812a-4fcb-940d-d5f0de7f8c5f
keywords:
- MDM_Policy_User_Config01_Experience02 (clase)
- MDM_Policy_User_Config01_Experience02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Config01_Experience02
- MDM_Policy_User_Config01_Experience02.InstanceID
- MDM_Policy_User_Config01_Experience02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a982728a3b2f2a899cdbdbd6239a29c5310a258e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491735"
---
# <a name="mdm_policy_user_config01_experience02-class"></a><span data-ttu-id="63827-105">\_Clase Experience02 de usuario de directiva MDM \_ \_ Config01 \_</span><span class="sxs-lookup"><span data-stu-id="63827-105">MDM\_Policy\_User\_Config01\_Experience02 class</span></span>

<span data-ttu-id="63827-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="63827-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="63827-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="63827-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="63827-108">La **clase \_ Config01 de usuario de directiva de MDM \_ \_ \_ Experience02** representa las directivas de experiencia disponibles.</span><span class="sxs-lookup"><span data-stu-id="63827-108">The **MDM\_Policy\_User\_Config01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="63827-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="63827-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="63827-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63827-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Config01_Experience02
{
  string InstanceID;
  string ParentID;
  sint32 AllowTailoredExperiencesWithDiagnosticData;
  sint32 AllowWindowsConsumerFeatures;
  sint32 AllowWindowsSpotlight;
  sint32 AllowWindowsSpotlightWindowsWelcomeExperience;
  sint32 AllowWindowsSpotlightOnActionCenter;
  sint32 ConfigureWindowsSpotlightOnLockScreen;
  sint32 AllowThirdPartySuggestionsInWindowsSpotlight;
};
```

## <a name="members"></a><span data-ttu-id="63827-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="63827-111">Members</span></span>

<span data-ttu-id="63827-112">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ Experience02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="63827-112">The **MDM\_Policy\_User\_Config01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="63827-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63827-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="63827-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="63827-114">Properties</span></span>

<span data-ttu-id="63827-115">La clase Config01 de usuario de la **\_ Directiva MDM \_ \_ \_ Experience02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="63827-115">The **MDM\_Policy\_User\_Config01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="63827-116">AllowTailoredExperiencesWithDiagnosticData</span><span class="sxs-lookup"><span data-stu-id="63827-116">AllowTailoredExperiencesWithDiagnosticData</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowtailoredexperienceswithdiagnosticdata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63827-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="63827-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63827-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="63827-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63827-119">AllowThirdPartySuggestionsInWindowsSpotlight</span><span class="sxs-lookup"><span data-stu-id="63827-119">AllowThirdPartySuggestionsInWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowthirdpartysuggestionsinwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63827-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="63827-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63827-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="63827-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63827-122">AllowWindowsConsumerFeatures</span><span class="sxs-lookup"><span data-stu-id="63827-122">AllowWindowsConsumerFeatures</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsconsumerfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63827-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="63827-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63827-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="63827-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63827-125">AllowWindowsSpotlight</span><span class="sxs-lookup"><span data-stu-id="63827-125">AllowWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63827-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="63827-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63827-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="63827-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63827-128">AllowWindowsSpotlightOnActionCenter</span><span class="sxs-lookup"><span data-stu-id="63827-128">AllowWindowsSpotlightOnActionCenter</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightonactioncenter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63827-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="63827-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63827-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="63827-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63827-131">AllowWindowsSpotlightWindowsWelcomeExperience</span><span class="sxs-lookup"><span data-stu-id="63827-131">AllowWindowsSpotlightWindowsWelcomeExperience</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightwindowswelcomeexperience)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63827-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="63827-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63827-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="63827-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="63827-134">ConfigureWindowsSpotlightOnLockScreen</span><span class="sxs-lookup"><span data-stu-id="63827-134">ConfigureWindowsSpotlightOnLockScreen</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-configurewindowsspotlightonlockscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="63827-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="63827-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="63827-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="63827-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="63827-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="63827-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63827-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="63827-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63827-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63827-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63827-140">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="63827-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="63827-141">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="63827-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="63827-142">Para esta clase, la cadena es "Experience".</span><span class="sxs-lookup"><span data-stu-id="63827-142">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="63827-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="63827-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="63827-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="63827-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="63827-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="63827-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="63827-146">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="63827-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="63827-147">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="63827-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="63827-148">Para esta clase, la cadena es "./User/Vendor/MSFT/Policy/Config".</span><span class="sxs-lookup"><span data-stu-id="63827-148">For this class, the string is "./User/Vendor/MSFT/Policy/Config"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="63827-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63827-149">Requirements</span></span>



| <span data-ttu-id="63827-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="63827-150">Requirement</span></span> | <span data-ttu-id="63827-151">Value</span><span class="sxs-lookup"><span data-stu-id="63827-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63827-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63827-152">Minimum supported client</span></span><br/> | <span data-ttu-id="63827-153">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="63827-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="63827-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="63827-154">Minimum supported server</span></span><br/> | <span data-ttu-id="63827-155">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="63827-155">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="63827-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="63827-156">Namespace</span></span><br/>                | <span data-ttu-id="63827-157">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="63827-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="63827-158">MOF</span><span class="sxs-lookup"><span data-stu-id="63827-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="63827-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="63827-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="63827-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="63827-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="63827-161"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="63827-161"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

