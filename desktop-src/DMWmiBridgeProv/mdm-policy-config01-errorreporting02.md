---
title: MDM_Policy_Config01_ErrorReporting02 (clase)
description: La \_ clase Config01 de ErrorReporting02 de directivas MDM \_ \_ configura las directivas de informes de errores.
ms.assetid: 41067b5e-0db5-43b3-b1d5-2d6c54c35388
keywords:
- MDM_Policy_Config01_ErrorReporting02 (clase)
- MDM_Policy_Config01_ErrorReporting02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_ErrorReporting02
- MDM_Policy_Config01_ErrorReporting02.InstanceID
- MDM_Policy_Config01_ErrorReporting02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d1c23cf5b0b01f05fa3712d6b1de11461c6f47da
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079175"
---
# <a name="mdm_policy_config01_errorreporting02-class"></a><span data-ttu-id="9acaa-105">\_ \_ Clase ErrorReporting02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="9acaa-105">MDM\_Policy\_Config01\_ErrorReporting02 class</span></span>

<span data-ttu-id="9acaa-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="9acaa-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="9acaa-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="9acaa-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="9acaa-108">La \_ clase Config01 de ErrorReporting02 de directivas MDM \_ \_ configura las directivas de informes de errores.</span><span class="sxs-lookup"><span data-stu-id="9acaa-108">The MDM\_Policy\_Config01\_ErrorReporting02 class configures the error reporting policies.</span></span>

<span data-ttu-id="9acaa-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="9acaa-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="9acaa-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9acaa-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_ErrorReporting02
{
  string InstanceID;
  string ParentID;
  string CustomizeConsentSettings;
  string DisableWindowsErrorReporting;
  string DisplayErrorNotification;
  string DoNotSendAdditionalData;
  string PreventCriticalErrorDisplay;
};
```

## <a name="members"></a><span data-ttu-id="9acaa-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="9acaa-111">Members</span></span>

<span data-ttu-id="9acaa-112">La clase Config01 de la **\_ Directiva MDM \_ \_ ErrorReporting02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9acaa-112">The **MDM\_Policy\_Config01\_ErrorReporting02** class has these types of members:</span></span>

-   [<span data-ttu-id="9acaa-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9acaa-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9acaa-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9acaa-114">Properties</span></span>

<span data-ttu-id="9acaa-115">La **clase \_ \_ Config01 de \_ ErrorReporting02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9acaa-115">The **MDM\_Policy\_Config01\_ErrorReporting02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="9acaa-116">CustomizeConsentSettings</span><span class="sxs-lookup"><span data-stu-id="9acaa-116">CustomizeConsentSettings</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-customizeconsentsettings)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9acaa-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9acaa-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9acaa-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9acaa-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9acaa-119">DisableWindowsErrorReporting</span><span class="sxs-lookup"><span data-stu-id="9acaa-119">DisableWindowsErrorReporting</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-disablewindowserrorreporting)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9acaa-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9acaa-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9acaa-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9acaa-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9acaa-122">DisplayErrorNotification</span><span class="sxs-lookup"><span data-stu-id="9acaa-122">DisplayErrorNotification</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-displayerrornotification)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9acaa-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9acaa-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9acaa-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9acaa-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9acaa-125">DoNotSendAdditionalData</span><span class="sxs-lookup"><span data-stu-id="9acaa-125">DoNotSendAdditionalData</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-donotsendadditionaldata)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9acaa-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9acaa-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9acaa-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9acaa-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9acaa-128">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="9acaa-128">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9acaa-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9acaa-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9acaa-130">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9acaa-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9acaa-131">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9acaa-131">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="9acaa-132">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="9acaa-132">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9acaa-133">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9acaa-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9acaa-134">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="9acaa-134">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9acaa-135">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="9acaa-135">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="9acaa-136">PreventCriticalErrorDisplay</span><span class="sxs-lookup"><span data-stu-id="9acaa-136">PreventCriticalErrorDisplay</span></span>](/windows/client-management/mdm/policy-csp-errorreporting#errorreporting-preventcriticalerrordisplay)
</dt> <dd> <dl> <dt>

<span data-ttu-id="9acaa-137">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="9acaa-137">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="9acaa-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="9acaa-138">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9acaa-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9acaa-139">Requirements</span></span>



| <span data-ttu-id="9acaa-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9acaa-140">Requirement</span></span> | <span data-ttu-id="9acaa-141">Value</span><span class="sxs-lookup"><span data-stu-id="9acaa-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9acaa-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9acaa-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9acaa-143">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="9acaa-143">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="9acaa-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9acaa-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9acaa-145">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="9acaa-145">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="9acaa-146">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="9acaa-146">Namespace</span></span><br/>                | <span data-ttu-id="9acaa-147">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="9acaa-147">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="9acaa-148">MOF</span><span class="sxs-lookup"><span data-stu-id="9acaa-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9acaa-149"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9acaa-149"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="9acaa-150">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9acaa-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9acaa-151"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9acaa-151"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

