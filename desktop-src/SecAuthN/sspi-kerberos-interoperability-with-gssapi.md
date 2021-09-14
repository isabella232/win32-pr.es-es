---
description: Se debe tener cuidado al usar el proveedor de compatibilidad de seguridad (SSP) de Kerberos si la interoperabilidad con GSSAPI es un requisito.
ms.assetid: 3ab29ee9-42d8-498b-b507-13f8efa0b0e2
title: Interoperabilidad de SSPI/Kerberos con GSSAPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9efaae6b2433d76dff290d57e27e893885692a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160970"
---
# <a name="sspikerberos-interoperability-with-gssapi"></a>Interoperabilidad de SSPI/Kerberos con GSSAPI

Se debe tener cuidado al usar el proveedor de [*compatibilidad*](../secgloss/s-gly.md) de seguridad (SSP) de [*Kerberos*](../secgloss/k-gly.md) si la interoperabilidad con GSSAPI es un requisito. Las convenciones de código siguientes permiten la interoperabilidad con aplicaciones basadas en GSSAPI:

-   [Windows nombres compatibles](#windows-compatible-names)
-   [Autenticación](#authentication)
-   [Integridad y privacidad de los mensajes](#message-integrity-and-privacy)

Puede encontrar código de ejemplo en Platform Software Development Kit (SDK) en Samples \\ Security SSPI GSS (Ejemplos de seguridad de \\ \\ SSPI GSS). Además, el ejemplo de UNIX equivalente se distribuye en las distribuciones MIT y Kerberos de Kerberos, el cliente y el servidor de GSS.

## <a name="windows-compatible-names"></a>Windows-Compatible nombres

Las funciones GSSAPI usan un formato de nombre conocido como nombre de servicio gss \_ nt como se especifica en \_ \_ rfc. Por ejemplo, sample@host.dom.com es un nombre que se puede usar en una aplicación basada en GSSAPI. El Windows operativo no reconoce el formato de nombre de servicio gss nt y se debe usar el nombre de entidad de seguridad de servicio completo , por \_ \_ ejemplo , \_ [](../secgloss/s-gly.md) sample/host.dom.com@REALM .

## <a name="authentication"></a>Authentication

Normalmente, la autenticación se controla cuando una conexión se configura por primera vez entre un cliente y un servidor. En este ejemplo, el cliente usa la [*interfaz del*](../secgloss/s-gly.md) proveedor de compatibilidad de seguridad (SSPI) y el servidor usa GSSAPI.

**Para configurar la autenticación en el cliente SSPI**

1.  Obtenga las [*credenciales de*](../secgloss/c-gly.md) salida mediante [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).
2.  Cree un nombre de servicio con **gss \_ import \_ name()** y obtenga las credenciales de entrada mediante **gss \_ acquire \_ cred**.
3.  Obtenga un token de autenticación para enviarlo al servidor mediante [**InitializeSecurityContext (Kerberos).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
4.  Envíe el token al servidor.

**Para configurar la autenticación en el servidor GSSAPI**

1.  Analice el mensaje del cliente para extraer el token de seguridad. Use la **función de contexto gss \_ accept \_ sec \_** y pase el token como argumento.
2.  Analice el mensaje del servidor para extraer el token de seguridad. Pase este token de seguridad [**a InitializeSecurityContext (Kerberos).**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta)
3.  Envíe un token de respuesta al cliente.

    La **función de contexto gss accept \_ \_ sec \_** puede devolver un token que puede devolver al cliente.

4.  Si es necesario continuar, envíe un token de respuesta al servidor; De lo contrario, la configuración de la autenticación se ha completado.
5.  Si es necesario continuar, espere el siguiente token del cliente; De lo contrario, la configuración de la autenticación se ha completado.

## <a name="message-integrity-and-privacy"></a>Integridad y privacidad de los mensajes

La mayoría de las aplicaciones basadas en GSSAPI usan la **función GSS \_ Wrap** para firmar un mensaje antes de enviarlo. Por el contrario, la **función \_ Unwrap de GSS** comprueba la firma. **GSS \_ Wrap** está disponible en la versión 2.0 de la API y ahora se usa ampliamente y se especifica en los estándares de Internet que describen el uso de GSSAPI para agregar seguridad a los protocolos. Anteriormente, las funciones **SignMessage** y **SealMessage** de GSS se usaban para la integridad de los [*mensajes y*](../secgloss/i-gly.md) la [*privacidad.*](../secgloss/p-gly.md) **GSS \_ Wrap** y **GSS \_ Unwrap** se usan para la integridad y la privacidad con el uso de privacidad controlada por el valor del argumento "conf \_ flag".

Si se especifica un protocolo basado en GSSAPI para usar las funciones **gss \_ get \_ mic** y **gss \_ verify \_ mic,** las funciones SSPI correctas [**serían MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) y [**VerifySignature.**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) Tenga en cuenta **que MakeSignature** y **VerifySignature** no interoperarán con **GSS \_ Wrap** cuando la marca conf esté establecida en cero o con \_ **GSS \_ Wrap**. Lo mismo se aplica a la combinación de [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) establecido solo para firma y **gss \_ verify \_ mic**.

> [!Note]  
> No use las [**funciones MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) o [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) cuando se llame a **GSS \_ Wrap** y **GSS \_ Unwrap.**

 

El SSPI equivalente a **GSS \_ Wrap** es [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) para integridad y privacidad.

En el ejemplo siguiente se muestra [**el uso de EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) para firmar los datos que se comprobarán mediante **GSS \_ Unwrap**.

En el cliente de SSPI:


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



En el servidor GSSAPI:


```C++
// Received message is in recv_buf. 
maj_stat = gss_unwrap(&min_stat, context, &recv_buf, &msg_buf,
    &conf_state, (gss_qop_t *) NULL);
(void) gss_release_buffer(&min_stat, &recv_buf);

// Original message is in msg_buf.
```



El SSPI equivalente a **GSS \_ Unwrap** es [**DecryptMessage (Kerberos).**](/windows/win32/api/sspi/nf-sspi-decryptmessage) Este es un ejemplo que muestra cómo usar **DecryptMessage (Kerberos)** para descifrar los datos cifrados por **GSS \_ Wrap**.

En el servidor GSSAPI:


```C++
// Seal the message.
send_buf.value = msg;
send_buf.length = msglen;

// If encrypt_flag = 1, privacy; encrypt_flag = 0, integrity.
maj_stat = gss_wrap(&min_stat, context, encrypt_flag,
    GSS_C_QOP_DEFAULT, &send_buf, &state, &msg_buf); 

// The message to send is in msg_buf.
```



En el cliente de SSPI:


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



 

 
