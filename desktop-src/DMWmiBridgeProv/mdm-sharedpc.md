---
title: MDM_SharedPC (clase)
description: La \_ clase SharedPC de MDM se usa para configurar las opciones de uso de equipos compartidos.
ms.assetid: 90985c4d-601e-4827-aee0-13524a69f759
keywords:
- MDM_SharedPC (clase)
- MDM_SharedPC clase, descrita
topic_type:
- apiref
api_name:
- MDM_SharedPC
- MDM_SharedPC.InstanceID
- MDM_SharedPC.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8c7b515e4b794e2048ab26c8e1a32bfe7d3c4b50
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104078902"
---
# <a name="mdm_sharedpc-class"></a><span data-ttu-id="2fcc2-105">\_Clase SharedPC de MDM</span><span class="sxs-lookup"><span data-stu-id="2fcc2-105">MDM\_SharedPC class</span></span>

<span data-ttu-id="2fcc2-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="2fcc2-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="2fcc2-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="2fcc2-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="2fcc2-108">La \_ clase SharedPC de MDM se usa para configurar las opciones de uso de equipos compartidos.</span><span class="sxs-lookup"><span data-stu-id="2fcc2-108">The MDM\_SharedPC class is used to configure settings for shared PC usage.</span></span>

<span data-ttu-id="2fcc2-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="2fcc2-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="2fcc2-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2fcc2-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv1")]
class MDM_SharedPC
{
  string  InstanceID;
  string  ParentID;
  boolean EnableSharedPCMode;
  boolean SetEduPolicies;
  boolean SetPowerPolicies;
  sint32  MaintenanceStartTime;
  boolean SignInOnResume;
  sint32  SleepTimeout;
  boolean EnableAccountManager;
  sint32  AccountModel;
  sint32  DeletionPolicy;
  sint32  DiskLevelDeletion;
  sint32  DiskLevelCaching;
  boolean RestrictLocalStorage;
  string  KioskModeAUMID;
  string  KioskModeUserTileDisplayText;
  sint32  InactiveThreshold;
  sint32  MaxPageFileSizeMB;
};
```

## <a name="members"></a><span data-ttu-id="2fcc2-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="2fcc2-111">Members</span></span>

<span data-ttu-id="2fcc2-112">La **clase \_ SharedPC de MDM** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="2fcc2-112">The **MDM\_SharedPC** class has these types of members:</span></span>

-   [<span data-ttu-id="2fcc2-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2fcc2-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2fcc2-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="2fcc2-114">Properties</span></span>

<span data-ttu-id="2fcc2-115">La **clase \_ SharedPC de MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="2fcc2-115">The **MDM\_SharedPC** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="2fcc2-116">AccountModel</span><span class="sxs-lookup"><span data-stu-id="2fcc2-116">AccountModel</span></span>](/windows/client-management/mdm/sharedpc-csp#accountmodel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-117">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-117">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-118">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fcc2-119">Para obtener más información, consulte [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="2fcc2-119">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="2fcc2-120">DeletionPolicy</span><span class="sxs-lookup"><span data-stu-id="2fcc2-120">DeletionPolicy</span></span>](/windows/client-management/mdm/sharedpc-csp#deletionpolicy)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-121">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-121">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-122">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-122">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fcc2-123">Para obtener más información, consulte [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="2fcc2-123">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="2fcc2-124">DiskLevelCaching</span><span class="sxs-lookup"><span data-stu-id="2fcc2-124">DiskLevelCaching</span></span>](/windows/client-management/mdm/sharedpc-csp#disklevelcaching)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-125">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-125">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-126">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-126">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fcc2-127">Para obtener más información, consulte [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="2fcc2-127">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="2fcc2-128">DiskLevelDeletion</span><span class="sxs-lookup"><span data-stu-id="2fcc2-128">DiskLevelDeletion</span></span>](/windows/client-management/mdm/sharedpc-csp#diskleveldeletion)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-129">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-129">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-130">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fcc2-131">Para obtener más información, consulte [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="2fcc2-131">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="2fcc2-132">EnableAccountManager</span><span class="sxs-lookup"><span data-stu-id="2fcc2-132">EnableAccountManager</span></span>](/windows/client-management/mdm/sharedpc-csp#enableaccountmanager)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-133">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-133">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-134">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-134">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fcc2-135">Para obtener más información, consulte [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="2fcc2-135">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="2fcc2-136">EnableSharedPCMode</span><span class="sxs-lookup"><span data-stu-id="2fcc2-136">EnableSharedPCMode</span></span>](/windows/client-management/mdm/sharedpc-csp#enablesharedpcmode)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-137">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-137">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-138">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-138">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fcc2-139">Para obtener más información, consulte [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="2fcc2-139">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="2fcc2-140">InactiveThreshold</span><span class="sxs-lookup"><span data-stu-id="2fcc2-140">InactiveThreshold</span></span>](/windows/client-management/mdm/sharedpc-csp#inactivethreshold)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-141">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-141">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-142">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fcc2-143">Para obtener más información, consulte [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="2fcc2-143">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

<span data-ttu-id="2fcc2-144">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-144">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-145">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-145">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-146">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-146">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-147">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2fcc2-147">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2fcc2-148">KioskModeAUMID</span><span class="sxs-lookup"><span data-stu-id="2fcc2-148">KioskModeAUMID</span></span>](/windows/client-management/mdm/sharedpc-csp#kioskmodeaumid)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-149">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-149">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-150">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-150">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fcc2-151">Para obtener más información, consulte [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="2fcc2-151">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="2fcc2-152">KioskModeUserTileDisplayText</span><span class="sxs-lookup"><span data-stu-id="2fcc2-152">KioskModeUserTileDisplayText</span></span>](/windows/client-management/mdm/sharedpc-csp#kioskmodeusertiledisplaytext)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-153">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-154">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-154">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fcc2-155">Para obtener más información, consulte [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="2fcc2-155">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="2fcc2-156">MaintenanceStartTime</span><span class="sxs-lookup"><span data-stu-id="2fcc2-156">MaintenanceStartTime</span></span>](/windows/client-management/mdm/sharedpc-csp#maintenancestarttime)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-157">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-157">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-158">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-158">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fcc2-159">Para obtener más información, consulte [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="2fcc2-159">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="2fcc2-160">MaxPageFileSizeMB</span><span class="sxs-lookup"><span data-stu-id="2fcc2-160">MaxPageFileSizeMB</span></span>](/windows/client-management/mdm/sharedpc-csp#maxpagefilesizemb)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-161">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-161">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-162">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-162">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fcc2-163">Para obtener más información, consulte [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="2fcc2-163">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

<span data-ttu-id="2fcc2-164">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-164">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-165">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-165">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-166">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-166">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-167">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="2fcc2-167">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="2fcc2-168">RestrictLocalStorage</span><span class="sxs-lookup"><span data-stu-id="2fcc2-168">RestrictLocalStorage</span></span>](/windows/client-management/mdm/sharedpc-csp#restrictlocalstorage)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-169">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-169">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-170">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-170">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fcc2-171">Para obtener más información, consulte [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="2fcc2-171">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="2fcc2-172">SetEduPolicies</span><span class="sxs-lookup"><span data-stu-id="2fcc2-172">SetEduPolicies</span></span>](/windows/client-management/mdm/sharedpc-csp#setedupolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-173">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-173">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-174">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-174">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fcc2-175">Para obtener más información, consulte [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="2fcc2-175">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="2fcc2-176">SetPowerPolicies</span><span class="sxs-lookup"><span data-stu-id="2fcc2-176">SetPowerPolicies</span></span>](/windows/client-management/mdm/sharedpc-csp#setpowerpolicies)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-177">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-177">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-178">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-178">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fcc2-179">Para obtener más información, consulte [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="2fcc2-179">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="2fcc2-180">SignInOnResume</span><span class="sxs-lookup"><span data-stu-id="2fcc2-180">SignInOnResume</span></span>](/windows/client-management/mdm/sharedpc-csp#signinonresume)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-181">Tipo de datos: **booleano**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-181">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-182">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-182">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fcc2-183">Para obtener más información, consulte [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="2fcc2-183">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> <dt>

[<span data-ttu-id="2fcc2-184">SleepTimeout</span><span class="sxs-lookup"><span data-stu-id="2fcc2-184">SleepTimeout</span></span>](/windows/client-management/mdm/sharedpc-csp#sleeptimeout)
</dt> <dd> <dl> <dt>

<span data-ttu-id="2fcc2-185">Tipo de datos: **sint32**</span><span class="sxs-lookup"><span data-stu-id="2fcc2-185">Data type: **sint32**</span></span>
</dt> <dt>

<span data-ttu-id="2fcc2-186">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="2fcc2-186">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="2fcc2-187">Para obtener más información, consulte [SHAREDPC CSP](/windows/client-management/mdm/sharedpc-csp).</span><span class="sxs-lookup"><span data-stu-id="2fcc2-187">For additional information, see [SharedPC CSP](/windows/client-management/mdm/sharedpc-csp).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="2fcc2-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2fcc2-188">Requirements</span></span>



| <span data-ttu-id="2fcc2-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="2fcc2-189">Requirement</span></span> | <span data-ttu-id="2fcc2-190">Value</span><span class="sxs-lookup"><span data-stu-id="2fcc2-190">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2fcc2-191">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fcc2-191">Minimum supported client</span></span><br/> | <span data-ttu-id="2fcc2-192">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="2fcc2-192">Windows 10 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2fcc2-193">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2fcc2-193">Minimum supported server</span></span><br/> | <span data-ttu-id="2fcc2-194">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="2fcc2-194">None supported</span></span><br/>                                                                       |
| <span data-ttu-id="2fcc2-195">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="2fcc2-195">Namespace</span></span><br/>                | <span data-ttu-id="2fcc2-196">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="2fcc2-196">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                              |
| <span data-ttu-id="2fcc2-197">MOF</span><span class="sxs-lookup"><span data-stu-id="2fcc2-197">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2fcc2-198"><dt>DMWmiBridgeProv1. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2fcc2-198"><dt>DMWmiBridgeProv1.mof</dt></span></span> </dl> |
| <span data-ttu-id="2fcc2-199">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2fcc2-199">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2fcc2-200"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2fcc2-200"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl>  |



 

