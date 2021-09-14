---
description: Las credenciales de Schannel se representan internamente como estructuras CERT \_ CONTEXT.
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: CryptoAPI 2.0 claves privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5180515b529e33ae385fa94688a7e8fb436bd32
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127361868"
---
# <a name="cryptoapi-20-private-keys"></a>CryptoAPI 2.0 claves privadas

Las credenciales de Schannel se representan internamente [**como estructuras CERT \_ CONTEXT.**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Schannel busca la clave [*privada asociada*](/windows/desktop/SecGloss/p-gly) a un contexto de certificado determinado mediante la propiedad CERT \_ KEY \_ PROV INFO PROP ID \_ del \_ \_ certificado. Con esta propiedad, Schannel accede a la *clave privada mediante* una llamada a la función [**CryptAcquireContext.**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) Para más información, consulte [Pares de claves públicas y privadas.](/windows/desktop/SecCrypto/public-private-key-pairs)

Cada credencial de Schannel contiene una referencia a una o varias claves privadas, cada una asociada a un certificado determinado. Las [*claves privadas*](/windows/desktop/SecGloss/p-gly) se controlan de forma bastante diferente en función de si la credencial es para un cliente o un servidor.

## <a name="client-private-keys"></a>Claves privadas de cliente

El [*proveedor de*](/windows/desktop/SecGloss/p-gly) servicios [*criptográficos*](/windows/desktop/SecGloss/c-gly) (CSP) en uso administra las claves privadas de cliente. Normalmente, las claves privadas de cliente las almacenan los CSP de tipo [PROV \_ RSA \_ FULL](/windows/desktop/SecCrypto/prov-rsa-full) o PROV \_ RSA \_ SIGNATURE.

Si la aplicación cliente realiza la llamada [**a CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) manualmente antes de llamar a [**AcquireCredentialsHandle,**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea)el cliente debe enlazar el identificador del CSP al contexto del certificado mediante la propiedad CERT \_ KEY \_ PROV HANDLE PROP \_ \_ \_ ID. Si Schannel encuentra este conjunto de propiedades, no usa la propiedad CERT \_ KEY \_ PROV \_ INFO PROP \_ \_ ID.

## <a name="server-private-keys"></a>Claves privadas del servidor

Las claves privadas del servidor las almacena uno de los siguientes CSP:

-   PROV \_ RSA \_ SCHANNEL
-   PROV \_ DH \_ SCHANNEL
-   CSP \_ de FORTEZZA PARA PROV

La elección de CSP depende del algoritmo de [*intercambio de claves seleccionado.*](/windows/desktop/SecGloss/k-gly) Las claves privadas del servidor deben ser de tipo AT \_ KEYEXCHANGE.

 

 
