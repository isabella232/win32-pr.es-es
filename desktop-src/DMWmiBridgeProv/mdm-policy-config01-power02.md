---
title: MDM_Policy_Config01_Power02 (clase)
description: La \_ clase Config01 de Power02 de directivas MDM \_ \_ configura las directivas de energía.
ms.assetid: 8913c38c-0d8d-456f-a412-d47c2ccd5d13
keywords:
- MDM_Policy_Config01_Power02 (clase)
- MDM_Policy_Config01_Power02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_Power02
- MDM_Policy_Config01_Power02.InstanceID
- MDM_Policy_Config01_Power02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6c9bdda57bbd85100e8bccb87990d928f448a972
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150261"
---
# <a name="mdm_policy_config01_power02-class"></a><span data-ttu-id="f6318-105">\_ \_ Clase Power02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="f6318-105">MDM\_Policy\_Config01\_Power02 class</span></span>

<span data-ttu-id="f6318-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="f6318-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="f6318-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="f6318-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="f6318-108">La \_ clase Config01 de Power02 de directivas MDM \_ \_ configura las directivas de energía.</span><span class="sxs-lookup"><span data-stu-id="f6318-108">The MDM\_Policy\_Config01\_Power02 class configures the power policies.</span></span>

<span data-ttu-id="f6318-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="f6318-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f6318-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f6318-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_Power02
{
  string InstanceID;
  string ParentID;
  string AllowStandbyWhenSleepingPluggedIn;
  string HibernateTimeoutPluggedIn;
  string HibernateTimeoutOnBattery;
  string DisplayOffTimeoutPluggedIn;
  string DisplayOffTimeoutOnBattery;
  string RequirePasswordWhenComputerWakesOnBattery;
  string RequirePasswordWhenComputerWakesPluggedIn;
  string StandbyTimeoutPluggedIn;
  string StandbyTimeoutOnBattery;
};
```

## <a name="members"></a><span data-ttu-id="f6318-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="f6318-111">Members</span></span>

<span data-ttu-id="f6318-112">La clase Config01 de la **\_ Directiva MDM \_ \_ Power02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="f6318-112">The **MDM\_Policy\_Config01\_Power02** class has these types of members:</span></span>

-   [<span data-ttu-id="f6318-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6318-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f6318-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="f6318-114">Properties</span></span>

<span data-ttu-id="f6318-115">La **clase \_ \_ Config01 de \_ Power02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="f6318-115">The **MDM\_Policy\_Config01\_Power02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="f6318-116">AllowStandbyWhenSleepingPluggedIn</span><span class="sxs-lookup"><span data-stu-id="f6318-116">AllowStandbyWhenSleepingPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-allowstandbywhensleepingpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6318-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6318-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6318-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f6318-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f6318-119">DisplayOffTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="f6318-119">DisplayOffTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6318-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6318-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6318-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f6318-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f6318-122">DisplayOffTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="f6318-122">DisplayOffTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6318-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6318-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6318-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f6318-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f6318-125">HibernateTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="f6318-125">HibernateTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6318-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6318-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6318-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f6318-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f6318-128">HibernateTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="f6318-128">HibernateTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6318-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6318-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6318-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f6318-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f6318-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="f6318-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6318-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6318-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6318-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6318-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6318-134">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f6318-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="f6318-135">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="f6318-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6318-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6318-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6318-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="f6318-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f6318-138">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="f6318-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f6318-139">RequirePasswordWhenComputerWakesOnBattery</span><span class="sxs-lookup"><span data-stu-id="f6318-139">RequirePasswordWhenComputerWakesOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakesonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6318-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6318-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6318-141">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f6318-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f6318-142">RequirePasswordWhenComputerWakesPluggedIn</span><span class="sxs-lookup"><span data-stu-id="f6318-142">RequirePasswordWhenComputerWakesPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakespluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6318-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6318-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6318-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f6318-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f6318-145">StandbyTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="f6318-145">StandbyTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6318-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6318-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6318-147">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f6318-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="f6318-148">StandbyTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="f6318-148">StandbyTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="f6318-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="f6318-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="f6318-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="f6318-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f6318-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f6318-151">Requirements</span></span>



| <span data-ttu-id="f6318-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="f6318-152">Requirement</span></span> | <span data-ttu-id="f6318-153">Value</span><span class="sxs-lookup"><span data-stu-id="f6318-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f6318-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6318-154">Minimum supported client</span></span><br/> | <span data-ttu-id="f6318-155">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="f6318-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f6318-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f6318-156">Minimum supported server</span></span><br/> | <span data-ttu-id="f6318-157">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="f6318-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="f6318-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="f6318-158">Namespace</span></span><br/>                | <span data-ttu-id="f6318-159">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="f6318-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="f6318-160">MOF</span><span class="sxs-lookup"><span data-stu-id="f6318-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f6318-161"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f6318-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="f6318-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f6318-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f6318-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f6318-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

