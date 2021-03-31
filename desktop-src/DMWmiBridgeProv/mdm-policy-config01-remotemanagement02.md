---
title: MDM_Policy_Config01_RemoteManagement02 (clase)
description: Directiva de \_ MDM \_ Config01 \_ RemoteManagement02 directivas de administración remota.
ms.assetid: 2eabbf72-00a4-4c61-9ae1-ff49067cb502
keywords:
- MDM_Policy_Config01_RemoteManagement02 (clase)
- MDM_Policy_Config01_RemoteManagement02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Config01_RemoteManagement02
- MDM_Policy_Config01_RemoteManagement02.InstanceID
- MDM_Policy_Config01_RemoteManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a76aa1a04735897d0b1c8f0e16572dd124b601c2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905227"
---
# <a name="mdm_policy_config01_remotemanagement02-class"></a><span data-ttu-id="613fc-105">\_ \_ Clase RemoteManagement02 de Config01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="613fc-105">MDM\_Policy\_Config01\_RemoteManagement02 class</span></span>

<span data-ttu-id="613fc-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="613fc-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="613fc-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="613fc-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="613fc-108">Directiva de \_ MDM \_ Config01 \_ RemoteManagement02 directivas de administración remota.</span><span class="sxs-lookup"><span data-stu-id="613fc-108">The MDM\_Policy\_Config01\_RemoteManagement02 remote management policies.</span></span>

<span data-ttu-id="613fc-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="613fc-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="613fc-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="613fc-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Config01_RemoteManagement02
{
  string InstanceID;
  string ParentID;
  string AllowBasicAuthentication_Client;
  string AllowBasicAuthentication_Service;
  string AllowCredSSPAuthenticationClient;
  string AllowCredSSPAuthenticationService;
  string AllowRemoteServerManagement;
  string AllowUnencryptedTraffic_Client;
  string AllowUnencryptedTraffic_Service;
  string DisallowDigestAuthentication;
  string DisallowNegotiateAuthenticationClient;
  string DisallowNegotiateAuthenticationService;
  string DisallowStoringOfRunAsCredentials;
  string SpecifyChannelBindingTokenHardeningLevel;
  string TrustedHosts;
  string TurnOnCompatibilityHTTPListener;
  string TurnOnCompatibilityHTTPSListener;
};
```

## <a name="members"></a><span data-ttu-id="613fc-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="613fc-111">Members</span></span>

<span data-ttu-id="613fc-112">La clase Config01 de la **\_ Directiva MDM \_ \_ RemoteManagement02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="613fc-112">The **MDM\_Policy\_Config01\_RemoteManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="613fc-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="613fc-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="613fc-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="613fc-114">Properties</span></span>

<span data-ttu-id="613fc-115">La **clase \_ \_ Config01 de \_ RemoteManagement02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="613fc-115">The **MDM\_Policy\_Config01\_RemoteManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="613fc-116">Cliente de AllowBasicAuthentication \_</span><span class="sxs-lookup"><span data-stu-id="613fc-116">AllowBasicAuthentication\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613fc-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="613fc-119">\_Servicio AllowBasicAuthentication</span><span class="sxs-lookup"><span data-stu-id="613fc-119">AllowBasicAuthentication\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613fc-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="613fc-122">AllowCredSSPAuthenticationClient</span><span class="sxs-lookup"><span data-stu-id="613fc-122">AllowCredSSPAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613fc-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="613fc-125">AllowCredSSPAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="613fc-125">AllowCredSSPAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613fc-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="613fc-128">AllowRemoteServerManagement</span><span class="sxs-lookup"><span data-stu-id="613fc-128">AllowRemoteServerManagement</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowremoteservermanagement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613fc-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="613fc-131">Cliente de AllowUnencryptedTraffic \_</span><span class="sxs-lookup"><span data-stu-id="613fc-131">AllowUnencryptedTraffic\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613fc-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="613fc-134">\_Servicio AllowUnencryptedTraffic</span><span class="sxs-lookup"><span data-stu-id="613fc-134">AllowUnencryptedTraffic\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613fc-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="613fc-137">DisallowDigestAuthentication</span><span class="sxs-lookup"><span data-stu-id="613fc-137">DisallowDigestAuthentication</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowdigestauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613fc-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="613fc-140">DisallowNegotiateAuthenticationClient</span><span class="sxs-lookup"><span data-stu-id="613fc-140">DisallowNegotiateAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613fc-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="613fc-143">DisallowNegotiateAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="613fc-143">DisallowNegotiateAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613fc-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="613fc-146">DisallowStoringOfRunAsCredentials</span><span class="sxs-lookup"><span data-stu-id="613fc-146">DisallowStoringOfRunAsCredentials</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowstoringofrunascredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613fc-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="613fc-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="613fc-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613fc-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613fc-152">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="613fc-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="613fc-153">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="613fc-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="613fc-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="613fc-156">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="613fc-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="613fc-157">SpecifyChannelBindingTokenHardeningLevel</span><span class="sxs-lookup"><span data-stu-id="613fc-157">SpecifyChannelBindingTokenHardeningLevel</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-specifychannelbindingtokenhardeninglevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-159">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613fc-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="613fc-160">TrustedHosts</span><span class="sxs-lookup"><span data-stu-id="613fc-160">TrustedHosts</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-trustedhosts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-162">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613fc-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="613fc-163">TurnOnCompatibilityHTTPListener</span><span class="sxs-lookup"><span data-stu-id="613fc-163">TurnOnCompatibilityHTTPListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttplistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613fc-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="613fc-166">TurnOnCompatibilityHTTPSListener</span><span class="sxs-lookup"><span data-stu-id="613fc-166">TurnOnCompatibilityHTTPSListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttpslistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="613fc-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="613fc-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="613fc-168">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="613fc-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="613fc-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="613fc-169">Requirements</span></span>



| <span data-ttu-id="613fc-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="613fc-170">Requirement</span></span> | <span data-ttu-id="613fc-171">Value</span><span class="sxs-lookup"><span data-stu-id="613fc-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="613fc-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="613fc-172">Minimum supported client</span></span><br/> | <span data-ttu-id="613fc-173">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="613fc-173">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="613fc-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="613fc-174">Minimum supported server</span></span><br/> | <span data-ttu-id="613fc-175">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="613fc-175">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="613fc-176">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="613fc-176">Namespace</span></span><br/>                | <span data-ttu-id="613fc-177">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="613fc-177">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="613fc-178">MOF</span><span class="sxs-lookup"><span data-stu-id="613fc-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="613fc-179"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="613fc-179"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="613fc-180">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="613fc-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="613fc-181"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="613fc-181"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

