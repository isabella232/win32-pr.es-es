---
description: Cómo generar, recuperar y exportar claves RSA/Schannel.
ms.assetid: 3069232f-d016-4973-ae39-89b0e2a03cd7
title: Claves RSA/Schannel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93c9d23de40f32a499013928086ccb52fc1d1e67
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160746"
---
# <a name="rsaschannel-keys"></a>Claves RSA/Schannel

## <a name="generating-and-retrieving-rsaschannel-keys"></a>Generación y recuperación de claves RSA/Schannel

[*RSA*](../secgloss/r-gly.md) / [*Las claves*](../secgloss/s-gly.md) de Schannel se pueden generar mediante una llamada a la [**función CryptGenKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) La llamada a **CryptGenKey requiere** un identificador de algoritmo AT \_ KEYEXCHANGE pasado en el *parámetro Algid.*

**Para generar un par de claves pública/privada RSA/Schannel**

1.  Llame a [**la función CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor [criptográfico RSA/Schannel de Microsoft](microsoft-rsa-schannel-cryptographic-provider.md).
2.  Llame a [**la función CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para generar las claves. AT KEYEXCHANGE debe pasarse para el parámetro Algid y los 16 bits superiores del parámetro dwFlags deben establecerse en el tamaño de clave \_ deseado (512 bits).   Se devuelve un identificador de estructura [**HCRYPTKEY**](hcryptkey.md) en el *parámetro hKey.*

**Para recuperar un puntero a claves de usuario RSA/Schannel generadas previamente**

1.  Llame a [**la función CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor [criptográfico RSA/Schannel de Microsoft](microsoft-rsa-schannel-cryptographic-provider.md).
2.  Llame a [**la función CryptGetUserKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) con el *parámetro dwKeySpec* establecido en AT \_ KEYEXCHANGE.

## <a name="exporting-rsaschannel-keys"></a>Exportación de claves RSA/Schannel

[*Las claves maestras*](../secgloss/m-gly.md) se pueden exportar en estructuras BLOB de clave simples. Esto debe implementarse de la misma manera que la exportación de claves de cifrado masivo [*rc4*](../secgloss/r-gly.md) normales o estándar de cifrado de datos [](../secgloss/d-gly.md) (DES), [](../secgloss/b-gly.md)como se describe en Blob de clave [simple](https://www.bing.com/search?q=Simple+Key+BLOB). El **miembro aiKeyAlg** de la estructura [**PUBLICKEYSTRUC**](/windows/desktop/api/Wincrypt/ns-wincrypt-publickeystruc) se establece en el identificador del algoritmo de la clave maestra (CALG \_ PCT1 \_ MASTER, CALG \_ SSL2 \_ MASTER, CALG SSL3 MASTER o \_ \_ CALG \_ TLS1 \_ MASTER).

Si la función [**CPExportKey**](https://www.bing.com/search?q=**CPExportKey**) exporta una clave maestra SSL2 y se establece la marca FALLBACK CRYPT SSL2, para ayudar a evitar ataques de reversión de versiones, establezca los primeros ocho bytes del relleno del bloque de cifrado en 0x03 en lugar de en datos \_ \_ aleatorios. [](../secgloss/p-gly.md)

Si se **especifica la \_ constante CRYPT DESTROYKEY** en el parámetro *dwFlags* de la función [**CPExportKey,**](https://www.bing.com/search?q=**CPExportKey**) el CSP destruye la clave o el identificador de clave después de exportar la clave. Esta marca está pensada para usarse solo con [*blobs opacos.*](../secgloss/o-gly.md)

 

 
