---
description: En el ejemplo siguiente se muestra el código de servidor RSA/Schannel típico para crear una clave maestra.
ms.assetid: 617cda1e-0619-4162-85eb-d1f5aa35fd1c
title: Código de servidor RSA para crear la clave maestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c337ef8093dc2dead96e55e481781ff902ee2485
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687586"
---
# <a name="rsa-server-code-for-creating-the-master-key"></a><span data-ttu-id="a0d28-103">Código de servidor RSA para crear la clave maestra</span><span class="sxs-lookup"><span data-stu-id="a0d28-103">RSA Server Code for Creating the Master Key</span></span>

<span data-ttu-id="a0d28-104">En el ejemplo siguiente se muestra el código de servidor RSA/Schannel típico para crear una [*clave maestra*](../secgloss/m-gly.md).</span><span class="sxs-lookup"><span data-stu-id="a0d28-104">The following example shows typical RSA/Schannel server-side code for creating a [*master key*](../secgloss/m-gly.md).</span></span>


```C++
//--------------------------------------------------------------------
//   Define and initialize local variables.

HCRYPTPROV hProv         = <server's key container>;
PBYTE      pbKeyExchange = <pointer to RSA envelope>;
DWORD      dwKeyExchange = <size of RSA envelope>;
HCRYPTKEY  hPublicKey;
HCRYPTKEY  hMasterKey;
ALG_ID     Algid;
DWORD      dwFlags =0 ;
BYTE       rgbBlob[<max BLOB size>];
DWORD      cbBlob;

//--------------------------------------------------------------------
// Select the master key type.

switch(<protocol being used>)
{
    case <PCT 1.0>:
        Algid = CALG_PCT1_MASTER;
        break;

    case <SSL 2.0>:
        Algid = CALG_SSL2_MASTER;
        if(<we support SSL3>)
            dwFlags = CRYPT_SSL2_FALLBACK;
        break;

    case <SSL 3.0>:
        Algid = CALG_SSL3_MASTER;
        break;

    case <TLS 1.0>:
        Algid = CALG_TLS1_MASTER;
        break;
}

//--------------------------------------------------------------------
// Build a SIMPLEBLOB around the RSA envelope.
{
     BLOBHEADER *pBlobHeader = (BLOBHEADER *)rgbBlob;
     ALG_ID     *pAlgid      = (ALG_ID *)(pBlobHeader + 1);
     BYTE       *pData       = (BYTE *)(pAlgid + 1);

     pBlobHeader->bType    = SIMPLEBLOB;
     pBlobHeader->bVersion = CUR_BLOB_VERSION;
     pBlobHeader->reserved = 0;
     pBlobHeader->aiKeyAlg = Algid;

     *pAlgid = CALG_RSA_KEYX;

     ReverseMemCopy(
         pData, 
         pbKeyExchange, 
         cbKeyExchange);
}

//--------------------------------------------------------------------
// Decrypt the master key.

CryptGetUserKey(
         hProv, 
         AT_KEYEXCHANGE, 
         &hPublicKey);

CryptImportKey(
          hProv, 
          rgbBlob, 
          cbBlob, 
          hPublicKey, 
          dwFlags, 
          &hMasterKey);

CryptDestroyKey(hPublicKey);
```



 

 
