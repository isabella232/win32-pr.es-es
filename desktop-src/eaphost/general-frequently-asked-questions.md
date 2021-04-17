---
title: Preguntas frecuentes generales
description: Lea las respuestas a las preguntas más frecuentes sobre las API de EAPHost, como "¿Cuál es la duración de una autenticación?".
ms.assetid: 4025e8da-8cb1-477b-86bb-7756d9636224
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4eb0dd9b3b997d8682c3cab1ba91afc3ee2db7ba
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/18/2020
ms.locfileid: "105714501"
---
# <a name="general-frequently-asked-questions"></a><span data-ttu-id="8b052-103">Preguntas frecuentes generales</span><span class="sxs-lookup"><span data-stu-id="8b052-103">General Frequently Asked Questions</span></span>

<span data-ttu-id="8b052-104">En el siguiente tema se proporcionan respuestas a las preguntas más frecuentes sobre las API de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="8b052-104">The following topic provides answers to commonly-asked questions about the EAPHost APIs.</span></span>

### <a name="general-frequently-asked-questions"></a><span data-ttu-id="8b052-105">Preguntas frecuentes generales</span><span class="sxs-lookup"><span data-stu-id="8b052-105">General Frequently Asked Questions</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8b052-106">Pregunta</span><span class="sxs-lookup"><span data-stu-id="8b052-106">Question</span></span></th>
<th><span data-ttu-id="8b052-107">Respuesta</span><span class="sxs-lookup"><span data-stu-id="8b052-107">Answer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="8b052-108">¿Qué es un suplicante?</span><span class="sxs-lookup"><span data-stu-id="8b052-108">What is a supplicant?</span></span></td>
<td><span data-ttu-id="8b052-109">El suplicante es la entidad que se va a autenticar mediante EAPHost.</span><span class="sxs-lookup"><span data-stu-id="8b052-109">The supplicant is the entity to be authenticated using EAPHost.</span></span> <span data-ttu-id="8b052-110">Los suplicantes típicos son los clientes de [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) , 802,3 clientes y el servicio de enrutamiento y acceso remoto (RRAS), los clientes de punto a punto (PPP).</span><span class="sxs-lookup"><span data-stu-id="8b052-110">Typical supplicants are [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) clients, 802.3 clients, and Routing and Remote Access Service (RRAS), Point-to-Point (PPP) clients.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b052-111">¿Qué es un elemento del mismo nivel?</span><span class="sxs-lookup"><span data-stu-id="8b052-111">What is a peer?</span></span></td>
<td><span data-ttu-id="8b052-112">El elemento del mismo nivel es el lado cliente de una autenticación EAP.</span><span class="sxs-lookup"><span data-stu-id="8b052-112">The peer is the client side of an EAP authentication.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b052-113">¿Cómo difiere un elemento del mismo nivel de un suplicante?</span><span class="sxs-lookup"><span data-stu-id="8b052-113">How does a peer differ from a supplicant?</span></span></td>
<td><span data-ttu-id="8b052-114">El solicitante transporta los paquetes, mientras que un elemento del mismo nivel no lo hace.</span><span class="sxs-lookup"><span data-stu-id="8b052-114">The supplicant transports packets, whereas a peer does not.</span></span> <span data-ttu-id="8b052-115">Sin embargo, los términos del mismo nivel, el suplicante y el cliente son principalmente sinónimos.</span><span class="sxs-lookup"><span data-stu-id="8b052-115">Nonetheless, the terms peer, supplicant and client are largely synonymous.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b052-116">¿Qué es un autenticador?</span><span class="sxs-lookup"><span data-stu-id="8b052-116">What is an authenticator?</span></span></td>
<td><span data-ttu-id="8b052-117">El autenticador es el punto de acceso inalámbrico, el servidor de acceso a la red (NAS) o el dispositivo de acceso a la red (NAD) que autentica al solicitante.</span><span class="sxs-lookup"><span data-stu-id="8b052-117">The authenticator is the wireless access point, network access server (NAS), or network access device (NAD) that authenticates the supplicant.</span></span> <span data-ttu-id="8b052-118">El autenticador también se conoce como servidor EAP.</span><span class="sxs-lookup"><span data-stu-id="8b052-118">The authenticator is also known as the EAP server.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b052-119">¿Cuál es la duración de una autenticación?</span><span class="sxs-lookup"><span data-stu-id="8b052-119">What is the lifetime of an authentication?</span></span></td>
<td><span data-ttu-id="8b052-120">La duración de una sesión de autenticación única en el lado cliente es todo lo que se produce entre las funciones [<strong>EapHostPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerbeginsession) y [<strong>EapHostPeerEndSession</strong>] (/Previous-Versions/Windows/Desktop/API/eappapis/NF-eappapis-eaphostpeerendsession) a las que se llama.</span><span class="sxs-lookup"><span data-stu-id="8b052-120">The lifetime of a single authentication session on the client side is everything that occurs between the [<strong>EapHostPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerbeginsession) and [<strong>EapHostPeerEndSession</strong>](/previous-versions/windows/desktop/api/eappapis/nf-eappapis-eaphostpeerendsession) functions being called.</span></span> <span data-ttu-id="8b052-121">La vigencia en el lado del autenticador es todo lo que se produce entre las funciones [<strong>EapPeerBeginSession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerbeginsession) y [<strong>EapPeerEndSession</strong>] (/Previous-Versions/Windows/Desktop/API/eapmethodpeerapis/NF-eapmethodpeerapis-eappeerendsession).</span><span class="sxs-lookup"><span data-stu-id="8b052-121">The lifetime on the authenticator side is everything that occurs between the [<strong>EapPeerBeginSession</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerbeginsession) and [<strong>EapPeerEndSession</strong>](/previous-versions/windows/desktop/api/eapmethodpeerapis/nf-eapmethodpeerapis-eappeerendsession) functions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b052-122">¿Qué es un BLOB?</span><span class="sxs-lookup"><span data-stu-id="8b052-122">What is a BLOB?</span></span> <span data-ttu-id="8b052-123">¿Por qué se puede convertir un BLOB de configuración (binario) en XML?</span><span class="sxs-lookup"><span data-stu-id="8b052-123">Why would I convert a configuration (binary) BLOB to XML?</span></span></td>
<td><span data-ttu-id="8b052-124">Un BLOB es un objeto binario grande.</span><span class="sxs-lookup"><span data-stu-id="8b052-124">A BLOB is a binary large object.</span></span> <span data-ttu-id="8b052-125">XML tiene varias ventajas con respecto a un BLOB de configuración binaria.</span><span class="sxs-lookup"><span data-stu-id="8b052-125">XML has several advantages over a binary configuration BLOB.</span></span> <span data-ttu-id="8b052-126">Los datos de configuración que se almacenan en XML son legibles para el usuario, editables y multiplataforma.</span><span class="sxs-lookup"><span data-stu-id="8b052-126">Configuration data that is stored in XML is human-readable, human-editable, and cross-platform.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b052-127">¿Cuándo se vuelve a convertir un BLOB XML almacenado en un BLOB binario?</span><span class="sxs-lookup"><span data-stu-id="8b052-127">When do I convert a stored XML BLOB back to a binary BLOB?</span></span></td>
<td><span data-ttu-id="8b052-128">Es posible almacenar un BLOB binario o XML, pero siempre debe volver a convertir el BLOB XML en un BLOB binario antes de usarlo con las API de tiempo de ejecución; las API de tiempo de ejecución no pueden aceptar un directorio XML.</span><span class="sxs-lookup"><span data-stu-id="8b052-128">It's possible to store a binary BLOB or XML BLOB, but you must always convert the XML BLOB back to a binary BLOB before use with run-time APIs; the run-time APIs cannot accept an XML directory.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b052-129">¿Qué son los métodos nativos?</span><span class="sxs-lookup"><span data-stu-id="8b052-129">What are native methods?</span></span></td>
<td><span data-ttu-id="8b052-130">Los métodos EAP nativos usan la nueva API de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="8b052-130">Native EAP methods use the new EAPHost API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b052-131">¿Qué son los métodos heredados?</span><span class="sxs-lookup"><span data-stu-id="8b052-131">What are legacy methods?</span></span></td>
<td><span data-ttu-id="8b052-132">Los métodos EAP heredados se definen en la [Referencia del Protocolo de autenticación extensible](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference).</span><span class="sxs-lookup"><span data-stu-id="8b052-132">Legacy EAP methods are defined in the [Extensible Authentication Protocol Reference](/previous-versions/windows/desktop/eap/extensible-authentication-protocol-reference).</span></span> <span data-ttu-id="8b052-133">Los métodos EAP heredados están disponibles para su uso en Windows Vista y Windows Server 2008.</span><span class="sxs-lookup"><span data-stu-id="8b052-133">The legacy EAP methods are available for use in Windows Vista and Windows Server 2008.</span></span> <span data-ttu-id="8b052-134">Es posible que estos métodos no estén disponibles para su uso en versiones posteriores del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="8b052-134">These methods may not be available for use in subsequent versions of the operating system.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b052-135">¿Cuál es la diferencia entre los métodos heredados y nativos?</span><span class="sxs-lookup"><span data-stu-id="8b052-135">What's the difference between legacy and native methods?</span></span></td>
<td><span data-ttu-id="8b052-136">Las API nativas son más sencillas y tienen menos características.</span><span class="sxs-lookup"><span data-stu-id="8b052-136">The native APIs are simpler and have fewer features.</span></span> <span data-ttu-id="8b052-137">Todos los nuevos métodos EAP deben escribirse con la API de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="8b052-137">All new EAP methods should be written using the EAPHost API.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b052-138">¿Qué es la &quot; Directiva de grupo &quot; ?</span><span class="sxs-lookup"><span data-stu-id="8b052-138">What is &quot;group policy&quot;?</span></span></td>
<td><span data-ttu-id="8b052-139">Para obtener una descripción de la Directiva de grupo, vea [Directiva de grupo colección](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="8b052-139">For a description of group policy, see [Group Policy Collection](/previous-versions/windows/it-pro/windows-server-2003/cc779838(v=ws.10)).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b052-140">¿Pueden las funciones de EAPHost invalidar la Directiva de configuración especificada por la Directiva de grupo?</span><span class="sxs-lookup"><span data-stu-id="8b052-140">Can EAPHost functions override configuration policy specified by group policy?</span></span></td>
<td><span data-ttu-id="8b052-141">No, nunca.</span><span class="sxs-lookup"><span data-stu-id="8b052-141">No, never.</span></span> <span data-ttu-id="8b052-142">Si se usa la Directiva de grupo, la configuración de directiva de grupo siempre invalidará las opciones de configuración de EAPHost.</span><span class="sxs-lookup"><span data-stu-id="8b052-142">If group policy is in use, group policy settings will always override EAPHost configuration settings.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b052-143">¿Qué es el inicio de sesión único (SSO)?</span><span class="sxs-lookup"><span data-stu-id="8b052-143">What is Single-Sign-On (SSO)?</span></span></td>
<td><span data-ttu-id="8b052-144">[802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) es un mecanismo de autenticación de nivel 2.</span><span class="sxs-lookup"><span data-stu-id="8b052-144">[802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) is a layer 2 authentication mechanism.</span></span> <span data-ttu-id="8b052-145">En función de la configuración de SSO, SSO permite a los usuarios autenticarse en la red mediante la autenticación de [802.1 x](/previous-versions/windows/embedded/ms890287(v=msdn.10)) antes o inmediatamente después de iniciar sesión en Windows.</span><span class="sxs-lookup"><span data-stu-id="8b052-145">Depending on the SSO configuration, SSO enables users to authenticate to the network using [802.1X](/previous-versions/windows/embedded/ms890287(v=msdn.10)) authentication before or immediately after logging on to Windows.</span></span> <span data-ttu-id="8b052-146">SSO puede configurarse para usar credenciales de Windows para la autenticación de red (en cuyo caso los usuarios escriben sus credenciales una sola vez) o usan credenciales diferentes para la autenticación de Windows y de red.</span><span class="sxs-lookup"><span data-stu-id="8b052-146">SSO can be configured to use Windows credentials for network authentication (in which case users enter their credentials only once) or use different credentials for Windows and network authentication.</span></span> <span data-ttu-id="8b052-147">Para obtener más información, consulte [SSO y PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="8b052-147">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b052-148">Qué es el proveedor de acceso previo al inicio de sesión (PLAP)</span><span class="sxs-lookup"><span data-stu-id="8b052-148">What is Pre-Logon Access Provider (PLAP)</span></span></td>
<td><span data-ttu-id="8b052-149">Para obtener más información, consulte [SSO y PLAP](understanding-sso-and-plap.md).</span><span class="sxs-lookup"><span data-stu-id="8b052-149">For more information, see [SSO and PLAP](understanding-sso-and-plap.md).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b052-150">¿Qué es el protocolo de autenticación extensible protegido (PEAP)?</span><span class="sxs-lookup"><span data-stu-id="8b052-150">What is Protected Extensible Authentication Protocol (PEAP)?</span></span></td>
<td><span data-ttu-id="8b052-151">Para obtener más información, vea [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) y [acerca del Protocolo de autenticación extensible](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol).</span><span class="sxs-lookup"><span data-stu-id="8b052-151">For more information, see [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)) and [About Extensible Authentication Protocol](/previous-versions/windows/desktop/eap/about-extensible-authentication-protocol).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b052-152">¿Cómo se trata PEAP con la reanudación de la sesión y la reautenticación?</span><span class="sxs-lookup"><span data-stu-id="8b052-152">How does PEAP deal with session resumption and re-authentication?</span></span></td>
<td><span data-ttu-id="8b052-153">La reanudación de la sesión y la reautenticación suele producirse durante la itinerancia en una red inalámbrica.</span><span class="sxs-lookup"><span data-stu-id="8b052-153">Session resumption and re-authentication typically occurs while roaming on a wireless network.</span></span> <span data-ttu-id="8b052-154">La API de protección de datos de Windows (DPAPI) proporciona una manera de proteger y enlazar datos a un usuario y, opcionalmente, la sesión de inicio de sesión.</span><span class="sxs-lookup"><span data-stu-id="8b052-154">Windows Data Protection API (DPAPI) provides a way to protect and bind data to a user and optionally the logon session.</span></span> <span data-ttu-id="8b052-155">El autor de la llamada proporciona a [<strong>CryptProtectMemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptprotectmemory) un búfer sin cifrar y DPAPI cifrará la memoria en su lugar.</span><span class="sxs-lookup"><span data-stu-id="8b052-155">The caller gives [<strong>CryptProtectMemory</strong>](/windows/desktop/api/dpapi/nf-dpapi-cryptprotectmemory) an unencrypted buffer and DPAPI will encrypt the memory in place.</span></span> <span data-ttu-id="8b052-156">Más adelante, el autor de la llamada puede pasar el búfer cifrado a [<strong>CryptUnprotectMemory</strong>] (/Windows/Desktop/API/DPAPI/NF-DPAPI-cryptunprotectmemory) y DPAPI descifrará la memoria, una vez más.</span><span class="sxs-lookup"><span data-stu-id="8b052-156">Later, the caller can pass in the encrypted buffer to [<strong>CryptUnprotectMemory</strong>](/windows/desktop/api/dpapi/nf-dpapi-cryptunprotectmemory) and DPAPI will decrypt the memory, once again in place.</span></span> <span data-ttu-id="8b052-157">Para obtener más información, consulte la [extensión de aplicación interna TLS (TSL/IA)](https://go.microsoft.com/fwlink/p/?linkid=84011) y [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="8b052-157">For more information, see [TLS Inner Application Extension (TSL/IA)](https://go.microsoft.com/fwlink/p/?linkid=84011) and [PEAP](/previous-versions/windows/it-pro/windows-server-2003/cc757996(v=ws.10)).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b052-158">¿Qué es la seguridad de nivel de EAP-Transport (EAP-TLS)?</span><span class="sxs-lookup"><span data-stu-id="8b052-158">What is EAP-Transport Level Security (EAP-TLS)?</span></span></td>
<td><span data-ttu-id="8b052-159">EAP-TLS es un protocolo cliente-servidor en el que se suelen usar perfiles de certificado distintos para el cliente y el servidor. Para obtener más información, consulte [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).</span><span class="sxs-lookup"><span data-stu-id="8b052-159">EAP-TLS is a client-server protocol in which distinct certificate profiles are typically used for the client and server.For more information, see [IETF RTC 2716](/previous-versions/windows/embedded/ms885336(v=msdn.10)).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b052-160">Cómo implementar un cambio de contraseña con la API de autoridad de seguridad local (LSA)?</span><span class="sxs-lookup"><span data-stu-id="8b052-160">How do I implement a password change using the Local Security Authority (LSA) API?</span></span></td>
<td><span data-ttu-id="8b052-161">Use la función [<strong>LsaCallAuthenticationPackage</strong>] (/Windows/Desktop/API/ntsecapi/NF-ntsecapi-lsacallauthenticationpackage) para implementar un cambio de contraseña.</span><span class="sxs-lookup"><span data-stu-id="8b052-161">Use the [<strong>LsaCallAuthenticationPackage</strong>](/windows/desktop/api/ntsecapi/nf-ntsecapi-lsacallauthenticationpackage) function to implement a password change.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b052-162">¿Por qué deseo habilitar el seguimiento en EAPHost?</span><span class="sxs-lookup"><span data-stu-id="8b052-162">Why would I want to enable tracing in EAPHost?</span></span></td>
<td><span data-ttu-id="8b052-163">Los registros de seguimiento contienen información de depuración (disponible solo en inglés) que puede ayudar a los desarrolladores y asociados de Microsoft a encontrar las causas raíz de cualquier problema experimentado con el proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="8b052-163">The trace logs contain debugging information (available in English only) that may assist Microsoft developers and partners in finding the root causes of any issues being experienced with the authentication process.</span></span> <span data-ttu-id="8b052-164">Para obtener más información, vea [Habilitar el seguimiento](enabling-tracing.md).</span><span class="sxs-lookup"><span data-stu-id="8b052-164">For more information, see [Enabling Tracing](enabling-tracing.md).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b052-165">¿Por qué encuentro el código de error, NTE_BAD_KEY_STATE (0x8009000BL) cuando uso la API de [Criptografía](/windows/desktop/SecCrypto/cryptography-portal) para iniciar sesión en el intercambio de EAP-TLS?</span><span class="sxs-lookup"><span data-stu-id="8b052-165">Why do I encounter the error code, NTE_BAD_KEY_STATE (0x8009000BL) when I use the [Cryptography](/windows/desktop/SecCrypto/cryptography-portal) API to sign into the EAP-TLS exchange?</span></span></td>
<td><span data-ttu-id="8b052-166">En Winerror. h NTE_BAD_KEY_STATE (0x8009000BL) se define como una &quot; clave no válida para su uso en el estado especificado &quot; .</span><span class="sxs-lookup"><span data-stu-id="8b052-166">In Winerror.h NTE_BAD_KEY_STATE (0x8009000BL) is defined as a &quot;key not valid for use in specified state&quot;.</span></span> <span data-ttu-id="8b052-167">Este error se devuelve normalmente en los escenarios siguientes.</span><span class="sxs-lookup"><span data-stu-id="8b052-167">This error is typically returned in the following scenarios.</span></span>
<ul>
<li><span data-ttu-id="8b052-168">Al intentar exportar un BLOB de clave privada no exportable</span><span class="sxs-lookup"><span data-stu-id="8b052-168">When attempting to export a non-exportable private key BLOB</span></span></li>
<li><span data-ttu-id="8b052-169">Cuando se intenta generar de forma incorrecta un identificador hash de función pseudoaleatorios (PRF) mediante [<strong>CryptCreateHash</strong>] (/Windows/Desktop/API/wincrypt/NF-wincrypt-cryptcreatehash)</span><span class="sxs-lookup"><span data-stu-id="8b052-169">When unsuccessfully attempting to generate a pseudo-random function (PRF) hash handle using [<strong>CryptCreateHash</strong>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptcreatehash)</span></span></li>
</ul>
<span data-ttu-id="8b052-170">Para obtener más información, consulte [Finalizar mensajes en el protocolo TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span><span class="sxs-lookup"><span data-stu-id="8b052-170">For more information, see [Finish Messages in the TLS 1.0 Protocol](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="8b052-171">¿Qué es una función pseudoaleatorios (PRF)?</span><span class="sxs-lookup"><span data-stu-id="8b052-171">What is a pseudo-random function (PRF)?</span></span></td>
<td><span data-ttu-id="8b052-172">Una función que toma una clave, una etiqueta y una inicialización como entrada y, a continuación, genera una salida de longitud arbitraria.</span><span class="sxs-lookup"><span data-stu-id="8b052-172">A function that takes a key, label, and seed as input, then produces an output of arbitrary length.</span></span> <span data-ttu-id="8b052-173">Para obtener más información, consulte [Finalizar mensajes en el protocolo TLS 1,0](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span><span class="sxs-lookup"><span data-stu-id="8b052-173">For more information, see [Finish Messages in the TLS 1.0 Protocol](/windows/desktop/SecCrypto/finish-messages-in-the-tls-1-0-protocol).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="8b052-174">¿Cómo se enlaza EAPHost a adaptadores de red?</span><span class="sxs-lookup"><span data-stu-id="8b052-174">How does EAPHost bind to network adapters?</span></span></td>
<td><span data-ttu-id="8b052-175">EAPHost permite que varios suplicantes operen simultáneamente, y cada suplicante puede enlazar a varios adaptadores de red.</span><span class="sxs-lookup"><span data-stu-id="8b052-175">EAPHost allows multiple supplicants to operate simultaneously, and each supplicant can bind to multiple network adapters.</span></span> <span data-ttu-id="8b052-176">Los suplicantes de EAPHost proporcionan enlaces a los niveles de red y controlan el proceso de autenticación.</span><span class="sxs-lookup"><span data-stu-id="8b052-176">EAPHost supplicants provide binding to the network layers and drive the authentication process.</span></span> <span data-ttu-id="8b052-177">Los suplicantes contienen la configuración de autenticación.</span><span class="sxs-lookup"><span data-stu-id="8b052-177">Supplicants contain authentication configuration.</span></span> <span data-ttu-id="8b052-178">Los suplicantes también guardan el estado y proporcionan una seguridad de conexión posterior.</span><span class="sxs-lookup"><span data-stu-id="8b052-178">Supplicants also save the state and provide subsequent connection security.</span></span> <span data-ttu-id="8b052-179">Dado que EAPHost no se enlaza directamente a ningún mecanismo de red, es posible la extensibilidad del suplicante.</span><span class="sxs-lookup"><span data-stu-id="8b052-179">Because EAPHost doesn't directly bind to any network mechanism, supplicant extensibility is possible.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="8b052-180">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="8b052-180">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8b052-181">Preguntas más frecuentes sobre Suplicador de EAPHost</span><span class="sxs-lookup"><span data-stu-id="8b052-181">EAPHost Supplicant FAQs</span></span>](eaphost-supplicant-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="8b052-182">Preguntas más frecuentes sobre el método EAPHost</span><span class="sxs-lookup"><span data-stu-id="8b052-182">EAPHost Method FAQs</span></span>](eap-method-frequently-asked-questions.md)
</dt> <dt>

[<span data-ttu-id="8b052-183">Preguntas más frecuentes sobre el desarrollo de EAPHost</span><span class="sxs-lookup"><span data-stu-id="8b052-183">EAPHost Development FAQs</span></span>](eaphost-development-frequently-asked-questions.md)
</dt> </dl>

