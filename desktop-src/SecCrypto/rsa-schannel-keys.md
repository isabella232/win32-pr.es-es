---
description: Cómo generar, recuperar y exportar claves RSA/Schannel.
ms.assetid: 3069232f-d016-4973-ae39-89b0e2a03cd7
title: Claves RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c9d23de40f32a499013928086ccb52fc1d1e67
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541795"
---
# <a name="rsaschannel-keys"></a>Claves RSA/Schannel

## <a name="generating-and-retrieving-rsaschannel-keys"></a>Generación y recuperación de claves RSA/Schannel

[*RSA*](../secgloss/r-gly.md) / Las claves [*Schannel*](../secgloss/s-gly.md) se pueden generar mediante una llamada a la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) . La llamada a **CryptGenKey** requiere un \_ identificador de algoritmo at KEYEXCHANGE pasado en el parámetro *algid* .

**Para generar un par de claves pública/privada de RSA/Schannel**

1.  Llame a la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el [proveedor de servicios criptográficos RSA/Schannel de Microsoft](microsoft-rsa-schannel-cryptographic-provider.md).
2.  Llame a la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para generar las claves. EN \_ KEYEXCHANGE se debe pasar para el parámetro *algid* y los 16 bits superiores del parámetro *dwFlags* deben establecerse en el tamaño de clave deseado (512 bits). Se devuelve un identificador de estructura [**HCRYPTKEY**](hcryptkey.md) en el parámetro *hKey* .

**Para recuperar un puntero a claves de usuario RSA/Schannel generadas previamente**

1.  Llame a la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el [proveedor de servicios criptográficos RSA/Schannel de Microsoft](microsoft-rsa-schannel-cryptographic-provider.md).
2.  Llame a la función [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) , con el parámetro *DWKEYSPEC* establecido en en \_ KEYEXCHANGE.

## <a name="exporting-rsaschannel-keys"></a>Exportar claves RSA/Schannel

[*Las claves maestras*](../secgloss/m-gly.md) se pueden exportar en estructuras BLOB de clave simple. Esto se debe implementar del mismo modo que la exportación de [*claves de cifrado masivo*](../secgloss/b-gly.md)estándar [*RC4*](../secgloss/r-gly.md) o de [*cifrado de datos*](../secgloss/d-gly.md) (des), como se describe en [BLOB de clave simple](https://www.bing.com/search?q=Simple+Key+BLOB). El miembro **aiKeyAlg** de la estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) se establece en el identificador de algoritmo de la clave maestra (CALG \_ PCT1 \_ Master, CALG \_ SSL2 \_ Master, CALG \_ SSL3 \_ Master o CALG \_ TLS1 \_ Master).

Si la función [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) está exportando una clave maestra de SSL2 \_ y \_ se ha establecido la marca de reserva de CRYPT SSL2, para ayudar a evitar los ataques de reversión de versiones, establezca los primeros ocho bytes del [*relleno*](../secgloss/p-gly.md) de bloque de cifrado en 0x03 en lugar de en datos aleatorios.

Si se especifica la constante **CRYPT \_ DESTROYKEY** en el parámetro *DwFlags* de la función [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) , el CSP destruye la clave o el identificador de la clave después de exportar la clave. Esta marca está pensada para usarse solo con [*blobs opacos*](../secgloss/o-gly.md).

 

 
