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
# <a name="shamd5-rsa-signature-type"></a>Tipo de firma RSA SHA/MD5

Los CSP de provisión de \_ RSA \_ Schannel deben admitir el hash de CALG \_ SSL3 \_ SHAMD5 que es compatible con el proveedor de servicios criptográficos de base de Microsoft usado en la autenticación de cliente SSL 3,0 y TLS 1,0. [](../secgloss/h-gly.md) Este hash se compone de una concatenación de un hash [*MD5*](../secgloss/m-gly.md) y un hash Sha firmado con una clave privada RSA o Diffie-Hellman. Se crea un identificador para un valor hash de este tipo mediante la función [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) o [**CPCreateHash**](https://www.bing.com/search?q=**CPCreateHash**) con CALG \_ SSL3 \_ SHAMD5 como parámetro *algid* . Los ejemplos de uso de funciones hash se pueden ver en [el ejemplo c programa: crear y aplicar un algoritmo hash a una clave de sesión y un](example-c-program-creating-and-hashing-a-session-key.md) [programa de ejemplo c: firmar un hash y comprobar la firma hash](example-c-program-signing-a-hash-and-verifying-the-hash-signature.md).

 

 
