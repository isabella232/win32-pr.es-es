---
description: En el ejemplo siguiente se muestra el código típico del lado cliente RSA/Schannel para crear una clave maestra.
ms.assetid: 9ce4877f-e6e6-4b94-9503-092d2702b31f
title: Código de cliente RSA para crear la clave maestra
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c110519938d7aa44bd4ba4af62e258d870d40652713de38f8f8fc7fa9308e5b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117974779"
---
# <a name="rsa-client-code-for-creating-the-master-key"></a>Código de cliente RSA para crear la clave maestra

En el ejemplo siguiente se muestra el código típico del lado cliente RSA/Schannel para crear una [*clave maestra*](../secgloss/m-gly.md).


```C++
//--------------------------------------------------------------------
//   Define and initialize local variables.

HCRYPTPROV hProv      = <protocol engine's key container>;
HCRYPTKEY  hPublicKey = <server's public key>;
HCRYPTKEY  hMasterKey;       // handle for master key to be created.
ALG_ID     Algid;
DWORD      dwGenFlags =CRYPT_EXPORTABLE;
DWORD          dwExportFlags =0;
BYTE       rgbBlob[<max BLOB size>];
DWORD      cbBlob;

//--------------------------------------------------------------------
// The method for creating the master key depends upon the protocol 
// in use. Schannel protocols include:
//           PCT 1.0
//           SSL 2.0
//           SSL 3.0
//           TLS 1.0     

//--------------------------------------------------------------------
// Select the master key type.

switch(<protocol being used>)
{
    case <PCT 1.0>:
        Algid = CALG_PCT1_MASTER;
        break;

    case <SSL 2.0>:
        Algid = CALG_SSL2_MASTER;
        dwGenFlags |=,key size. << 16;
        if(<SSL3 or TLS is supported>)
            dwExportFlags |= CRYPT_SSL2_FALLBACK;
        break;

    case <SSL 3.0>:
        Algid = CALG_SSL3_MASTER;
        break;

    case <TLS 1.0>:
        Algid = CALG_TLS1_MASTER;
        break;
}

//--------------------------------------------------------------------
// Generate the master key.

CryptGenKey(
         hProv, 
         Algid, 
         dwGenFlags, 
          &hMasterKey);

//--------------------------------------------------------------------
// Export the master key.

cbBlob = sizeof(rgbBlob);
CryptExportKey(
         hMasterKey, 
         hPublicKey, 
         SIMPLEBLOB,
         dwExportFlags, 
         rgbBlob, 
         &cbBlob);
```



 

 
