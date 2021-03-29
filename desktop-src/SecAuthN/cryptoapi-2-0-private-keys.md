---
description: Las credenciales de Schannel se representan internamente como estructuras de contexto de certificado \_ .
ms.assetid: 3d2deb61-8e86-4461-8f2a-4880ca5b9d34
title: CryptoAPI 2.0 claves privadas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b5180515b529e33ae385fa94688a7e8fb436bd32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105648463"
---
# <a name="cryptoapi-20-private-keys"></a>CryptoAPI 2.0 claves privadas

Las credenciales de Schannel se representan internamente como estructuras de [**\_ contexto de certificado**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) . Schannel busca la [*clave privada*](/windows/desktop/SecGloss/p-gly) asociada a un contexto de certificado determinado mediante la propiedad de certificado de la clave de la información de identificador de la clave de certificado del certificado \_ \_ \_ \_ \_ . Con esta propiedad, Schannel obtiene acceso a la *clave privada* mediante una llamada a la función [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) . Para obtener más información, vea [pares de claves pública y privada](/windows/desktop/SecCrypto/public-private-key-pairs).

Cada credencial Schannel contiene una referencia a una o varias claves privadas, cada una asociada a un certificado determinado. Las [*claves privadas*](/windows/desktop/SecGloss/p-gly) se tratan de forma bastante diferente en función de si la credencial es para un cliente o un servidor.

## <a name="client-private-keys"></a>Claves privadas de cliente

El [*proveedor de servicios criptográficos*](/windows/desktop/SecGloss/c-gly) (CSP) administra las [*claves privadas*](/windows/desktop/SecGloss/p-gly) del cliente en uso. Normalmente, las claves privadas de cliente las almacenan los CSP de la firma RSA [ \_ \_ Full](/windows/desktop/SecCrypto/prov-rsa-full) o Prov \_ RSA \_ .

Si la aplicación cliente hace que la llamada a [**CryptAcquireContext**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptacquirecontexta) sea manual, antes de llamar a [**AcquireCredentialsHandle**](/windows/win32/api/sspi/nf-sspi-acquirecredentialshandlea), el cliente debe enlazar el identificador del CSP con el contexto de certificado mediante la propiedad de identificador de prop identificador de la clave de certificado \_ \_ \_ \_ \_ . Si Schannel encuentra este conjunto de propiedades, no utiliza la propiedad del identificador de propiedades de la clave de certificado \_ \_ \_ \_ \_ .

## <a name="server-private-keys"></a>Claves privadas de servidor

Las claves privadas del servidor se almacenan en uno de los siguientes CSP:

-   aprovisionamiento de \_ RSA \_ Schannel
-   PROV \_ DH \_ Schannel
-   CSP de PROV \_ Fortezza

La elección de CSP depende del algoritmo de [*intercambio de claves*](/windows/desktop/SecGloss/k-gly)seleccionado. Las claves privadas del servidor deben ser de tipo en \_ KEYEXCHANGE.

 

 
