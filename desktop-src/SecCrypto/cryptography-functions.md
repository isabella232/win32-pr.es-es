---
description: Enumera las funciones proporcionadas por CryptoAPI.
ms.assetid: 9a65f73d-6f8c-4271-a2d0-d91ad952f9c6
title: 'Funciones de criptografía '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b65c04d3cb1ff619d03d7f0340fc4f94826722f8ed6c0457987b8ec432a66128
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117768347"
---
# <a name="cryptography-functions"></a>Funciones de criptografía 

Las funciones de criptografía se clasifican según el uso como se muestra a continuación:

-   [Funciones CryptXML](#cryptxml-functions)
-   [Funciones de firmante](#signer-functions)
-   [Funciones de criptografía base](#base-cryptography-functions)
    -   [Funciones del proveedor de servicios](#service-provider-functions)
    -   [Generación de claves y funciones Exchange claves](#key-generation-and-exchange-functions)
    -   [Funciones de codificación y codificación de objetos](#object-encoding-and-decoding-functions)
    -   [Funciones de cifrado y descifrado de datos](#data-encryption-and-decryption-functions)
    -   [Funciones hash y firma digital](#hash-and-digital-signature-functions)
-   [Funciones de almacén de certificados y certificados](#certificate-and-certificate-store-functions)
    -   [Funciones del almacén de certificados](#certificate-and-certificate-store-functions)
    -   [Funciones de mantenimiento de almacén de certificados y certificados](#certificate-and-certificate-store-maintenance-functions)
    -   [Funciones de certificado](#certificate-functions)
    -   [Funciones de lista de revocación de certificados](#certificate-revocation-list-functions)
    -   [Funciones de lista de confianza de certificados](#certificate-trust-list-functions)
    -   [Funciones de propiedad extendida](#extended-property-functions)
-   [Funciones MakeCert](#makecert-functions)
-   [Funciones de comprobación de certificados](#certificate-verification-functions)
    -   [Funciones de comprobación mediante CCL](#verification-functions-using-ctls)
    -   [Funciones de comprobación de la cadena de certificados](#certificate-chain-verification-functions)
-   [Funciones de mensajes](#message-functions)
    -   [Funciones de mensaje de bajo nivel](#low-level-message-functions)
    -   [Funciones de mensaje simplificadas](#simplified-message-functions)
-   [Funciones auxiliares](#auxiliary-functions)
    -   [Administración de datos functions](#data-management-functions)
    -   [Funciones de conversión de datos](#data-conversion-functions)
    -   [Funciones de uso mejorado de claves](#enhanced-key-usage-functions)
    -   [Funciones de identificador de clave](#key-identifier-functions)
    -   [Funciones de compatibilidad de OID](#oid-support-functions)
    -   [Funciones de recuperación de objetos remotos](#remote-object-retrieval-functions)
    -   [Funciones PFX](#pfx-functions)
-   [Funciones de copia de seguridad y restauración de Servicios de certificados](#certificate-services-backup-and-restore-functions)
-   [Funciones de devolución de llamada](#callback-functions)
-   [Funciones de definición de catálogo](#catalog-definition-functions)
-   [Funciones de catálogo](#catalog-functions)
-   [WinTrust Functions](#wintrust-functions)
-   [Funciones de localizador de objetos](#object-locator-functions)

## <a name="cryptxml-functions"></a>Funciones CryptXML

Las funciones XML criptográficas proporcionan una API para crear y representar firmas digitales mediante datos con formato XML. Para obtener información sobre las firmas con formato XML, vea la especificación XML-Signature sintaxis y procesamiento en <https://go.microsoft.com/fwlink/p/?linkid=139649> .



| Función                                                                          | Descripción                                                                                                                                                                                                                                                                                                      |
|-----------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**A \_ SHAFinal**](a-shafinal.md)                                                 | Calcula el hash final de los datos especificados por la función MD5Update.                                                                                                                                                                                                                                           |
| [**UN \_ SHAInit**](a-shainit.md)                                                   | Inicia el hash de un flujo de datos.                                                                                                                                                                                                                                                                       |
| [**UN \_ SHAUpdate**](a-shaupdate.md)                                               | Agrega datos a un objeto hash especificado.                                                                                                                                                                                                                                                                            |
| [**CryptXmlCreateReference**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlcreatereference)                        | Crea una referencia a una firma XML.                                                                                                                                                                                                                                                                         |
| [**CryptXmlAddObject**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmladdobject)                                    | Agrega el **elemento Object** a signature en el contexto de documento abierto para la codificación.                                                                                                                                                                                                                        |
| [**CryptXmlClose**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlclose)                                            | Cierra un identificador de objeto XML criptográfico.                                                                                                                                                                                                                                                                        |
| [**CryptXmlDigestReference**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmldigestreference)                        | Lo usa una aplicación para digerir la referencia resuelta. Esta función aplica transformaciones antes de actualizar el resumen.                                                                                                                                                                                            |
| [**CryptXmlDllCloseDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllclosedigest)                          | Libera el CRYPT \_ XML DIGEST asignado por la función \_ [**CryptXmlDllCreateDigest.**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)                                                                                                                                                                                               |
| [**CryptXmlDllCreateDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatedigest)                        | Crea un objeto de resumen para el método especificado.                                                                                                                                                                                                                                                                |
| [**CryptXmlDllCreateKey**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllcreatekey)                              | Analiza el elemento **KeyValue** y crea un identificador de clave BCrypt de Cryptography API: Next Generation (CNG) para comprobar una firma.                                                                                                                                                                                   |
| [**CryptXmlDllDigestData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldlldigestdata)                            | Coloca los datos en la síntesis.                                                                                                                                                                                                                                                                                       |
| [**CryptXmlDllEncodeAlgorithm**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodealgorithm)                  | Codifica elementos **SignatureMethod** o **DigestMethod** para algoritmos ágiles con parámetros predeterminados.                                                                                                                                                                                                           |
| [**CryptXmlDllEncodeKeyValue**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllencodekeyvalue)                    | Codifica un elemento **KeyValue.**                                                                                                                                                                                                                                                                                  |
| [**CryptXmlDllFinalizeDigest**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllfinalizedigest)                    | Recupera el valor de resumen.                                                                                                                                                                                                                                                                                      |
| [**CryptXmlDllGetAlgorithmInfo**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetalgorithminfo)                | Descodifica el algoritmo XML y devuelve información sobre el algoritmo.                                                                                                                                                                                                                                           |
| [**CryptXmlDllGetInterface**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllgetinterface)                        | Recupera un puntero a las funciones de extensión criptográfica para el algoritmo especificado.                                                                                                                                                                                                                        |
| [**CryptXmlDllSignData**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllsigndata)                                | Firma los datos.                                                                                                                                                                                                                                                                                                      |
| [**CryptXmlDllVerifySignature**](/windows/win32/api/cryptxml/nc-cryptxml-cryptxmldllverifysignature)                  | Comprueba una firma.                                                                                                                                                                                                                                                                                            |
| [**CryptXmlEncode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlencode)                                          | Codifica los datos de firma mediante la función de devolución de llamada del escritor XML proporcionada.                                                                                                                                                                                                                                       |
| [**CryptXmlGetAlgorithmInfo**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetalgorithminfo)                      | Descodifica la estructura CRYPT \_ XML ALGORITHM y devuelve información sobre el \_ algoritmo.                                                                                                                                                                                                                         |
| [**CryptXmlGetDocContext**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetdoccontext)                            | Devuelve el contexto de documento especificado por el identificador proporcionado.                                                                                                                                                                                                                                                   |
| [**CryptXmlGetReference**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetreference)                              | Devuelve el **elemento Reference** especificado por el identificador proporcionado.                                                                                                                                                                                                                                              |
| [**CryptXmlGetSignature**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetsignature)                              | Devuelve un elemento **Signatura** XML.                                                                                                                                                                                                                                                                            |
| [**CryptXmlGetStatus**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgetstatus)                                    | Devuelve una [**estructura CRYPT \_ XML \_ STATUS**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_status) que contiene información de estado sobre el objeto especificado por el identificador proporcionado.                                                                                                                                                           |
| [**CryptXmlGetTransforms**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlgettransforms)                            | Devuelve información sobre el motor de cadena de transformación predeterminado.                                                                                                                                                                                                                                                    |
| [**CryptXmlImportPublicKey**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlimportpublickey)                        | Importa la clave pública especificada por el identificador proporcionado.                                                                                                                                                                                                                                                         |
| [**CryptXmlOpenToEncode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlopentoencode)                              | Abre una firma digital XML para codificar y devuelve un identificador del elemento **Signature** abierto. El identificador encapsula un contexto de documento con una única estructura [**CRYPT \_ XML \_ SIGNATURE**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) y permanece abierto hasta que se llama a la función [**CryptXmlClose.**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlclose) |
| [**CryptXmlOpenToDecode**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlopentodecode)                              | Abre una firma digital XML para descodificar y devuelve el identificador del contexto del documento que encapsula una [**estructura CRYPT \_ XML \_ SIGNATURE.**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) El contexto del documento puede incluir uno o varios **elementos Signature.**                                                                 |
| [**CryptXmlSetHMACSecret**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsethmacsecret)                            | Establece el secreto HMAC en el identificador antes de llamar a la [**función CryptXmlSign**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsign) o [**CryptXmlVerify.**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlverifysignature)                                                                                                                                                        |
| [**CryptXmlSign**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlsign)                                              | Crea una firma criptográfica de **un elemento SignedInfo.**                                                                                                                                                                                                                                                   |
| [**CryptXmlVerifySignature**](/windows/desktop/api/Cryptxml/nf-cryptxml-cryptxmlverifysignature)                        | Realiza una validación de firma criptográfica de **un elemento SignedInfo.**                                                                                                                                                                                                                                       |
| [*DEVOLUCIÓN DE LLAMADA DE ESCRITURA XML DE PFN \_ CRYPT \_ \_ \_*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_write_callback)            | Crea una transformación para un proveedor de datos especificado.                                                                                                                                                                                                                                                               |
| [*TRANSFORMACIÓN CREATE DE PFN \_ CRYPT \_ XML \_ \_*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_create_transform)        | Escribe datos XML criptográficos.                                                                                                                                                                                                                                                                                   |
| [*LECTURA DEL \_ PROVEEDOR DE DATOS XML CRYPT \_ DE \_ \_ PFN \_*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_data_provider_read)   | Lee datos XML criptográficos.                                                                                                                                                                                                                                                                                    |
| [*CIERRE DEL PROVEEDOR DE DATOS XML DE PFN \_ CRYPT \_ \_ \_ \_*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_data_provider_close) | Libera el proveedor de datos XML criptográfico.                                                                                                                                                                                                                                                                    |
| [*PFN \_ CRYPT \_ XML \_ ENUM \_ ALG \_ INFO*](/windows/desktop/api/Cryptxml/nc-cryptxml-pfn_crypt_xml_enum_alg_info)             | Enumera las entradas info del ALGORITMO [**XML de CRYPT \_ predefinidas \_ \_ y**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm_info) registradas.                                                                                                                                                                                                    |



 

## <a name="signer-functions"></a>Funciones de firmante

Proporciona funciones para firmar y los datos de marca de tiempo.



| Función                                                   | Descripción                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SignerFreeSignerContext**](signerfreesignercontext.md) | Libera una estructura [**SIGNER \_ CONTEXT**](signer-context.md) asignada por una llamada anterior a la [**función SignerSignEx.**](signersignex.md)                                                                                                                                                                                                                                                                      |
| [**SignError**](signerror.md)                             | Llama a [**la función GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) y convierte el código de retorno en **un HRESULT**.                                                                                                                                                                                                                                                                                                            |
| [**SignerSign**](signersign.md)                           | Firma el archivo especificado.                                                                                                                                                                                                                                                                                                                                                                                           |
| [**SignerSignEx**](signersignex.md)                       | Firma el archivo especificado y devuelve un puntero a los datos firmados.                                                                                                                                                                                                                                                                                                                                                  |
| [**SignerSignEx2**](signersignex2.md)                     | Firma y marca de tiempo el archivo especificado, lo que permite varias firmas anidadas.                                                                                                                                                                                                                                                                                                                                      |
| [**SignerTimeStamp**](signertimestamp.md)                 | Marca de tiempo el sujeto especificado. Esta función admite la marca de tiempo Authenticode. Para realizar la marca de tiempo de infraestructura de clave pública (RFC 3161) X.509, use la [**función SignerTimeStampEx2.**](signertimestampex2.md)                                                                                                                                                                                       |
| [**SignerTimeStampEx**](signertimestampex.md)             | Marca de tiempo el asunto especificado y, opcionalmente, devuelve un puntero a una estructura [**SIGNER \_ CONTEXT**](signer-context.md) que contiene un puntero a [*UN BLOB*](../secgloss/b-gly.md). Esta función admite la marca de tiempo Authenticode. Para realizar la marca de tiempo de infraestructura de clave pública (RFC 3161) X.509, use la [**función SignerTimeStampEx2.**](signertimestampex2.md) |
| [**SignerTimeStampEx2**](signertimestampex2.md)           | Marca de tiempo el asunto especificado y, opcionalmente, devuelve un puntero a una estructura [**SIGNER \_ CONTEXT**](signer-context.md) que contiene un puntero a [*UN BLOB*](../secgloss/b-gly.md). Esta función se puede usar para realizar marcas de tiempo de infraestructura de clave pública X.509 compatible con RFC 3161.                                                                                     |
| [**SignerTimeStampEx3**](signertimestampex3.md)           | Marca de tiempo el asunto especificado y admite la configuración de marcas de tiempo en varias firmas.                                                                                                                                                                                                                                                                                                                          |



 

## <a name="base-cryptography-functions"></a>Funciones de criptografía base

Las funciones criptográficas base proporcionan el medio más flexible de desarrollar aplicaciones de criptografía. Toda la comunicación con un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP) se produce a través de estas funciones.

Un CSP es un módulo independiente que realiza todas las operaciones criptográficas. Se requiere al menos un CSP con cada aplicación que use funciones criptográficas. En ocasiones, una sola aplicación puede usar más de un CSP.

Si se usa más de un CSP, el que se va a usar se puede especificar en las llamadas a la función criptográfica CryptoAPI. Un CSP, el proveedor de servicios criptográficos base de Microsoft, se incluye con [*CryptoAPI*](../secgloss/c-gly.md). Muchas de las funciones cryptoAPI usan este CSP como proveedor predeterminado si no se especifica ningún otro CSP.

Cada CSP proporciona una implementación diferente de la compatibilidad criptográfica proporcionada a CryptoAPI. Algunos proporcionan algoritmos criptográficos más sólidos; otros contienen componentes de hardware, como [*tarjetas inteligentes.*](../secgloss/s-gly.md) Además, algunos CSP pueden comunicarse ocasionalmente directamente con los usuarios, como cuando se realizan firmas [*digitales*](../secgloss/d-gly.md) mediante la clave privada de firma [*del usuario.*](../secgloss/s-gly.md)

Las funciones criptográficas base se encuentran en los siguientes grupos amplios:

-   Funciones del proveedor de servicios
-   Generación de claves y funciones Exchange claves
-   Funciones de codificación y codificación de objetos
-   Funciones de cifrado y descifrado de datos
-   Funciones hash y firma digital

### <a name="service-provider-functions"></a>Funciones del proveedor de servicios

Las aplicaciones usan las siguientes funciones de servicio para conectar y desconectar un [*proveedor de servicios criptográficos*](../secgloss/c-gly.md) (CSP).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Función</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta"><strong>CryptAcquireContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Adquiere un identificador para el contenedor de claves del usuario <a href="/windows/desktop/SecGloss/k-gly"><em>actual</em></a> dentro de un CSP determinado.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcontextaddref"><strong>CryptContextAddRef</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Incrementa el recuento <a href="/windows/desktop/SecGloss/r-gly"><em>de referencias</em></a> en un <a href="hcryptprov.md"><strong>identificador HCRYPTPROV.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumprovidersa"><strong>CryptEnumProviders</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Enumera los proveedores en un equipo.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumprovidertypesa"><strong>CryptEnumProviderTypes</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Enumera los tipos de proveedores admitidos en el equipo.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultprovidera"><strong>CryptGetDefaultProvider</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Determina el CSP predeterminado para el usuario actual o para el equipo para un tipo de proveedor especificado.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetprovparam"><strong>CryptGetProvParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Recupera los parámetros que rigen las operaciones de un CSP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalldefaultcontext"><strong>CryptInstallDefaultContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Instala un contexto <a href="hcryptprov.md"><strong>HCRYPTPROV</strong></a> adquirido previamente para que se utilice como contexto predeterminado.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptreleasecontext"><strong>CryptReleaseContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Libera el identificador adquirido por la <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta"><strong>función CryptAcquireContext.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovidera"><strong>CryptSetProvider</strong></a> y <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetproviderexa"> <strong>CryptSetProviderEx</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Especifica el CSP predeterminado del usuario para un tipo de CSP determinado.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetprovparam"><strong>CryptSetProvParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Especifica los atributos de un CSP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptuninstalldefaultcontext"><strong>CryptUninstallDefaultContext</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Quita un contexto predeterminado instalado previamente por <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalldefaultcontext"><strong>CryptInstallDefaultContext.</strong></a></td>
</tr>
<tr class="even">
<td><a href="freecryptprovfromcertex.md"><strong>FreeCryptProvFromCertEx</strong></a></td>
<td>Libera el identificador a un proveedor <a href="/windows/desktop/SecGloss/c-gly"><em>de servicios criptográficos</em></a> (CSP) o a una clave cryptography API: Next Generation (CNG).</td>
</tr>
</tbody>
</table>



 

### <a name="key-generation-and-exchange-functions"></a>Generación de claves y funciones Exchange claves

Las funciones de generación e intercambio de [*claves intercambian claves*](../secgloss/e-gly.md) con otros usuarios y crean, configuran y destruyen [*claves criptográficas*](../secgloss/c-gly.md).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Función</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey"><strong>CryptDeriveKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Crea una clave derivada de una contraseña.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroykey"><strong>CryptDestroyKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Destruye una clave.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatekey"><strong>CryptDuplicateKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Realiza una copia exacta de una clave, incluido <a href="/windows/desktop/SecGloss/s-gly"><em>el estado</em></a> de la clave.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportkey"><strong>CryptExportKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Transfiere una clave del CSP a un <a href="/windows/desktop/SecGloss/k-gly"><em>BLOB de clave</em></a> en el espacio de memoria de la aplicación.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey"><strong>CryptGenKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Crea una clave aleatoria.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenrandom"><strong>CryptGenRandom</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Genera datos aleatorios.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyparam"><strong>CryptGetKeyParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Recupera los parámetros de una clave.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetuserkey"><strong>CryptGetUserKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Obtiene un identificador para el intercambio de claves o la clave de firma.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey"><strong>CryptImportKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Transfiere una clave de un <a href="/windows/desktop/SecGloss/k-gly"><em>BLOB de clave</em></a> a un CSP.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam"><strong>CryptSetKeyParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Especifica los parámetros de una clave.</td>
</tr>
</tbody>
</table>



 

### <a name="object-encoding-and-decoding-functions"></a>Funciones de codificación y codificación de objetos

Se trata de funciones generalizadas de codificación y decodización. Se usan para codificar y descodificar [*certificados,*](../secgloss/c-gly.md)listas de [*revocación*](../secgloss/c-gly.md) de certificados (CRL), [](../secgloss/c-gly.md)solicitudes de certificado y extensiones de certificado.

| Función                                           | Descripción                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)     | Descodifica una estructura de tipo *lpszStructType*.                                                                                                    |
| [**CryptDecodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) | Descodifica una estructura de tipo *lpszStructType*. [**CryptDecodeObjectEx admite**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) la opción de asignación de memoria de un paso. |
| [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)     | Codifica una estructura de tipo *lpszStructType*.                                                                                                    |
| [**CryptEncodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) | Codifica una estructura de tipo *lpszStructType*. [**CryptEncodeObjectEx admite**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) la opción de asignación de memoria de un paso. |



 

### <a name="data-encryption-and-decryption-functions"></a>Funciones de cifrado y descifrado de datos

Las siguientes funciones admiten operaciones de cifrado y descifrado. [**CryptEncrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt) y [**CryptDecrypt**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt) requieren una [*clave criptográfica antes*](../secgloss/c-gly.md) de llamarse. Para ello, se usa [**la función CryptGenKey,**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey) [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)o [**CryptImportKey.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey) El algoritmo de cifrado se especifica cuando se crea la clave. [**CryptSetKeyParam puede**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyparam) establecer parámetros de cifrado adicionales.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Función</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecrypt"><strong>CryptDecrypt</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Descifra una sección de <a href="/windows/desktop/SecGloss/c-gly"><em>texto cifrado</em></a> mediante la clave de cifrado especificada.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencrypt"><strong>CryptEncrypt</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Cifra una sección de texto <a href="/windows/desktop/SecGloss/p-gly"><em>no cifrado</em></a> mediante la clave de cifrado especificada.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectdata"><strong>CryptProtectData</strong></a></td>
<td>Realiza el cifrado en los datos de una <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)"><strong>DATA_BLOB</strong></a> estructura.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory"><strong>CryptProtectMemory</strong></a></td>
<td>Cifra la memoria para proteger la información confidencial.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectdata"><strong>CryptUnprotectData</strong></a></td>
<td>Realiza una comprobación de descifrado e integridad de los datos de una <a href="/previous-versions/windows/desktop/legacy/aa381414(v=vs.85)"><strong>DATA_BLOB</strong></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptunprotectmemory"><strong>CryptUnprotectMemory</strong></a></td>
<td>Descifra la memoria cifrada mediante <a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptprotectmemory"><strong>CryptProtectMemory</strong></a>.</td>
</tr>
</tbody>
</table>



 

### <a name="hash-and-digital-signature-functions"></a>Funciones hash y firma digital

Estas funciones [*calculan hashes*](../secgloss/h-gly.md) de datos y también crean y [*comprueban firmas digitales.*](../secgloss/d-gly.md) Los hashes también se conocen como resúmenes de mensajes.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Función</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatehash"><strong>CryptCreateHash</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Crea un objeto hash vacío.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdestroyhash"><strong>CryptDestroyHash</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Destruye un objeto hash.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptduplicatehash"><strong>CryptDuplicateHash</strong></a></td>
<td>Duplica un objeto hash.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgethashparam"><strong>CryptGetHashParam</strong></a></td>
<td>Recupera un parámetro de objeto hash.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashdata"><strong>CryptHashData</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Aplica un algoritmo hash a un bloque de datos y lo agrega al objeto hash especificado.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashsessionkey"><strong>CryptHashSessionKey</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Aplica un algoritmo hash a una clave de sesión y la agrega al objeto hash especificado.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsethashparam"><strong>CryptSetHashParam</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Establece un parámetro de objeto hash.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignhasha"><strong>CryptSignHash</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Firma el objeto hash especificado.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign"><strong>CryptUIWizDigitalSign</strong></a></td>
<td>Muestra un asistente que firma digitalmente un documento o <a href="/windows/desktop/SecGloss/b-gly"><em>un BLOB.</em></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizfreedigitalsigncontext"><strong>CryptUIWizFreeDigitalSignContext</strong></a></td>
<td>Libera un puntero a una <a href="/windows/desktop/api/Cryptuiapi/ns-cryptuiapi-cryptui_wiz_digital_sign_context"><strong>CRYPTUI_WIZ_DIGITAL_SIGN_CONTEXT</strong></a> estructura.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifysignaturea"><strong>CryptVerifySignature</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Comprueba una firma digital, dado un identificador al objeto hash.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Cryptuiapi/nc-cryptuiapi-pfncfilterproc"><strong>PFNCFILTERPROC</strong></a></td>
<td>Filtra los certificados que aparecen en el Asistente para firma digital que muestra la <a href="/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizdigitalsign"><strong>función CryptUIWizDigitalSign.</strong></a></td>
</tr>
</tbody>
</table>



 

## <a name="certificate-and-certificate-store-functions"></a>Funciones de almacén de certificados y certificados

Las funciones de almacén de certificados y certificados administran el uso, el almacenamiento y la recuperación de [*certificados,*](../secgloss/c-gly.md)listas de [*revocación*](../secgloss/c-gly.md) de certificados (CRL) y listas de confianza de certificados [](../secgloss/c-gly.md) (CL). Estas funciones se dividen en los siguientes grupos:

-   Funciones del almacén de certificados
-   Funciones de mantenimiento de almacén de certificados y certificados
-   Funciones de certificado
-   Funciones de lista de revocación de certificados
-   Funciones de lista de confianza de certificados
-   Funciones de propiedad extendida
-   Funciones MakeCert

### <a name="certificate-store-functions"></a>Funciones del almacén de certificados

Un sitio de usuario puede, con el tiempo, recopilar muchos certificados. Normalmente, un sitio tiene certificados para el usuario del sitio, así como otros certificados que describen a las personas y entidades con las que se comunica el usuario. Para cada entidad, puede haber más de un certificado. Para cada certificado individual, debe haber una cadena de comprobación de certificados que proporciona una pista a un certificado [*raíz de confianza.*](../secgloss/r-gly.md) [*Los almacenes de*](../secgloss/c-gly.md) certificados y sus funciones relacionadas proporcionan funcionalidad para almacenar, recuperar, enumerar, comprobar y usar la información almacenada en los certificados.

| Función                                                               | Descripción                                                                                                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection)           | Agrega un almacén de certificados relacionado a un almacén de certificados de recopilación.                                                                                                                                                                                                                                                                       |
| [**CertCloseStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certclosestore)                               | Cierra un identificador de almacén de certificados.                                                                                                                                                                                                                                                                                                        |
| [**CertControlStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcontrolstore)                           | Permite notificar a una aplicación cuando hay una diferencia entre el contenido de un almacén almacenado en caché y el contenido del almacén que se conserva en el almacenamiento. También proporciona la desincronización del almacén almacenado en caché, si es necesario, y proporciona un medio para confirmar los cambios realizados en el almacén almacenado en caché en el almacenamiento persistente.<br/> |
| [**CertDuplicateStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatestore)                       | Duplica un identificador de almacén incrementando el recuento [*de referencias*](../secgloss/r-gly.md).                                                                                                                                                                                            |
| [**CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore)                 | Enumera los almacenes físicos de un almacén del sistema especificado.                                                                                                                                                                                                                                                                              |
| [**CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore)                     | Enumera todos los almacenes del sistema disponibles.                                                                                                                                                                                                                                                                                                   |
| [**CertEnumSystemStoreLocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation)     | Enumera todas las ubicaciones que tienen un almacén del sistema disponible.                                                                                                                                                                                                                                                                      |
| [**CertGetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetstoreproperty)                   | Obtiene una propiedad de almacén.                                                                                                                                                                                                                                                                                                                    |
| [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)                                 | Abre un almacén de certificados con un tipo de proveedor de almacén especificado.                                                                                                                                                                                                                                                                          |
| [**CertOpenSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopensystemstorea)                     | Abre un almacén de certificados del sistema basado en un protocolo de subsistema.                                                                                                                                                                                                                                                                           |
| [**CertRegisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregisterphysicalstore)         | Agrega un almacén físico a una colección de almacenes del sistema del Registro.                                                                                                                                                                                                                                                                              |
| [**CertRegisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certregistersystemstore)             | Registra un almacén del sistema.                                                                                                                                                                                                                                                                                                                 |
| [**CertRemoveStoreFromCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection) | Quita un almacén de certificados relacionado de un almacén de recopilación.                                                                                                                                                                                                                                                                              |
| [**CertSaveStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsavestore)                                 | Guarda el almacén de certificados.                                                                                                                                                                                                                                                                                                              |
| [**CertSetStoreProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetstoreproperty)                   | Establece una propiedad de almacén.                                                                                                                                                                                                                                                                                                                    |
| [**CertUnregisterPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregisterphysicalstore)     | Quita un almacén físico de una colección de almacenes del sistema especificada.                                                                                                                                                                                                                                                                        |
| [**CertUnregisterSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certunregistersystemstore)         | Anula el registro de un almacén del sistema especificado.                                                                                                                                                                                                                                                                                                     |
| [**CryptUIWizExport**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizexport)                           | Presenta un asistente que exporta un certificado, una lista de certificados de confianza (CTL), una lista de revocación de certificados (CRL) o un almacén de certificados.                                                                                                                                                                                                      |
| [**CryptUIWizImport**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuiwizimport)                           | Presenta un asistente que importa un certificado, una lista de certificados de confianza (CTL), una lista de revocación de certificados (CRL) o un almacén de certificados.                                                                                                                                                                                                      |



 

### <a name="certificate-and-certificate-store-maintenance-functions"></a>Funciones de mantenimiento de almacén de certificados y certificados

CryptoAPI proporciona un conjunto de funciones generales de mantenimiento del almacén de certificados y certificados.

| Función                                                                                                                              | Descripción                                                                                    |
|---------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------|
| [**CertAddSerializedElementToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddserializedelementtostore)                                                            | Agrega el certificado serializado o el elemento CRL al almacén.                                   |
| [**CertCreateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecontext)                                                                                        | Crea el contexto especificado a partir de los bytes codificados. El nuevo contexto no se coloca en un almacén. |
| [**CertEnumSubjectInSortedCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsubjectinsortedctl)                                                                      | Enumera los objetos TrustedSubject en un contexto de CTL ordenado.                                        |
| [**CertFindSubjectInCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinctl)                                                                                  | Busca el asunto especificado en una CTL.                                                          |
| [**CertFindSubjectInSortedCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindsubjectinsortedctl)                                                                      | Busca el asunto especificado en una CTL ordenada.                                                   |
| [**OpenPersonalTrustDBDialog**](/windows/desktop/api/wintrust/nf-wintrust-openpersonaltrustdbdialog) y [ **OpenPersonalTrustDBDialogEx**](/windows/desktop/api/wintrust/nf-wintrust-openpersonaltrustdbdialogex) | Muestra el **cuadro de diálogo** Certificados .                                                      |



 

### <a name="certificate-functions"></a>Funciones de certificado

La [*mayoría de*](../secgloss/c-gly.md) las funciones de certificado tienen funciones relacionadas para tratar con [*CRL*](../secgloss/c-gly.md) y [*CL.*](../secgloss/c-gly.md) Para obtener más información sobre las funciones CRL y CTL relacionadas, vea Funciones de lista de revocación de certificados y Funciones de lista de confianza de certificados.

| Función                                                                             | Descripción                                                                                                                                                                                                                                     |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAddCertificateContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatecontexttostore)         | Agrega un contexto de certificado al almacén de certificados.                                                                                                                                                                                            |
| [**CertAddCertificateLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcertificatelinktostore)               | Agrega un vínculo de un almacén de certificados a un contexto de certificado en un almacén diferente.                                                                                                                                                               |
| [**CertAddEncodedCertificateToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcertificatetostore)         | Convierte el certificado codificado en un contexto de certificado y, a continuación, agrega el contexto al almacén de certificados.                                                                                                                                  |
| [**CertAddRefServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponse)                 | Incrementa el recuento de referencias para un **identificador HCERT \_ SERVER \_ OCSP \_ RESPONSE.**                                                                                                                                                                 |
| [**CertAddRefServerOcspResponseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddrefserverocspresponsecontext)   | Incrementa el recuento de referencias para una [**estructura CERT \_ SERVER \_ OCSP \_ RESPONSE \_ CONTEXT.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_server_ocsp_response_context)                                                                                                              |
| [**CertCloseServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcloseserverocspresponse)                   | Cierra un identificador [*de respuesta de servidor*](../secgloss/o-gly.md) de protocolo de estado de certificado en línea (OCSP).                                               |
| [**CertCreateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatecontext)                 | Crea un contexto de certificado a partir de un certificado codificado. El contexto creado no se coloca en un almacén de certificados.                                                                                                                               |
| [**CertCreateSelfSignCertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreateselfsigncertificate)               | Crea un certificado autofirmado.                                                                                                                                                                                                              |
| [**CertDeleteCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecertificatefromstore)             | Elimina un certificado del almacén de certificados.                                                                                                                                                                                               |
| [**CertDuplicateCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatecontext)           | Duplica un contexto de certificado incrementando su recuento [*de referencias.*](../secgloss/r-gly.md)                                                                                           |
| [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)                   | Enumera los contextos de certificado en el almacén de certificados.                                                                                                                                                                                   |
| [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore)                     | Busca el primer o el siguiente contexto de certificado en el almacén de certificados que cumple un criterio de búsqueda.                                                                                                                                           |
| [**CertFreeCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatecontext)                     | Libera un contexto de certificado.                                                                                                                                                                                                                    |
| [**CertGetIssuerCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetissuercertificatefromstore)       | Obtiene un contexto de certificado del almacén de certificados para el primer emisor o el siguiente del certificado de sujeto especificado.                                                                                                                      |
| [**CertGetServerOcspResponseContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetserverocspresponsecontext)         | Recupera un contexto de respuesta [](../secgloss/o-gly.md) de protocolo de estado de certificado en línea (OCSP) válido sin bloqueo para el identificador especificado. |
| [**CertGetSubjectCertificateFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetsubjectcertificatefromstore)     | Obtiene del almacén de certificados el contexto de certificado del firmante, que se identifica de forma única por su emisor y número de serie.                                                                                                                  |
| [**CertGetValidUsages**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetvalidusages)                                     | Devuelve una matriz de usos que constan de la intersección de los usos válidos para todos los certificados de una matriz de certificados.                                                                                                               |
| [**CertOpenServerOcspResponse**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenserverocspresponse)                     | Abre un identificador para una [*respuesta del protocolo de estado de*](../secgloss/o-gly.md) certificado en línea (OCSP) asociada a una cadena de certificados de servidor.       |
| [**CertRetrieveLogoOrBiometricInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-certretrievelogoorbiometricinfo)           | Realiza una recuperación url del logotipo o la información biométrica especificada en la extensión de certificado **szOID \_ LOGOTYPE \_ EXT** o **szOID \_ BIOMETRIC \_ EXT.**                                                                                  |
| [**CertSelectCertificate**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea)                               | Presenta un cuadro de diálogo que permite al usuario seleccionar certificados de un conjunto de certificados que coinciden con un criterio determinado.                                                                                                                       |
| [**CertSelectCertificateChains**](/windows/desktop/api/Wincrypt/nf-wincrypt-certselectcertificatechains)                   | Recupera cadenas de certificados en función de los criterios de selección especificados.                                                                                                                                                                             |
| [**CertSelectionGetSerializedBlob**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-certselectiongetserializedblob)             | Función auxiliar que se usa para recuperar un blob de certificado [*serializado*](../secgloss/b-gly.md) de una [**estructura CERT \_ SELECTUI \_ INPUT.**](/windows/desktop/api/Cryptuiapi/ns-cryptuiapi-cert_selectui_input)                                               |
| [**CertSerializeCertificateStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecertificatestoreelement) | Serializa el certificado codificado de un contexto de certificado y una representación codificada de sus propiedades.                                                                                                                                         |
| [**CertVerifySubjectCertificateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifysubjectcertificatecontext)   | Realiza las comprobaciones de comprobación habilitadas en el certificado del firmante mediante el emisor.                                                                                                                                                           |
| [**CryptUIDlgCertMgr**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgcertmgr)                                       | Muestra un cuadro de diálogo que permite al usuario administrar certificados.                                                                                                                                                                              |
| [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md)                   | Muestra un cuadro de diálogo que permite a un usuario seleccionar un certificado.                                                                                                                                                                               |
| [**CryptUIDlgSelectCertificateFromStore**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgselectcertificatefromstore) | Muestra un cuadro de diálogo que permite la selección de un certificado de un almacén especificado.                                                                                                                                                        |
| [**CryptUIDlgViewCertificate**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcertificatea)                       | Presenta un cuadro de diálogo que muestra un certificado especificado.                                                                                                                                                                                    |
| [**CryptUIDlgViewContext**](/windows/desktop/api/Cryptuiapi/nf-cryptuiapi-cryptuidlgviewcontext)                               | Muestra un certificado, CRL o CTL.                                                                                                                                                                                                            |
| [**CryptUIDlgViewSignerInfo**](cryptuidlgviewsignerinfo.md)                         | Muestra un cuadro de diálogo que contiene la información del firmante de un mensaje firmado.                                                                                                                                                                |
| [**GetFriendlyNameOfCert**](/windows/desktop/api/CryptDlg/nf-cryptdlg-getfriendlynameofcerta)                               | Recupera el nombre para mostrar de un certificado.                                                                                                                                                                                                   |
| [**RKeyCloseKeyService**](rkeyclosekeyservice.md)                                   | Cierra un identificador de servicio clave.                                                                                                                                                                                                                    |
| [**RKeyOpenKeyService**](rkeyopenkeyservice.md)                                     | Abre un identificador de servicio clave en un equipo remoto.                                                                                                                                                                                                |
| [**RKeyPFXInstall**](rkeypfxinstall.md)                                             | Instala un certificado en un equipo remoto.                                                                                                                                                                                                    |



 

### <a name="certificate-revocation-list-functions"></a>Funciones de lista de revocación de certificados

Estas funciones administran el almacenamiento y la recuperación de listas [*de revocación de certificados*](../secgloss/c-gly.md) (CRL).

| Función                                                             | Descripción                                                                                                                                                                           |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAddCRLContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrlcontexttostore)         | Agrega un contexto CRL al almacén de certificados.                                                                                                                                          |
| [**CertAddCRLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddcrllinktostore)               | Agrega un vínculo de un almacén a un contexto crl en un almacén diferente.                                                                                                                         |
| [**CertAddEncodedCRLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedcrltostore)         | Convierte la CRL codificada en un contexto CRL y, a continuación, agrega el contexto al almacén de certificados.                                                                                        |
| [**CertCreateCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecrlcontext)                 | Crea un contexto CRL a partir de una CRL codificada. El contexto creado no se coloca en un almacén de certificados.                                                                                     |
| [**CertDeleteCRLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletecrlfromstore)             | Elimina una CRL del almacén de certificados.                                                                                                                                             |
| [**CertDuplicateCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecrlcontext)           | Duplica un contexto CRL incrementando el recuento [*de referencias*](../secgloss/r-gly.md).                                         |
| [**CertEnumCRLsInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcrlsinstore)                   | Enumera los contextos de CRL en un almacén.                                                                                                                                               |
| [**CertFindCertificateInCRL**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateincrl)         | Busca en [*la lista de revocación de*](../secgloss/c-gly.md) certificados (CRL) el certificado especificado. |
| [**CertFindCRLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcrlinstore)                     | Busca el primer contexto de CRL, o el siguiente, en el almacén de certificados que coincide con un criterio específico.                                                                                     |
| [**CertFreeCRLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecrlcontext)                     | Libera un contexto crl.                                                                                                                                                                  |
| [**CertGetCRLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlfromstore)                   | Obtiene el primer contexto crl del almacén de certificados para el certificado de emisor especificado o el siguiente.                                                                                 |
| [**CertSerializeCRLStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializecrlstoreelement) | Serializa la CRL codificada del contexto CRL y sus propiedades.                                                                                                                          |



 

### <a name="certificate-trust-list-functions"></a>Funciones de lista de confianza de certificados

Estas funciones administran el almacenamiento y la recuperación de listas [*de confianza de certificados*](../secgloss/c-gly.md) (CL).

| Función                                                               | Descripción                                                                                                          |
|------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| [**CertAddCTLContextToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctlcontexttostore)           | Agrega un contexto de CTL al almacén de certificados.                                                                         |
| [**CertAddCTLLinkToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddctllinktostore)                 | Agrega un vínculo de un almacén a un contexto crl en un almacén diferente.                                                        |
| [**CertAddEncodedCTLToStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddencodedctltostore)           | Convierte la CTL codificada en un contexto de CTL y, a continuación, agrega el contexto al almacén de certificados.                       |
| [**CertCreateCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlcontext)                   | Crea un contexto de CTL a partir de una lista de confianza de certificado codificada. El contexto creado no se coloca en un almacén de certificados. |
| [**CertDeleteCTLFromStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certdeletectlfromstore)               | Elimina una CTL del almacén de certificados.                                                                            |
| [**CertDuplicateCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatectlcontext)             | Duplica un contexto de CTL incrementando el recuento de referencias.                                                        |
| [**CertEnumCTLsInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumctlsinstore)                     | Enumera los contextos de CTL en el almacén de certificados.                                                                |
| [**CertFindCTLInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindctlinstore)                       | Busca el primer contexto de CTL, o el siguiente, en el almacén de certificados que coincide con un criterio específico.                     |
| [**CertFreeCTLContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreectlcontext)                       | Libera un contexto de CTL.                                                                                                 |
| [**CertModifyCertificatesToTrust**](/windows/desktop/api/CryptDlg/nf-cryptdlg-certmodifycertificatestotrust) | Modifica el conjunto de certificados de una CTL para un propósito determinado.                                                       |
| [**CertSerializeCTLStoreElement**](/windows/desktop/api/Wincrypt/nf-wincrypt-certserializectlstoreelement)   | Serializa la CTL codificada del contexto de CTL y sus propiedades.                                                         |



 

### <a name="extended-property-functions"></a>Funciones de propiedad extendida

Las siguientes funciones funcionan con propiedades extendidas de certificados, CRL y CL.

| Función                                                                             | Descripción                                                      |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------|
| [**CertEnumCertificateContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatecontextproperties) | Enumera las propiedades del contexto de certificado especificado. |
| [**CertEnumCRLContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcrlcontextproperties)                 | Enumera las propiedades del contexto crl especificado.         |
| [**CertEnumCTLContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumctlcontextproperties)                 | Enumera las propiedades del contexto de CTL especificado.         |
| [**CertGetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty)       | Recupera las propiedades del certificado.                                |
| [**CertGetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty)                       | Recupera las propiedades de CRL.                                        |
| [**CertGetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetctlcontextproperty)                       | Recupera las propiedades de CTL.                                        |
| [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty)       | Establece las propiedades del certificado.                                     |
| [**CertSetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty)                       | Establece las propiedades de CRL.                                             |
| [**CertSetCTLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetctlcontextproperty)                       | Establece las propiedades de CTL.                                             |



 

## <a name="makecert-functions"></a>Funciones MakeCert

Las funciones siguientes admiten la [herramienta MakeCert.](makecert.md)



| Función                                                                               | Descripción                                                                                                                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**FreeCryptProvFromCert**](freecryptprovfromcert.md)                                 | Libera el identificador a un proveedor [*de*](../secgloss/c-gly.md) servicios criptográficos (CSP) y, opcionalmente, elimina el contenedor temporal creado por la [**función GetCryptProvFromCert.**](getcryptprovfromcert.md) |
| [**GetCryptProvFromCert**](getcryptprovfromcert.md)                                   | Obtiene un identificador para un CSP y una especificación de clave para un contexto de certificado.                                                                                                                                                                                                                                |
| [**PvkFreeCryptProv**](pvkfreecryptprov.md)                                           | Libera el identificador a un CSP y, opcionalmente, elimina el contenedor temporal creado por la [**función PvkGetCryptProv.**](pvkgetcryptprov.md)                                                                                                                                                          |
| [**PvkGetCryptProv**](pvkgetcryptprov.md)                                             | Obtiene un identificador para un CSP basado en un nombre [*de archivo*](../secgloss/p-gly.md) de clave privada o un nombre de contenedor de claves.                                                                                                                                          |
| [**PvkPrivateKeyAcquireContextFromMemory**](pvkprivatekeyacquirecontextfrommemory.md) | Crea un contenedor temporal en el CSP y carga una clave privada de la memoria en el contenedor.                                                                                                                                                                                                         |
| [**PvkPrivateKeySave**](pvkprivatekeysave.md)                                         | Guarda una clave privada y su clave [*pública correspondiente*](../secgloss/p-gly.md) en un archivo especificado.                                                                                                                                                          |
| [**SignError**](signerror.md)                                                         | Llama [**a GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) y convierte el código de retorno en **un valor HRESULT.**                                                                                                                                                                                                              |



 

## <a name="certificate-verification-functions"></a>Funciones de comprobación de certificados

Los certificados se comprueban mediante [*CCL o*](../secgloss/c-gly.md) cadenas de certificados. Las funciones se proporcionan para ambos:

-   Funciones de comprobación mediante CTL
-   Funciones de comprobación de la cadena de certificados

### <a name="verification-functions-using-ctls"></a>Funciones de comprobación mediante CTL

Estas funciones usan LASCL en el proceso de comprobación. Puede encontrar funciones adicionales para trabajar con CCL en Funciones de lista de confianza de certificados y Funciones de propiedad extendida.

Las funciones siguientes usan las CTL directamente para la comprobación.

| Función                                                         | Descripción                                  |
|------------------------------------------------------------------|----------------------------------------------|
| [**CertVerifyCTLUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyctlusage)                 | Comprueba el uso de una CTL.                 |
| [**CryptMsgEncodeAndSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgencodeandsignctl)     | Codifica y firma una CTL como un mensaje.        |
| [**CryptMsgGetAndVerifySigner**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetandverifysigner) | Recupera y comprueba una CTL de un mensaje. |
| [**CryptMsgSignCTL**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgsignctl)                       | Firma un mensaje que contiene una CTL.         |



 

### <a name="certificate-chain-verification-functions"></a>Funciones de comprobación de la cadena de certificados

Las cadenas de certificados se han creado para proporcionar información de confianza sobre certificados individuales.

| Nombre de la función                                                                                                    | Descripción                                                                                                                                                                                                         |
|------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertCreateCertificateChainEngine**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecertificatechainengine)                                     | Crea un nuevo motor de cadena no predeterminado para una aplicación.                                                                                                                                                          |
| [**CertCreateCTLEntryFromCertificateContextProperties**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatectlentryfromcertificatecontextproperties) | Crea una entrada CTL cuyos atributos son las propiedades del contexto de certificado.                                                                                                                                      |
| [**CertDuplicateCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certduplicatecertificatechain)                                           | Duplica una cadena de certificados incrementando [](../secgloss/r-gly.md) el recuento de referencias de la cadena y devolviendo un puntero a la cadena.                    |
| [**CertFindChainInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindchaininstore)                                                             | Busca el primer contexto de cadena de certificados, o el siguiente, en un almacén.                                                                                                                                                     |
| [**CertFreeCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechain)                                                     | Libera una cadena de certificados al reducir su recuento de referencias.                                                                                                                                                          |
| [**CertFreeCertificateChainEngine**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechainengine)                                         | Libera un motor de cadena de certificados no predeterminado.                                                                                                                                                                        |
| [**CertFreeCertificateChainList**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfreecertificatechainlist)                                             | Libera la matriz de punteros a contextos de cadena.                                                                                                                                                                      |
| [**CertGetCertificateChain**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatechain)                                                       | Compila un contexto de cadena a partir de un certificado final y vuelve a un certificado [*raíz de confianza,*](../secgloss/r-gly.md)si es posible.                |
| [**CertIsValidCRLForCertificate**](/windows/desktop/api/Wincrypt/nf-wincrypt-certisvalidcrlforcertificate)                                             | Comprueba una [*CRL*](../secgloss/c-gly.md) para determinar si incluiría un certificado específico si ese certificado se revoca. |
| [**CertSetCertificateContextPropertiesFromCTLEntry**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextpropertiesfromctlentry)       | Establece las propiedades en el contexto del certificado mediante los atributos de la entrada CTL.                                                                                                                                   |
| [**CertVerifyCertificateChainPolicy**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycertificatechainpolicy)                                     | Comprueba una cadena de certificados para comprobar su validez, incluido su cumplimiento con los criterios de directiva de validez especificados.                                                                                            |



 

## <a name="message-functions"></a>Funciones de mensajes

[*Las funciones de mensaje*](../secgloss/c-gly.md) de CryptoAPI constan de dos grupos de funciones: funciones de mensaje de bajo nivel y [*funciones de mensaje simplificadas.*](../secgloss/s-gly.md)

Las funciones de mensaje de bajo nivel crean y funcionan directamente con mensajes PKCS \# 7. Estas funciones codifican los datos PKCS 7 para la transmisión y descodifican los datos \# PKCS \# 7 recibidos. También descifran y comprueban las firmas de los mensajes recibidos. Para obtener información general sobre los mensajes estándar y de bajo nivel de PKCS \# 7, vea [Mensajes de bajo nivel.](low-level-messages.md)

Las funciones de mensaje simplificadas están en un nivel superior y encapsulan varias funciones de mensaje de bajo nivel y funciones de certificado en funciones únicas que realizan una tarea específica de una manera específica. Estas funciones reducen el número de llamadas de función necesarias para realizar una tarea, lo que simplifica el uso de CryptoAPI. Para obtener información general sobre los mensajes simplificados, vea [Mensajes simplificados.](simplified-messages.md)

-   Funciones de mensaje de bajo nivel
-   Funciones de mensaje simplificadas

### <a name="low-level-message-functions"></a>Funciones de mensaje de bajo nivel

Las funciones de mensaje de bajo nivel proporcionan la funcionalidad necesaria para codificar los datos para la transmisión y descodificar los mensajes PKCS \# 7 recibidos. También se proporciona funcionalidad para descifrar y comprobar las firmas de los mensajes recibidos. No se recomienda el uso de estas funciones de mensaje de bajo nivel en la mayoría de las aplicaciones. Para la mayoría de las aplicaciones, se prefiere el uso de funciones de mensaje simplificadas, que encapsulan varias funciones de mensaje de bajo nivel en una sola llamada de función.

| Función                                                                                   | Descripción                                                                                                                                                                                                                    |
|--------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptMsgCalculateEncodedLength**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcalculateencodedlength)                   | Calcula la longitud de un mensaje criptográfico codificado.                                                                                                                                                                     |
| [**CryptMsgClose**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgclose)                                                     | Cierra un identificador de un mensaje criptográfico.                                                                                                                                                                                    |
| [**CryptMsgControl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcontrol)                                                 | Realiza una función de control especial después de [**la CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate) final de un mensaje criptográfico codificado o descodificado.                                                                                   |
| [**CryptMsgCountersign**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersign)                                         | Contrasigna una firma ya existente en un mensaje.                                                                                                                                                                       |
| [**CryptMsgCountersignEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgcountersignencoded)                           | Contrasigna una firma ya existente (SignerInfo codificado, tal como se define en PKCS \# 7).                                                                                                                                       |
| [**CryptMsgDuplicate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgduplicate)                                             | Duplica un identificador de mensaje criptográfico incrementando el recuento [*de referencias*](../secgloss/r-gly.md). El recuento de referencias realiza un seguimiento de la duración del mensaje. |
| [**CryptMsgGetParam**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsggetparam)                                               | Adquiere un parámetro después de codificar o codificar un mensaje criptográfico.                                                                                                                                                       |
| [**CryptMsgOpenToDecode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentodecode)                                       | Abre un mensaje criptográfico para la decodificación.                                                                                                                                                                                    |
| [**CryptMsgOpenToEncode**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgopentoencode)                                       | Abre un mensaje criptográfico para la codificación.                                                                                                                                                                                    |
| [**CryptMsgUpdate**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgupdate)                                                   | Actualiza el contenido de un mensaje criptográfico.                                                                                                                                                                               |
| [**CryptMsgVerifyCountersignatureEncoded**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencoded)     | Comprueba una [*contrasignación en*](../secgloss/c-gly.md) términos de la estructura SignerInfo (tal y como se define en PKCS \# 7).                                                   |
| [**CryptMsgVerifyCountersignatureEncodedEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmsgverifycountersignatureencodedex) | Comprueba que el *parámetro pbSignerInfoCounterSignature* contiene el [*hash*](../secgloss/h-gly.md) cifrado del **campo encryptedDigest** de la estructura de *parámetros pbSignerInfo.*   |



 

### <a name="simplified-message-functions"></a>Funciones de mensaje simplificadas

[*Las funciones de mensaje simplificadas*](../secgloss/s-gly.md) encapsulan funciones de mensaje de bajo nivel en una sola función para realizar una tarea especificada.

| Función                                                                               | Descripción                                                                                                                                                                                                                                                                  |
|----------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptDecodeMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodemessage)                                       | Descodifica un mensaje criptográfico.                                                                                                                                                                                                                                             |
| [**CryptDecryptAndVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptandverifymessagesignature) | Descifra el mensaje especificado y comprueba el firmante.                                                                                                                                                                                                                     |
| [**CryptDecryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecryptmessage)                                     | Descifra el mensaje especificado.                                                                                                                                                                                                                                              |
| [**CryptEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencryptmessage)                                     | Cifra el mensaje para el destinatario o los destinatarios.                                                                                                                                                                                                                        |
| [**CryptGetMessageCertificates**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagecertificates)                     | Devuelve el [*almacén de certificados*](../secgloss/c-gly.md) que contiene los certificados y las [*CRL del mensaje.*](../secgloss/c-gly.md) |
| [**CryptGetMessageSignerCount**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetmessagesignercount)                       | Devuelve el recuento de firmantes en el mensaje firmado.                                                                                                                                                                                                                          |
| [**CryptHashMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashmessage)                                           | Crea un hash del mensaje.                                                                                                                                                                                                                                               |
| [**CryptSignAndEncryptMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencryptmessage)                       | Firma el mensaje y, a continuación, lo cifra para el destinatario o los destinatarios.                                                                                                                                                                                                     |
| [**CryptSignMessageWithKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessagewithkey)                             | Firma un mensaje con la clave privada de un CSP especificada en los parámetros de la función.                                                                                                                                                                                       |
| [**CryptSignMessage**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignmessage)                                           | Firma el mensaje.                                                                                                                                                                                                                                                           |
| [**CryptVerifyDetachedMessageHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifydetachedmessagehash)               | Comprueba un mensaje con hash que contiene un hash desasociado.                                                                                                                                                                                                                     |
| [**CryptVerifyDetachedMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifydetachedmessagesignature)     | Comprueba un mensaje firmado que contiene una firma o firmas desasociadas.                                                                                                                                                                                                  |
| [**CryptVerifyMessageHash**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagehash)                               | Comprueba un mensaje con hash.                                                                                                                                                                                                                                                   |
| [**CryptVerifyMessageSignature**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignature)                     | Comprueba un mensaje firmado.                                                                                                                                                                                                                                                   |
| [**CryptVerifyMessageSignatureWithKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifymessagesignaturewithkey)       | Comprueba la firma de un mensaje firmado mediante la información de clave pública especificada.                                                                                                                                                                                             |



 

## <a name="auxiliary-functions"></a>Funciones auxiliares

Las funciones auxiliares se agrupan de la siguiente manera:

-   Administración de datos functions
-   Funciones de conversión de datos
-   Funciones de uso mejorado de claves
-   Funciones de identificador de clave
-   Funciones de compatibilidad de OID
-   Funciones de recuperación de objetos remotos
-   Funciones PFX

### <a name="data-management-functions"></a>Administración de datos functions

Las siguientes funciones cryptoAPI administran datos y certificados.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Función</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificate"><strong>CertCompareCertificate</strong></a></td>
<td>Compara dos certificados para determinar si son idénticos.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparecertificatename"><strong>CertCompareCertificateName</strong></a></td>
<td>Compara dos nombres de certificado para determinar si son idénticos.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcompareintegerblob"><strong>CertCompareIntegerBlob</strong></a></td>
<td>Compara dos blobs <a href="/windows/desktop/SecGloss/b-gly"><em>enteros</em></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certcomparepublickeyinfo"><strong>CertComparePublicKeyInfo</strong></a></td>
<td>Compara dos <a href="/windows/desktop/SecGloss/p-gly"><em>claves públicas para</em></a> determinar si son idénticas.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindattribute"><strong>CertFindAttribute</strong></a></td>
<td>Busca el primer atributo identificado por su <a href="/windows/desktop/SecGloss/o-gly"><em>identificador de objeto</em></a> (OID).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindextension"><strong>CertFindExtension</strong></a></td>
<td>Busca la primera extensión identificada por su OID.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certfindrdnattr"><strong>CertFindRDNAttr</strong></a></td>
<td>Busca el primer atributo <a href="/windows/desktop/SecGloss/r-gly"><em>RDN</em></a> identificado por su OID en la lista de nombres de los nombres <em>distintivos relativos</em>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certgetintendedkeyusage"><strong>CertGetIntendedKeyUsage</strong></a></td>
<td>Adquiere los bytes de uso de clave previstos del certificado.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certgetpublickeylength"><strong>CertGetPublicKeyLength</strong></a></td>
<td>Adquiere la longitud de bits de la clave pública o privada a partir de <a href="/windows/desktop/SecGloss/p-gly"><em>la clave pública BLOB</em></a>.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certisrdnattrsincertificatename"><strong>CertIsRDNAttrsInCertificateName</strong></a></td>
<td>Compara los atributos del <a href="/windows/desktop/SecGloss/c-gly"><em>nombre</em></a> del certificado con los atributos CERT_RDN <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_rdn"><strong>para</strong></a> determinar si todos los atributos se incluyen allí.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certisstronghashtosign"><strong>CertIsStrongHashToSign</strong></a></td>
<td>Determina si el algoritmo hash especificado y la clave pública del certificado de firma se pueden usar para realizar una firma segura.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycrlrevocation"><strong>CertVerifyCRLRevocation</strong></a></td>
<td>Comprueba que el certificado de sujeto no está en la lista <a href="/windows/desktop/SecGloss/c-gly"><em>de revocación de certificados</em></a> (CRL).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifycrltimevalidity"><strong>CertVerifyCRLTimeValidity</strong></a></td>
<td>Comprueba la validez de hora de una CRL.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation"><strong>CertVerifyRevocation</strong></a></td>
<td>Comprueba que el certificado de sujeto no está en la CRL.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifytimevalidity"><strong>CertVerifyTimeValidity</strong></a></td>
<td>Comprueba la validez de hora de un certificado.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyvaliditynesting"><strong>CertVerifyValidityNesting</strong></a></td>
<td>Comprueba que la validez de la hora del sujeto se anida dentro de la validez de la hora del emisor.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8"><strong>CryptExportPKCS8</strong></a></td>
<td>Esta función se reemplaza por la <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8ex"><strong>función CryptExportPKCS8Ex.</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpkcs8ex"><strong>CryptExportPKCS8Ex</strong></a></td>
<td>Exporta la clave privada en formato #8 PKCS.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfo"><strong>CryptExportPublicKeyInfo</strong></a></td>
<td>Exporta la información de clave pública asociada a la clave privada correspondiente del proveedor.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfoex"><strong>CryptExportPublicKeyInfoEx</strong></a></td>
<td>Exporta la información de clave pública asociada a la clave privada correspondiente del proveedor. Esta función difiere de <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfo"><strong>CryptExportPublicKeyInfo</strong></a> en que el usuario puede especificar el algoritmo de clave pública, lo que invalida el valor predeterminado proporcionado por el CSP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfofrombcryptkeyhandle"><strong>CryptExportPublicKeyInfoFromBCryptKeyHandle</strong></a></td>
<td>Exporta la información de clave pública asociada a la clave privada correspondiente de un proveedor.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindcertificatekeyprovinfo"><strong>CryptFindCertificateKeyProvInfo</strong></a></td>
<td>Enumera los proveedores criptográficos y <a href="/windows/desktop/SecGloss/k-gly"><em>sus</em></a> contenedores de claves para buscar la clave privada que corresponde a la clave pública de un certificado.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindlocalizedname"><strong>CryptFindLocalizedName</strong></a></td>
<td>Busca el nombre localizado de un nombre especificado, por ejemplo, busca el nombre localizado para el nombre del almacén del sistema raíz.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashcertificate"><strong>CryptHashCertificate</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Aplica un algoritmo hash al contenido codificado.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashcertificate2"><strong>CryptHashCertificate2</strong></a></td>
<td>Aplica un algoritmo hash a un bloque de datos mediante un proveedor de hash Cryptography API: Next Generation (CNG).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashpublickeyinfo"><strong>CryptHashPublicKeyInfo</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Calcula el hash de la información de clave pública codificada.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-crypthashtobesigned"><strong>CryptHashToBeSigned</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Calcula el hash de que se va a firmar la información en el contenido firmado codificado &quot; &quot; (<a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_signed_content_info"><strong>CERT_SIGNED_CONTENT_INFO</strong></a>).</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8"><strong>CryptImportPKCS8</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Importa la <a href="/windows/desktop/SecGloss/p-gly"><em>clave privada en</em></a> formato de #8 PKCS a un proveedor de servicios <a href="/windows/desktop/SecGloss/c-gly"><em>criptográficos</em></a> (CSP).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfo"><strong>CryptImportPublicKeyInfo</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Convierte e importa información de clave pública en el proveedor y devuelve un identificador de la clave pública.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex"><strong>CryptImportPublicKeyInfoEx</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Convierte e importa la información de clave pública en el proveedor y devuelve un identificador de la clave pública. Se proporcionan parámetros adicionales (sobre los especificados por <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfo"><strong>CryptImportPublicKeyInfo)</strong></a>que se pueden usar para invalidar los valores predeterminados para complementar <a href="/windows/desktop/api/Wincrypt/ns-wincrypt-cert_public_key_info"><strong>CERT_PUBLIC_KEY_INFO</strong></a>.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2"><strong>CryptImportPublicKeyInfoEx2</strong></a></td>
<td>Importa una clave pública en un proveedor asimétrico CNG.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemalloc"><strong>CryptMemAlloc</strong></a></td>
<td>Asigna memoria para un búfer. Todas las funciones Crypt32.lib que devuelven búferes asignados usan esta memoria.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemfree"><strong>CryptMemFree</strong></a></td>
<td>Libera la memoria asignada por <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemalloc"><strong>CryptMemAlloc</strong></a> o <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemrealloc"><strong>CryptMemRealloc.</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptmemrealloc"><strong>CryptMemRealloc</strong></a></td>
<td>Libera la memoria asignada actualmente para un búfer y asigna memoria para un nuevo búfer.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptqueryobject"><strong>CryptQueryObject</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Recupera información sobre el contenido de un blob o un archivo.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate"><strong>CryptSignAndEncodeCertificate</strong></a></td>
<td>Codifica la información que se va a firmar, firma esta información codificada y codifica &quot; la información firmada y &quot; codificada resultante.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsigncertificate"><strong>CryptSignCertificate</strong></a></td>
<td>Firma la &quot; información que se va a firmar en el contenido codificado y &quot; firmado.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipaddprovider"><strong>CryptSIPAddProvider</strong></a></td>
<td>Agrega un paquete de interfaz de sujeto (SIP).</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipcreateindirectdata"><strong>CryptSIPCreateIndirectData</strong></a></td>
<td>Devuelve una <a href="/windows/win32/api/mssip/ns-mssip-sip_indirect_data"><strong>SIP_INDIRECT_DATA</strong></a> estructura que contiene un <a href="/windows/desktop/SecGloss/h-gly"><em>hash</em></a> de la estructura SIP_SUBJECTINFO <a href="/windows/win32/api/mssip/ns-mssip-sip_subjectinfo"><strong>proporcionada,</strong></a> el algoritmo de resumen y un atributo de codificación. El hash se puede usar como referencia indirecta a los datos.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipgetcaps"><strong>CryptSIPGetCaps</strong></a></td>
<td>Recupera las funciones de un SIP.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipgetsigneddatamsg"><strong>CryptSIPGetSignedDataMsg</strong></a></td>
<td>Recupera una firma Authenticode del archivo.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipload"><strong>CryptSIPLoad</strong></a></td>
<td>Carga la biblioteca de vínculos dinámicos que implementa un paquete de interfaz de asunto y asigna las funciones de exportación de biblioteca adecuadas a <a href="/windows/win32/api/mssip/ns-mssip-sip_dispatch_info"><strong>SIP_DISPATCH_INFO</strong></a> estructura.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipputsigneddatamsg"><strong>CryptSIPPutSignedDataMsg</strong></a></td>
<td>Almacena una firma Authenticode en el archivo de destino.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipremoveprovider"><strong>CryptSIPRemoveProvider</strong></a></td>
<td>Quita un OBJETO SIP agregado por una llamada anterior a la <a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipaddprovider"><strong>función CryptSIPAddProvider.</strong></a></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipremovesigneddatamsg"><strong>CryptSIPRemoveSignedDataMsg</strong></a></td>
<td>Quita una firma Authenticode especificada.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipretrievesubjectguid"><strong>CryptSIPRetrieveSubjectGuid</strong></a></td>
<td>Recupera un GUID basado en la información de encabezado de un archivo especificado.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipretrievesubjectguidforcatalogfile"><strong>CryptSIPRetrieveSubjectGuidForCatalogFile</strong></a></td>
<td>Recupera el GUID del asunto asociado al archivo especificado.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Mssip/nf-mssip-cryptsipverifyindirectdata"><strong>CryptSIPVerifyIndirectData</strong></a></td>
<td>Valida los datos hash indirectos en el asunto proporcionado.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Dpapi/nf-dpapi-cryptupdateprotectedstate"><strong>CryptUpdateProtectedState</strong></a></td>
<td>Migra las claves maestras del usuario actual <a href="/windows/desktop/SecGloss/s-gly"><em></em></a> después de que haya cambiado el identificador de seguridad (SID) del usuario.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignature"><strong>CryptVerifyCertificateSignature</strong></a></td>
<td>Comprueba la firma de un certificado de sujeto o <a href="/windows/desktop/SecGloss/c-gly"><em>una CRL</em></a> mediante la información de clave pública.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignatureex"><strong>CryptVerifyCertificateSignatureEx</strong></a></td>
<td>Una versión extendida de <a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptverifycertificatesignature"><strong>CryptVerifyCertificateSignature.</strong></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-getencschannel"><strong>GetEncSChannel</strong></a></td>
<td>Almacena el contenido cifrado de dll de Schannel en memoria.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Mssip/nc-mssip-pcryptsipgetcaps"><strong>pCryptSIPGetCaps</strong></a></td>
<td>Implementado por un SIP para informar de las funcionalidades.</td>
</tr>
</tbody>
</table>



 

### <a name="data-conversion-functions"></a>Funciones de conversión de datos

Las siguientes funciones de CryptoAPI convierten los miembros de la estructura de certificados en formularios diferentes.

| Función                                           | Descripción                                                                                                                                                                                                                                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertAlgIdToOID**](/windows/desktop/api/Wincrypt/nf-wincrypt-certalgidtooid)           | Convierte un identificador de algoritmo CryptoAPI (id. de ALG) en una cadena de identificador de objeto (OID) de la notación de sintaxis abstracta One \_ (ASN.1). [](../secgloss/a-gly.md) [](../secgloss/o-gly.md) |
| [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)     | Adquiere el nombre del firmante o emisor de un certificado y lo convierte en una cadena de caracteres terminada en NULL.                                                                                                                                                                                                               |
| [**CertNameToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certnametostra)             | Convierte un blob de nombre de [*certificado*](../secgloss/b-gly.md) en una cadena terminada en cero.                                                                                                                                                                                                      |
| [**CertOIDToAlgId**](/windows/desktop/api/Wincrypt/nf-wincrypt-certoidtoalgid)           | Convierte la cadena del identificador de objeto ASN.1 en el identificador del algoritmo CSP.                                                                                                                                                                                                                                                 |
| [**CertRDNValueToStr**](/windows/desktop/api/Wincrypt/nf-wincrypt-certrdnvaluetostra)     | Convierte un valor de nombre en una cadena terminada en NULL.                                                                                                                                                                                                                                                                           |
| [**CertStrToName**](/windows/desktop/api/Wincrypt/nf-wincrypt-certstrtonamea)             | Convierte una cadena [*X.500*](../secgloss/x-gly.md) terminada en NULL en un nombre de certificado codificado.                                                                                                                                                                                          |
| [**CryptBinaryToString**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptbinarytostringa) | Convierte una secuencia binaria en una cadena con formato.                                                                                                                                                                                                                                                                          |
| [**CryptFormatObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptformatobject)     | Da formato a los datos codificados y devuelve una cadena Unicode.                                                                                                                                                                                                                                                                          |
| [**CryptStringToBinary**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptstringtobinarya) | Convierte una cadena con formato en una secuencia binaria.                                                                                                                                                                                                                                                                            |



 

### <a name="enhanced-key-usage-functions"></a>Funciones mejoradas de uso de claves

Las siguientes funciones se tratan con la [*extensión de uso mejorado*](../secgloss/e-gly.md) de claves (EKU) y la propiedad extendida EKU de los certificados. La extensión EKU y la propiedad extendida especifican y limitan los usos válidos de un certificado. Las extensiones forman parte del propio certificado. El emisor del certificado los establece y son de solo lectura. Las propiedades extendidas por certificado son valores asociados a un certificado que se puede establecer en una aplicación.

| Función                                                                             | Descripción                                                                    |
|--------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [**CertAddEnhancedKeyUsageIdentifier**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddenhancedkeyusageidentifier)       | Agrega un identificador de uso a la propiedad EKU de un certificado.                       |
| [**CertGetEnhancedKeyUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetenhancedkeyusage)                           | Adquiere, a partir de un certificado, información sobre la extensión o propiedad EKU. |
| [**CertRemoveEnhancedKeyUsageIdentifier**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremoveenhancedkeyusageidentifier) | Quita el identificador de uso de la propiedad extendida EKU de un certificado.       |
| [**CertSetEnhancedKeyUsage**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetenhancedkeyusage)                           | Establece la propiedad EKU de un certificado.                                       |



 

### <a name="key-identifier-functions"></a>Funciones de identificador de clave

Las funciones de identificador de clave permiten al usuario crear, establecer, recuperar o buscar un identificador de clave o sus propiedades.

Un identificador de clave es el identificador único de un par de claves pública [*y privada.*](../secgloss/p-gly.md) Puede ser cualquier identificador único, pero normalmente es el hash SHA1 de 20 bytes de una estructura [**CERT PUBLIC KEY INFO \_ \_ \_ codificada.**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_public_key_info) Se puede obtener un identificador de clave a través del identificador prop del IDENTIFICADOR DE CLAVE \_ \_ CERT DEL \_ \_ certificado. El identificador de clave permite el uso de ese [*par de claves*](../secgloss/k-gly.md) para cifrar o descifrar mensajes sin usar el certificado.

Los identificadores de clave no están asociados a [*CRL*](../secgloss/c-gly.md) ni [*ACL.*](../secgloss/c-gly.md)

Un identificador de clave puede tener las mismas propiedades que un contexto de certificado. Para obtener más información, [**vea CertCreateContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-certcreatecontext).

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Función</th>
<th>Descripción</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptcreatekeyidentifierfromcsp"><strong>CryptCreateKeyIdentifierFromCSP</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Crea un identificador de clave a partir de <a href="/windows/desktop/SecGloss/p-gly"><em>blob de clave pública de CSP.</em></a></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties"><strong>CryptEnumKeyIdentifierProperties</strong></a></td>
<td>Enumera los identificadores clave y sus propiedades.</td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetkeyidentifierproperty"><strong>CryptGetKeyIdentifierProperty</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Adquiere una propiedad específica a partir de un identificador de clave especificado.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetkeyidentifierproperty"><strong>CryptSetKeyIdentifierProperty</strong></a></td>
<td><blockquote>
[!Important]<br />
Esta API está en desuso. El software nuevo y existente debe empezar a <a href="/windows/desktop/SecCNG/cng-portal">usar Cryptography Next Generation API.</a> Microsoft puede quitar esta API en futuras versiones.
</blockquote>
<br/> Establece una propiedad de un identificador de clave especificado.</td>
</tr>
</tbody>
</table>



 

### <a name="oid-support-functions"></a>Funciones de compatibilidad de OID

Estas funciones proporcionan [*compatibilidad con el*](../secgloss/o-gly.md) identificador de objetos (OID). Estas funciones instalan, registran y envían a OID y codifican funciones específicas del tipo.

Las siguientes funciones de CryptoAPI usan estas funciones de compatibilidad con OID:

-   [**CryptEncodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobject)
-   [**CryptEncodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptencodeobjectex)
-   [**CryptDecodeObject**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobject)
-   [**CryptDecodeObjectEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex)
-   [**CertVerifyRevocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certverifyrevocation)
-   [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore)

Para obtener información general sobre este proceso, vea [Extending CryptoAPI Functionality](extending-cryptoapi-functionality.md).

Las funciones siguientes funcionan con ID.

| Función                                                                       | Descripción                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptEnumOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidfunction)                           | Enumera las funciones de OID registradas identificadas por su tipo de codificación, nombre de función y OID.                                                                                                                 |
| [**CryptEnumOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo)                                   | Enumera la información de OID registrada identificada por su grupo y llama *a pfnEnumOIDInfo para* buscar coincidencias.                                                                                                       |
| [**CryptFindOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfindoidinfo)                                   | Usa la clave y el grupo especificados para buscar información de OID.                                                                                                                                                          |
| [**CryptFreeOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptfreeoidfunctionaddress)             | Libera el recuento de identificadores que se incrementó y devolvió [**mediante CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress) o [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress). |
| [**CryptGetDefaultOIDDllList**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoiddlllist)                 | Adquiere la lista de entradas DLL predeterminadas registradas para el conjunto de funciones y el tipo de codificación especificados.                                                                                                              |
| [**CryptGetDefaultOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetdefaultoidfunctionaddress) | Adquiere la primera o la siguiente función predeterminada instalada o carga el archivo DLL que contiene la función predeterminada.                                                                                                 |
| [**CryptGetOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionaddress)               | Busca en la lista de funciones instaladas un tipo de codificación y una coincidencia de OID. Si no se encuentra una coincidencia allí, se busca una coincidencia en el Registro.                                                                  |
| [**CryptGetOIDFunctionValue**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetoidfunctionvalue)                   | Adquiere el valor para el tipo de codificación, el nombre de función, el OID y el nombre de valor especificados.                                                                                                                            |
| [**CryptInitOIDFunctionSet**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinitoidfunctionset)                     | Inicializa y devuelve un identificador del conjunto de funciones OID identificado por el nombre de función proporcionado.                                                                                                                 |
| [**CryptInstallOIDFunctionAddress**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptinstalloidfunctionaddress)       | Instala un conjunto de direcciones de función OID a las que se puede llamar.                                                                                                                                                                 |
| [**CryptRegisterDefaultOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisterdefaultoidfunction)     | Registra el archivo DLL que contiene la función predeterminada a la que se va a llamar para el tipo de codificación y el nombre de función especificados.                                                                                               |
| [**CryptRegisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidfunction)                   | Registra el archivo DLL que contiene la función a la que se va a llamar para el tipo de codificación, el nombre de función y el OID especificados.                                                                                                 |
| [**CryptRegisterOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptregisteroidinfo)                           | Registra la información de OID especificada en la estructura [**\_ CRYPT OID \_ INFO**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_oid_info) y la conserva en el registro.                                                                                |
| [**CryptSetOIDFunctionValue**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptsetoidfunctionvalue)                   | Establece el valor del tipo de codificación, nombre de función, OID y nombre de valor especificados.                                                                                                                                |
| [**CryptUnregisterDefaultOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisterdefaultoidfunction) | Quita el registro del archivo DLL que contiene la función predeterminada a la que se va a llamar para el tipo de codificación y el nombre de función especificados.                                                                            |
| [**CryptUnregisterOIDFunction**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidfunction)               | Quita el registro del archivo DLL que contiene la función a la que se va a llamar para el tipo de codificación, el nombre de función y el OID especificados.                                                                              |
| [**CryptUnregisterOIDInfo**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptunregisteroidinfo)                       | Quita el registro de la información de OID especificada.                                                                                                                                                        |



 

### <a name="remote-object-retrieval-functions"></a>Funciones de recuperación remota de objetos

Las siguientes funciones permiten al usuario recuperar un objeto de infraestructura de clave pública (PKI), adquirir la dirección URL de un certificado, CTL o CRL, o extraer una dirección URL de un objeto.

| Función                                                     | Descripción                                                            |
|--------------------------------------------------------------|------------------------------------------------------------------------|
| [**CryptGetObjectUrl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgetobjecturl)               | Adquiere la dirección URL del objeto remoto a partir de un certificado, CTL o CRL. |
| [**CryptRetrieveObjectByUrl**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptretrieveobjectbyurla) | Recupera el objeto PKI de una ubicación especificada por una dirección URL.           |



 

### <a name="pfx-functions"></a>Funciones PFX

Las siguientes funciones admiten blobs en formato [](../secgloss/b-gly.md)Exchange información personal (PFX).

| Función                                             | Descripción                                                                                                                                                                                                                                                                  |
|------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**PFXExportCertStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxexportcertstore)     | Las exportaciones del certificado [*al que se hace referencia*](../secgloss/c-gly.md) almacenan los certificados y, si están disponibles, sus claves [*privadas asociadas.*](../secgloss/p-gly.md) |
| [**PFXExportCertStoreEx**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxexportcertstoreex) | Las exportaciones del certificado al que se hace referencia almacenan los certificados y, si están disponibles, sus claves privadas asociadas.                                                                                                                                                             |
| [**PFXImportCertStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfximportcertstore)     | Importa un BLOB PFX y devuelve el identificador de un almacén que contiene certificados y las claves privadas asociadas.                                                                                                                                                            |
| [**PFXIsPFXBlob**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxispfxblob)                 | Intenta descodificar la capa externa de un BLOB como un paquete PFX.                                                                                                                                                                                                                |
| [**PFXVerifyPassword**](/windows/desktop/api/Wincrypt/nf-wincrypt-pfxverifypassword)       | Intenta descodificar la capa externa de un BLOB como un paquete PFX y descifrarlo con la contraseña dada.                                                                                                                                                                      |



 

## <a name="certificate-services-backup-and-restore-functions"></a>Funciones de copia de seguridad y restauración de Servicios de certificados

Servicios de certificados incluye funciones para realizar copias de seguridad y restaurar la base de datos de Servicios de certificados. Estas funciones de copia de seguridad y restauración de Servicios de certificados se incluyen en Certadm.dll. A diferencia de los demás elementos de API asociados a Servicios de certificados, estas funciones no se encapsulan en un objeto que se pueda usar para llamar a métodos de clase. En su lugar, se llama a las API de copia de seguridad y restauración cargando primero la biblioteca de Certadm.dll en la memoria mediante una llamada a [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) y, a continuación, determinando la dirección de las funciones mediante una llamada a [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress). Cuando haya terminado de llamar a las funciones de copia de seguridad y restauración de Servicios de certificados, llame a [**FreeLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-freelibrary) para liberar Certadm.dll recursos de la memoria.

> [!Note]
> Las funciones de copia de seguridad y restauración Certadm.dll no copian ni restauran las [*claves privadas del servicio de certificados.*](../secgloss/p-gly.md) Para obtener información sobre la copia de seguridad de las claves privadas de Servicios de certificados, vea Copia de seguridad y [restauración de la clave privada de Servicios de certificados](backing-up-and-restoring-the-certificate-services-private-key.md).
> 
> Para llamar a las funciones de copia de seguridad y restauración, debe tener privilegios de copia de [*seguridad y restauración*](../secgloss/p-gly.md). Para obtener más información, vea [Establecer los privilegios de copia de seguridad y restauración.](setting-the-backup-and-restore-privileges.md)

 

> [!Note]  
> Si se llamó previamente a **CoInitializeEx** en el mismo subproceso usado para llamar a las API de copia de seguridad y restauración de Servicios de certificados, la marca COINIT APARTMENTTHREADED se debe haber pasado a \_ **CoInitializeEx**. Es decir, cuando se usa el mismo subproceso, no se puede llamar a la API de copia de seguridad y restauración de Servicios de certificados si el subproceso ha pasado previamente la marca COINIT MULTITHREADED en una llamada \_ a **CoInitializeEx**.

 

Las API de copia de seguridad de Servicios de certificados se definen en Certbcli.h. Sin embargo, al crear el programa, use Certsrv.h como archivo de incluir.

Las siguientes API se exportan mediante Certadm.dll.

| Función                                                                         | Descripción                                                                                                           |
|----------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [**CertSrvBackupClose**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupclose)                                 | Cierra un archivo abierto.                                                                                                |
| [**CertSrvBackupEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupend)                                     | Finaliza una sesión de copia de seguridad.                                                                                                |
| [**CertSrvBackupFree**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupfree)                                   | Libera un búfer asignado por las API de copia de seguridad y restauración.                                                              |
| [**CertSrvBackupGetBackupLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetbackuplogsw)                 | Devuelve una lista de archivos de registro de los que es necesario realizar una copia de seguridad.                                                                |
| [**CertSrvBackupGetDatabaseNames**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdatabasenamesw)           | Devuelve una lista de archivos de base de datos de los que es necesario realizar una copia de seguridad.                                                           |
| [**CertSrvBackupGetDynamicFileList**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupgetdynamicfilelistw)       | Recupera la lista de nombres de archivos dinámicos de Servicios de certificados de los que se debe realizar una copia de seguridad para el contexto de copia de seguridad especificado. |
| [**CertSrvBackupOpenFile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupopenfilew)                           | Abre un archivo como preparación para la copia de seguridad.                                                                        |
| [**CertSrvBackupPrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuppreparew)                             | Prepara la base de datos para la copia de seguridad en línea.                                                                          |
| [**CertSrvBackupRead**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackupread)                                   | Lee el contenido de un archivo abierto.                                                                                 |
| [**CertSrvBackupTruncateLogs**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvbackuptruncatelogs)                   | Trunca los archivos de registro.                                                                                              |
| [**CertSrvIsServerOnline**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvisserveronlinew)                           | Determina si un servidor de Servicios de certificados está en línea (en ejecución activa).                                        |
| [**CertSrvRestoreEnd**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreend)                                   | Finaliza una sesión de restauración.                                                                                               |
| [**CertSrvRestoreGetDatabaseLocations**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoregetdatabaselocationsw) | Recupera las ubicaciones de base de datos (que se usan para escenarios de copia de seguridad y restauración).                                            |
| [**CertSrvRestorePrepare**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestorepreparew)                           | Comienza una sesión de restauración.                                                                                             |
| [**CertSrvRestoreRegister**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterw)                         | Registra una operación de restauración.                                                                                        |
| [**CertSrvRestoreRegisterComplete**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregistercomplete)         | Completa una operación de restauración registrada previamente.                                                                  |
| [**CertSrvRestoreRegisterThroughFile**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvrestoreregisterthroughfile)   | Registra una operación de restauración.                                                                                        |
| [**CertSrvServerControl**](/windows/desktop/api/Certbcli/nf-certbcli-certsrvservercontrolw)                             | Envía un comando de control a la instancia de Servicios de certificados.                                                         |



 

## <a name="callback-functions"></a>Funciones de devolución de llamada

Las funciones de devolución de llamada de esta [](../secgloss/c-gly.md) sección se usan para registrar o instalar proveedores de almacén de certificados definidos por la aplicación y para proporcionar funcionalidad relacionada a través de funciones de devolución de llamada. Las funciones [*cryptoAPI*](../secgloss/c-gly.md) implementan las funciones de devolución de llamada. Las funciones de devolución de llamada permiten a la aplicación controlar, en parte, la forma en que las funciones cryptoAPI manipulan los datos.

| Función de devolución de llamada                                                                                                        | Usar                                                                                                                                                                                                                                                                                                                                           |
|--------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CertChainFindByIssuerCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_chain_find_by_issuer_callback)                                                   | Función de devolución de llamada definida por la aplicación que permite a la aplicación filtrar los certificados que se podrían agregar a la cadena de certificados.                                                                                                                                                                                                     |
| [**CertDllOpenStoreProv**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_dll_open_store_prov_func)                                                                     | Define la función open del proveedor de almacén.                                                                                                                                                                                                                                                                                                     |
| [**CertEnumPhysicalStoreCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_physical_store)                                                   | Función de devolución de llamada utilizada por [**la función CertEnumPhysicalStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumphysicalstore) para dar formato y presentar información sobre cada almacén físico encontrado.                                                                                                                                                                                 |
| [**CertEnumSystemStoreCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_system_store)                                                       | Función de devolución de llamada utilizada por [**la función CertEnumSystemStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstore) para dar formato y presentar información sobre cada almacén físico encontrado.                                                                                                                                                                                     |
| [**CertEnumSystemStoreLocationCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_enum_system_store_location)                                       | Función de devolución de llamada utilizada por [**la función CertEnumSystemStoreLocation**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumsystemstorelocation) para dar formato y presentar información sobre cada almacén físico encontrado.                                                                                                                                                                     |
| [**CertStoreProvCloseCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_close)                                                         | Determina lo que sucede cuando el recuento de referencias de un [*almacén*](../secgloss/r-gly.md) abierto se convierte en cero.                                                                                                                                                                                    |
| [**CertStoreProvControl**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_control)                                                                     | Permite notificar a una aplicación cuando hay una diferencia entre el contenido de un almacén almacenado en caché en uso y el contenido de ese almacén a medida que se conserva en el almacenamiento.                                                                                                                                                                   |
| [**CertStoreProvDeleteCertCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_delete_cert)                                               | Determina las acciones que se deben realizar antes de eliminar un certificado de un almacén de certificados.                                                                                                                                                                                                                                                      |
| [**CertStoreProvDeleteCRLCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_delete_crl)                                                 | Determina las acciones que se deben realizar antes de eliminar una lista de [*revocación*](../secgloss/c-gly.md) de certificados (CRL) de un almacén de certificados.                                                                                                                        |
| [**CertStoreProvDeleteCTL**](certstoreprovdeletectl.md)                                                                 | Determina si se puede eliminar una CTL.                                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvFindCert**](certstoreprovfindcert.md)                                                                   | Busca el primer o el siguiente certificado en un almacén que coincida con los criterios especificados.                                                                                                                                                                                                                                                             |
| [**CertStoreProvFindCRL**](certstoreprovfindcrl.md)                                                                     | Busca la primera CRL, o la siguiente, en un almacén que coincida con los criterios especificados.                                                                                                                                                                                                                                                                     |
| [**CertStoreProvFindCTL**](certstoreprovfindctl.md)                                                                     | Busca la primera CTL, o la siguiente, en un almacén que coincida con los criterios especificados.                                                                                                                                                                                                                                                                     |
| [**CertStoreProvFreeFindCert**](certstoreprovfreefindcert.md)                                                           | Libera un contexto de certificado encontrado anteriormente.                                                                                                                                                                                                                                                                                                 |
| [**CertStoreProvFreeFindCRL**](certstoreprovfreefindcrl.md)                                                             | Libera un contexto de CRL encontrado anteriormente.                                                                                                                                                                                                                                                                                                         |
| [**CertStoreProvFreeFindCTL**](certstoreprovfreefindctl.md)                                                             | Libera un contexto de CTL encontrado anteriormente.                                                                                                                                                                                                                                                                                                         |
| [**CertStoreProvGetCertProperty**](certstoreprovgetcertproperty.md)                                                     | Recupera una propiedad especificada de un certificado.                                                                                                                                                                                                                                                                                              |
| [**CertStoreProvGetCRLProperty**](certstoreprovgetcrlproperty.md)                                                       | Recupera una propiedad especificada de una CRL.                                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvGetCTLProperty**](certstoreprovgetctlproperty.md)                                                       | Recupera una propiedad especificada de una CTL.                                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvReadCertCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_read_cert)                                                   | Actualmente no se usa, pero se puede exportar a futuros CSP.                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvReadCRLCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_read_crl)                                                     | Actualmente no se usa, pero se puede exportar a futuros CSP.                                                                                                                                                                                                                                                                                      |
| [**CertStoreProvReadCTL**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_store_prov_read_ctl)                                                                     | Lea la copia del proveedor del contexto de CTL y, si existe, cree un nuevo contexto de CTL.                                                                                                                                                                                                                                                     |
| [**CertStoreProvSetCertPropertyCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_cert_property)                                     | Determina las acciones que se deben realizar antes de una llamada a [**CertSetCertificateContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcertificatecontextproperty) o [**CertGetCertificateContextProperty.**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcertificatecontextproperty)                                                                                                                             |
| [**CertStoreProvSetCRLPropertyCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_crl_property)                                       | Determina las acciones que se deben realizar antes de una llamada a [**CertSetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certsetcrlcontextproperty) o [**CertGetCRLContextProperty**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetcrlcontextproperty).                                                                                                                                                             |
| [**CertStoreProvSetCTLProperty**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_set_ctl_property)                                                       | Determina si una propiedad se puede establecer en una CTL.                                                                                                                                                                                                                                                                                            |
| [**CertStoreProvWriteCertCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_cert)                                                 | Determina las acciones que se deben realizar antes de agregar un certificado a un almacén.                                                                                                                                                                                                                                                                        |
| [**CertStoreProvWriteCRLCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_crl)                                                   | Determina las acciones que se deben realizar antes de agregar una CRL a un almacén.                                                                                                                                                                                                                                                                                |
| [**CertStoreProvWriteCTL**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_cert_store_prov_write_ctl)                                                                   | Determina si se puede agregar una CTL al almacén.                                                                                                                                                                                                                                                                                           |
| [**CRYPT \_ ENUM \_ KEYID \_ PROP**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_keyid_prop)                                                                | Función de devolución de llamada usada por [**la función CryptEnumKeyIdentifierProperties.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumkeyidentifierproperties)                                                                                                                                                                                                                          |
| [**FUNCIÓN \_ OID DE CRYPT ENUM \_ \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_oid_func)                                                            | Función de devolución de llamada usada por [**la función CryptEnumOIDFunction.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidfunction)                                                                                                                                                                                                                                                  |
| [**INFORMACIÓN DE \_ \_ OID DE CRYPT ENUM \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_enum_oid_info)                                                                    | Función de devolución de llamada usada por [**la función CryptEnumOIDInfo.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptenumoidinfo)                                                                                                                                                                                                                                                          |
| [**CryptGetSignerCertificateCallback**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_get_signer_certificate)                                           | Función de devolución de llamada usada con la [**estructura \_ CRYPT VERIFY \_ MESSAGE \_ PARA**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_verify_message_para) para obtener y comprobar el certificado de un firmante de mensajes.                                                                                                                                                                                 |
| [**PCRYPT \_ DECRYPT \_ PRIVATE \_ KEY \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_decrypt_private_key_func)                                           | Función de devolución de llamada usada por [**la función CryptImportPKCS8.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8)                                                                                                                                                                                                                                                          |
| [**PCRYPT \_ ENCRYPT \_ PRIVATE \_ KEY \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_encrypt_private_key_func)                                           | Función de devolución de llamada usada al crear la [**estructura CRYPT \_ ENCRYPTED PRIVATE \_ KEY \_ \_ INFO.**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_encrypted_private_key_info)                                                                                                                                                                                                          |
| [**PCRYPT \_ RESOLVE \_ HCRYPTPROV \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pcrypt_resolve_hcryptprov_func)                                              | Función de devolución de llamada usada por [**la función CryptImportPKCS8.**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpkcs8)                                                                                                                                                                                                                                                          |
| [**DEVOLUCIÓN DE LLAMADA \_ DE ERROR DE ANÁLISIS DE CDF \_ \_ \_ PFN**](/windows/win32/api/mscat/nc-mscat-pfn_cdf_parse_error_callback)                                                 | Función definida por el usuario llamada para errores de función de definición de catálogo al analizar un archivo de definición de catálogo (CDF).                                                                                                                                                                                                                          |
| [**PFN \_ CERT \_ CREATE \_ CONTEXT \_ SORT \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cert_create_context_sort_func)                                      | Se llama para cada entrada de contexto ordenada cuando se crea un contexto.                                                                                                                                                                                                                                                                               |
| [**CLAVE DE CIFRADO DE CONTENIDO DE IMPORTACIÓN DE CONTENIDO DE \_ PFN CMSG \_ \_ \_ \_ CNG \_**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_content_encrypt_key)                         | Función [*instalable*](../secgloss/o-gly.md) de identificador de objeto CNG (OID) para importar una clave de cifrado de contenido (CEK) ya descifrada.                                                                                                                                       |
| [**PFN \_ CMSG \_ CNG \_ IMPORT \_ KEY \_ AGREE**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_agree)                                              | Importa una clave de cifrado de contenido para un destinatario de transporte de claves de un mensaje envoltorio.                                                                                                                                                                                                                                                       |
| [**PFN \_ CMSG \_ CNG \_ IMPORT \_ KEY \_ TRANS**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_cng_import_key_trans)                                              | Una función instalable de OID [](../secgloss/d-gly.md) de CNG para importar y descifrar una clave de cifrado de contenido (CEK) de destinatario de transporte de [*claves,*](../secgloss/e-gly.md) cifrada.                                                                   |
| [**ACUERDO DE \_ CLAVE DE EXPORTACIÓN DE CMSG \_ \_ DE \_ PFN**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_agree)                                                       | Cifra y exporta la clave de cifrado de contenido para un destinatario del contrato de clave de un mensaje envoltorio.                                                                                                                                                                                                                                        |
| [**PFN \_ CMSG \_ EXPORT \_ KEY \_ TRANS**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_key_trans)                                                       | Cifra y exporta la clave de cifrado de contenido para un destinatario de transporte de claves de un mensaje con sobres.                                                                                                                                                                                                                                        |
| [**LISTA DE CORREO \_ DE EXPORTACIÓN DE CMSG \_ \_ DE \_ PFN**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_export_mail_list)                                                       | Cifra y exporta la clave de cifrado de contenido para un destinatario de la lista de distribución de correo de un mensaje con sobres.                                                                                                                                                                                                                                         |
| [**CLAVE DE CIFRADO DE CONTENIDO DE PFN \_ CMSG \_ \_ \_ \_ GEN**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_gen_content_encrypt_key)                                        | Genera la clave [*simétrica que se*](../secgloss/s-gly.md) usa para cifrar el contenido de un mensaje envoltorio.                                                                                                                                                                                     |
| [**ACUERDO DE \_ CLAVE DE IMPORTACIÓN DE CMSG \_ \_ DE \_ PFN**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_key_agree)                                                       | Importa una clave de cifrado de contenido para un destinatario de transporte de claves de un mensaje envoltorio.                                                                                                                                                                                                                                                       |
| [**PFN \_ CMSG \_ IMPORT \_ KEY \_ TRANS**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_key_trans)                                                       | Importa una clave de cifrado de contenido para un destinatario de transporte de claves de un mensaje envoltorio.                                                                                                                                                                                                                                                       |
| [**LISTA DE \_ CORREO DE IMPORTACIÓN DE CMSG \_ \_ DE \_ PFN**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_cmsg_import_mail_list)                                                       | Importa una clave de cifrado de contenido para un destinatario de transporte de claves de un mensaje envoltorio.                                                                                                                                                                                                                                                       |
| [**PFN \_ CRYPT \_ EXPORT \_ PUBLIC \_ KEY \_ INFO \_ EX2 \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_export_public_key_info_ex2_func)                    | Lo llama [**CryptExportPublicKeyInfoEx para**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptexportpublickeyinfoex) exportar un BLOB de clave pública y codificarlo.                                                                                                                                                                                                                         |
| [**PFN \_ CRYPT \_ EXTRACT \_ ENCODED \_ SIGNATURE \_ PARAMETERS \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_extract_encoded_signature_parameters_func) | Se llama para descodificar y devolver el identificador del algoritmo hash y, opcionalmente, los parámetros de firma.                                                                                                                                                                                                                                            |
| [**PFN \_ CRYPT \_ SIGN \_ AND \_ ENCODE \_ HASH \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_sign_and_encode_hash_func)                                 | Se llama para firmar y codificar un hash calculado.                                                                                                                                                                                                                                                                                                    |
| [**FUNCIÓN DE COMPROBACIÓN DE FIRMA CODIFICADA DE CIFRADO \_ \_ DE \_ \_ \_ PFN**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_crypt_verify_encoded_signature_func)                          | Se llama para descifrar una firma codificada y compararla con un hash calculado.                                                                                                                                                                                                                                                                     |
| [**PFN \_ IMPORT \_ PUBLIC \_ KEY \_ INFO \_ EX2 \_ FUNC**](/windows/win32/api/wincrypt/nc-wincrypt-pfn_import_public_key_info_ex2_func)                                 | Lo llama [**CryptImportPublicKeyInfoEx2**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportpublickeyinfoex2) para [](../secgloss/p-gly.md) descodificar el identificador del algoritmo de clave pública, cargar el proveedor de algoritmos e importar el [*par de claves*](../secgloss/k-gly.md). |
| [**PFNCCERTDISPLAYPROC**](pfnccertdisplayproc.md)                                                                       | Función de devolución de llamada definida por el usuario que permite al autor de la llamada de la función [**CryptUIDlgSelectCertificate**](cryptuidlgselectcertificate.md) controlar la presentación de los certificados que el usuario selecciona para ver.                                                                                                                               |
| [**PFNCMFILTERPROC**](/windows/desktop/api/CryptDlg/nc-cryptdlg-pfncmfilterproc)                                                                               | Filtra cada certificado para decidir si aparecerá en el cuadro de diálogo de selección de certificado que muestra la [**función CertSelectCertificate.**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea)                                                                                                                                                                |
| [**PFNCMHOOKPROC**](/windows/desktop/api/CryptDlg/nc-cryptdlg-pfncmhookproc)                                                                                   | Se llama antes de que el cuadro de diálogo de selección de certificado generado por la [**función CertSelectCertificate**](/windows/win32/api/cryptdlg/nf-cryptdlg-certselectcertificatea) procese los mensajes.                                                                                                                                                                                 |



 

## <a name="catalog-definition-functions"></a>Funciones de definición de catálogo

Estas funciones se usan para crear un catálogo. MakeCat llama a todas estas [funciones.](makecat.md)

| Función                                                                           | Descripción                                                                                                               |
|------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| [**CryptCATCDFClose**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfclose)                                       | Cierra un archivo de definición de catálogo y libera la memoria de la estructura [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) correspondiente. |
| [**CryptCATCDFEnumAttributesWithCDFTag**](cryptcatcdfenumattributeswithcdftag.md) | Enumera los atributos de los archivos de miembro en la **sección CatalogFiles** de una CDF.                                       |
| [**CryptCATCDFEnumCatAttributes**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfenumcatattributes)               | Enumera los atributos de nivel de catálogo dentro de **la sección CatalogHeader** de una CDF.                                        |
| [**CryptCATCDFEnumMembersByCDFTagEx**](cryptcatcdfenummembersbycdftagex.md)       | Enumera los miembros de archivo individuales en la **sección CatalogFiles** de una CDF.                                          |
| [**CryptCATCDFOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcdfopen)                                         | Abre una CDF existente para leer e inicializa una [**estructura CRYPTCATCDF.**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)                         |



 

## <a name="catalog-functions"></a>Funciones de catálogo

Estas funciones se usan para administrar un catálogo.

| Función                                                                             | Descripción                                                                                                                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CryptCATAdminAcquireContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext)                   | Adquiere un identificador para un contexto de administrador de catálogo. Este identificador se puede usar en llamadas posteriores a las funciones [**CryptCATAdminAddCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog), [**CryptCATAdminEnumCatalogFromHash**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminenumcatalogfromhash)y [**CryptCATAdminRemoveCatalog.**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminremovecatalog) |
| [**CryptCATAdminAcquireContext2**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext2)                 | Adquiere un identificador para un contexto de administrador de catálogo para un algoritmo hash y una directiva hash determinados.                                                                                                                                                                                                                                   |
| [**CryptCATAdminAddCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog)                           | Agrega un catálogo a la base de datos del catálogo.                                                                                                                                                                                                                                                                                            |
| [**CryptCATAdminCalcHashFromFileHandle**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadmincalchashfromfilehandle)   | Calcula el hash de un archivo.                                                                                                                                                                                                                                                                                                    |
| [**CryptCATAdminCalcHashFromFileHandle2**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadmincalchashfromfilehandle2) | Calcula el hash de un archivo mediante el algoritmo especificado.                                                                                                                                                                                                                                                                   |
| [**CryptCATAdminEnumCatalogFromHash**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminenumcatalogfromhash)         | Enumera los catálogos que contienen un hash especificado.                                                                                                                                                                                                                                                                             |
| [**CryptCATAdminReleaseCatalogContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminreleasecatalogcontext)     | Libera un identificador para un contexto de catálogo devuelto anteriormente por la [**función CryptCATAdminAddCatalog.**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminaddcatalog)                                                                                                                                                                                             |
| [**CryptCATAdminReleaseContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminreleasecontext)                   | Libera el identificador asignado previamente por la [**función CryptCATAdminAcquireContext.**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminacquirecontext)                                                                                                                                                                                                        |
| [**CryptCATAdminRemoveCatalog**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminremovecatalog)                     | Elimina un archivo de catálogo y quita la entrada de ese catálogo de la base de datos Windows catálogo.                                                                                                                                                                                                                                         |
| [**CryptCATAdminResolveCatalogPath**](/windows/desktop/api/Mscat/nf-mscat-cryptcatadminresolvecatalogpath)           | Recupera la ruta de acceso completa del catálogo especificado.                                                                                                                                                                                                                                                                       |
| [**CryptCATCatalogInfoFromContext**](/windows/desktop/api/Mscat/nf-mscat-cryptcatcataloginfofromcontext)             | Recupera información de catálogo de un contexto de catálogo especificado.                                                                                                                                                                                                                                                                    |
| [**CryptCATClose**](/windows/desktop/api/Mscat/nf-mscat-cryptcatclose)                                               | Cierra un identificador de catálogo abierto anteriormente por la [**función CryptCATOpen.**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen)                                                                                                                                                                                                                                    |
| [**CryptCATEnumerateAttr**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumerateattr)                               | Enumera los atributos asociados a un miembro de un catálogo.                                                                                                                                                                                                                                                                   |
| [**CryptCATEnumerateCatAttr**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumeratecatattr)                         | Enumera los atributos asociados a un catálogo.                                                                                                                                                                                                                                                                               |
| [**CryptCATEnumerateMember**](/windows/desktop/api/Mscat/nf-mscat-cryptcatenumeratemember)                           | Enumera los miembros de un catálogo.                                                                                                                                                                                                                                                                                               |
| [**CryptCATGetAttrInfo**](/windows/desktop/api/Mscat/nf-mscat-cryptcatgetattrinfo)                                   | Recupera información sobre un atributo de un miembro de un catálogo.                                                                                                                                                                                                                                                                 |
| [**CryptCATGetMemberInfo**](/windows/desktop/api/Mscat/nf-mscat-cryptcatgetmemberinfo)                               | Recupera información de miembros de PKCS 7 del \# catálogo. Además de recuperar la información de miembro para una etiqueta de referencia especificada, esta función abre un contexto de miembro.                                                                                                                                                    |
| [**CryptCATOpen**](/windows/desktop/api/Mscat/nf-mscat-cryptcatopen)                                                 | Abre un catálogo y devuelve un identificador de contexto al catálogo abierto.                                                                                                                                                                                                                                                                 |
| [**IsCatalogFile**](/windows/desktop/api/Mscat/nf-mscat-iscatalogfile)                                               | Recupera un valor booleano que indica si el archivo especificado es un archivo de catálogo.                                                                                                                                                                                                                                             |



 

## <a name="wintrust-functions"></a>WinTrust Functions

Las siguientes funciones se usan para realizar varias operaciones de confianza.

| Función                                                                               | Descripción                                                                                                                                                          |
|----------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WintrustAddActionID**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustaddactionid)                                     | Agrega una acción del proveedor de confianza al sistema del usuario.                                                                                                                   |
| [**WintrustGetRegPolicyFlags**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustgetregpolicyflags)                         | Recupera las marcas de directiva de un proveedor de directivas.                                                                                                                        |
| [**WintrustAddDefaultForUsage**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustadddefaultforusage)                       | Especifica el identificador de uso predeterminado y la información de devolución de llamada de un proveedor.                                                                                       |
| [**WintrustGetDefaultForUsage**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustgetdefaultforusage)                       | Recupera el identificador de uso predeterminado y la información de devolución de llamada.                                                                                                     |
| [**WintrustLoadFunctionPointers**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustloadfunctionpointers)                   | Carga los puntos de entrada de función para un GUID de acción especificado.                                                                                                             |
| [**WintrustRemoveActionID**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustremoveactionid)                               | Quita una acción agregada por la [**función WintrustAddActionID.**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustaddactionid)                                                                          |
| [**WintrustSetDefaultIncludePEPageHashes**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetdefaultincludepepagehashes) | Establece la configuración predeterminada que determina si se incluyen hashes de página al crear datos indirectos del paquete de interfaz de sujeto (SIP) para archivos ejecutables portátiles. |
| [**WintrustSetRegPolicyFlags**](/windows/desktop/api/Wintrust/nf-wintrust-wintrustsetregpolicyflags)                         | Establece las marcas de directiva para un proveedor de directivas.                                                                                                                             |
| [**WinVerifyTrust**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrust)                                               | Realiza una acción de comprobación de confianza en un objeto especificado.                                                                                                          |
| [**WinVerifyTrustEx**](/windows/desktop/api/Wintrust/nf-wintrust-winverifytrustex)                                           | Realiza una acción de comprobación de confianza en un objeto especificado y toma un puntero a una estructura DE \_ DATOS WINTRUST.                                                        |
| [**WTHelperCertCheckValidSignature**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpercertcheckvalidsignature)             | Comprueba si una firma es válida.                                                                                                                                 |
| [**WTHelperCertFindIssuerCertificate**](wthelpercertfindissuercertificate.md)         | Busca un certificado de emisor de los almacenes de certificados especificados que coincida con el certificado de sujeto especificado.                                                    |
| [**WTHelperCertIsSelfSigned**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpercertisselfsigned)                           | Comprueba si un certificado es autofirmado.                                                                                                                         |
| [**WTHelperGetFileHash**](wthelpergetfilehash.md)                                     | Comprueba la firma de un archivo firmado y obtiene el valor hash y el identificador del algoritmo para el archivo.                                                            |
| [**WTHelperGetProvCertFromChain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovcertfromchain)                   | Recupera un certificado de proveedor de confianza de la cadena de certificados.                                                                                                   |
| [**WTHelperGetProvPrivateDataFromChain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovprivatedatafromchain)     | Recibe una [**estructura \_ \_ PRIVDATA CRYPT PROVIDER**](/windows/desktop/api/Wintrust/ns-wintrust-crypt_provider_privdata) de la cadena mediante el identificador del proveedor.                                           |
| [**WTHelperGetProvSignerFromChain**](/windows/desktop/api/Wintrust/nf-wintrust-wthelpergetprovsignerfromchain)               | Recupera un firmante o contrasignador por índice de la cadena.                                                                                                         |
| [**WTHelperProvDataFromStateData**](/windows/desktop/api/Wintrust/nf-wintrust-wthelperprovdatafromstatedata)                 | Recupera información del proveedor de confianza de un identificador especificado.                                                                                                        |



 

## <a name="object-locator-functions"></a>Funciones de localizador de objetos

Las siguientes funciones de devolución de llamada se pueden implementar mediante un proveedor personalizado que está pensado para que lo llame el paquete de seguridad de Canal seguro (Schannel) para recuperar certificados.



| Función                                                                                                             | Descripción                                             |
|----------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| [**PFN \_ CRYPT \_ OBJECT \_ LOCATOR \_ PROVIDER \_ FLUSH**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_flush)                      | Especifica que un objeto ha cambiado.                   |
| [**PROVEEDOR DE LOCALIZADOR DE OBJETOS \_ PFN CRYPT \_ \_ \_ \_ GET**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_get)                          | Recupera un objeto .                                    |
| [**VERSIÓN DEL PROVEEDOR DE LOCALIZADOR DE OBJETOS \_ PFN CRYPT \_ \_ \_ \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_release)                  | Libera el proveedor.                                  |
| [**CONTRASEÑA GRATUITA \_ DEL PROVEEDOR DE LOCALIZADOR DE \_ \_ OBJETOS \_ \_ \_ PFN CRYPT**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_password)     | Libera la contraseña usada para cifrar una matriz de bytes PFX. |
| [**PROVEEDOR DE LOCALIZADOR DE OBJETOS \_ PFN CRYPT \_ \_ \_ \_ GRATIS**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free)                        | Libera el objeto devuelto por el proveedor.           |
| [**IDENTIFICADOR LIBRE \_ DEL PROVEEDOR DE LOCALIZADOR DE \_ \_ OBJETOS \_ \_ \_ PFN CRYPT**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_free_identifier) | Libera la memoria de un identificador de objeto.               |
| [**INICIALIZACIÓN DEL \_ PROVEEDOR DE LOCALIZADOR DE \_ \_ OBJETOS \_ PFN CRYPT \_**](/windows/desktop/api/Wincrypt/nc-wincrypt-pfn_crypt_object_locator_provider_initialize)            | Inicializa el proveedor.                               |



 

 

 
