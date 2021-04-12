---
title: Constantes de autenticación (WSManDisp. h)
description: Especifique el método de autenticación y cómo controlar los servidores de certificados para el transporte HTTPS de solicitudes.
ms.assetid: adfefbc9-c386-48db-a0c2-145aa4f91bfa
ms.tgt_platform: multiple
topic_type:
- apiref
api_name:
- WSManFlagCredUsernamePassword
- WSManFlagSkipCACheck
- WSManFlagSkipCNCheck
- WSManFlagUseNoAuthentication
- WSManFlagUseDigest
- WSManFlagUseNegotiate
- WSManFlagUseBasic
- WSManFlagUseKerberos
- WSManFlagNoEncryption
- WSManFlagUseClientCertificate
- WSManFlagUseCredSsp
- WSManFlagSkipRevocationCheck
- WSManFlagAllowNegotiateImplicitCredentials
- WSManFlagUseSsl
api_location:
- WSManDisp.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce45d1474cf6c925149c05ae348231333c3356e6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104535158"
---
# <a name="authentication-constants"></a><span data-ttu-id="88c94-103">Constantes de autenticación</span><span class="sxs-lookup"><span data-stu-id="88c94-103">Authentication Constants</span></span>

<span data-ttu-id="88c94-104">Las constantes de autenticación son constantes en la enumeración **\_ \_ WSManSessionFlags** que especifican el método de autenticación y cómo controlar los servidores de certificados para el transporte https de las solicitudes.</span><span class="sxs-lookup"><span data-stu-id="88c94-104">Authentication constants are constants in the **\_\_WSManSessionFlags** enumeration that specify the authentication method and how to handle certificate servers for HTTPS transport of requests.</span></span>

<span data-ttu-id="88c94-105">Una o varias de las constantes enumeradas en la lista siguiente son necesarias en el parámetro *Flags* en las llamadas a [**WSMan. createSession**](wsman-createsession.md) o en [**IWSMan:: createSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) llamadas que se conectan a un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="88c94-105">One or more of the constants listed in the following list are required in the *flags* parameter in calls to [**WSMan.CreateSession**](wsman-createsession.md) or in [**IWSMan::CreateSession**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsman-createsession) calls that connect to a remote computer.</span></span>

<dl> <dt>

<span data-ttu-id="88c94-106"><span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**</span><span class="sxs-lookup"><span data-stu-id="88c94-106"><span id="WSManFlagCredUsernamePassword"></span><span id="wsmanflagcredusernamepassword"></span><span id="WSMANFLAGCREDUSERNAMEPASSWORD"></span>**WSManFlagCredUsernamePassword**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c94-107">4096 (0x1000)</span><span class="sxs-lookup"><span data-stu-id="88c94-107">4096 (0x1000)</span></span>
</dt> <dt>



<span data-ttu-id="88c94-108">Use el nombre de usuario y la contraseña como credenciales.</span><span class="sxs-lookup"><span data-stu-id="88c94-108">Use the user name and password as the credentials.</span></span> <span data-ttu-id="88c94-109">Establezca esta marca cuando cree un objeto [**ConnectionOptions**](connectionoptions.md) y proporcione el [**nombre de usuario**](connectionoptions-username.md) y la [**contraseña**](connectionoptions-password.md).</span><span class="sxs-lookup"><span data-stu-id="88c94-109">Set this flag when you create a [**ConnectionOptions**](connectionoptions.md) object and supply [**Username**](connectionoptions-username.md) and [**Password**](connectionoptions-password.md).</span></span> <span data-ttu-id="88c94-110">Las credenciales pueden ser una cuenta de dominio o una cuenta en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="88c94-110">The credentials can be a domain account or an account on the local computer.</span></span> <span data-ttu-id="88c94-111">De forma predeterminada, la cuenta debe ser miembro del grupo Administradores local en el equipo local o remoto.</span><span class="sxs-lookup"><span data-stu-id="88c94-111">By default, the account must be a member of the local Administrators group on the local or remote computer.</span></span> <span data-ttu-id="88c94-112">Sin embargo, el servicio WinRM se puede configurar para permitir a otros usuarios.</span><span class="sxs-lookup"><span data-stu-id="88c94-112">However, the WinRM service can be configured to allow other users.</span></span> <span data-ttu-id="88c94-113">Para obtener más información, vea [instalación y configuración de administración remota de Windows](installation-and-configuration-for-windows-remote-management.md).</span><span class="sxs-lookup"><span data-stu-id="88c94-113">For more information, see [Installation and Configuration for Windows Remote Management](installation-and-configuration-for-windows-remote-management.md).</span></span> <span data-ttu-id="88c94-114">Puede establecer esta marca cuando especifique las credenciales para negociar la autenticación (también conocida como [*autenticación integrada de Windows*](windows-remote-management-glossary.md)) o para la [*autenticación básica*](windows-remote-management-glossary.md).</span><span class="sxs-lookup"><span data-stu-id="88c94-114">You can set this flag when you specify credentials for Negotiate authentication (also known as [*Windows Integrated Authentication*](windows-remote-management-glossary.md)) or for [*Basic authentication*](windows-remote-management-glossary.md).</span></span>

<span data-ttu-id="88c94-115">El método de scripting asociado es [**WSMan. SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md)y el método de C++ es [**IWSManEx. SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).</span><span class="sxs-lookup"><span data-stu-id="88c94-115">The associated scripting method is [**WSMan.SessionFlagCredUsernamePassword**](wsman-sessionflagcredusernamepassword.md), and the C++ method is [**IWSManEx.SessionFlagCredUsernamePassword**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagcredusernamepassword).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88c94-116"><span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**</span><span class="sxs-lookup"><span data-stu-id="88c94-116"><span id="WSManFlagSkipCACheck"></span><span id="wsmanflagskipcacheck"></span><span id="WSMANFLAGSKIPCACHECK"></span>**WSManFlagSkipCACheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c94-117">8192 (0x2000)</span><span class="sxs-lookup"><span data-stu-id="88c94-117">8192 (0x2000)</span></span>
</dt> <dt>



<span data-ttu-id="88c94-118">Al conectarse a través de HTTPS, el cliente no valida que el certificado de servidor está firmado por una entidad de certificación (CA) de confianza.</span><span class="sxs-lookup"><span data-stu-id="88c94-118">When connecting over HTTPS, the client does not validate that the server certificate is signed by a trusted certification authority (CA).</span></span> <span data-ttu-id="88c94-119">Use este valor solo si el equipo remoto es de confianza por otros medios, por ejemplo, si el equipo remoto forma parte de una red que es físicamente segura y está aislada, o el equipo remoto aparece como un host de confianza en la configuración de WinRM.</span><span class="sxs-lookup"><span data-stu-id="88c94-119">Use this value only when the remote computer is trusted by other means, for example, if the remote computer is part of a network that is physically secure and isolated or the remote computer is listed as a trusted host in the WinRM configuration.</span></span>

<span data-ttu-id="88c94-120">El método de scripting asociado es [**WSMan. SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md)y el método de C++ es [**IWSManEx. SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).</span><span class="sxs-lookup"><span data-stu-id="88c94-120">The associated scripting method is [**WSMan.SessionFlagSkipCACheck**](wsman-sessionflagskipcacheck.md), and the C++ method is [**IWSManEx.SessionFlagSkipCACheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcacheck).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88c94-121"><span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**</span><span class="sxs-lookup"><span data-stu-id="88c94-121"><span id="WSManFlagSkipCNCheck"></span><span id="wsmanflagskipcncheck"></span><span id="WSMANFLAGSKIPCNCHECK"></span>**WSManFlagSkipCNCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c94-122">16384 (0x4000)</span><span class="sxs-lookup"><span data-stu-id="88c94-122">16384 (0x4000)</span></span>
</dt> <dt>



<span data-ttu-id="88c94-123">Al conectarse a través de HTTPS, el cliente no validará que el nombre común (CN) del certificado de servidor coincida con el nombre del equipo en la cadena de conexión.</span><span class="sxs-lookup"><span data-stu-id="88c94-123">When connecting over HTTPS, the client will not validate that the common name (CN) in the server certificate matches the computer name in the connection string.</span></span> <span data-ttu-id="88c94-124">Use solo cuando el equipo remoto sea de confianza por otros medios, por ejemplo, si el equipo remoto forma parte de una red que es físicamente segura y aislada, o el equipo remoto aparece como un host de confianza en la configuración de WinRM.</span><span class="sxs-lookup"><span data-stu-id="88c94-124">Use only when the remote computer is trusted by other means, for example, if the remote computer is part of a network that is physically secure and isolated or the remote computer is listed as a trusted host in the WinRM configuration.</span></span>

<span data-ttu-id="88c94-125">El método de scripting asociado es [**WSMan. SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md)y el método de C++ es [**IWSManEx. SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).</span><span class="sxs-lookup"><span data-stu-id="88c94-125">The associated scripting method is [**WSMan.SessionFlagSkipCNCheck**](wsman-sessionflagskipcncheck.md), and the C++ method is [**IWSManEx.SessionFlagSkipCNCheck**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagskipcncheck).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88c94-126"><span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**</span><span class="sxs-lookup"><span data-stu-id="88c94-126"><span id="WSManFlagUseNoAuthentication"></span><span id="wsmanflagusenoauthentication"></span><span id="WSMANFLAGUSENOAUTHENTICATION"></span>**WSManFlagUseNoAuthentication**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c94-127">32768 (0x8000)</span><span class="sxs-lookup"><span data-stu-id="88c94-127">32768 (0x8000)</span></span>
</dt> <dt>



<span data-ttu-id="88c94-128">No usar autenticación.</span><span class="sxs-lookup"><span data-stu-id="88c94-128">Use no authentication.</span></span> <span data-ttu-id="88c94-129">Especifique esta constante al probar una conexión a un equipo remoto para determinar si un servicio que implementa el protocolo WS-Management está configurado para escuchar solicitudes de datos.</span><span class="sxs-lookup"><span data-stu-id="88c94-129">Specify this constant when testing a connection to a remote computer to determine if a service that implements the WS-Management protocol is configured to listen for data requests.</span></span> <span data-ttu-id="88c94-130">**WSManFlagUseNoAuthentication** no se puede combinar con ninguna otra constante de [**sesión**](session.md) .</span><span class="sxs-lookup"><span data-stu-id="88c94-130">**WSManFlagUseNoAuthentication** cannot be combined with any other [**Session**](session.md) constant.</span></span> <span data-ttu-id="88c94-131">El método de scripting asociado es [**WSMan. SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md)y el método de C++ es [**WSManEx. SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).</span><span class="sxs-lookup"><span data-stu-id="88c94-131">The associated scripting method is [**WSMan.SessionFlagUseNoAuthentication**](wsman-sessionflagusenoauthentication.md), and the C++ method is [**WSManEx.SessionFlagUseNoAuthentication**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenoauthentication).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88c94-132"><span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**</span><span class="sxs-lookup"><span data-stu-id="88c94-132"><span id="WSManFlagUseDigest"></span><span id="wsmanflagusedigest"></span><span id="WSMANFLAGUSEDIGEST"></span>**WSManFlagUseDigest**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c94-133">65536 (0x10000)</span><span class="sxs-lookup"><span data-stu-id="88c94-133">65536 (0x10000)</span></span>
</dt> <dt>



<span data-ttu-id="88c94-134">Usar autenticación implícita.</span><span class="sxs-lookup"><span data-stu-id="88c94-134">Use Digest authentication.</span></span> <span data-ttu-id="88c94-135">Solo el equipo cliente puede iniciar una solicitud de autenticación Implícita.</span><span class="sxs-lookup"><span data-stu-id="88c94-135">Only the client computer can initiate a Digest authentication request.</span></span> <span data-ttu-id="88c94-136">El cliente envía una solicitud al servidor para autenticar y recibe una cadena de token del servidor.</span><span class="sxs-lookup"><span data-stu-id="88c94-136">The client sends a request to the server to authenticate and receives a token string from the server.</span></span> <span data-ttu-id="88c94-137">Después, el cliente envía la solicitud de recurso, incluido el nombre de usuario y un hash criptográfico de la contraseña combinada con la cadena de token.</span><span class="sxs-lookup"><span data-stu-id="88c94-137">The client then sends the resource request, including the user name and a cryptographic hash of the password combined with the token string.</span></span> <span data-ttu-id="88c94-138">La autenticación implícita es compatible con HTTP y HTTPS.</span><span class="sxs-lookup"><span data-stu-id="88c94-138">Digest authentication is supported for HTTP and HTTPS.</span></span> <span data-ttu-id="88c94-139">Las aplicaciones y scripts de cliente de WinRM pueden especificar la autenticación implícita, pero no el servicio.</span><span class="sxs-lookup"><span data-stu-id="88c94-139">WinRM client scripts and applications can specify Digest authentication, but not the service.</span></span>

<span data-ttu-id="88c94-140">El método de scripting asociado es [**WSMan. SessionFlagUseDigest**](wsman-sessionflagusedigest.md)y el método de C++ es [**IWSManEx. SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).</span><span class="sxs-lookup"><span data-stu-id="88c94-140">The associated scripting method is [**WSMan.SessionFlagUseDigest**](wsman-sessionflagusedigest.md), and the C++ method is [**IWSManEx.SessionFlagUseDigest**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusedigest).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88c94-141"><span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**</span><span class="sxs-lookup"><span data-stu-id="88c94-141"><span id="WSManFlagUseNegotiate"></span><span id="wsmanflagusenegotiate"></span><span id="WSMANFLAGUSENEGOTIATE"></span>**WSManFlagUseNegotiate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c94-142">131072 (0x20000)</span><span class="sxs-lookup"><span data-stu-id="88c94-142">131072 (0x20000)</span></span>
</dt> <dt>



<span data-ttu-id="88c94-143">Use negociar autenticación.</span><span class="sxs-lookup"><span data-stu-id="88c94-143">Use Negotiate authentication.</span></span> <span data-ttu-id="88c94-144">El cliente envía una solicitud al servidor para realizar la autenticación.</span><span class="sxs-lookup"><span data-stu-id="88c94-144">The client sends a request to the server to authenticate.</span></span> <span data-ttu-id="88c94-145">El servidor determina si se usa Kerberos o NTLM.</span><span class="sxs-lookup"><span data-stu-id="88c94-145">The server determines whether to use Kerberos or NTLM.</span></span> <span data-ttu-id="88c94-146">Kerberos está seleccionado para autenticar una cuenta de dominio y se ha seleccionado NTLM para las cuentas de equipo local.</span><span class="sxs-lookup"><span data-stu-id="88c94-146">Kerberos is selected to authenticate a domain account and NTLM is selected for local computer accounts.</span></span> <span data-ttu-id="88c94-147">El nombre de usuario debe especificarse con el formato dominio \\ nombreDeUsuario para un usuario de dominio o \\ nombre de usuario ServerName para un usuario local en un equipo servidor.</span><span class="sxs-lookup"><span data-stu-id="88c94-147">The user name should be specified in the form domain\\username for a domain user or servername\\username for a local user on a server computer.</span></span>

<span data-ttu-id="88c94-148">[Control de cuentas de usuario (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) afecta al acceso al servicio WinRM.</span><span class="sxs-lookup"><span data-stu-id="88c94-148">[User Account Control (UAC)](https://support.microsoft.com/help/922708/how-to-use-user-account-control-uac-in-windows-vista) affects access to the WinRM service.</span></span> <span data-ttu-id="88c94-149">Cuando se usa Negotiate Authentication en un grupo de trabajo o un dominio, solo la cuenta de administrador integrada puede tener acceso al servicio.</span><span class="sxs-lookup"><span data-stu-id="88c94-149">When Negotiate authentication is used in a workgroup or domain, only the built-in Administrator account can access the service.</span></span> <span data-ttu-id="88c94-150">Para permitir que todas las cuentas del grupo administradores tengan acceso al servicio, establezca la siguiente clave del registro en 1: **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Policies \\ System \\ LocalAccountTokenFilterPolicy**.</span><span class="sxs-lookup"><span data-stu-id="88c94-150">To allow all accounts in the Administrators group to access the service, set the following registry key to 1: **HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Windows\\CurrentVersion\\Policies\\system\\LocalAccountTokenFilterPolicy**.</span></span>

<span data-ttu-id="88c94-151">El método de scripting asociado es [**WSMan. SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md)y el método de C++ es [**IWSManEx. SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).</span><span class="sxs-lookup"><span data-stu-id="88c94-151">The associated scripting method is [**WSMan.SessionFlagUseNegotiate**](wsman-sessionflagusenegotiate.md), and the C++ method is [**IWSManEx.SessionFlagUseNegotiate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusenegotiate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88c94-152"><span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**</span><span class="sxs-lookup"><span data-stu-id="88c94-152"><span id="WSManFlagUseBasic"></span><span id="wsmanflagusebasic"></span><span id="WSMANFLAGUSEBASIC"></span>**WSManFlagUseBasic**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c94-153">262144 (0x40000)</span><span class="sxs-lookup"><span data-stu-id="88c94-153">262144 (0x40000)</span></span>
</dt> <dt>



<span data-ttu-id="88c94-154">Use la autenticación básica.</span><span class="sxs-lookup"><span data-stu-id="88c94-154">Use Basic authentication.</span></span> <span data-ttu-id="88c94-155">El cliente presenta las credenciales en forma de nombre de usuario y contraseña, que se transmiten directamente en el mensaje de solicitud.</span><span class="sxs-lookup"><span data-stu-id="88c94-155">The client presents credentials in the form of a user name and password, directly transmitted in the request message.</span></span> <span data-ttu-id="88c94-156">Solo puede especificar credenciales que identifiquen una cuenta de administrador local en el equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="88c94-156">You can specify only credentials that identify a local administrator account on the remote computer.</span></span>

<span data-ttu-id="88c94-157">El método de scripting asociado es [**WSMan. SessionFlagUseBasic**](wsman-sessionflagusebasic.md)y el método de C++ es [**IWSManEx. SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).</span><span class="sxs-lookup"><span data-stu-id="88c94-157">The associated scripting method is [**WSMan.SessionFlagUseBasic**](wsman-sessionflagusebasic.md), and the C++ method is [**IWSManEx.SessionFlagUseBasic**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusebasic).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88c94-158"><span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**</span><span class="sxs-lookup"><span data-stu-id="88c94-158"><span id="WSManFlagUseKerberos"></span><span id="wsmanflagusekerberos"></span><span id="WSMANFLAGUSEKERBEROS"></span>**WSManFlagUseKerberos**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c94-159">524288 (0x80000)</span><span class="sxs-lookup"><span data-stu-id="88c94-159">524288 (0x80000)</span></span>
</dt> <dt>



<span data-ttu-id="88c94-160">Utilice la autenticación Kerberos.</span><span class="sxs-lookup"><span data-stu-id="88c94-160">Use Kerberos authentication.</span></span> <span data-ttu-id="88c94-161">El cliente y el servidor se autentican mutuamente mediante vales Kerberos.</span><span class="sxs-lookup"><span data-stu-id="88c94-161">The client and server mutually authenticate using Kerberos tickets.</span></span>

<span data-ttu-id="88c94-162">El método de scripting asociado es [**WSMan. SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md)y el método de C++ es [**IWSManEx. WSMan. SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).</span><span class="sxs-lookup"><span data-stu-id="88c94-162">The associated scripting method is [**WSMan.SessionFlagUseKerberos**](wsman-sessionflagusekerberos.md), and the C++ method is [**IWSManEx.WSMan.SessionFlagUseKerberos**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagusekerberos).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88c94-163"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span><span class="sxs-lookup"><span data-stu-id="88c94-163"><span id="WSManFlagNoEncryption"></span><span id="wsmanflagnoencryption"></span><span id="WSMANFLAGNOENCRYPTION"></span>**WSManFlagNoEncryption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c94-164">1048576 (0x100000)</span><span class="sxs-lookup"><span data-stu-id="88c94-164">1048576 (0x100000)</span></span>
</dt> <dt>



<span data-ttu-id="88c94-165">No usar cifrado.</span><span class="sxs-lookup"><span data-stu-id="88c94-165">Use no encryption.</span></span> <span data-ttu-id="88c94-166">No se permite el tráfico no cifrado de forma predeterminada y debe habilitarse tanto en el cliente como en el servidor.</span><span class="sxs-lookup"><span data-stu-id="88c94-166">Unencrypted traffic is not allowed by default and must be enabled on both the client and server.</span></span>

<span data-ttu-id="88c94-167">El método de scripting asociado es [**WSMan. SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md)y el método de C++ es [**IWSManEx. SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span><span class="sxs-lookup"><span data-stu-id="88c94-167">The associated scripting method is [**WSMan.SessionFlagNoEncryption**](wsman-sessionflagnoencryption.md), and the C++ method is [**IWSManEx.SessionFlagNoEncryption**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex-sessionflagnoencryption).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88c94-168"><span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**</span><span class="sxs-lookup"><span data-stu-id="88c94-168"><span id="WSManFlagUseClientCertificate"></span><span id="wsmanflaguseclientcertificate"></span><span id="WSMANFLAGUSECLIENTCERTIFICATE"></span>**WSManFlagUseClientCertificate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c94-169">2097152 (0x200000)</span><span class="sxs-lookup"><span data-stu-id="88c94-169">2097152 (0x200000)</span></span>
</dt> <dt>



<span data-ttu-id="88c94-170">Use la autenticación basada en certificados de cliente.</span><span class="sxs-lookup"><span data-stu-id="88c94-170">Use client certificate-based authentication.</span></span>

<span data-ttu-id="88c94-171">El método de scripting asociado es [**WSMan. SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md)y el método de C++ es [**IWSManEx2. SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).</span><span class="sxs-lookup"><span data-stu-id="88c94-171">The associated scripting method is [**WSMan.SessionFlagUseClientCertificate**](wsman-sessionflaguseclientcert.md), and the C++ method is [**IWSManEx2.SessionFlagUseClientCertificate**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex2-sessionflaguseclientcertificate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88c94-172"><span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**</span><span class="sxs-lookup"><span data-stu-id="88c94-172"><span id="WSManFlagUseCredSsp"></span><span id="wsmanflagusecredssp"></span><span id="WSMANFLAGUSECREDSSP"></span>**WSManFlagUseCredSsp**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c94-173">16777216 (0x1000000)</span><span class="sxs-lookup"><span data-stu-id="88c94-173">16777216 (0x1000000)</span></span>
</dt> <dt>



<span data-ttu-id="88c94-174">Use la autenticación del proveedor de compatibilidad para seguridad de credenciales (CredSSP).</span><span class="sxs-lookup"><span data-stu-id="88c94-174">Use Credential Security Support Provider (CredSSP) authentication.</span></span>

<span data-ttu-id="88c94-175">El método de scripting asociado es [**WSMan. SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md)y el método de C++ es [**IWSManEx3. SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).</span><span class="sxs-lookup"><span data-stu-id="88c94-175">The associated scripting method is [**WSMan.SessionFlagUseCredSsp**](wsman-sessionflagusecredssp.md), and the C++ method is [**IWSManEx3.SessionFlagUseCredSsp**](/windows/desktop/api/WSManDisp/nf-wsmandisp-iwsmanex3-sessionflagusecredssp).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88c94-176"><span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**</span><span class="sxs-lookup"><span data-stu-id="88c94-176"><span id="WSManFlagSkipRevocationCheck"></span><span id="wsmanflagskiprevocationcheck"></span><span id="WSMANFLAGSKIPREVOCATIONCHECK"></span>**WSManFlagSkipRevocationCheck**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c94-177">0x2000000</span><span class="sxs-lookup"><span data-stu-id="88c94-177">0x2000000</span></span>
</dt> <dt>



<span data-ttu-id="88c94-178">No Compruebe la revocación de certificados durante la autenticación.</span><span class="sxs-lookup"><span data-stu-id="88c94-178">Do not check for certificate revocation during authentication.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88c94-179"><span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**</span><span class="sxs-lookup"><span data-stu-id="88c94-179"><span id="WSManFlagAllowNegotiateImplicitCredentials"></span><span id="wsmanflagallownegotiateimplicitcredentials"></span><span id="WSMANFLAGALLOWNEGOTIATEIMPLICITCREDENTIALS"></span>**WSManFlagAllowNegotiateImplicitCredentials**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c94-180">0x4000000</span><span class="sxs-lookup"><span data-stu-id="88c94-180">0x4000000</span></span>
</dt> <dt>



<span data-ttu-id="88c94-181">Permitir credenciales implícitas.</span><span class="sxs-lookup"><span data-stu-id="88c94-181">Allow implicit credentials.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="88c94-182"><span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**</span><span class="sxs-lookup"><span data-stu-id="88c94-182"><span id="WSManFlagUseSsl"></span><span id="wsmanflagusessl"></span><span id="WSMANFLAGUSESSL"></span>**WSManFlagUseSsl**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="88c94-183">0x8000000</span><span class="sxs-lookup"><span data-stu-id="88c94-183">0x8000000</span></span>
</dt> <dt>



<span data-ttu-id="88c94-184">Usar capa de sockets seguros, habilita HTTPS.</span><span class="sxs-lookup"><span data-stu-id="88c94-184">Use Secure Socket Layer, enables HTTPS.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="88c94-185">Requisitos</span><span class="sxs-lookup"><span data-stu-id="88c94-185">Requirements</span></span>



| <span data-ttu-id="88c94-186">Requisito</span><span class="sxs-lookup"><span data-stu-id="88c94-186">Requirement</span></span> | <span data-ttu-id="88c94-187">Value</span><span class="sxs-lookup"><span data-stu-id="88c94-187">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="88c94-188">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88c94-188">Minimum supported client</span></span><br/> | <span data-ttu-id="88c94-189">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="88c94-189">Windows Vista</span></span><br/>                                                                 |
| <span data-ttu-id="88c94-190">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="88c94-190">Minimum supported server</span></span><br/> | <span data-ttu-id="88c94-191">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="88c94-191">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="88c94-192">Encabezado</span><span class="sxs-lookup"><span data-stu-id="88c94-192">Header</span></span><br/>                   | <dl> <span data-ttu-id="88c94-193"><dt>WSManDisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="88c94-193"><dt>WSManDisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="88c94-194">IDL</span><span class="sxs-lookup"><span data-stu-id="88c94-194">IDL</span></span><br/>                      | <dl> <span data-ttu-id="88c94-195"><dt>WSManDisp. idl</dt></span><span class="sxs-lookup"><span data-stu-id="88c94-195"><dt>WSManDisp.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="88c94-196">Vea también</span><span class="sxs-lookup"><span data-stu-id="88c94-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="88c94-197">Constantes de sesión</span><span class="sxs-lookup"><span data-stu-id="88c94-197">Session Constants</span></span>](session-constants.md)
</dt> </dl>

 

 





