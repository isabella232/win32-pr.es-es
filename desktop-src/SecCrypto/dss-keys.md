---
description: Explica cómo generar, recuperar, comprobar y exportar claves y firmas DSS.
ms.assetid: d28fe531-af4b-4b5e-ab67-47ef70f8fa5b
title: Claves de DSS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f6ab8adcc4d551c4196e99ce48f5afdd380dc3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648179"
---
# <a name="dss-keys"></a>Claves de DSS

-   [Generación y recuperación de claves de DSS](#generating-and-retrieving-dss-keys)
-   [Generación de firmas de DSS](#generating-dss-signatures)
-   [Comprobación de una firma DSS](#verifying-a-dss-signature)
-   [Exportación de claves DSS](#exporting-dss-keys)

## <a name="generating-and-retrieving-dss-keys"></a>Generación y recuperación de claves de DSS

Las claves DSS se pueden generar mediante una llamada a la función [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) . La llamada a **CryptGenKey** requiere que \_ se pase en Signature o CALG \_ DSS \_ Sign en el argumento *algid* . Esta llamada generará los valores P (módulo primo), Q (Prime), G (generator), X (exponente secreto) e y (clave pública) desde cero y los conservará en un [*BLOB de clave*](../secgloss/k-gly.md) en el almacenamiento local.

**Para generar un par de claves de firma DSS**

1.  Llame a la función [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor de servicios criptográficos de Microsoft DSS.
2.  Llame a [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) para generar las claves. Se \_ debe pasar en Signature o CALG \_ DSS \_ Sign para el argumento *algid* y los 16 bits superiores del argumento *dwFlags* deben establecerse en el tamaño de clave deseado. Si los 16 bits superiores son cero, se usará el tamaño de clave predeterminado de 1.024 bits. En el argumento *hKey* se devuelve un identificador [**HCRYPTKEY**](hcryptkey.md) .

**Para recuperar un puntero a las claves de firma previamente generadas**

1.  Llame a [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor de servicios criptográficos de Microsoft DSS.
2.  Llame a la función [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) con el argumento *dwKeySpec* establecido en \_ Signature o CALG \_ DSS \_ Sign.

**Para recuperar los valores P, Q y G**

1.  Llame a [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor de servicios criptográficos de Microsoft DSS.
2.  Llame a [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) con el argumento *dwKeySpec* establecido en \_ Signature o CALG \_ DSS \_ Sign.
3.  Llame a [**CryptGetKeyParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam) con el argumento *hKey* establecido en el puntero recuperado en el paso anterior. El argumento *dwParam* debe establecerse en la marca deseada; KP \_ P, KP \_ Q o KP \_ G. El valor se devuelve en el argumento *pbData* y la longitud de los datos se devuelve en el argumento *pdwDataLen* . El valor se devuelve sin información de encabezado y en formato [*Little-Endian*](../secgloss/l-gly.md) .

## <a name="generating-dss-signatures"></a>Generación de firmas de DSS

Los datos que se van a firmar [*deben aplicarse*](../secgloss/h-gly.md) en primer lugar mediante el algoritmo [*Sha*](../secgloss/s-gly.md) . Una vez que se aplica un algoritmo hash a los datos, se genera una firma [*DSS*](../secgloss/d-gly.md) mediante una llamada a la función [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) .

**Para generar una firma DSS**

1.  Llame a [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor de servicios criptográficos de Microsoft DSS.
2.  Llame a [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) con el argumento *ALGID* establecido en CALG \_ Sha para obtener un identificador de un objeto hash Sha.
3.  Llame a [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) con el argumento *hHash* establecido en el identificador recuperado en el paso anterior. Esto crea un hash de los datos y devuelve un identificador para el hash en el argumento *phHash* de la llamada a la función [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) .
4.  Llame a [**CryptSignHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha) con el argumento *hHash* establecido en el identificador recuperado en el paso anterior. \_ \_ \_ En el parámetro *dwKeySpec* se puede pasar en Signature o CALG DSS Sign. La firma se devuelve a la dirección proporcionada en el argumento *pbSignature* y la longitud de la firma se devuelve a la dirección proporcionada en el argumento *pdwSigLen* . Se puede pasar un puntero **null** en el argumento *pbSignature* y, en este caso, no se genera la firma, pero la longitud de la firma se devuelve a la dirección proporcionada en el parámetro *pdwSigLen* .

## <a name="verifying-a-dss-signature"></a>Comprobación de una firma DSS

Para comprobar una firma DSS, se debe importar la clave pública DSS del firmante, se debe aplicar un algoritmo hash a los [*datos firmados*](../secgloss/s-gly.md) y, a continuación, se puede comprobar la firma.

**Para comprobar una firma DSS**

1.  Llame a [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor de servicios criptográficos de Microsoft DSS.
2.  Llame a [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) para importar la clave pública de DSS del firmante.
3.  Llame a [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) con el argumento *ALGID* establecido en CALG \_ Sha para obtener un identificador de un objeto hash Sha.
4.  Llame a [**CryptHashData**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata) con el argumento *hHash* establecido en el identificador recuperado en el paso anterior y con *pbData* que apunta a los datos firmados. Esto crea un hash de los datos y devuelve un identificador para el hash en el argumento *phHash* de la llamada a la función [**CryptCreateHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash) .
5.  Llame a [**CryptVerifySignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea) con la siguiente configuración:

    *hHash* se establece en el identificador del hash realizado en el paso anterior.

    *pbSignature* apunta a la firma que se va a comprobar.

    *dwSigLen* se establece en la longitud de la firma.

    *hPubKey* se establece en el identificador de la clave pública importada en el paso 2.

    *dwFlags* se establece en cero.

## <a name="exporting-dss-keys"></a>Exportación de claves DSS

Cuando se envían [*datos firmados*](../secgloss/s-gly.md) a alguien en el que la firma debe ser comprobada por el destinatario, se debe proporcionar la clave pública del firmante al destinatario y normalmente se envía junto con los datos firmados. Por lo tanto, es necesario poder exportar las claves [*DSS*](../secgloss/d-gly.md) en un formato [*BLOB de clave*](../secgloss/k-gly.md) .

**Para exportar la clave pública de DSS**

1.  Llame a [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) para obtener un identificador para el proveedor de servicios criptográficos de Microsoft DSS.
2.  Llame a [**CryptGetUserKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey) con el argumento *dwKeySpec* establecido en \_ Signature o CALG \_ DSS \_ Sign.
3.  Llame a [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey) con *hKey* establecido en el identificador recuperado en el paso anterior, *DwBlobType* establecido en PUBLICKEYBLOB y *dwFlags* establecido en cero. El [*BLOB de clave pública*](../secgloss/p-gly.md) de DSS se devuelve en *pbData* y la longitud del [*BLOB de clave*](../secgloss/k-gly.md) se devuelve en *pdwDataLen*. Se puede pasar un puntero **nulo** en *pbData* y, en este caso, solo se devolverá la longitud del BLOB de la clave DSS. El BLOB devuelto al hacer la llamada a **CryptExportKey** está en el formato descrito en [blobs de clave del proveedor de DSS](dss-provider-key-blobs.md).

**Para exportar la clave privada de DSS**

-   Siga el mismo procedimiento que para exportar una clave pública de DSS, salvo que al realizar la llamada a [**CryptExportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey), *dwBlobType* se establece en PRIVATEKEYBLOB. El BLOB devuelto al hacer la llamada a **CryptExportKey** está en el formato descrito en [blobs de clave del proveedor de DSS](dss-provider-key-blobs.md).

 

 
