---
description: Cuando un cliente y un servidor finalizan la configuración del contexto de seguridad, se pueden usar las funciones de compatibilidad con mensajes.
ms.assetid: a65054bd-31cb-4842-af59-82cfe799fb70
title: Firmar un mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 36f8151a66120575bfcaeda62955a7f6aa47e8e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105668261"
---
# <a name="signing-a-message"></a><span data-ttu-id="14d38-103">Firmar un mensaje</span><span class="sxs-lookup"><span data-stu-id="14d38-103">Signing a Message</span></span>

<span data-ttu-id="14d38-104">Cuando un cliente y un servidor finalizan la configuración del [*contexto de seguridad*](../secgloss/s-gly.md), se pueden usar las funciones de compatibilidad con mensajes.</span><span class="sxs-lookup"><span data-stu-id="14d38-104">When a client and server finish setting up the [*security context*](../secgloss/s-gly.md), message support functions can be used.</span></span> <span data-ttu-id="14d38-105">El cliente y el servidor usan el token de contexto de seguridad creado cuando se estableció la sesión para llamar a las funciones [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) y [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) .</span><span class="sxs-lookup"><span data-stu-id="14d38-105">The client and server use the security context token created when the session was established to call [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) and [**VerifySignature**](/windows/desktop/api/Sspi/nf-sspi-verifysignature) functions.</span></span> <span data-ttu-id="14d38-106">El token de contexto se puede usar con [**EncryptMessage (general)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) y [**DecryptMessage (general)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) para la [*privacidad*](../secgloss/p-gly.md)de las comunicaciones.</span><span class="sxs-lookup"><span data-stu-id="14d38-106">The context token can be used with [**EncryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-encryptmessage) and [**DecryptMessage (General)**](/windows/win32/api/sspi/nf-sspi-decryptmessage) for communications [*privacy*](../secgloss/p-gly.md).</span></span>

<span data-ttu-id="14d38-107">En el ejemplo siguiente se muestra el lado cliente que genera un mensaje firmado para enviar al servidor.</span><span class="sxs-lookup"><span data-stu-id="14d38-107">The following example shows the client side generating a signed message to send to the server.</span></span> <span data-ttu-id="14d38-108">Antes de llamar a [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), el cliente llama a [**QueryContextAttributes (general)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) con una estructura de [**\_ tamaños SecPkgContext**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) para determinar la longitud del búfer necesario para contener la firma del mensaje.</span><span class="sxs-lookup"><span data-stu-id="14d38-108">Before calling [**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature), the client calls [**QueryContextAttributes (General)**](/windows/win32/api/sspi/nf-sspi-querycontextattributesa) with a [**SecPkgContext\_Sizes**](/windows/desktop/api/Sspi/ns-sspi-secpkgcontext_sizes) structure to determine the length of the buffer needed to hold the message signature.</span></span> <span data-ttu-id="14d38-109">Si el miembro **cbMaxSignature** es cero, el [*paquete de seguridad*](../secgloss/s-gly.md) no admite la firma de mensajes.</span><span class="sxs-lookup"><span data-stu-id="14d38-109">If the **cbMaxSignature** member is zero, the [*security package*](../secgloss/s-gly.md) does not support signing messages.</span></span> <span data-ttu-id="14d38-110">De lo contrario, este miembro indica el tamaño del búfer que se va a asignar para recibir la firma.</span><span class="sxs-lookup"><span data-stu-id="14d38-110">Otherwise, this member indicates the size of the buffer to allocate to receive the signature.</span></span>

<span data-ttu-id="14d38-111">En el ejemplo se da por supuesto que se inicializa una variable **SecHandle** denominada *phContext* y una estructura de **socket** denominada *s* .</span><span class="sxs-lookup"><span data-stu-id="14d38-111">The example assumes that a **SecHandle** variable named *phContext* and a **SOCKET** structure named *s* are initialized.</span></span> <span data-ttu-id="14d38-112">Para obtener las declaraciones e iniciaciones de estas variables, vea [usar SSPI con un cliente de Windows Sockets](using-sspi-with-a-windows-sockets-client.md) y [usar SSPI con un servidor de Windows Sockets](using-sspi-with-a-windows-sockets-server.md).</span><span class="sxs-lookup"><span data-stu-id="14d38-112">For the declarations and initiations of these variables, see [Using SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md) and [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span> <span data-ttu-id="14d38-113">En este ejemplo se incluyen las llamadas a funciones en SECUR32. lib, que deben incluirse entre las bibliotecas de vínculos.</span><span class="sxs-lookup"><span data-stu-id="14d38-113">This example includes calls to functions in Secur32.lib, which must be included among the link libraries.</span></span>


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



<span data-ttu-id="14d38-114">[**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) devuelve **true** si el contexto está configurado para permitir la firma de mensajes y si el descriptor de búfer de entrada tiene el formato correcto.</span><span class="sxs-lookup"><span data-stu-id="14d38-114">[**MakeSignature**](/windows/desktop/api/Sspi/nf-sspi-makesignature) returns **TRUE** if the context is set up to allow signing messages and if the input buffer descriptor is correctly formatted.</span></span> <span data-ttu-id="14d38-115">Una vez firmado el mensaje, el mensaje y la firma con sus longitudes se envían al equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="14d38-115">After the message is signed, the message and the signature with their lengths are sent to the remote computer.</span></span>

> [!Note]  
> <span data-ttu-id="14d38-116">Se envían los datos del contenido de las estructuras [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) , no las estructuras **SecBuffer** ni la estructura [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) .</span><span class="sxs-lookup"><span data-stu-id="14d38-116">The data contents of the [**SecBuffer**](/windows/desktop/api/Sspi/ns-sspi-secbuffer) structures are sent, not the **SecBuffer** structures themselves nor the [**SecBufferDesc**](/windows/desktop/api/Sspi/ns-sspi-secbufferdesc) structure.</span></span> <span data-ttu-id="14d38-117">La aplicación receptora crea nuevas estructuras **SecBuffer** y una nueva estructura **SecBufferDesc** para comprobar la firma.</span><span class="sxs-lookup"><span data-stu-id="14d38-117">New **SecBuffer** structures and a new **SecBufferDesc** structure are created by the receiving application to verify the signature.</span></span>

 

 

 
