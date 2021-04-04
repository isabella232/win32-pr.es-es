---
description: Validar la cadena de certificados
ms.assetid: e0c36f04-1694-40d8-94a1-06ee7de08777
title: Validar la cadena de certificados
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 13436513ae9199feb7ba5fcba399537da198ba85
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277586"
---
# <a name="validating-the-certificate-chain"></a>Validar la cadena de certificados

En este tema se describe cómo validar la cadena de certificados del controlador cuando se usa el protocolo de protección de la salida certificada (COPP).

La cadena de certificados del controlador gráfico es un documento XML. La cadena de certificados contiene tres certificados. El primer certificado se denomina *certificado de hoja* y es el certificado COPP del controlador. El siguiente certificado es el certificado de firma del proveedor de hardware independiente (IHV). El último certificado es el certificado de firma de Microsoft. Para asegurarse de que el controlador de gráficos es un dispositivo COPP legítimo, la aplicación debe validar los tres certificados. Un programa malintencionado puede impedir que COPP funcione si una aplicación no valida correctamente los certificados de la cadena.

Las cadenas de certificados COPP utilizan el juego de caracteres UTF-8. Los datos binarios de los certificados, como la clave pública RSA, se codifican en Base64 y se almacenan en orden Big-Endian. (*Big-Endian* significa que el byte más significativo se almacena en la ubicación de memoria con la dirección más baja).

Algunos elementos de un certificado contienen valores booleanos para indicar que existe una característica del certificado. Si la característica existe, el valor del elemento secundario correspondiente se establece en 1. Si una característica no está presente, ese elemento secundario no está presente en el certificado.

### <a name="xml-element-definitions"></a>Definiciones de elementos XML

A continuación se enumeran las definiciones de los elementos del esquema de certificado:

-   **CertificateCollection**. Elemento raíz del documento XML. Contiene elementos de certificado, uno para cada certificado de la cadena.
-   **Certificado**. Contiene un certificado. Este elemento contiene datos y elementos de firma.
-   **Data**. Contiene información sobre el certificado. En concreto, contiene la clave pública y el tipo del certificado. El elemento de datos contiene los siguientes elementos secundarios:
    -   **PublicKey**. Contiene la clave pública RSA del certificado. El elemento PublicKey contiene un elemento KeyValue, que contiene un elemento RSAKeyValue. El elemento RSAKeyValue tiene dos elementos secundarios, el módulo y el exponente, y estos definen la clave pública. Los elementos de módulo y exponente se codifican en Base64 y se almacenan en orden Big-Endian.
    -   **KeyUsage**. Si el certificado es el certificado COPP del controlador, este elemento debe contener un elemento secundario denominado EncryptKey. Si el certificado es el certificado de firma de IHV o el certificado de firma de Microsoft, debe contener un elemento secundario denominado SignCertificate. Ambos elementos secundarios contienen valores booleanos.
    -   **SecurityLevel**. Este elemento se debe omitir.
    -   **ManufacturerData**. Especifica el fabricante y el modelo del dispositivo de gráficos. Este elemento es meramente informativo.
    -   **Features**. Contiene elementos secundarios que especifican el uso del certificado. El único que es relevante para COPP es el elemento COPPCertificate. Pueden estar presentes otros elementos secundarios; Si es así, se deben omitir. Si el elemento COPPCertificate existe, el certificado es un certificado COPP. Este elemento debe estar presente en el nodo hoja de un certificado COPP válido. Este elemento contiene un valor booleano.
-   **Firma**. Contiene la firma para este certificado. Contiene los siguientes elementos secundarios:
    -   **SignedInfo**. Contiene información sobre la firma. El elemento secundario importante de este elemento es el elemento DigestValue, que contiene el valor codificado en base64 del hash SHA-1 sobre el elemento de datos. El valor de síntesis se usa al comprobar el certificado en la lista de revocación de certificados (CRL).
    -   **SignatureValue**. Este valor se calcula sobre el elemento de datos y se calcula de acuerdo con el esquema de firma digital RSASSA-PSS definido en Public-Key Cryptography Standards (PKCS) \# 1 (versión 2,1). Para obtener información acerca de PKCS \# 1, visite [https://www.rsa.com/](https://www.rsa.com/) .
    -   **KeyInfo**. Contiene la clave pública RSA del siguiente certificado de la cadena. Este elemento se usa para comprobar que los datos del elemento de datos no se han alterado. Este elemento tiene el mismo formato que el elemento PublicKey.

### <a name="certificate-validation"></a>Validación de certificados

La aplicación debe realizar los pasos siguientes para validar correctamente la cadena de certificados. Si se produce un error en algún paso, o si no existe ningún elemento al que se hace referencia en estos procedimientos, se produce un error en la validación.

### <a name="validate-certificate-collection-procedure"></a>Procedimiento para validar la colección de certificados

Para validar la cadena de certificados, realice los pasos siguientes:

1.  Compruebe que CertificateCollection sea XML con formato correcto.
2.  Compruebe que CertificateCollection está codificado en formato UTF-8.
3.  Compruebe que el atributo version del elemento CertificateCollection sea 2,0 o posterior.
4.  Compruebe que la cadena de certificados contiene exactamente tres elementos de certificado.
5.  Recorra en bucle cada elemento de certificado de la cadena de certificados y realice el procedimiento de validación del certificado, que se describe a continuación, en cada uno de ellos.

### <a name="validate-certificate-procedure"></a>Procedimiento de validación de certificado

Para validar un certificado de la cadena, realice los pasos siguientes:

1.  Compruebe que ninguno de los elementos secundarios del elemento de datos está duplicado. Por ejemplo, debería haber solo un elemento PublicKey.
2.  Asegúrese de que el elemento Data/PublicKey/KeyValue/RSAKeyValue/Modul existe. El valor descodificado en Base64 debe tener una longitud de 256 bytes para todos los certificados excepto la raíz. En el certificado raíz, este elemento debe tener una longitud de 128 bytes.
3.  Asegúrese de que el elemento Data/PublicKey/KeyValue/RSAKeyValue/Exponent exista. El valor descodificado en Base64 no debe ser mayor que 4 bytes.
4.  Si este certificado es el certificado de hoja, compruebe lo siguiente:
    -   El elemento KeyUsage contiene un elemento EncryptKey con el valor 1.
    -   El elemento Features contiene un elemento COPPCertificate con el valor 1.
5.  Si este certificado no es el certificado de hoja, compruebe lo siguiente:
    -   El módulo y el exponente del elemento Data/PublicKey coinciden exactamente con el módulo y el exponente del elemento Signature/KeyInfo del certificado anterior.
    -   El elemento KeyUsage contiene un elemento SignCertificate con el valor 1.
6.  Use el algoritmo hash SHA-1 para aplicar un algoritmo hash a cada byte del elemento de datos del certificado. Se debe aplicar un algoritmo hash a todos los bytes del primer carácter de la <Data> etiqueta al último carácter de la etiqueta de cierre </Data> . El valor hash se utiliza para comprobar el certificado con respecto a la lista de revocación de certificados (CRL), como se describe en [listas de revocación de certificados](certificate-revocation-lists.md) .
7.  Compare el valor hash del paso 6 con el valor descodificado en base64 del elemento Signature/SignedInfo/Reference/DigestValue. Estos valores deben coincidir.
8.  Realice el procedimiento de comprobación de firma, que se describe a continuación.
9.  Si este certificado no es el certificado final de la cadena, guarde el valor Signature/KeyInfo/KeyValue/RSAKeyValue para la siguiente iteración del bucle.
10. Si este certificado es el certificado final de la cadena, asegúrese de que el valor de Signature/KeyInfo/KeyValue/RSAKeyValue coincide con la clave pública de Microsoft. La clave pública de Microsoft tiene los siguientes valores codificados en Base64:
    -   Módulo

        `pjoeWLSTLDonQG8She6QhkYbYott9fPZ8tHdB128ZETcghn5KHoyin7HkJEcPJ0Eg4UdSv a0KDIYDjA3EXd69R3CN2Wp/QyOo0ZPYWYp3NXpJ700tKPgIplzo5wVd/69g7j+j8M66W7V NmDwaNs9mDc1p2+VVMsDhOsV/Au6E+E=`

    -   Exponente `AQAB`

### <a name="verify-signature-procedure"></a>Comprobar el procedimiento de firma

El valor del elemento SignatureValue se calcula sobre el elemento de datos de acuerdo con el esquema de firma digital RSASSA-PSS definido en la \# versión 2,1 de PKCS 1 (en adelante denominado PKCS). Para comprobar esta firma, realice los pasos siguientes:

1.  Descodifique los valores de módulo y exponente en el elemento Signature/KeyInfo/KeyValue/RSAKeyValue. Estos valores definen la clave pública RSA del certificado de firma.
2.  Descodifique el elemento Signature/SignatureValue.
3.  Calcule la operación RSASSA-PSS-Verify, definida en la sección 8.1.2 de PKCS.

Para la operación RSASSA-PSS-Verify, utilice las siguientes entradas:

-   (*n*,*e*) es la clave pública del paso 1.
-   *M* son todos los bytes del elemento de datos, incluidas las etiquetas <Data> y</Data> que contienen el elemento.
-   *S* es el valor de firma descodificado del paso 2.

La operación RSASSA-PSS-Verify usa la operación EMSA-PSS-encode, que se define en la sección 9.1.1. de PKCS. Para esta operación, COPP usa las siguientes opciones:

-   Hash = SHA-1
-   *hLen* = 20
-   MGF (función de generación de máscara) = MGF1
-   *sLen* = 0

La función de generación de máscara MGF1 se define en el Apéndice B. 2 de PKCS. Para esta función, COPP usa las siguientes opciones:

-   Hash = SHA-1
-   *hLen* = 20

La salida de la operación RSASSA-PSS-Verify indica si la firma es válida o no es válida.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Uso del Protocolo de protección de la salida certificada (COPP)](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



