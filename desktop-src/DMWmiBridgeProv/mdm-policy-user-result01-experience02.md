---
title: MDM_Policy_User_Result01_Experience02 (clase)
description: La \_ clase Result01 de usuario de directiva de MDM \_ \_ \_ Experience02 representa las directivas de experiencia disponibles.
ms.assetid: 729dfc75-7458-426f-8173-9ba75b4ee306
keywords:
- MDM_Policy_User_Result01_Experience02 (clase)
- MDM_Policy_User_Result01_Experience02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_User_Result01_Experience02
- MDM_Policy_User_Result01_Experience02.InstanceID
- MDM_Policy_User_Result01_Experience02.ParentID
api_location:
- Mofs\DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 320941108309264a2cce3be6e63edca305c1cd40
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905271"
---
# <a name="mdm_policy_user_result01_experience02-class"></a><span data-ttu-id="7be92-105">\_Clase Experience02 de usuario de directiva MDM \_ \_ Result01 \_</span><span class="sxs-lookup"><span data-stu-id="7be92-105">MDM\_Policy\_User\_Result01\_Experience02 class</span></span>

<span data-ttu-id="7be92-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="7be92-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="7be92-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="7be92-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="7be92-108">La **clase \_ Result01 de usuario de directiva de MDM \_ \_ \_ Experience02** representa las directivas de experiencia disponibles.</span><span class="sxs-lookup"><span data-stu-id="7be92-108">The **MDM\_Policy\_User\_Result01\_Experience02** class represents the experience policies available.</span></span>

<span data-ttu-id="7be92-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="7be92-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7be92-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7be92-110">Syntax</span></span>

``` syntax
[InPartition("local-user"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_User_Result01_Experience02
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

## <a name="members"></a><span data-ttu-id="7be92-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="7be92-111">Members</span></span>

<span data-ttu-id="7be92-112">La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ Experience02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="7be92-112">The **MDM\_Policy\_User\_Result01\_Experience02** class has these types of members:</span></span>

-   [<span data-ttu-id="7be92-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7be92-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7be92-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="7be92-114">Properties</span></span>

<span data-ttu-id="7be92-115">La clase Result01 de usuario de la **\_ Directiva MDM \_ \_ \_ Experience02** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="7be92-115">The **MDM\_Policy\_User\_Result01\_Experience02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="7be92-116">AllowTailoredExperiencesWithDiagnosticData</span><span class="sxs-lookup"><span data-stu-id="7be92-116">AllowTailoredExperiencesWithDiagnosticData</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowtailoredexperienceswithdiagnosticdata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7be92-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7be92-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7be92-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7be92-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7be92-119">AllowThirdPartySuggestionsInWindowsSpotlight</span><span class="sxs-lookup"><span data-stu-id="7be92-119">AllowThirdPartySuggestionsInWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowthirdpartysuggestionsinwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7be92-120">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7be92-120">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7be92-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7be92-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7be92-122">AllowWindowsConsumerFeatures</span><span class="sxs-lookup"><span data-stu-id="7be92-122">AllowWindowsConsumerFeatures</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsconsumerfeatures)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7be92-123">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7be92-123">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7be92-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7be92-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7be92-125">AllowWindowsSpotlight</span><span class="sxs-lookup"><span data-stu-id="7be92-125">AllowWindowsSpotlight</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlight)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7be92-126">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7be92-126">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7be92-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7be92-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7be92-128">AllowWindowsSpotlightOnActionCenter</span><span class="sxs-lookup"><span data-stu-id="7be92-128">AllowWindowsSpotlightOnActionCenter</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightonactioncenter)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7be92-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7be92-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7be92-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7be92-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7be92-131">AllowWindowsSpotlightWindowsWelcomeExperience</span><span class="sxs-lookup"><span data-stu-id="7be92-131">AllowWindowsSpotlightWindowsWelcomeExperience</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-allowwindowsspotlightwindowswelcomeexperience)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7be92-132">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7be92-132">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7be92-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7be92-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="7be92-134">ConfigureWindowsSpotlightOnLockScreen</span><span class="sxs-lookup"><span data-stu-id="7be92-134">ConfigureWindowsSpotlightOnLockScreen</span></span>](/windows/client-management/mdm/policy-csp-experience#experience-configurewindowsspotlightonlockscreen)
</dt> <dd> <dl> <dt>

<span data-ttu-id="7be92-135">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="7be92-135">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="7be92-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="7be92-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="7be92-137">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="7be92-137">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7be92-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7be92-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7be92-139">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7be92-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7be92-140">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7be92-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7be92-141">Identifica el nombre del nodo primario.</span><span class="sxs-lookup"><span data-stu-id="7be92-141">Identifies the name of the parent node.</span></span> <span data-ttu-id="7be92-142">Para esta clase, la cadena es "Experience".</span><span class="sxs-lookup"><span data-stu-id="7be92-142">For this class, the string is "Experience".</span></span>

</dd> <dt>

<span data-ttu-id="7be92-143">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="7be92-143">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7be92-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="7be92-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="7be92-145">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="7be92-145">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7be92-146">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="7be92-146">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="7be92-147">Describe la ruta de acceso completa al nodo primario.</span><span class="sxs-lookup"><span data-stu-id="7be92-147">Describes the full path to the parent node.</span></span> <span data-ttu-id="7be92-148">Para esta clase, la cadena es "./User/Vendor/MSFT/Policy/Result".</span><span class="sxs-lookup"><span data-stu-id="7be92-148">For this class, the string is "./User/Vendor/MSFT/Policy/Result"</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="7be92-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7be92-149">Requirements</span></span>



| <span data-ttu-id="7be92-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="7be92-150">Requirement</span></span> | <span data-ttu-id="7be92-151">Value</span><span class="sxs-lookup"><span data-stu-id="7be92-151">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7be92-152">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7be92-152">Minimum supported client</span></span><br/> | <span data-ttu-id="7be92-153">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="7be92-153">Windows 10 \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7be92-154">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7be92-154">Minimum supported server</span></span><br/> | <span data-ttu-id="7be92-155">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="7be92-155">None supported</span></span><br/>                                                                            |
| <span data-ttu-id="7be92-156">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="7be92-156">Namespace</span></span><br/>                | <span data-ttu-id="7be92-157">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="7be92-157">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                                   |
| <span data-ttu-id="7be92-158">MOF</span><span class="sxs-lookup"><span data-stu-id="7be92-158">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7be92-159"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7be92-159"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl>       |
| <span data-ttu-id="7be92-160">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7be92-160">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7be92-161"><dt>\\DMWmiBridgeProv.dllMOF</dt></span><span class="sxs-lookup"><span data-stu-id="7be92-161"><dt>Mofs\\DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

