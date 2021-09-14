---
description: Se usa con operaciones de codificación y descodificación.
ms.assetid: 713c95ae-e5d0-416c-ba0c-4b5399aa8a33
title: Constantes para extensiones de Netscape
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06999a879d0d289bb95cdb8ba5506200154d60e4
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127259591"
---
# <a name="constants-for-netscape-extensions"></a>Constantes para extensiones de Netscape

Las siguientes extensiones de Netscape se usan con operaciones de codificación y descodificación. Las constantes predefinidas de Netscape y las cadenas de identificador de objeto no se usan directamente con las funciones de codificación o descodificación, [**CryptEncodeObject,**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobject) [**CryptEncodeObjectEx,**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptencodeobjectex) [**CryptSignAndEncodeCertificate,**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptsignandencodecertificate) [**CryptDecodeObject**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobject)o [**CryptDecodeObjectEx.**](/windows/win32/api/Wincrypt/nf-wincrypt-cryptdecodeobjectex) En su lugar, estas extensiones requieren el uso de *lpszStructType mostrado.*

Para obtener detalles adicionales que se aplican a algunas extensiones de Netscape, vea los comentarios siguientes a la tabla.



| Identificadores de objeto de extensión de certificado de Netscape                      | *lpszStructType*                                           | *PvStructInfo correspondiente*                                                                                                                                                                                                                                                                                                                                                                                                                         |
|------------------------------------------------------------------------|------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| dirección URL BASE de szOID \_ \_ \_ NETSCAPE"2.16.840.1.113730.1.2"<br/>           | X509 \_ ANY STRING o \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ VALOR \_ DE NOMBRE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). El **miembro dwValueType** se establece en CERT \_ RDN \_ IA5 \_ STRING. El **miembro pbData** del miembro Value apunta a una cadena IA5 agregada al principio de todas las direcciones URL  \_ relativas de un certificado. Esta extensión se puede considerar una optimización para reducir el tamaño de las extensiones de dirección URL.                                                                                                       |
| szOID \_ NETSCAPE \_ CA POLICY \_ \_ URL"2.16.840.1.113730.1.8"<br/>     | X509 \_ ANY STRING o \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ VALOR \_ DE NOMBRE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). El **miembro dwValueType** se establece en CERT \_ RDN \_ IA5 \_ STRING. El **miembro pbData** del miembro Value apunta a una cadena IA5, la dirección URL relativa o absoluta de la página web que describe las directivas bajo las que se emitió el  \_ certificado.                                                                                                                                                            |
| szOID \_ NETSCAPE \_ CA \_ REVOCATION \_ URL"2.16.840.1.113730.1.4"<br/> | X509 \_ ANY STRING o \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ VALOR \_ DE NOMBRE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). El **miembro dwValueType** se establece en CERT \_ RDN \_ IA5 \_ STRING. El miembro **pbData** del miembro Value apunta a una cadena IA5 que es la dirección URL relativa o absoluta usada para comprobar el estado de revocación de los certificados firmados por la entidad de certificación a la que pertenece el certificado  \_ actual. [](../secgloss/c-gly.md) |
| szOID \_ NETSCAPE \_ CERT RENEWAL \_ \_ URL"2.16.840.1.113730.1.7"<br/>  | X509 \_ ANY STRING o \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ VALOR \_ DE NOMBRE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). El **miembro dwValueType** se establece en CERT \_ RDN \_ IA5 \_ STRING. El **miembro pbData** del miembro Value apunta a una cadena IA5 que es la dirección URL relativa o absoluta de un formulario de renovación de  \_ certificado.                                                                                                                                                                                                     |
| szOID \_ NETSCAPE \_ CERT \_ SEQUENCE"2.16.840.1.113730.2.5"<br/>      | SECUENCIA DE INFORMACIÓN \_ \_ DE CONTENIDO PKCS DE \_ \_ \_ CUALQUIERA                     | [**SECUENCIA DE INFORMACIÓN \_ DE CONTENIDO DE CIFRADO DE \_ \_ \_ \_ CUALQUIERA**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)                                                                                                                                                                                                                                                                                                                                                                |
| szOID \_ NETSCAPE \_ CERT \_ TYPE"2.16.840.1.113730.1.1"<br/>          | X509 \_ BITS                                                 | [**CRYPT \_ BIT \_ BLOB**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_bit_blob)                                                                                                                                                                                                                                                                                                                                                                                                           |
| szOID \_ NETSCAPE \_ COMMENT"2.16.840.1.113730.1.13"<br/>            | X509 \_ ANY STRING o \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ VALOR \_ DE NOMBRE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). El **miembro dwValueType** se establece en CERT \_ RDN \_ IA5 \_ STRING. El **miembro pbData** del miembro Value apunta a una cadena IA5 que es un comentario que se va a mostrar cuando se vea el  \_ certificado.                                                                                                                                                                                                         |
| szOID \_ NETSCAPE \_ REVOCATION \_ URL"2.16.840.1.113730.1.3"<br/>     | X509 \_ ANY STRING o \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ VALOR \_ DE NOMBRE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). El **miembro dwValueType** se establece en CERT \_ RDN \_ IA5 \_ STRING. El **miembro pbData** del miembro Value apunta a una cadena IA5 que es una dirección URL relativa o absoluta que se usa para comprobar el estado de  \_ revocación del certificado.                                                                                                                                                                              |
| szOID \_ NETSCAPE \_ SSL SERVER \_ \_ NAME"2.16.840.1.113730.1.12"<br/>  | X509 \_ ANY STRING o \_ X509 \_ UNICODE ANY \_ \_ STRING<br/> | [**CERT \_ VALOR \_ DE NOMBRE**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value). El **miembro dwValueType** se establece en CERT \_ RDN \_ IA5 \_ STRING. El **miembro pbData** del miembro Value apunta a una cadena IA5 que es una expresión de shell que se usa para coincidir con el nombre de host del servidor SSL mediante este  \_ certificado.                                                                                                                                                                       |



 

Para todas las funciones de codificación que usan X509 ANY STRING o \_ \_ X5O9 \_ UNICODE ANY STRING \_ \_ **lpszStructType,** se usa X509 ANY STRING si el formato de cadena del miembro pbData del miembro Value es ASCII y \_ \_ X509 UNICODE ANY STRING   [](../secgloss/a-gly.md) \_ \_ \_ si el formato de cadena es UNICODE. En el caso de Unicode, la cadena debe convertirse en una cadena IA5 antes de codificar estableciendo el miembro dwValueType de la estructura CERT NAME VALUE en \_ CERT  [**\_ \_**](/windows/win32/api/Wincrypt/ns-wincrypt-cert_name_value) \_ RDN \_ IA5 \_ STRING.

Para las funciones de decodificación, el usuario selecciona el formato de la cadena de salida. Use X509 ANY STRING si el formato de cadena deseado es \_ \_ ASCII y X509 UNICODE ANY STRING si el formato de cadena \_ deseado es \_ \_ Unicode.

Para la extensión szOID NETSCAPE CERT RENEWAL URL, la estructura de datos contiene una dirección URL relativa o absoluta que apunta a un \_ formulario de renovación de \_ \_ \_ certificados. Se accederá al formulario de renovación con un método HTTP GET mediante una dirección URL que es la concatenación de renewal-URL y certificate-serial-number. El número de serie del certificado se codifica como una cadena de dígitos hexadecimales ASCII. Por ejemplo, si netscape-base-url es https:// una dirección *URL* de entidad de certificación /, netscape-cert-renewal-url es cgi-bin/check-renew.cgi? y el número de serie del certificado es 173420, la dirección URL resultante sería: https://*certification authority URL*/cgi-bin/check-renew.cgi?02a56c. El documento devuelto debe ser un formulario HTML que permita al usuario solicitar una renovación de su certificado.

Para la extensión SZOID NETSCAPE CERT SEQUENCE mediante \_ \_ \_ ASN ENCODING X509, el certificado se codifica como una estructura \_ \_ PKCS CONTENT \_ INFO que encapsula una \_ secuencia de ANY. El valor del **miembro contentType** es **pszObjId**, mientras que el campo de contenido es la estructura siguiente:

SequenceOfAny ::= SEQUENCE OF ANY

Los [**\_ \_ blobs CRYPT DER**](/previous-versions/windows/desktop/legacy/aa381414(v=vs.85))de la secuencia de información de contenido de [**CRYPT \_ de \_ \_ \_ \_ cualquier**](/windows/win32/api/Wincrypt/ns-wincrypt-crypt_content_info_sequence_of_any)miembro **rgValue** apuntan a certificados X509 codificados.

Para las extensiones \_ szOID NETSCAPE \_ CERT \_ TYPE, se definen los bits siguientes.



| Valor de bit | Tipo correspondiente                      |
|-----------|-----------------------------------------|
| 0x80      | TIPO DE \_ CERTIFICADO DE \_ \_ AUTENTICACIÓN DE CLIENTE \_ SSL DE NETSCAPE \_ |
| 0x40      | NETSCAPE \_ SSL \_ SERVER \_ AUTH \_ CERT \_ TYPE |
| 0x04      | NETSCAPE \_ SSL \_ CA \_ CERT \_ TYPE           |



 

Para las extensiones szOID NETSCAPE REVOCATION URL, se puede usar una dirección URL relativa o absoluta para comprobar el estado \_ \_ de \_ revocación de un certificado. La comprobación de revocación se realizará como un método HTTP GET mediante una dirección URL que es la concatenación de revocation-URL y certificate-serial-number. El número de serie del certificado se codifica como una cadena de dígitos hexadecimales ASCII. Por ejemplo, si netscape-base-url es https: \/ /www.certs-r-us.com/, netscape-revocation-url es cgi-bin/check-rev.cgi? y el número de serie del certificado es 173420, la dirección URL resultante sería: https: \/ /www.certs-r-us.com/cgi-bin/check-rev.cgi?02a56c.

El servidor debe devolver un documento con un content-type de application/x-netscape-revocation. El documento debe contener un único dígito ASCII, "1" si el certificado no es válido actualmente y "0" si es válido actualmente.

Tenga en cuenta que para todas las direcciones URL que incluyen el número de serie del certificado, el número de serie se codificará como una cadena que consta de un número par de dígitos hexadecimales. Si el número de dígitos significativos es impar, la cadena tendrá un único cero inicial para asegurarse de que se genera un número par de dígitos.

 

 
