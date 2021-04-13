---
description: En el ejemplo siguiente se muestra el código para recibir y comprobar un mensaje firmado. En el ejemplo se recibe el búfer de firma y su tamaño en SignatureBuffer y SignatureBufferSize, y en el búfer de mensajes y su tamaño en MessageBuffer y MessageBufferSize.
ms.assetid: 3e71aa0f-d135-4311-96f3-305762543627
title: Comprobación de un mensaje
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ebf62be707efcbd3ab3a5eca5345261ca1a0fde
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104360233"
---
# <a name="verifying-a-message"></a><span data-ttu-id="0f3dd-104">Comprobación de un mensaje</span><span class="sxs-lookup"><span data-stu-id="0f3dd-104">Verifying a Message</span></span>

<span data-ttu-id="0f3dd-105">En el ejemplo siguiente se muestra el código para recibir y comprobar un mensaje firmado.</span><span class="sxs-lookup"><span data-stu-id="0f3dd-105">The following example shows code to receive and verify a signed message.</span></span> <span data-ttu-id="0f3dd-106">En el ejemplo se recibe el búfer de firma y su tamaño en SignatureBuffer y SignatureBufferSize, y en el búfer de mensajes y su tamaño en MessageBuffer y MessageBufferSize.</span><span class="sxs-lookup"><span data-stu-id="0f3dd-106">The example receives the signature buffer and its size in SignatureBuffer and SignatureBufferSize and the message buffer and its size in MessageBuffer and MessageBufferSize.</span></span>

<span data-ttu-id="0f3dd-107">En el ejemplo se da por supuesto que se inicializa una variable **SecHandle** denominada phContext y una estructura de **socket** denominada s.</span><span class="sxs-lookup"><span data-stu-id="0f3dd-107">The example assumes that a **SecHandle** variable named phContext and a **SOCKET** structure named s are initialized.</span></span> <span data-ttu-id="0f3dd-108">Para obtener las declaraciones e iniciaciones de estas variables, vea [usar SSPI con un cliente de Windows Sockets](using-sspi-with-a-windows-sockets-client.md) y [usar SSPI con un servidor de Windows Sockets](using-sspi-with-a-windows-sockets-server.md).</span><span class="sxs-lookup"><span data-stu-id="0f3dd-108">For the declarations and initiations of these variables, see [Using SSPI with a Windows Sockets Client](using-sspi-with-a-windows-sockets-client.md) and [Using SSPI with a Windows Sockets Server](using-sspi-with-a-windows-sockets-server.md).</span></span> <span data-ttu-id="0f3dd-109">Este código incluye llamadas a funciones en SECUR32. lib, que deben incluirse entre las bibliotecas de vínculos.</span><span class="sxs-lookup"><span data-stu-id="0f3dd-109">This code includes calls to functions in Secur32.lib, which must be included among the link libraries.</span></span>


```C++
//--------------------------------------------------------------------
//  Declare and initialize local variables.
#include <windows.h>
#include <stdio.h>
#include <sspi.h>

#define SECURITY_WIN32
#define MaxMessageLength 1024
#define BUFSIZ 512

void main()
{
    BYTE MessageBuffer[BUFSIZ];
    BYTE SignatureBuffer[BUFSIZ];
    DWORD MessageBufferSize;
    DWORD SignatureBufferSize;
    SECURITY_STATUS SecStatus;
    SecBufferDesc InputBufferDescriptor;
    SecBuffer InputSecurityToken[2];
    ULONG fQOP;

    //------------------------------------------------------------------
    //    Receive the message.

    if(!(ReceiveMsg(
         s,
         MessageBuffer,
         MaxMessageLength,
         &MessageBufferSize)))
    {
         MyHandleError("Error. Message not received.");
    }

    //------------------------------------------------------------------
    //    Receive the signature.

    if(!(ReceiveMsg(
         s,
         SignatureBuffer,
         MaxMessageLength,
         &SignatureBufferSize)))
    {
         MyHandleError("Error. Signature not received.");
    }

    //------------------------------------------------------------------
    // Build the input buffer descriptor.

    InputBufferDescriptor.cBuffers = 2;
    InputBufferDescriptor.pBuffers = InputSecurityToken;
    InputBufferDescriptor.ulVersion = SECBUFFER_VERSION;

    //-------------------------------------------------------------------
    // Build the security buffer for the message.

    InputSecurityToken[0].BufferType = SECBUFFER_DATA;
    InputSecurityToken[0].cbBuffer = MessageBufferSize;
    InputSecurityToken[0].pvBuffer = MessageBuffer;

    //-------------------------------------------------------------------
    // Build the security buffer for the signature.

    InputSecurityToken[1].BufferType = SECBUFFER_TOKEN;
    InputSecurityToken[1].cbBuffer = SignatureBufferSize;
    InputSecurityToken[1].pvBuffer = SignatureBuffer;

    //--------------------------------------------------------------------
    // Call VerifySignature. 

    SecStatus = VerifySignature(
          &phContext,
          &InputBufferDescriptor,  // input message descriptor
          0,                       // no sequence number
          &fQOP                    // quality of protection
          );
    if(SecStatus == SEC_E_OK)
    {
         printf("The signature verified the message.\n");
    }
    else
         if(SecStatus == SEC_E_MESSAGE_ALTERED)
         {
              printf("The message was altered in transit.\n");
         }
         else
              if(SecStatus == SEC_E_OUT_OF_SEQUENCE )
              {
                  printf("The message is out of sequence.\n");
              }
              else
              {
                  printf("An unknown error occurred in VerifyMessage.\n");
              }
}
```



 

 



