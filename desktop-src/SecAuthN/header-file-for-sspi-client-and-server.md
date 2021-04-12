---
description: El siguiente archivo de encabezado debe incluirse con los ejemplos de SSPI Client y Server como SspiExample. h. Declara las funciones que controlan la comunicación con el paquete de seguridad.
ms.assetid: 358c2cd6-674b-4d70-9657-800b0d1b2fe7
title: Archivo de encabezado para el cliente y el servidor SSPI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75f2702186f7a0a9def4405890f39f588dbbfa84
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423859"
---
# <a name="header-file-for-sspi-client-and-server"></a><span data-ttu-id="a5980-104">Archivo de encabezado para el cliente y el servidor SSPI</span><span class="sxs-lookup"><span data-stu-id="a5980-104">Header File for SSPI Client and Server</span></span>

<span data-ttu-id="a5980-105">El siguiente archivo de encabezado debe incluirse con los ejemplos de SSPI Client y Server como SspiExample. h.</span><span class="sxs-lookup"><span data-stu-id="a5980-105">The following header file should be included with both the client and the server SSPI samples as SspiExample.h.</span></span> <span data-ttu-id="a5980-106">Declara las funciones que controlan la comunicación con el paquete de seguridad.</span><span class="sxs-lookup"><span data-stu-id="a5980-106">It declares functions that handle communication with the security package.</span></span>


```C++
//  SspiExample.h
#include <sspi.h>
#include <windows.h>

BOOL SendMsg (SOCKET s, PBYTE pBuf, DWORD cbBuf);
BOOL ReceiveMsg (SOCKET s, PBYTE pBuf, DWORD cbBuf, DWORD *pcbRead);
BOOL SendBytes (SOCKET s, PBYTE pBuf, DWORD cbBuf);
BOOL ReceiveBytes (SOCKET s, PBYTE pBuf, DWORD cbBuf, DWORD *pcbRead);
void cleanup();

BOOL GenClientContext (
    BYTE *pIn,
    DWORD cbIn,
    BYTE *pOut,
    DWORD *pcbOut,
    BOOL *pfDone,
    CHAR *pszTarget,
    CredHandle *hCred,
    struct _SecHandle *hcText
);

BOOL GenServerContext (
   BYTE *pIn,
   DWORD cbIn,
   BYTE *pOut,
   DWORD *pcbOut,
   BOOL *pfDone,
   BOOL  fNewCredential
);

BOOL EncryptThis (
         PBYTE pMessage, 
         ULONG cbMessage,
         BYTE ** ppOutput,
         LPDWORD pcbOutput,
         ULONG securityTrailer
    );

PBYTE DecryptThis(
         PBYTE achData, 
         LPDWORD pcbMessage,
         struct _SecHandle *hCtxt,
         ULONG   cbSecurityTrailer
);

BOOL 
SignThis (
         PBYTE pMessage, 
         ULONG cbMessage,
         BYTE ** ppOutput,
         LPDWORD pcbOutput
);

PBYTE VerifyThis(
          PBYTE pBuffer, 
          LPDWORD pcbMessage,
          struct _SecHandle *hCtxt,
          ULONG   cbMaxSignature
);

void PrintHexDump(DWORD length, PBYTE buffer);

BOOL ConnectAuthSocket (
   SOCKET *s, 
   CredHandle *hCred, 
   struct _SecHandle *hcText
);

BOOL CloseAuthSocket (SOCKET s);

BOOL DoAuthentication (SOCKET s);

void MyHandleError(char *s);

```



 

 



