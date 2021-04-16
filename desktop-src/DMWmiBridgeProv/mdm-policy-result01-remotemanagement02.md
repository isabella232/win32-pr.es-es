---
title: MDM_Policy_Result01_RemoteManagement02 (clase)
description: La \_ clase Result01 de la Directiva MDM \_ \_ RemoteManagement02 representa las directivas de administración remota.
ms.assetid: f6eb96ff-a40e-4602-a812-786d1a89bf12
keywords:
- MDM_Policy_Result01_RemoteManagement02 (clase)
- MDM_Policy_Result01_RemoteManagement02 clase, descrita
topic_type:
- apiref
api_name:
- MDM_Policy_Result01_RemoteManagement02
- MDM_Policy_Result01_RemoteManagement02.InstanceID
- MDM_Policy_Result01_RemoteManagement02.ParentID
api_location:
- DMWmiBridgeProv.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0a60228e39c8e1d6604534c8bd052ec7d40105e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104489209"
---
# <a name="mdm_policy_result01_remotemanagement02-class"></a><span data-ttu-id="c182e-105">\_ \_ Clase RemoteManagement02 de Result01 de directivas MDM \_</span><span class="sxs-lookup"><span data-stu-id="c182e-105">MDM\_Policy\_Result01\_RemoteManagement02 class</span></span>

<span data-ttu-id="c182e-106">\[Algunos datos se relacionan con productos de versiones preliminares que pueden modificarse sustancialmente antes de su lanzamiento comercial.</span><span class="sxs-lookup"><span data-stu-id="c182e-106">\[Some information relates to pre-released product which may be substantially modified before it's commercially released.</span></span> <span data-ttu-id="c182e-107">Microsoft no ofrece ninguna garantía, expresa o implícita, con respecto a la información que se ofrece aquí.\]</span><span class="sxs-lookup"><span data-stu-id="c182e-107">Microsoft makes no warranties, express or implied, with respect to the information provided here.\]</span></span>

<span data-ttu-id="c182e-108">La \_ clase Result01 de la Directiva MDM \_ \_ RemoteManagement02 representa las directivas de administración remota.</span><span class="sxs-lookup"><span data-stu-id="c182e-108">The MDM\_Policy\_Result01\_RemoteManagement02 class represents the remote management policies.</span></span>

<span data-ttu-id="c182e-109">La siguiente sintaxis es código MOF simplificado e incluye todas las propiedades heredadas.</span><span class="sxs-lookup"><span data-stu-id="c182e-109">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="c182e-110">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c182e-110">Syntax</span></span>

``` syntax
[InPartition("local-system"), dynamic, provider("DMWmiBridgeProv")]
class MDM_Policy_Result01_RemoteManagement02
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

## <a name="members"></a><span data-ttu-id="c182e-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="c182e-111">Members</span></span>

<span data-ttu-id="c182e-112">La clase Result01 de la **\_ Directiva MDM \_ \_ RemoteManagement02** tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="c182e-112">The **MDM\_Policy\_Result01\_RemoteManagement02** class has these types of members:</span></span>

-   [<span data-ttu-id="c182e-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c182e-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c182e-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="c182e-114">Properties</span></span>

<span data-ttu-id="c182e-115">La **clase \_ \_ Result01 de \_ RemoteManagement02 de directivas MDM** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="c182e-115">The **MDM\_Policy\_Result01\_RemoteManagement02** class has these properties.</span></span>

<dl> <dt>

[<span data-ttu-id="c182e-116">Cliente de AllowBasicAuthentication \_</span><span class="sxs-lookup"><span data-stu-id="c182e-116">AllowBasicAuthentication\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-117">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-118">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c182e-118">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c182e-119">\_Servicio AllowBasicAuthentication</span><span class="sxs-lookup"><span data-stu-id="c182e-119">AllowBasicAuthentication\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowbasicauthentication-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-120">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-120">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-121">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c182e-121">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c182e-122">AllowCredSSPAuthenticationClient</span><span class="sxs-lookup"><span data-stu-id="c182e-122">AllowCredSSPAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-123">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-123">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-124">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c182e-124">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c182e-125">AllowCredSSPAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="c182e-125">AllowCredSSPAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowcredsspauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-126">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-127">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c182e-127">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c182e-128">AllowRemoteServerManagement</span><span class="sxs-lookup"><span data-stu-id="c182e-128">AllowRemoteServerManagement</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowremoteservermanagement)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-129">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-130">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c182e-130">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c182e-131">Cliente de AllowUnencryptedTraffic \_</span><span class="sxs-lookup"><span data-stu-id="c182e-131">AllowUnencryptedTraffic\_Client</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-client)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-132">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-132">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-133">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c182e-133">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c182e-134">\_Servicio AllowUnencryptedTraffic</span><span class="sxs-lookup"><span data-stu-id="c182e-134">AllowUnencryptedTraffic\_Service</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-allowunencryptedtraffic-service)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-135">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-136">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c182e-136">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c182e-137">DisallowDigestAuthentication</span><span class="sxs-lookup"><span data-stu-id="c182e-137">DisallowDigestAuthentication</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowdigestauthentication)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-138">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-139">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c182e-139">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c182e-140">DisallowNegotiateAuthenticationClient</span><span class="sxs-lookup"><span data-stu-id="c182e-140">DisallowNegotiateAuthenticationClient</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationclient)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-141">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-141">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-142">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c182e-142">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c182e-143">DisallowNegotiateAuthenticationService</span><span class="sxs-lookup"><span data-stu-id="c182e-143">DisallowNegotiateAuthenticationService</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallownegotiateauthenticationservice)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-144">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-144">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-145">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c182e-145">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c182e-146">DisallowStoringOfRunAsCredentials</span><span class="sxs-lookup"><span data-stu-id="c182e-146">DisallowStoringOfRunAsCredentials</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-disallowstoringofrunascredentials)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-147">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-148">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c182e-148">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c182e-149">**InstanceID**</span><span class="sxs-lookup"><span data-stu-id="c182e-149">**InstanceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-150">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-151">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c182e-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c182e-152">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c182e-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

<span data-ttu-id="c182e-153">**ParentID**</span><span class="sxs-lookup"><span data-stu-id="c182e-153">**ParentID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-154">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-154">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-155">Tipo de acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="c182e-155">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c182e-156">Calificadores: [ **clave**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="c182e-156">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c182e-157">SpecifyChannelBindingTokenHardeningLevel</span><span class="sxs-lookup"><span data-stu-id="c182e-157">SpecifyChannelBindingTokenHardeningLevel</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-specifychannelbindingtokenhardeninglevel)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-158">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-158">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-159">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c182e-159">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c182e-160">TrustedHosts</span><span class="sxs-lookup"><span data-stu-id="c182e-160">TrustedHosts</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-trustedhosts)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-161">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-161">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-162">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c182e-162">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c182e-163">TurnOnCompatibilityHTTPListener</span><span class="sxs-lookup"><span data-stu-id="c182e-163">TurnOnCompatibilityHTTPListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttplistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-164">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-164">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-165">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c182e-165">Access type: Read/write</span></span>
</dt> </dl>

</dd> <dt>

[<span data-ttu-id="c182e-166">TurnOnCompatibilityHTTPSListener</span><span class="sxs-lookup"><span data-stu-id="c182e-166">TurnOnCompatibilityHTTPSListener</span></span>](/windows/client-management/mdm/policy-csp-remotemanagement#remotemanagement-turnoncompatibilityhttpslistener)
</dt> <dd> <dl> <dt>

<span data-ttu-id="c182e-167">Tipo de datos: **cadena**</span><span class="sxs-lookup"><span data-stu-id="c182e-167">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="c182e-168">Tipo de acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="c182e-168">Access type: Read/write</span></span>
</dt> </dl>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c182e-169">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c182e-169">Requirements</span></span>



| <span data-ttu-id="c182e-170">Requisito</span><span class="sxs-lookup"><span data-stu-id="c182e-170">Requirement</span></span> | <span data-ttu-id="c182e-171">Value</span><span class="sxs-lookup"><span data-stu-id="c182e-171">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c182e-172">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c182e-172">Minimum supported client</span></span><br/> | <span data-ttu-id="c182e-173">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="c182e-173">Windows 10 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c182e-174">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c182e-174">Minimum supported server</span></span><br/> | <span data-ttu-id="c182e-175">No se admite ninguno</span><span class="sxs-lookup"><span data-stu-id="c182e-175">None supported</span></span><br/>                                                                      |
| <span data-ttu-id="c182e-176">Espacio de nombres</span><span class="sxs-lookup"><span data-stu-id="c182e-176">Namespace</span></span><br/>                | <span data-ttu-id="c182e-177">Dmmap de MDM raíz de \\ cimv2 \\ \\</span><span class="sxs-lookup"><span data-stu-id="c182e-177">Root\\cimv2\\mdm\\dmmap</span></span><br/>                                                             |
| <span data-ttu-id="c182e-178">MOF</span><span class="sxs-lookup"><span data-stu-id="c182e-178">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c182e-179"><dt>DMWmiBridgeProv. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c182e-179"><dt>DMWmiBridgeProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="c182e-180">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="c182e-180">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c182e-181"><dt>DMWmiBridgeProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c182e-181"><dt>DMWmiBridgeProv.dll</dt></span></span> </dl> |



 

