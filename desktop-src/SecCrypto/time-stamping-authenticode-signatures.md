---
description: La marca de tiempo de Authenticode se basa en \# Contrafirmas estándar PKCS 9. Las herramientas de firma de Microsoft permiten a los desarrolladores adjuntar marcas de tiempo al mismo tiempo que colocan firmas Authenticode.
ms.assetid: d0bd3e2f-1eee-4f71-9467-974994f720d5
title: Marcas de tiempo de las firmas de Authenticode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3631d402da56d4078cecce65075c92dff0ec7e1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277004"
---
# <a name="time-stamping-authenticode-signatures"></a>Marcas de tiempo de las firmas de Authenticode

Las firmas de Microsoft Authenticode proporcionan garantías de integridad y de creación de datos binarios. La marca de tiempo de Authenticode se basa en \# Contrafirmas estándar PKCS 9. Las herramientas de firma de Microsoft permiten a los desarrolladores adjuntar marcas de tiempo al mismo tiempo que colocan firmas Authenticode. La marca de tiempo permite que se puedan comprobar las firmas de Authenticode incluso después de que los certificados usados para la firma hayan expirado.

## <a name="a-brief-introduction-to-authenticode"></a>Breve introducción a Authenticode

[*Authenticode*](../secgloss/a-gly.md) aplica la tecnología de firma digital para garantizar la creación e integridad de datos binarios, como software instalable. Un explorador Web del cliente u otros componentes del sistema pueden usar las firmas de Authenticode para comprobar la integridad de los datos cuando se descarga o se instala el software. Las firmas de Authenticode se pueden usar con muchos formatos de software, como. cab,. exe,. ocx y. dll.

Microsoft mantiene una lista de [*entidades de certificación*](/security/trusted-root/participants-list) (CA) públicas. Los emisores de certificados Authenticode incluyen actualmente [SSL.com](https://www.ssl.com/), [DigiCert](https://www.digicert.com/), [Sectigo (comodo)](https://www.sectigo.com/)y [GlobalSign](https://www.globalsign.com/).

## <a name="about-cryptographic-time-stamping"></a>Acerca de la marca de tiempo criptográfica

En el pasado, se propone una variedad de métodos de marca de tiempo criptográficos. Consulte, por ejemplo, ha y Stornetta "cómo Time-Stamp un documento digital" en el *diario de Cryptology* (1991) y Benaloh y de Mare "acumuladores unidireccionales: una alternativa descentralizada a las firmas digitales" en las *notas de la Conferencia Springer-Verlag en Computer Science* Vol. 765 (EUROCRYPT ' 93). Un resumen extendido de este artículo está disponible en [Microsoft Research](https://research.microsoft.com/research/pubs/view.aspx?id=233&type=Publication&0sr=a). (Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones). Dado que la hora es una cantidad física, en lugar de una cantidad matemática, estos métodos suelen preocuparse de cómo vincular objetos para que se pueda determinar su orden de creación o cómo agrupar eficazmente los objetos que se pueden describir tal como se han creado simultáneamente.

Los sistemas que pretenden autenticar el tiempo como una cantidad siempre requieren algún tipo de confianza. En una configuración fuertemente adversarial, se pueden usar protocolos complejos para garantizar cierto grado de sincronía. Sin embargo, estos protocolos requieren una interacción extensa entre las partes afectadas. En la práctica, si solo necesita la certificación del tiempo de una fuente de confianza, el origen puede actuar simplemente como notario si proporciona una instrucción firmada (certificación) en la que se presentó el objeto para la firma en el momento indicado.

El método de contrafirma de la marca de tiempo que se implementa a continuación permite comprobar las firmas incluso después de que el certificado de firma haya expirado o se haya revocado. La marca de tiempo permite que el comprobador sepa de forma confiable el tiempo que se ha colocado la firma y, por tanto, confía en la firma si era válida en ese momento. La hora autor debe tener un origen de hora confiable y protegido.

## <a name="pkcs-7-signed-documents-and-countersignatures"></a>\#Documentos firmados PKCS 7 y Contrafirmas

PKCS \# 7 es un formato estándar para los datos criptográficos, incluidos los datos firmados, los certificados y [*las listas de revocación de certificados*](../secgloss/c-gly.md) (CRL). El tipo PKCS \# 7 determinado de interés en el contexto de la marca de tiempo es los datos firmados, correspondientes al \# tipo de contenido [**SignedData**](signeddata.md) definido PKCS 7.

El \# paquete PKCS 7 se compone de [**SignedData**](signeddata.md) que identifica el contenido real y determinada información sobre los bloques de firma y SignerInfo. Un SignerInfo puede contener una contrafirma, que de forma recursiva es otro SignerInfo. En principio, una secuencia de esas contrafirmaciones puede estar presente. La contrafirma es un atributo no autenticado con respecto a la firma en el SignerInfo; es decir, se puede colocar después de la firma original. En el formulario de esquema:

[**SignedData**](signeddata.md) (PKCS \# 7)

-   Versión (de PKCS \# 7, versión en general 1)
-   DigestAlgorithms (colección de todos los algoritmos usados por los bloques de firma de SignerInfo para el procesamiento optimizado)
-   ContentInfo (contentType es igual a [**SignedData**](signeddata.md), más contenido o referencia al contenido)
-   Certificados opcionales (colección de todos los certificados utilizados)
-   CRL opcionales (colección de todas las CRL)
-   SignerInfo bloques de firma (la firma real, formada por uno o varios bloques de firma SignerInfo)

SignerInfo (bloque de firma)

-   Versión (de PKCS \# 7, versión en general 1)
-   Certificado (emisor y número de serie para identificar de forma única el certificado del firmante en [**SignedData**](signeddata.md))
-   DigestAlgorithm más el DigestEncryptionAlgorithm más el resumen (hash), además de EncryptedDigest (firma real)
-   AuthenticatedAttributes opcional (por ejemplo, firmado por este firmante)
-   UnauthenticatedAttributes opcional (por ejemplo, no firmado por este firmante)

Un ejemplo de atributo autenticado es la hora de firma (OID 1.2.840.113549.1.9.5) porque forma parte de lo que el servicio de marca de tiempo firma. Un ejemplo de atributo no autenticado es la contrafirma (OID 1.2.840.113549.1.9.6) porque se puede colocar después de la firma. En este caso, el propio SignerInfo contiene un SignerInfo (la contrafirma).

> [!Note]  
> El objeto que está firmado en la contrafirma es la firma original (es decir, el EncryptedDigest de SignerInfo original).

 

## <a name="signtool-and-the-authenticode-process"></a>SignTool y el proceso de Authenticode

[SignTool](signtool.md) está disponible para la firma y la marca de tiempo de los datos binarios. La herramienta se instala en la \\ carpeta bin de la ruta de instalación del kit de desarrollo de software (SDK) de Microsoft Windows.

La firma y la marca de tiempo de los datos binarios son relativamente sencillas mediante [SignTool](signtool.md). El publicador debe obtener un certificado de firma de código de una entidad de certificación de firma de código comercial. Para mayor comodidad, Microsoft publica y actualiza una lista de entidades de certificación públicas, incluidas las que emiten certificados Authenticode. Cuando está listo para publicar, los archivos objeto se firman y se marcan por hora con los parámetros de línea de comandos adecuados con la herramienta SignTool. El resultado de cualquier operación de SignTool siempre es un \# formato PKCS 7 [**SignedData**](signeddata.md).

SignTool acepta como entrada datos binarios sin formato que se van a firmar con una marca de tiempo o datos binarios firmados previamente para la marca de tiempo. Los datos que se han firmado anteriormente se pueden marcar con el comando de la marca de tiempo de **SignTool** .



| Argumento             | Descripción                                                                                                                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/T** *HTTPAddress* | Indica que el archivo debe marcarse con el tiempo. Se debe proporcionar una dirección URL que especifique una dirección de un servidor de marca de tiempo. **/t** se puede usar con los comandos de **firma de SignTool** y de marca de tiempo de **SignTool** . |



 

Para obtener más información sobre las herramientas que pueden ser útiles en este contexto, vea [herramientas de criptografía](cryptography-tools.md) y [SignTool](signtool.md).

## <a name="implementation-details-and-wire-format"></a>Detalles de implementación y formato de conexión

[SignTool](signtool.md) se basa en la implementación de Authenticode de Windows para crear y obtener firmas de marca de tiempo. [*Authenticode*](../secgloss/a-gly.md) funciona en archivos binarios, por ejemplo,. cab,. exe,. dll o. ocx. Authenticode crea primero la firma, lo que genera un archivo PKCS \# 7 [**SignedData**](signeddata.md). Este **SignedData** se debe contrafirmar, tal y como se describe en PKCS \# 9.

El proceso de contrafirma se realiza en cuatro pasos:

1.  Copie la firma (es decir, encryptedDigest) del SignerInfo de PKCS \# 7 [**SignedData**](signeddata.md).
2.  Construya una solicitud de marca de tiempo cuyo contenido sea la firma original. Envíelo al servidor de marca de tiempo de la [*notación de sintaxis abstracta uno*](../secgloss/a-gly.md) (ASN. 1) codificado como TimeStampRequest.
3.  Recibir una marca de tiempo, con el formato de un segundo \# [**SignedData**](signeddata.md)PKCS 7, que se devuelve desde el servidor de marca de tiempo.
4.  Copie el SignerInfo de la marca de tiempo directamente en el \# [**SignedData**](signeddata.md)PKCS 7 original, como una \# contrafirma PKCS 9 (es decir, un atributo no autenticado en el SignerInfo del original).

## <a name="time-stamp-request"></a>Solicitud de marca de tiempo

La solicitud de marca de tiempo se envía dentro de un mensaje HTTP 1,1 POST. En el encabezado HTTP, la Directiva CacheControl está establecida en no-cache y la Directiva Content-Type se establece en application/octet-stream. El cuerpo del mensaje HTTP es una codificación Base64 de la codificación de [*reglas de codificación distinguida*](../secgloss/d-gly.md) (der) de la solicitud de marca de tiempo.

Aunque no se usa actualmente, la Directiva de longitud de contenido también debe usarse para construir el mensaje HTTP, ya que ayuda al servidor de marca de tiempo a ubicar el lugar en el que se encuentra la solicitud en HTTP POST.

También pueden estar presentes otros encabezados HTTP y deben omitirse si no los entiende el solicitante o el servidor de marca de tiempo.

La solicitud de marca de tiempo es un mensaje codificado ASN. 1. El formato de la solicitud es el siguiente.

``` syntax
TimeStampRequest ::= SEQUENCE {
   countersignatureType OBJECT IDENTIFIER,
   attributes Attributes OPTIONAL, 
   content  ContentInfo
}
```

CountersignatureType es el [*identificador de objeto*](../secgloss/o-gly.md) (OID) que lo identifica como una contrafirma de marca de tiempo y debe ser el OID exacto 1.3.6.1.4.1.311.3.2.1.

No hay ningún atributo incluido actualmente en la solicitud de marca de tiempo.

El contenido es un ContentInfo, tal y como se define en PKCS \# 7. El contenido son los datos que se van a firmar. En cuanto a la marca de tiempo de la firma, el ContentType debe ser datos y el contenido debe ser el encryptedDigest (firma) del SignerInfo del \# contenido PKCS 7 para que sea una marca de tiempo.

## <a name="time-stamp-response"></a>Respuesta de marca de tiempo

La respuesta de marca de tiempo también se envía dentro de un mensaje HTTP 1,1. En el encabezado HTTP, la Directiva Content-Type también se establece en application/octet-stream. El cuerpo del mensaje HTTP es una codificación Base64 de la codificación DER de la respuesta de la marca de tiempo.

La respuesta de marca de tiempo es un \# mensaje firmado PKCS 7 firmado por la hora autor. El ContentInfo del mensaje PKCS \# 7 es idéntico al ContentInfo recibido en la marca de tiempo. El \# contenido PKCS 7 contiene el atributo de hora de firma autenticado (definido en PKCS \# 99, OID 1.2.840.113549.9.5).

Después de que Authenticode reciba la marca de tiempo del servidor, Authenticode incorporará la marca de tiempo \# al [**SignedData**](signeddata.md) PKCS 7 original como una contrafirma. Para ello, \# se descartan los ContentInfo de los **SignedData** PKCS 7 devueltos y el SignerInfo de la marca de tiempo devuelta se copia como una contrafirma en el SignerInfo del archivo PKCS \# 7 **SignedData** original. La cadena de certificados de la hora autor también se copia en los certificados de la \# **SignedData** PKCS 7 original como atributo no autenticado del firmante original.

Para obtener más información sobre PKCS y otros asuntos de seguridad, consulte la [biblioteca de contenido del sitio web de RSA](https://www.rsa.com/content_library.aspx).

 

 
