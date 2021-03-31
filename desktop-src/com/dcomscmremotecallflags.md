---
title: DCOMSCMRemoteCallFlags
description: Controla el comportamiento de las llamadas desde el administrador de control de servicios (DCOMSCM) DCOM local a un DCOMSCM remoto.
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- Valor del registro DCOMSCMRemoteCallFlags COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda58975e40ac6ac1633db8aa78f2c7636f9103
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "104078424"
---
# <a name="dcomscmremotecallflags"></a><span data-ttu-id="c531e-104">DCOMSCMRemoteCallFlags</span><span class="sxs-lookup"><span data-stu-id="c531e-104">DCOMSCMRemoteCallFlags</span></span>

<span data-ttu-id="c531e-105">Controla el comportamiento de las llamadas desde el administrador de control de servicios (DCOMSCM) DCOM local a un DCOMSCM remoto.</span><span class="sxs-lookup"><span data-stu-id="c531e-105">Controls the behavior of calls from the local DCOM Service Control Manager (DCOMSCM) to a remote DCOMSCM.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="c531e-106">Entrada del Registro</span><span class="sxs-lookup"><span data-stu-id="c531e-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a><span data-ttu-id="c531e-107">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c531e-107">Remarks</span></span>

<span data-ttu-id="c531e-108">Se trata de un valor de **Registro \_ DWORD** .</span><span class="sxs-lookup"><span data-stu-id="c531e-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="c531e-109">Value</span><span class="sxs-lookup"><span data-stu-id="c531e-109">Value</span></span> | <span data-ttu-id="c531e-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="c531e-110">Description</span></span>                                       |
|-------|---------------------------------------------------|
| <span data-ttu-id="c531e-111">0x1</span><span class="sxs-lookup"><span data-stu-id="c531e-111">0x1</span></span>   | <span data-ttu-id="c531e-112">**activación de DCOMSCM \_ \_ usar \_ todo \_ AUTHNSERVICES**</span><span class="sxs-lookup"><span data-stu-id="c531e-112">**DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES**</span></span>  |
| <span data-ttu-id="c531e-113">0x2</span><span class="sxs-lookup"><span data-stu-id="c531e-113">0x2</span></span>   | <span data-ttu-id="c531e-114">**activación de DCOMSCM no \_ \_ permitir \_ llamada no segura \_**</span><span class="sxs-lookup"><span data-stu-id="c531e-114">**DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL**</span></span> |
| <span data-ttu-id="c531e-115">0x4</span><span class="sxs-lookup"><span data-stu-id="c531e-115">0x4</span></span>   | <span data-ttu-id="c531e-116">**DCOMSCM \_ Resolve \_ usar \_ todo \_ AUTHNSERVICES**</span><span class="sxs-lookup"><span data-stu-id="c531e-116">**DCOMSCM\_RESOLVE\_USE\_ALL\_AUTHNSERVICES**</span></span>     |
| <span data-ttu-id="c531e-117">0x8</span><span class="sxs-lookup"><span data-stu-id="c531e-117">0x8</span></span>   | <span data-ttu-id="c531e-118">**DCOMSCM \_ resolver no \_ permitir \_ llamada no segura \_**</span><span class="sxs-lookup"><span data-stu-id="c531e-118">**DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL**</span></span>    |
| <span data-ttu-id="c531e-119">0x10</span><span class="sxs-lookup"><span data-stu-id="c531e-119">0x10</span></span>  | <span data-ttu-id="c531e-120">**DCOMSCM \_ ping \_ use \_ Mid \_ AUTHNSERVICE**</span><span class="sxs-lookup"><span data-stu-id="c531e-120">**DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE**</span></span>         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a><span data-ttu-id="c531e-121">DCOMSCM \_ Activation \_ use \_ All \_ AUTHNSERVICES Description</span><span class="sxs-lookup"><span data-stu-id="c531e-121">DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES Description</span></span>

<span data-ttu-id="c531e-122">Cuando el cliente emite una solicitud de activación que usa la configuración de seguridad predeterminada, el DCOMSCM local usa el servicio de autenticación Negotiate al hacer la llamada RPC de activación al DCOMSCM remoto.</span><span class="sxs-lookup"><span data-stu-id="c531e-122">When the client issues an activation request that uses the default security settings, the local DCOMSCM uses the Negotiate authentication service when making the activation RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="c531e-123">Si se produce un error en la llamada, el DCOMSCM local realiza la llamada RPC de activación sin seguridad.</span><span class="sxs-lookup"><span data-stu-id="c531e-123">If the call fails, the local DCOMSCM makes the activation RPC call using no security.</span></span>

<span data-ttu-id="c531e-124">**Windows Server 2003 y Windows XP/2000:** Si se produce un error en la llamada RPC de activación que usa el servicio de autenticación Negotiate, el DCOMSCM local realiza la llamada RPC de activación mediante Kerberos, NTLM u otros proveedores de seguridad configurados.</span><span class="sxs-lookup"><span data-stu-id="c531e-124">**Windows Server 2003 and Windows XP/2000:** If the activation RPC call that uses the Negotiate authentication service fails, the local DCOMSCM makes the activation RPC call using Kerberos, NTLM, or other configured security providers.</span></span> <span data-ttu-id="c531e-125">Si no funcionan los proveedores de seguridad, el DCOMSCM local realiza la llamada RPC de activación sin seguridad.</span><span class="sxs-lookup"><span data-stu-id="c531e-125">If no security providers work, the local DCOMSCM makes the activation RPC call using no security.</span></span>

<span data-ttu-id="c531e-126">Al establecer esta marca, se puede realizar el DCOMSCM local en Windows Vista o superior para que se comporte como sistemas anteriores a vista.</span><span class="sxs-lookup"><span data-stu-id="c531e-126">By setting this flag, the local DCOMSCM on Windows Vista or higher can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="c531e-127">No se recomienda establecer esta marca a menos que sea necesaria por motivos de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="c531e-127">It is not recommended to set this flag unless required for compatibility reasons.</span></span>

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a><span data-ttu-id="c531e-128">Activación de DCOMSCM no \_ \_ permitir \_ Descripción de llamada no segura \_</span><span class="sxs-lookup"><span data-stu-id="c531e-128">DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL Description</span></span>

<span data-ttu-id="c531e-129">Si se establece la marca de **activación DCOMSCM no \_ \_ permitir \_ \_ llamada no segura** , el DCOMSCM local no realiza una llamada RPC de activación no segura.</span><span class="sxs-lookup"><span data-stu-id="c531e-129">If the **DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL** flag is set, the local DCOMSCM does not make an unsecure activation RPC call.</span></span> <span data-ttu-id="c531e-130">Para permitir que los clientes realicen solicitudes de activación con una configuración de seguridad no predeterminada, especifique la estructura [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) al efectuar la solicitud de activación.</span><span class="sxs-lookup"><span data-stu-id="c531e-130">To enable clients to make activation requests with non-default security settings, specify the [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) structure when making the activation request.</span></span> <span data-ttu-id="c531e-131">En este caso, se omiten las marcas de activación **DCOMSCM \_ \_ use \_ All \_ AUTHNSERVICES** y **DCOMSCM \_ Activate \_ Disallow \_ insecure \_ Call** Flags.</span><span class="sxs-lookup"><span data-stu-id="c531e-131">In this case, the **DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES** and **DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL** flags are ignored.</span></span>

<span data-ttu-id="c531e-132">No se recomienda establecer esta marca a menos que todos los clientes y servidores de la red se autentiquen por completo.</span><span class="sxs-lookup"><span data-stu-id="c531e-132">It is not recommended to set this flag unless all the clients and servers in the network are fully authenticated.</span></span>

## <a name="dcomscm_resolve_use_all_authnservices-description"></a><span data-ttu-id="c531e-133">DCOMSCM \_ resolver \_ uso de \_ toda la descripción de \_ AUTHNSERVICES</span><span class="sxs-lookup"><span data-stu-id="c531e-133">DCOMSCM\_RESOLVE\_USE\_ALL\_AUTHNSERVICES Description</span></span>

<span data-ttu-id="c531e-134">Cuando el cliente no calcula las referencias de una referencia de objeto, el DCOMSCM local usa el servicio de autenticación Negotiate al hacer la llamada RPC de resolución de OXID al DCOMSCM remoto.</span><span class="sxs-lookup"><span data-stu-id="c531e-134">When the client unmarshals an object reference, the local DCOMSCM uses the Negotiate authentication service when making the OXID Resolution RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="c531e-135">Si se produce un error en la llamada, el DCOMSCM local realiza la llamada RPC de resolución de OXID sin seguridad.</span><span class="sxs-lookup"><span data-stu-id="c531e-135">If the call fails, the local DCOMSCM makes the OXID Resolution RPC call using no security.</span></span>

<span data-ttu-id="c531e-136">**Windows Server 2003 y Windows XP/2000:** Si se produce un error en la llamada RPC de resolución de OXID mediante el servicio de autenticación Negotiate, el DCOMSCM local realiza la llamada RPC de resolución OXID mediante Kerberos, NTLM u otros proveedores de seguridad configurados.</span><span class="sxs-lookup"><span data-stu-id="c531e-136">**Windows Server 2003 and Windows XP/2000:** If the OXID Resolution RPC call using the Negotiate authentication service fails, the local DCOMSCM makes the OXID Resolution RPC call by using Kerberos, NTLM, or other configured security providers.</span></span> <span data-ttu-id="c531e-137">Si no funcionan los proveedores de seguridad, el DCOMSCM local realiza la llamada RPC de resolución de OXID sin seguridad.</span><span class="sxs-lookup"><span data-stu-id="c531e-137">If no security providers work, then the local DCOMSCM makes the OXID Resolution RPC call using no security.</span></span>

<span data-ttu-id="c531e-138">Al establecer esta marca, se puede realizar el DCOMSCM local en Windows Vista o superior para que se comporte como sistemas anteriores a vista.</span><span class="sxs-lookup"><span data-stu-id="c531e-138">By setting this flag, the local DCOMSCM on Windows Vista or higher can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="c531e-139">No se recomienda establecer esta marca a menos que sea necesaria por motivos de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="c531e-139">It is not recommended to set this flag unless required for compatibility reasons.</span></span>

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a><span data-ttu-id="c531e-140">DCOMSCM \_ Resolve \_ denegar la descripción de la \_ llamada no segura \_</span><span class="sxs-lookup"><span data-stu-id="c531e-140">DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL Description</span></span>

<span data-ttu-id="c531e-141">Si está establecida la marca de **DCOMSCM \_ resolver \_ denegar \_ \_ llamada no segura** , el DCOMSCM local no realiza una llamada RPC de resolución de Oxid no segura.</span><span class="sxs-lookup"><span data-stu-id="c531e-141">If the **DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL** flag is set, the local DCOMSCM does not make an unsecure OXID Resolution RPC call.</span></span> <span data-ttu-id="c531e-142">Además, el DCOMSCM local no hace que una llamada RPC de ping de recolección de elementos no utilizados no sea segura.</span><span class="sxs-lookup"><span data-stu-id="c531e-142">In addition, the local DCOMSCM does not make an unsecure garbage collection Ping RPC call.</span></span> <span data-ttu-id="c531e-143">No se recomienda establecer esta marca a menos que todos los clientes y servidores de la red se autentiquen por completo.</span><span class="sxs-lookup"><span data-stu-id="c531e-143">It is not recommended to set this flag unless all the clients and servers in the network are fully authenticated.</span></span>

## <a name="dcomscm_ping_use_mid_authnservice-description"></a><span data-ttu-id="c531e-144">DCOMSCM \_ ping \_ usar \_ Mid \_ AUTHNSERVICE Descripción</span><span class="sxs-lookup"><span data-stu-id="c531e-144">DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE Description</span></span>

<span data-ttu-id="c531e-145">El DCOMSCM local usa el servicio de autenticación Negotiate al hacer que la llamada RPC de ping de recolección de elementos no utilizados se realice en el DCOMSCM remoto.</span><span class="sxs-lookup"><span data-stu-id="c531e-145">The local DCOMSCM uses the Negotiate authentication service when making the garbage-collection Ping RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="c531e-146">Si se produce un error en la llamada, el DCOMSCM local realiza la llamada RPC de ping de recolección de elementos no utilizados sin seguridad.</span><span class="sxs-lookup"><span data-stu-id="c531e-146">If the call fails, the local DCOMSCM makes the garbage-collection Ping RPC call using no security.</span></span>

<span data-ttu-id="c531e-147">**Windows Server 2003 y Windows XP/2000:** Si se produce un error en la llamada RPC de ping de recolección de elementos no utilizados con el servicio de autenticación Negotiate, el DCOMSCM local hace que la llamada RPC ping de la recolección de elementos no utilizados use Kerberos, NTLM y otros proveedores de seguridad configurados.</span><span class="sxs-lookup"><span data-stu-id="c531e-147">**Windows Server 2003 and Windows XP/2000:** If the garbage-collection Ping RPC call using the Negotiate authentication service fails, the local DCOMSCM makes the garbage collection Ping RPC call by using Kerberos, NTLM, and other configured security providers.</span></span> <span data-ttu-id="c531e-148">Si no funcionan los proveedores de seguridad, el DCOMSCM local hace que la llamada RPC del ping de recolección de elementos no utilizados no sea de seguridad.</span><span class="sxs-lookup"><span data-stu-id="c531e-148">If no security providers work, then the local DCOMSCM makes the garbage collection Ping RPC call using no security.</span></span>

<span data-ttu-id="c531e-149">Al establecer esta marca, se puede hacer que el DCOMSCM local en Windows Vista o superior se comporte como sistemas anteriores a vista.</span><span class="sxs-lookup"><span data-stu-id="c531e-149">By setting this flag, the local DCOMSCM on Windows Vista or above can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="c531e-150">No se recomienda establecer la marca **DCOMSCM \_ ping \_ use \_ Mid \_ AUTHNSERVICE** a menos que sea necesario por motivos de compatibilidad.</span><span class="sxs-lookup"><span data-stu-id="c531e-150">It is not recommended to set the **DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE** flag unless required for compatibility reasons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c531e-151">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c531e-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c531e-152">Autenticación para conexiones remotas</span><span class="sxs-lookup"><span data-stu-id="c531e-152">Authentication for Remote Connections</span></span>](/windows/desktop/WinRM/authentication-for-remote-connections)
</dt> <dt>

[<span data-ttu-id="c531e-153">EnableDCOM</span><span class="sxs-lookup"><span data-stu-id="c531e-153">EnableDCOM</span></span>](enabledcom.md)
</dt> <dt>

[<span data-ttu-id="c531e-154">Registrar servidores COM</span><span class="sxs-lookup"><span data-stu-id="c531e-154">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="c531e-155">Seguridad en COM</span><span class="sxs-lookup"><span data-stu-id="c531e-155">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 