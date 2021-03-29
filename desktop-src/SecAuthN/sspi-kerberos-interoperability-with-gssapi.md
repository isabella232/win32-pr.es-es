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
# <a name="sspikerberos-interoperability-with-gssapi"></a>Interoperabilidad de SSPI/Kerberos con GSSAPI

Se debe tener cuidado al usar el [](../secgloss/k-gly.md) [*proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSP) de Kerberos si la interoperabilidad con GSSAPI es un requisito. Las siguientes convenciones de código permiten la interoperabilidad con aplicaciones basadas en GSSAPI:

-   [Nombres compatibles con Windows](#windows-compatible-names)
-   [Autenticación](#authentication)
-   [Integridad y privacidad del mensaje](#message-integrity-and-privacy)

Puede encontrar código de ejemplo en el kit de desarrollo de software (SDK) de la plataforma en samples \\ Security \\ SSPI \\ GSS. Además, el ejemplo de UNIX equivalente se distribuye en las distribuciones de Kerberos MIT y Heimdal, el cliente de GSS y el servidor.

## <a name="windows-compatible-names"></a>Nombres de Windows-Compatible

Las funciones GSSAPI utilizan un formato de nombre conocido \_ como \_ nombre de servicio GSS NT \_ , tal como se especifica en la RFC. Por ejemplo, sample@host.dom.com es un nombre que se puede usar en una aplicación basada en GSSAPI. El sistema operativo Windows no reconoce el formato de \_ nombre de servicio NT GSS \_ \_ y se debe usar el nombre completo de la entidad de seguridad de [*servicio*](../secgloss/s-gly.md), por ejemplo sample/host.dom.com@REALM .

## <a name="authentication"></a>Autenticación

Normalmente, la autenticación se controla cuando una conexión se configura por primera vez entre un cliente y un servidor. En este ejemplo, el cliente usa la [*interfaz del proveedor de compatibilidad para seguridad*](../secgloss/s-gly.md) (SSPI) y el servidor usa GSSAPI.

**Para configurar la autenticación en el cliente SSPI**

1.  Obtener [*las credenciales*](../secgloss/c-gly.md) de salida mediante [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea).
2.  Cree un nombre de servicio **con \_ \_ el nombre de importación de GSS ()** y obtenga las credenciales de entrada mediante el uso de **GSS \_ adquire \_ CRED**.
3.  Obtener un token de autenticación para enviar al servidor mediante [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).
4.  Envíe el token al servidor.

**Para configurar la autenticación en el servidor GSSAPI**

1.  Analice el mensaje desde el cliente para extraer el token de seguridad. Use la función de **\_ contexto de aceptación \_ s \_ de GSS** , pasando el token como argumento.
2.  Analice el mensaje desde el servidor para extraer el token de seguridad. Pase este token de seguridad a [**InitializeSecurityContext (Kerberos)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta).
3.  Envíe un token de respuesta al cliente.

    La función de **contexto de aceptación de GSS en \_ \_ segundos \_** puede devolver un token que se puede enviar al cliente.

4.  Si es necesario continuar, envíe un token de respuesta al servidor; de lo contrario, se completa la configuración de la autenticación.
5.  Si es necesario continuar, espere al siguiente token del cliente; de lo contrario, se completa la configuración de la autenticación.

## <a name="message-integrity-and-privacy"></a>Integridad y privacidad del mensaje

La mayoría de las aplicaciones basadas en GSSAPI usan la función de **\_ ajuste GSS** para firmar un mensaje antes de enviarlo. Por el contrario, la función **GSS \_ Unwrap** comprueba la firma. **GSS \_ Wrap** está disponible en la versión 2,0 de la API y ahora se usa con frecuencia y se especifica en estándares de Internet que describen el uso de la GSSAPI para agregar seguridad a los protocolos. Anteriormente, las funciones GSS **SignMessage** y **SealMessage** se usaban para la [*integridad*](../secgloss/i-gly.md) del mensaje y la [*privacidad*](../secgloss/p-gly.md). **GSS \_ Wrap** y **el \_ desencapsulado de GSS** se usan para la integridad y la privacidad con el uso de privacidad controlado por el valor del argumento "conf \_ flag".

Si se especifica un protocolo basado en GSSAPI para usar las **funciones GSS \_ Get \_ MIC** y **GSS \_ Verify \_ MIC** , las funciones SSPI correctas serían [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) y [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature). Tenga en cuenta que **MakeSignature** y **VerifySignature** no interoperarán con el **\_ ajuste de GSS** cuando la marca de conf \_ esté establecida en cero o con el **\_ ajuste de GSS**. Lo mismo se aplica a la combinación del conjunto [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) para la firma solamente y la comprobación de la **GSS \_ \_**.

> [!Note]  
> No use las funciones [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) o [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) cuando se llame a **GSS \_ Wrap** y **\_ Unwrap de GSS** para.

 

La SSPI equivalente a **GSS \_ Wrap** es [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) para la integridad y la privacidad.

En el ejemplo siguiente se muestra el uso de [**EncryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) para firmar los datos que se comprobarán por **GSS \_ Unwrap**.

En el cliente SSPI:


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



La SSPI equivalente a **la \_ desencapsulación de GSS** es [**DecryptMessage (Kerberos)**](/windows/win32/api/sspi/nf-sspi-decryptmessage). Este es un ejemplo que muestra cómo usar **DecryptMessage (Kerberos)** para descifrar los datos que se cifraron mediante **GSS \_ Wrap**.

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



En el cliente SSPI:


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



 

 
