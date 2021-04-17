---
description: Los CSP de provisión de \_ RSA \_ Schannel deben admitir el hash de CALG \_ SSL3 \_ SHAMD5 que es compatible con el proveedor de servicios criptográficos de base de Microsoft usado en la autenticación de cliente SSL 3,0 y TLS 1,0.
ms.assetid: ca8be4fd-e7ca-4def-927d-b168628c566e
title: Tipo de firma RSA SHA/MD5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71dcd515c61a4baf3da1fb35e4b5e6d21d5c849e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686483"
---
# <a name="shamd5-rsa-signature-type"></a><span data-ttu-id="50edb-103">Tipo de firma RSA SHA/MD5</span><span class="sxs-lookup"><span data-stu-id="50edb-103">SHA/MD5 RSA Signature Type</span></span>

<span data-ttu-id="50edb-104">Los CSP de provisión de \_ RSA \_ Schannel deben admitir el hash de CALG \_ SSL3 \_ SHAMD5 que es compatible con el proveedor de servicios criptográficos de base de Microsoft usado en la autenticación de cliente SSL 3,0 y TLS 1,0. [](../secgloss/h-gly.md)</span><span class="sxs-lookup"><span data-stu-id="50edb-104">CSPs for PROV\_RSA\_SCHANNEL must support the CALG\_SSL3\_SHAMD5 [*hash*](../secgloss/h-gly.md) that is compatible with the Microsoft Base Cryptographic Provider used in SSL 3.0 and TLS 1.0 client authentication.</span></span> <span data-ttu-id="50edb-105">Este hash se compone de una concatenación de un hash [*MD5*](../secgloss/m-gly.md) y un hash Sha firmado con una clave privada RSA o Diffie-Hellman.</span><span class="sxs-lookup"><span data-stu-id="50edb-105">This hash consists of a concatenation of an [*MD5*](../secgloss/m-gly.md) hash and a SHA hash signed with an RSA or Diffie-Hellman private key.</span></span> <span data-ttu-id="50edb-106">Se crea un identificador para un valor hash de este tipo mediante la función [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) o [**CPCreateHash**](https://www.bing.com/search?q=**CPCreateHash**) con CALG \_ SSL3 \_ SHAMD5 como parámetro *algid* .</span><span class="sxs-lookup"><span data-stu-id="50edb-106">A handle to a hash value of this type is created by using the [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) or [**CPCreateHash**](https://www.bing.com/search?q=**CPCreateHash**) function with CALG\_SSL3\_SHAMD5 as the *Algid* parameter.</span></span> <span data-ttu-id="50edb-107">Los ejemplos de uso de funciones hash se pueden ver en [el ejemplo c programa: crear y aplicar un algoritmo hash a una clave de sesión y un](example-c-program-creating-and-hashing-a-session-key.md) [programa de ejemplo c: firmar un hash y comprobar la firma hash](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md).</span><span class="sxs-lookup"><span data-stu-id="50edb-107">Examples of using hash functions can be seen in [Example C Program: Creating and Hashing a Session Key](example-c-program-creating-and-hashing-a-session-key.md) and [Example C Program: Signing a Hash and Verifying the Hash Signature](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md).</span></span>

 

 
