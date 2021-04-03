---
description: Se usa con las operaciones de codificación y descodificación.
ms.assetid: 713c95ae-e5d0-416c-ba0c-4b5399aa8a33
title: Constantes para extensiones de Netscape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06999a879d0d289bb95cdb8ba5506200154d60e4
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/10/2021
ms.locfileid: "103914693"
---
# <a name="constants-for-netscape-extensions"></a>Constantes para extensiones de Netscape

Las siguientes extensiones de Netscape se utilizan con las operaciones de codificación y descodificación. Las cadenas predefinidas de Netscape y las cadenas de identificador de objeto no se usan directamente con las funciones de codificación o descodificación, [**CryptEncodeObject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobject), [**CryptEncodeObjectEx**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobjectex), [**CryptSignAndEncodeCertificate**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate), [**CryptDecodeObject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobject)o [**CryptDecodeObjectEx**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex). En su lugar, estas extensiones requieren el uso de *lpszStructType* mostrado.

Para obtener detalles adicionales que se aplican a algunas extensiones de Netscape, vea los comentarios que aparecen después de la tabla.



| Identificadores de objeto de extensión de certificado de Netscape                      | *lpszStructType*                                           | *PvStructInfo* correspondiente                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| szOID \_ \_ dirección URL base de Netscape \_ "2.16.840.1.113730.1.2"<br/>           | X509 \_ cualquier cadena \_ o X509 \_ Unicode en \_ una \_ cadena<br/> | [**Certificado \_ de \_valor de nombre**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). El miembro **dwValueType** se establece en el certificado \_ RDN \_ IA5 \_ cadena. El miembro **pbData** del miembro del **valor** apunta a una \_ cadena IA5 agregada al principio de todas las direcciones URL relativas de un certificado. Esta extensión se puede considerar una optimización para reducir el tamaño de las extensiones de dirección URL.                                                                                                       |
| szOID \_ dirección URL de la Directiva de CA de Netscape \_ \_ \_ "2.16.840.1.113730.1.8"<br/>     | X509 \_ cualquier cadena \_ o X509 \_ Unicode en \_ una \_ cadena<br/> | [**Certificado \_ de \_valor de nombre**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). El miembro **dwValueType** se establece en el certificado \_ RDN \_ IA5 \_ cadena. El miembro **pbData** del miembro del **valor** apunta a una \_ cadena IA5, la dirección URL relativa o absoluta de la página web que describe las directivas en las que se emitió el certificado.                                                                                                                                                            |
| szOID \_ \_ dirección URL de revocación de la CA de Netscape \_ \_ "2.16.840.1.113730.1.4"<br/> | X509 \_ cualquier cadena \_ o X509 \_ Unicode en \_ una \_ cadena<br/> | [**Certificado \_ de \_valor de nombre**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). El miembro **dwValueType** se establece en el certificado \_ RDN \_ IA5 \_ cadena. El miembro **pbData** del miembro del **valor** apunta a una \_ cadena IA5 que es la dirección URL relativa o absoluta usada para comprobar el estado de revocación de los certificados firmados por la [*entidad de certificación*](../secgloss/c-gly.md) a la que pertenece el certificado actual. |
| szOID \_ \_ dirección URL de renovación de certificados de Netscape \_ \_ "2.16.840.1.113730.1.7"<br/>  | X509 \_ cualquier cadena \_ o X509 \_ Unicode en \_ una \_ cadena<br/> | [**Certificado \_ de \_valor de nombre**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). El miembro **dwValueType** se establece en el certificado \_ RDN \_ IA5 \_ cadena. El miembro **pbData** del miembro del **valor** apunta a una \_ cadena IA5 que es la dirección URL relativa o absoluta de un formulario de renovación de certificado.                                                                                                                                                                                                     |
| szOID \_ secuencia de certificado de Netscape \_ \_ "2.16.840.1.113730.2.5"<br/>      | \_ \_ \_ secuencia de información de contenido PKCS \_ de \_ cualquier                     | [**\_ \_ secuencia de información de contenido cifrado \_ \_ de \_ cualquier**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)                                                                                                                                                                                                                                                                                                                                                                |
| szOID \_ tipo de certificado de Netscape \_ \_ "2.16.840.1.113730.1.1"<br/>          | \_Bits X509                                                 | [**\_BLOB de bit de cifrado \_**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_bit_blob)                                                                                                                                                                                                                                                                                                                                                                                                           |
| Comentario szOID de \_ Netscape \_ "2.16.840.1.113730.1.13"<br/>            | X509 \_ cualquier cadena \_ o X509 \_ Unicode en \_ una \_ cadena<br/> | [**Certificado \_ de \_valor de nombre**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). El miembro **dwValueType** se establece en el certificado \_ RDN \_ IA5 \_ cadena. El miembro **pbData** del miembro del **valor** apunta a una \_ cadena IA5 que es un comentario que se va a mostrar cuando se vea el certificado.                                                                                                                                                                                                         |
| szOID \_ \_ dirección URL de revocación de Netscape \_ "2.16.840.1.113730.1.3"<br/>     | X509 \_ cualquier cadena \_ o X509 \_ Unicode en \_ una \_ cadena<br/> | [**Certificado \_ de \_valor de nombre**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). El miembro **dwValueType** se establece en el certificado \_ RDN \_ IA5 \_ cadena. El miembro **pbData** del miembro del **valor** apunta a una \_ cadena IA5 que es una dirección URL relativa o absoluta que se usa para comprobar el estado de revocación del certificado.                                                                                                                                                                              |
| szOID \_ Netscape \_ SSL \_ nombre del servidor \_ "2.16.840.1.113730.1.12"<br/>  | X509 \_ cualquier cadena \_ o X509 \_ Unicode en \_ una \_ cadena<br/> | [**Certificado \_ de \_valor de nombre**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). El miembro **dwValueType** se establece en el certificado \_ RDN \_ IA5 \_ cadena. El miembro **pbData** del miembro del **valor** apunta a una \_ cadena IA5 que es una expresión de Shell que se usa para hacer coincidir el nombre de host del servidor SSL con este certificado.                                                                                                                                                                       |



 

En todas las funciones de codificación que usan la cadena X509 \_ any \_ o la X5O9 \_ Unicode \_ cualquier \_ cadena **lpszStructType**, \_ se utiliza X509 cualquier \_ cadena si el formato de cadena del miembro **pbData** del miembro del **valor** es [*ASCII*](../secgloss/a-gly.md), y se usa la cadena X509 \_ Unicode \_ \_ si el formato de la cadena es Unicode. En el caso de Unicode, la cadena se debe convertir en una \_ cadena IA5 antes de la codificación estableciendo el miembro **dwValueType** de la estructura del [**\_ \_ valor CERT Name**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value) en la \_ cadena CERT \_ IA5 IA5 \_ .

En el caso de las funciones de descodificación, el usuario selecciona el formato de la cadena de salida. Use X509 \_ cualquier \_ cadena si el formato de cadena deseado es ASCII, y X509 \_ Unicode \_ cualquier \_ cadena si el formato de cadena deseado es Unicode.

En el caso de la \_ extensión szOID Netscape \_ CERT \_ Renovation \_ URL, la estructura de datos contiene una dirección URL relativa o absoluta que señala a un formulario de renovación de certificados. Se tendrá acceso al formulario de renovación con un método HTTP GET mediante una dirección URL que es la concatenación de la dirección URL de renovación y el número de serie de certificado. El certificado-número de serie se codifica como una cadena de dígitos hexadecimales ASCII. Por ejemplo, si la dirección URL de la *entidad de certificación* de Netscape-base es https:///, la dirección URL de Netscape-CERT-Renovation-URL es cgi-bin/check-Renew. cgi?, y el número de serie del certificado es 173420, la dirección URL resultante sería: https://URL de la *entidad de certificación*/cgi-bin/check-Renew.cgi? 02a56c. El documento devuelto debe ser un formulario HTML que permitirá al usuario solicitar una renovación de su certificado.

En el caso de la extensión de secuencia de certificados szOID de \_ Netscape \_ mediante la \_ \_ codificación X509 ASN \_ , el certificado se codifica como una \_ \_ estructura de información de contenido PKCS que ajusta una secuencia de cualquiera. El valor del miembro **ContentType** es **pszObjId**, mientras que el campo de contenido es la estructura siguiente:

SequenceOfAny:: = secuencia de cualquier

Los [**\_ \_ blobs de cifrado der**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85))de la [**\_ \_ secuencia de información de contenido cifrado \_ \_ de cualquier punto de \_**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)miembro de **rgValue** de cualquier punto para codificar los certificados X509.

En el caso de \_ las extensiones de tipo de certificado de szOID Netscape \_ \_ , se definen los bits siguientes.



| Valor de bit | Tipo correspondiente                      |
|-----------|-----------------------------------------|
| 0x80      | \_tipo de \_ \_ certificado de autenticación de cliente SSL \_ de \_ Netscape |
| 0x40      | \_tipo de \_ \_ certificado de autenticación del servidor SSL \_ de \_ Netscape |
| 0x04      | \_tipo de \_ certificado de CA SSL \_ de Netscape \_           |



 

En el caso de las extensiones de la \_ \_ dirección URL de revocación de Netscape de szOID \_ , se puede usar una dirección URL relativa o absoluta para comprobar el estado de revocación de un certificado. La comprobación de revocación se realizará como un método HTTP GET mediante una dirección URL que es la concatenación de la dirección URL de revocación y el número de serie de certificado. El certificado-número de serie se codifica como una cadena de dígitos hexadecimales ASCII. Por ejemplo, si Netscape-base-URL es https: \/ /www.certs-r-us.com/, Netscape-revocación-URL es cgi-bin/check-Rev. cgi? y el número de serie del certificado es 173420, la dirección URL resultante sería: https: \/ /www.certs-r-us.com/cgi-bin/check-Rev.cgi?02a56c.

El servidor debe devolver un documento con un tipo de contenido de aplicación/x-Netscape-revocación. El documento debe contener un solo dígito ASCII, "1" si el certificado no es válido actualmente, y "0" si es válido actualmente.

Tenga en cuenta que para todas las direcciones URL que incluyen el número de serie del certificado, el número de serie se codificará como una cadena que consta de un número par de dígitos hexadecimales. Si el número de dígitos significativos es impar, la cadena tendrá un solo cero inicial para asegurarse de que se genera un número par de dígitos.

 

 
