---
description: Cuando un cliente y un servidor terminan de configurar el contexto de seguridad, se pueden usar funciones de compatibilidad de mensajes.
ms.assetid: a65054bd-31cb-4842-af59-82cfe799fb70
title: Firmar un mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36f8151a66120575bfcaeda62955a7f6aa47e8e5
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127374958"
---
# <a name="signing-a-message"></a>Firmar un mensaje

Cuando un cliente y un servidor terminan de configurar el contexto [*de seguridad,*](../secgloss/s-gly.md)se pueden usar funciones de compatibilidad con mensajes. El cliente y el servidor usan el token de contexto de seguridad creado cuando se estableció la sesión para llamar a las funciones [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) [**y VerifySignature.**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) El token de contexto se puede usar [**con EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) y [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) para la privacidad de [*las comunicaciones.*](../secgloss/p-gly.md)

En el ejemplo siguiente se muestra el lado cliente que genera un mensaje firmado para enviarlo al servidor. Antes de llamar a [**MakeSignature,**](/windows/desktop/api/Sspi/nf-sspi-makesignature)el cliente llama a [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) con una estructura [**SecPkgContext \_ Sizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) para determinar la longitud del búfer necesario para contener la firma del mensaje. Si el **miembro cbMaxSignature** es cero, el paquete [*de seguridad*](../secgloss/s-gly.md) no admite mensajes de firma. De lo contrario, este miembro indica el tamaño del búfer que se va a asignar para recibir la firma.

En el ejemplo se supone que se **inicializan** una variable SecHandle denominada *phContext* y una **estructura SOCKET** denominada *s.* Para obtener las declaraciones e iniciaciones de estas variables, vea Using [SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md) y [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md). En este ejemplo se incluyen llamadas a funciones de Secur32.lib, que deben incluirse entre las bibliotecas de vínculos.


```C++
//--------------------------------------------------------------------
//   Declare and initialize local variables.

SecPkgContext_Sizes ContextSizes;
char *MessageBuffer = "This is a sample buffer to be signed.";
DWORD MessageBufferSize = strlen(MessageBuffer);
SecBufferDesc InputBufferDescriptor;
SecBuffer InputSecurityToken[2];

ss = QueryContextAttributes(
    &phContext,
    SECPKG_ATTR_SIZES,
    &ContextSizes
    );
if(ContextSizes.cbMaxSignature == 0)
{
     MyHandleError("This session does not support message signing.");
}
//--------------------------------------------------------------------
// The message as a byte string is in the variable 
// MessageBuffer, and its length is in MessageBufferSize. 

//--------------------------------------------------------------------
// Build the buffer descriptor and the buffers 
// to pass to the MakeSignature call.

InputBufferDescriptor.cBuffers = 2;
InputBufferDescriptor.pBuffers = InputSecurityToken;
InputBufferDescriptor.ulVersion = SECBUFFER_VERSION;

//--------------------------------------------------------------------
// Build a security buffer for the message itself. If 
// the SECBUFFER_READONLY attribute is set, the buffer will not be
// signed.

InputSecurityToken[0].BufferType = SECBUFFER_DATA;
InputSecurityToken[0].cbBuffer = MessageBufferSize;
InputSecurityToken[0].pvBuffer = MessageBuffer;

//--------------------------------------------------------------------
// Allocate and build a security buffer for the message
// signature.

InputSecurityToken[1].BufferType = SECBUFFER_TOKEN;
InputSecurityToken[1].cbBuffer = ContextSizes.cbMaxSignature;
InputSecurityToken[1].pvBuffer = 
        (void *)malloc(ContextSizes.cbMaxSignature);

//--------------------------------------------------------------------
// Call MakeSignature 
// For the NTLM package, the sequence number need not be specified 
// because the package provides sequencing.
// The quality of service parameter is ignored.

Ss = MakeSignature(
    &phContext,
    0,                       // no quality of service
    &InputBufferDescriptor,  // input message descriptor
    0                        // no sequence number
    );
if (SEC_SUCCESS(ss))
{
     printf("Have made a signature.\n");
}
else
{ 
    MyHandleError("MakeSignature Failed."); 
}

//--------------------------------------------------------------------
//  Send the message.

if(!SendMsg(
    s,
    (BYTE *)InputSecurityToken[0].pvBuffer,
    InputSecurityToken[0].cbBuffer))
{
     MyHandleError("The message was not sent.");
}

//--------------------------------------------------------------------
//   Send the signature.

if(!SendMsg(
     s,
    (BYTE *)InputSecurityToken[1].pvBuffer,
    InputSecurityToken[1].cbBuffer ))
{
     MyHandleError("The signature was not sent.");
}
```



[**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) devuelve **TRUE si** el contexto está configurado para permitir la firma de mensajes y si el descriptor del búfer de entrada tiene el formato correcto. Una vez firmado el mensaje, el mensaje y la firma con sus longitudes se envían al equipo remoto.

> [!Note]  
> Se envía el contenido de datos de las [**estructuras SecBuffer,**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) no las propias estructuras **SecBuffer** ni [**la estructura SecBufferDesc.**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) La **aplicación** receptora crea nuevas estructuras secBuffer y una nueva estructura **SecBufferDesc** para comprobar la firma.

 

 

 
