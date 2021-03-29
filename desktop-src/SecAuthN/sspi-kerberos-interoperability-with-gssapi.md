---
description: Se debe tener cuidado al usar el proveedor de compatibilidad para seguridad (SSP) de Kerberos si la interoperabilidad con GSSAPI es un requisito.
ms.assetid: 3ab29ee9-42d8-498b-b507-13f8efa0b0e2
title: Interoperabilidad de SSPI/Kerberos con GSSAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9efaae6b2433d76dff290d57e27e893885692a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103808348"
---
# <a name="sspikerberos-interoperability-with-gssapi"></a><span data-ttu-id="dac01-103">Interoperabilidad de SSPI/Kerberos con GSSAPI</span><span class="sxs-lookup"><span data-stu-id="dac01-103">SSPI/Kerberos Interoperability with GSSAPI</span></span>

<span data-ttu-id="dac01-104">Se debe tener cuidado al usar el [](../secgloss/k-gly.md) [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSP) de Kerberos si la interoperabilidad con GSSAPI es un requisito.</span><span class="sxs-lookup"><span data-stu-id="dac01-104">Care must be taken when using the [*Kerberos*](../secgloss/k-gly.md) [*security support provider*](../secgloss/s-gly.md) (SSP) if interoperability with GSSAPI is a requirement.</span></span> <span data-ttu-id="dac01-105">Las siguientes convenciones de código permiten la interoperabilidad con aplicaciones basadas en GSSAPI:</span><span class="sxs-lookup"><span data-stu-id="dac01-105">The following code conventions allow interoperability with GSSAPI-based applications:</span></span>

-   [<span data-ttu-id="dac01-106">Nombres compatibles con Windows</span><span class="sxs-lookup"><span data-stu-id="dac01-106">Windows-Compatible Names</span></span>](#windows-compatible-names)
-   [<span data-ttu-id="dac01-107">Autenticación</span><span class="sxs-lookup"><span data-stu-id="dac01-107">Authentication</span></span>](#authentication)
-   [<span data-ttu-id="dac01-108">Integridad y privacidad del mensaje</span><span class="sxs-lookup"><span data-stu-id="dac01-108">Message Integrity and Privacy</span></span>](#message-integrity-and-privacy)

<span data-ttu-id="dac01-109">Puede encontrar código de ejemplo en el kit de desarrollo de software (SDK) de la plataforma en samples \\ Security \\ SSPI \\ GSS.</span><span class="sxs-lookup"><span data-stu-id="dac01-109">You can find sample code in the Platform Software Development Kit (SDK) under Samples\\Security\\SSPI\\GSS.</span></span> <span data-ttu-id="dac01-110">Además, el ejemplo de UNIX equivalente se distribuye en las distribuciones de Kerberos MIT y Heimdal, el cliente de GSS y el servidor.</span><span class="sxs-lookup"><span data-stu-id="dac01-110">In addition, the equivalent UNIX sample is distributed in the MIT and Heimdal Kerberos distributions, GSS client and server.</span></span>

## <a name="windows-compatible-names"></a><span data-ttu-id="dac01-111">Nombres de Windows-Compatible</span><span class="sxs-lookup"><span data-stu-id="dac01-111">Windows-Compatible Names</span></span>

<span data-ttu-id="dac01-112">Las funciones GSSAPI utilizan un formato de nombre conocido \_ como \_ nombre de servicio GSS NT \_ , tal como se especifica en la RFC.</span><span class="sxs-lookup"><span data-stu-id="dac01-112">GSSAPI functions use a name format known as gss\_nt\_service\_name as specified in the RFC.</span></span> <span data-ttu-id="dac01-113">Por ejemplo, sample@host.dom.com es un nombre que se puede usar en una aplicación basada en GSSAPI.</span><span class="sxs-lookup"><span data-stu-id="dac01-113">For example, sample@host.dom.com is a name that can be used in a GSSAPI-based application.</span></span> <span data-ttu-id="dac01-114">El sistema operativo Windows no reconoce el formato de \_ nombre de servicio NT GSS \_ \_ y se debe usar el nombre completo de la entidad de seguridad de [*servicio*](../secgloss/s-gly.md), por ejemplo sample/host.dom.com@REALM .</span><span class="sxs-lookup"><span data-stu-id="dac01-114">The Windows operating system does not recognize the gss\_nt\_service\_name format, and the full [*service principal name*](../secgloss/s-gly.md), for example sample/host.dom.com@REALM, must be used.</span></span>

## <a name="authentication"></a><span data-ttu-id="dac01-115">Autenticación</span><span class="sxs-lookup"><span data-stu-id="dac01-115">Authentication</span></span>

<span data-ttu-id="dac01-116">Normalmente, la autenticación se controla cuando una conexión se configura por primera vez entre un cliente y un servidor.</span><span class="sxs-lookup"><span data-stu-id="dac01-116">Authentication is usually handled when a connection is first set up between a client and a server.</span></span> <span data-ttu-id="dac01-117">En este ejemplo, el cliente usa la [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI) y el servidor usa GSSAPI.</span><span class="sxs-lookup"><span data-stu-id="dac01-117">In this sample, the client is using [*Security Support Provider Interface*](../secgloss/s-gly.md) (SSPI) and the server is using GSSAPI.</span></span>

<span data-ttu-id="dac01-118">**Para configurar la autenticación en el cliente SSPI**</span><span class="sxs-lookup"><span data-stu-id="dac01-118">**To set up authentication in the SSPI client**</span></span>

1.  <span data-ttu-id="dac01-119">Obtener [*las credenciales*](../secgloss/c-gly.md) de salida mediante [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).</span><span class="sxs-lookup"><span data-stu-id="dac01-119">Get outbound [*credentials*](../secgloss/c-gly.md) by using [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).</span></span>
2.  <span data-ttu-id="dac01-120">Cree un nombre de servicio **con \_ \_ el nombre de importación de GSS ()** y obtenga las credenciales de entrada mediante el uso de **GSS \_ adquire \_ CRED**.</span><span class="sxs-lookup"><span data-stu-id="dac01-120">Create a service name with **gss\_import\_name()** and get inbound credentials by using **gss\_acquire\_cred**.</span></span>
3.  <span data-ttu-id="dac01-121">Obtener un token de autenticación para enviar al servidor mediante [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span><span class="sxs-lookup"><span data-stu-id="dac01-121">Get an authentication token to send to the server by using [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span>
4.  <span data-ttu-id="dac01-122">Envíe el token al servidor.</span><span class="sxs-lookup"><span data-stu-id="dac01-122">Send the token to the server.</span></span>

<span data-ttu-id="dac01-123">**Para configurar la autenticación en el servidor GSSAPI**</span><span class="sxs-lookup"><span data-stu-id="dac01-123">**To set up authentication in the GSSAPI server**</span></span>

1.  <span data-ttu-id="dac01-124">Analice el mensaje desde el cliente para extraer el token de seguridad.</span><span class="sxs-lookup"><span data-stu-id="dac01-124">Parse the message from the client to extract the security token.</span></span> <span data-ttu-id="dac01-125">Use la función de **\_ contexto de aceptación \_ s \_ de GSS** , pasando el token como argumento.</span><span class="sxs-lookup"><span data-stu-id="dac01-125">Use the **gss\_accept\_sec\_context** function, passing the token as an argument.</span></span>
2.  <span data-ttu-id="dac01-126">Analice el mensaje desde el servidor para extraer el token de seguridad.</span><span class="sxs-lookup"><span data-stu-id="dac01-126">Parse the message from the server to extract the security token.</span></span> <span data-ttu-id="dac01-127">Pase este token de seguridad a [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span><span class="sxs-lookup"><span data-stu-id="dac01-127">Pass this security token to [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).</span></span>
3.  <span data-ttu-id="dac01-128">Envíe un token de respuesta al cliente.</span><span class="sxs-lookup"><span data-stu-id="dac01-128">Send a response token to the client.</span></span>

    <span data-ttu-id="dac01-129">La función de **contexto de aceptación de GSS en \_ \_ segundos \_** puede devolver un token que se puede enviar al cliente.</span><span class="sxs-lookup"><span data-stu-id="dac01-129">The **gss\_accept\_sec\_context** function can return a token that you can send back to the client.</span></span>

4.  <span data-ttu-id="dac01-130">Si es necesario continuar, envíe un token de respuesta al servidor; de lo contrario, se completa la configuración de la autenticación.</span><span class="sxs-lookup"><span data-stu-id="dac01-130">If it is necessary to continue, send a response token to the server; otherwise, the setup of authentication is complete.</span></span>
5.  <span data-ttu-id="dac01-131">Si es necesario continuar, espere al siguiente token del cliente; de lo contrario, se completa la configuración de la autenticación.</span><span class="sxs-lookup"><span data-stu-id="dac01-131">If it is necessary to continue, wait for the next token from the client; otherwise, the setup of authentication is complete.</span></span>

## <a name="message-integrity-and-privacy"></a><span data-ttu-id="dac01-132">Integridad y privacidad del mensaje</span><span class="sxs-lookup"><span data-stu-id="dac01-132">Message Integrity and Privacy</span></span>

<span data-ttu-id="dac01-133">La mayoría de las aplicaciones basadas en GSSAPI usan la función de **\_ ajuste GSS** para firmar un mensaje antes de enviarlo.</span><span class="sxs-lookup"><span data-stu-id="dac01-133">Most GSSAPI-based applications use the **GSS\_Wrap** function to sign a message before sending it.</span></span> <span data-ttu-id="dac01-134">Por el contrario, la función **GSS \_ Unwrap** comprueba la firma.</span><span class="sxs-lookup"><span data-stu-id="dac01-134">Conversely, the **GSS\_Unwrap** function verifies the signature.</span></span> <span data-ttu-id="dac01-135">**GSS \_ Wrap** está disponible en la versión 2,0 de la API y ahora se usa con frecuencia y se especifica en estándares de Internet que describen el uso de la GSSAPI para agregar seguridad a los protocolos.</span><span class="sxs-lookup"><span data-stu-id="dac01-135">**GSS\_Wrap** is available in version 2.0 of the API and is now widely used and specified in Internet standards that describe using the GSSAPI for adding security to protocols.</span></span> <span data-ttu-id="dac01-136">Anteriormente, las funciones GSS **SignMessage** y **SealMessage** se usaban para la [*integridad*](../secgloss/i-gly.md) del mensaje y la [*privacidad*](../secgloss/p-gly.md).</span><span class="sxs-lookup"><span data-stu-id="dac01-136">Earlier, the GSS **SignMessage** and **SealMessage** functions were used for message [*integrity*](../secgloss/i-gly.md) and [*privacy*](../secgloss/p-gly.md).</span></span> <span data-ttu-id="dac01-137">**GSS \_ Wrap** y **el \_ desencapsulado de GSS** se usan para la integridad y la privacidad con el uso de privacidad controlado por el valor del argumento "conf \_ flag".</span><span class="sxs-lookup"><span data-stu-id="dac01-137">**GSS\_Wrap** and **GSS\_Unwrap** are used for both integrity and privacy with the use of privacy controlled by the value of the "conf\_flag" argument.</span></span>

<span data-ttu-id="dac01-138">Si se especifica un protocolo basado en GSSAPI para usar las **funciones GSS \_ Get \_ MIC** y **GSS \_ Verify \_ MIC** , las funciones SSPI correctas serían [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) y [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature).</span><span class="sxs-lookup"><span data-stu-id="dac01-138">If a GSSAPI-based protocol is specified to use the **gss\_get\_mic** and **gss\_verify\_mic** functions, the correct SSPI functions would be [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature).</span></span> <span data-ttu-id="dac01-139">Tenga en cuenta que **MakeSignature** y **VerifySignature** no interoperarán con el **\_ ajuste de GSS** cuando la marca de conf \_ esté establecida en cero o con el **\_ ajuste de GSS**.</span><span class="sxs-lookup"><span data-stu-id="dac01-139">Be aware that **MakeSignature** and **VerifySignature** will not interoperate with **GSS\_Wrap** when conf\_flag is set to zero, or with **GSS\_Wrap**.</span></span> <span data-ttu-id="dac01-140">Lo mismo se aplica a la combinación del conjunto [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) para la firma solamente y la comprobación de la **GSS \_ \_**.</span><span class="sxs-lookup"><span data-stu-id="dac01-140">The same is true for mixing [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) set for signature only and **gss\_verify\_mic**.</span></span>

> [!Note]  
> <span data-ttu-id="dac01-141">No use las funciones [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) o [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) cuando se llame a **GSS \_ Wrap** y **\_ Unwrap de GSS** para.</span><span class="sxs-lookup"><span data-stu-id="dac01-141">Do not use the [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) or [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions when **GSS\_Wrap** and **GSS\_Unwrap** are called for.</span></span>

 

<span data-ttu-id="dac01-142">La SSPI equivalente a **GSS \_ Wrap** es [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) para la integridad y la privacidad.</span><span class="sxs-lookup"><span data-stu-id="dac01-142">The SSPI equivalent to **GSS\_Wrap** is [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) for both integrity and privacy.</span></span>

<span data-ttu-id="dac01-143">En el ejemplo siguiente se muestra el uso de [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) para firmar los datos que se comprobarán por **GSS \_ Unwrap**.</span><span class="sxs-lookup"><span data-stu-id="dac01-143">The following example shows using [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) to sign data that will be verified by **GSS\_Unwrap**.</span></span>

<span data-ttu-id="dac01-144">En el cliente SSPI:</span><span class="sxs-lookup"><span data-stu-id="dac01-144">In the SSPI client:</span></span>


```C++
// Need three descriptors, two for the SSP and
// one to hold the application data. 
in_buf_desc.cBuffers = 3;
in_buf_desc.pBuffers = wrap_bufs;
in_buf_desc.ulVersion = SECBUFFER_VERSION;
wrap_bufs[0].cbBuffer = sizes.cbSecurityTrailer;
wrap_bufs[0].BufferType = SECBUFFER_TOKEN;
wrap_bufs[0].pvBuffer = malloc(sizes.cbSecurityTrailer);

// This buffer holds the application data.
wrap_bufs[1].BufferType = SECBUFFER_DATA;
wrap_bufs[1].cbBuffer = in_buf.cbBuffer;
wrap_bufs[1].pvBuffer = malloc(wrap_bufs[1].cbBuffer);
memcpy(wrap_bufs[1].pvBuffer, in_buf.pvBuffer, in_buf.cbBuffer);
wrap_bufs[2].BufferType = SECBUFFER_PADDING;
wrap_bufs[2].cbBuffer = sizes.cbBlockSize;
wrap_bufs[2].pvBuffer = malloc(wrap_bufs[2].cbBuffer);
maj_stat = EncryptMessage(&context,
SignOnly ? KERB_WRAP_NO_ENCRYPT : 0,
&in_buf_desc, 0);

// Send a message to the server.
```



<span data-ttu-id="dac01-145">En el servidor GSSAPI:</span><span class="sxs-lookup"><span data-stu-id="dac01-145">In the GSSAPI server:</span></span>


```C++
// Received message is in recv_buf. 
maj_stat = gss_unwrap(&min_stat, context, &recv_buf, &msg_buf,
    &conf_state, (gss_qop_t *) NULL);
(void) gss_release_buffer(&min_stat, &recv_buf);

// Original message is in msg_buf.
```



<span data-ttu-id="dac01-146">La SSPI equivalente a **la \_ desencapsulación de GSS** es [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span><span class="sxs-lookup"><span data-stu-id="dac01-146">The SSPI equivalent to **GSS\_Unwrap** is [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage).</span></span> <span data-ttu-id="dac01-147">Este es un ejemplo que muestra cómo usar **DecryptMessage (Kerberos)** para descifrar los datos que se cifraron mediante **GSS \_ Wrap**.</span><span class="sxs-lookup"><span data-stu-id="dac01-147">Here is an example that shows how to use **DecryptMessage (Kerberos)** to decrypt data that was encrypted by **GSS\_Wrap**.</span></span>

<span data-ttu-id="dac01-148">En el servidor GSSAPI:</span><span class="sxs-lookup"><span data-stu-id="dac01-148">In the GSSAPI server:</span></span>


```C++
// Seal the message.
send_buf.value = msg;
send_buf.length = msglen;

// If encrypt_flag = 1, privacy; encrypt_flag = 0, integrity.
maj_stat = gss_wrap(&min_stat, context, encrypt_flag,
    GSS_C_QOP_DEFAULT, &send_buf, &state, &msg_buf); 

// The message to send is in msg_buf.
```



<span data-ttu-id="dac01-149">En el cliente SSPI:</span><span class="sxs-lookup"><span data-stu-id="dac01-149">In the SSPI client:</span></span>


```C++
wrap_buf_desc.cBuffers = 2;
wrap_buf_desc.pBuffers = wrap_bufs;
wrap_buf_desc.ulVersion = SECBUFFER_VERSION; 

// This buffer is for SSPI.
wrap_bufs[0].BufferType = SECBUFFER_STREAM;
wrap_bufs[0].pvBuffer = xmit_buf.pvBuffer;
wrap_bufs[0].cbBuffer = xmit_buf.cbBuffer;

// This buffer holds the application data.
wrap_bufs[1].BufferType = SECBUFFER_DATA;
wrap_bufs[1].cbBuffer = 0;
wrap_bufs[1].pvBuffer = NULL;
maj_stat = DecryptMessage(
&context,
&wrap_buf_desc,
0, // no sequence number
&qop
);

// This is where the data is.
msg_buf = wrap_bufs[1];

// Check QOP of received message.
// If QOP is KERB_WRAP_NO_ENCRYPT, the message is signed only; 
// otherwise, it is encrypted.
```



 

 
