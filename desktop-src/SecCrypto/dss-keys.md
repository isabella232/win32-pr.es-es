---
description: Explica cómo generar, recuperar, comprobar y exportar claves y firmas de DSS.
ms.assetid: d28fe531-af4b-4b5e-ab67-47ef70f8fa5b
title: Claves DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6ab8adcc4d551c4196e99ce48f5afdd380dc3a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127476481"
---
# <a name="dss-keys"></a>Claves DSS

-   [Generación y recuperación de claves DSS](#generating-and-retrieving-dss-keys)
-   [Generación de firmas DSS](#generating-dss-signatures)
-   [Comprobación de una firma de DSS](#verifying-a-dss-signature)
-   [Exportación de claves DSS](#exporting-dss-keys)

## <a name="generating-and-retrieving-dss-keys"></a>Generación y recuperación de claves DSS

Las claves DSS se pueden generar mediante una llamada a la [**función CryptGenKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) La llamada a **CryptGenKey** requiere que se pase AT \_ SIGNATURE o CALG \_ DSS \_ SIGN en el argumento *Algid.* Esta llamada generará los valores P (módulo prime), Q (prime), G (generator), X (exponente secreto) e Y (clave pública) desde cero y los conservará en un [*blob*](../secgloss/k-gly.md) de clave en el almacenamiento local.

**Para generar un par de claves de firma de DSS**

1.  Llame a [**la función CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor criptográfico de Microsoft DSS.
2.  Llame [**a CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para generar las claves. At SIGNATURE o CALG DSS SIGN deben pasarse para el argumento Algid y los 16 bits superiores del argumento \_ \_ \_ *dwFlags*  deben establecerse en el tamaño de clave deseado. Si los 16 bits superiores son cero, se usará el tamaño de clave predeterminado de 1024 bits. Se [**devuelve un identificador HCRYPTKEY**](hcryptkey.md) en el argumento *hKey.*

**Para recuperar un puntero a las claves de firma generadas previamente**

1.  Llame [**a CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor criptográfico de Microsoft DSS.
2.  Llame a [**la función CryptGetUserKey con**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) el argumento *dwKeySpec* establecido en AT \_ SIGNATURE o CALG \_ DSS \_ SIGN.

**Para recuperar los valores P, Q y G**

1.  Llame [**a CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor criptográfico de Microsoft DSS.
2.  Llame [**a CryptGetUserKey con**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) el argumento *dwKeySpec* establecido en AT \_ SIGNATURE o CALG \_ DSS \_ SIGN.
3.  Llame [**a CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) con el *argumento hKey* establecido en el puntero recuperado en el paso anterior. El *argumento dwParam* debe establecerse en la marca deseada; KP \_ P, KP \_ Q o KP \_ G. El valor se devuelve en el *argumento pbData* y la longitud de los datos se devuelve en el *argumento pdwDataLen.* El valor se devuelve sin información de encabezado y en [*formato little-endian.*](../secgloss/l-gly.md)

## <a name="generating-dss-signatures"></a>Generación de firmas DSS

Los datos que se deben firmar primero deben [*ser hash mediante*](../secgloss/h-gly.md) el algoritmo [*SHA.*](../secgloss/s-gly.md) Una vez que se aplica un algoritmo hash a los datos, se genera una [*firma DSS*](../secgloss/d-gly.md) mediante una llamada a la [**función CryptSignHash.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha)

**Para generar una firma de DSS**

1.  Llame [**a CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor criptográfico de Microsoft DSS.
2.  Llame [**a CryptCreateHash con**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) el argumento *Algid* establecido en CALG SHA para obtener un \_ identificador para un objeto hash SHA.
3.  Llame [**a CryptHashData con**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) el argumento *hHash* establecido en el identificador recuperado en el paso anterior. Esto crea un hash de los datos y devuelve un identificador al hash en el *argumento phHash* de la llamada a la función [**CryptCreateHash.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)
4.  Llame [**a CryptSignHash con**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) el argumento *hHash* establecido en el identificador recuperado en el paso anterior. Se puede pasar AT \_ SIGNATURE o CALG \_ DSS \_ SIGN en el parámetro *dwKeySpec.* La firma se devuelve a la dirección proporcionada en el *argumento pbSignature* y la longitud de la firma se devuelve a la dirección proporcionada en el *argumento pdwSigLen.* Se **puede** pasar un puntero NULL en el argumento *pbSignature* y, en este caso, no se genera la firma, pero la longitud de la firma se devuelve a la dirección proporcionada en el *parámetro pdwSigLen.*

## <a name="verifying-a-dss-signature"></a>Comprobación de una firma de DSS

Para comprobar una firma DSS, se debe importar la clave [](../secgloss/s-gly.md) pública de DSS del firmante, se deben hash los datos firmados y, a continuación, se puede comprobar la firma.

**Para comprobar una firma de DSS**

1.  Llame [**a CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor criptográfico de Microsoft DSS.
2.  Llame [**a CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) para importar la clave pública DSS del firmante.
3.  Llame [**a CryptCreateHash con**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) el argumento *Algid* establecido en CALG SHA para obtener un \_ identificador para un objeto hash SHA.
4.  Llame [**a CryptHashData con**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) el argumento *hHash* establecido en el identificador recuperado en el paso anterior y con *pbData* que apunte a los datos firmados. Esto crea un hash de los datos y devuelve un identificador al hash en el *argumento phHash* de la llamada a la función [**CryptCreateHash.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash)
5.  Llame [**a CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) con la siguiente configuración:

    *hHash se* establece en el identificador del hash realizado en el paso anterior.

    *pbSignature* apunta a la firma que se va a comprobar.

    *dwSigLen* se establece en la longitud de la firma.

    *hPubKey* se establece en el identificador de la clave pública importada en el paso 2.

    *dwFlags* se establece en cero.

## <a name="exporting-dss-keys"></a>Exportación de claves DSS

Cuando envía [](../secgloss/s-gly.md) datos firmados a alguien en el que el destinatario tendrá que comprobar la firma, la clave pública del firmante se debe proporcionar al destinatario y normalmente se envía junto con los datos firmados. Por lo tanto, es necesario poder exportar las claves [*DSS*](../secgloss/d-gly.md) en un formato [*blob de*](../secgloss/k-gly.md) clave.

**Para exportar la clave pública de DSS**

1.  Llame [**a CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor criptográfico de Microsoft DSS.
2.  Llame [**a CryptGetUserKey con**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) el argumento *dwKeySpec* establecido en AT \_ SIGNATURE o CALG \_ DSS \_ SIGN.
3.  Llame [**a CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) con *hKey* establecido en el identificador recuperado en el paso anterior, *dwBlobType* establecido en PUBLICKEYBLOB y *dwFlags* establecido en cero. El [*blob*](../secgloss/p-gly.md) de clave pública de DSS se devuelve en *pbData* y la longitud de la clave [*BLOB*](../secgloss/k-gly.md) se devuelve en *pdwDataLen.* Se puede pasar un puntero **NULL** en *pbData* y, en este caso, solo se devolverá la longitud del BLOB de clave DSS. El BLOB devuelto al realizar la llamada a **CryptExportKey** tiene el formato descrito en blobs de claves del proveedor [de DSS](dss-provider-key-blobs.md).

**Para exportar la clave privada de DSS**

-   Siga el mismo procedimiento que para exportar una clave pública DSS, salvo que al realizar la llamada a [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), *dwBlobType* se establece en PRIVATEKEYBLOB. El BLOB devuelto al realizar la llamada a **CryptExportKey** tiene el formato descrito en blobs de claves del proveedor [de DSS](dss-provider-key-blobs.md).

 

 
