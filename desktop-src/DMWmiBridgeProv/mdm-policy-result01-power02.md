---
title: MDM_Policy_Result01_Power02 (clase)
description: La \_ clase Result01 de la Directiva MDM \_ \_ Power02 representa las directivas de energía.
ms.assetid: 1458228f-f442-4fd4-b402-e0a4c06ecaa5
keywords:
- MDM_Policy_Result01_Power02 (clase)
- MDM_Policy_Result01_Power02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_Power02
- MDM_Policy_Result01_Power02.InstanceID
- MDM_Policy_Result01_Power02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91635811e876500cb4d3df792067b1eba3d861b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996055"
---
# <a name="mdm_policy_result01_power02-class"></a><span data-ttu-id="c8b5b-105">\_ \_ Clase Power02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="c8b5b-105">MDM\_Policy\_Result01\_Power02 class</span></span>

<span data-ttu-id="c8b5b-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="c8b5b-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c8b5b-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="c8b5b-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c8b5b-108">La \_ clase Result01 de la Directiva MDM \_ \_ Power02 representa las directivas de energía.</span><span class="sxs-lookup"><span data-stu-id="c8b5b-108">The MDM\_Policy\_Result01\_Power02 class represents the power policies.</span></span>

<span data-ttu-id="c8b5b-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c8b5b-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c8b5b-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c8b5b-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_Power02
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

## <a name="members"></a><span data-ttu-id="c8b5b-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="c8b5b-111">Members</span></span>

<span data-ttu-id="c8b5b-112">La clase Result01 de la **\_ Directiva MDM \_ \_ Power02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c8b5b-112">The **MDM\_Policy\_Result01\_Power02** class has these types of members:</span></span>

-   [<span data-ttu-id="c8b5b-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c8b5b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c8b5b-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c8b5b-114">Properties</span></span>

<span data-ttu-id="c8b5b-115">La **clase \_ \_ Result01 de \_ Power02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c8b5b-115">The **MDM\_Policy\_Result01\_Power02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c8b5b-116">AllowStandbyWhenSleepingPluggedIn</span><span class="sxs-lookup"><span data-stu-id="c8b5b-116">AllowStandbyWhenSleepingPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-allowstandbywhensleepingpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b5b-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c8b5b-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8b5b-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c8b5b-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c8b5b-119">DisplayOffTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="c8b5b-119">DisplayOffTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b5b-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c8b5b-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8b5b-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c8b5b-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c8b5b-122">DisplayOffTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="c8b5b-122">DisplayOffTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-displayofftimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b5b-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c8b5b-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8b5b-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c8b5b-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c8b5b-125">HibernateTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="c8b5b-125">HibernateTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b5b-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c8b5b-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8b5b-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c8b5b-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c8b5b-128">HibernateTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="c8b5b-128">HibernateTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-hibernatetimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b5b-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c8b5b-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8b5b-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c8b5b-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c8b5b-131">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c8b5b-131">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b5b-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c8b5b-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8b5b-133">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c8b5b-133">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8b5b-134">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c8b5b-134">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c8b5b-135">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c8b5b-135">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b5b-136">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c8b5b-136">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8b5b-137">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c8b5b-137">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c8b5b-138">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c8b5b-138">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c8b5b-139">RequirePasswordWhenComputerWakesOnBattery</span><span class="sxs-lookup"><span data-stu-id="c8b5b-139">RequirePasswordWhenComputerWakesOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakesonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b5b-140">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c8b5b-140">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8b5b-141">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c8b5b-141">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c8b5b-142">RequirePasswordWhenComputerWakesPluggedIn</span><span class="sxs-lookup"><span data-stu-id="c8b5b-142">RequirePasswordWhenComputerWakesPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-requirepasswordwhencomputerwakespluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b5b-143">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c8b5b-143">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8b5b-144">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c8b5b-144">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c8b5b-145">StandbyTimeoutOnBattery</span><span class="sxs-lookup"><span data-stu-id="c8b5b-145">StandbyTimeoutOnBattery</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutonbattery)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b5b-146">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c8b5b-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8b5b-147">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c8b5b-147">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c8b5b-148">StandbyTimeoutPluggedIn</span><span class="sxs-lookup"><span data-stu-id="c8b5b-148">StandbyTimeoutPluggedIn</span></span>](/windows/client-management/mdm/policy-csp-power#power-standbytimeoutpluggedin)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c8b5b-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c8b5b-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c8b5b-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c8b5b-150">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c8b5b-151">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c8b5b-151">Requirements</span></span>



| <span data-ttu-id="c8b5b-152">Requisito</span><span class="sxs-lookup"><span data-stu-id="c8b5b-152">Requirement</span></span> | <span data-ttu-id="c8b5b-153">Value</span><span class="sxs-lookup"><span data-stu-id="c8b5b-153">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c8b5b-154">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8b5b-154">Minimum supported client</span></span><br/> | <span data-ttu-id="c8b5b-155">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="c8b5b-155">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c8b5b-156">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c8b5b-156">Minimum supported server</span></span><br/> | <span data-ttu-id="c8b5b-157">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c8b5b-157">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c8b5b-158">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c8b5b-158">Namespace</span></span><br/>                | <span data-ttu-id="c8b5b-159">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="c8b5b-159">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c8b5b-160">MOF</span><span class="sxs-lookup"><span data-stu-id="c8b5b-160">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c8b5b-161"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c8b5b-161"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c8b5b-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c8b5b-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c8b5b-163"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c8b5b-163"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

