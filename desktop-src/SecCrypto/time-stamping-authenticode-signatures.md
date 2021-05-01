---
description: La marca de tiempo Authenticode se basa en contrasignaturas PKCS \# 7 estándar. Las herramientas de firma de Microsoft permiten a los desarrolladores fijar marcas de tiempo al mismo tiempo que fijan firmas Authenticode.
ms.assetid: d0bd3e2f-1eee-4f71-9467-974994f720d5
title: Firmas de authenticode de marca de tiempo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0232853441d2c11d331c175ac7e8dfd120b341ff
ms.sourcegitcommit: dc2f43e0f23f4a4ce239118cf9a5180f3ff0dd1d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/30/2021
ms.locfileid: "108327190"
---
# <a name="time-stamping-authenticode-signatures"></a>Firmas de authenticode de marca de tiempo

Las firmas de Microsoft Authenticode proporcionan garantías de creación e integridad para los datos binarios. La marca de tiempo Authenticode se basa en contrasignaturas PKCS \# 7 estándar. Las herramientas de firma de Microsoft permiten a los desarrolladores fijar marcas de tiempo al mismo tiempo que fijan firmas Authenticode. La marca de tiempo permite que las firmas Authenticode se puedan verificar incluso después de que los certificados usados para la firma han expirado.

## <a name="a-brief-introduction-to-authenticode"></a>Breve introducción a Authenticode

[*Authenticode aplica*](../secgloss/a-gly.md) la tecnología de firma digital para garantizar la creación y la integridad de los datos binarios, como el software instalable. Un explorador web cliente u otros componentes del sistema pueden usar las firmas Authenticode para comprobar la integridad de los datos cuando se descarga o instala el software. Las firmas authenticode se pueden usar con muchos formatos de software, incluidos .cab, .exe, .ocx y .dll.

Microsoft mantiene una lista de entidades de [*certificación (CA)*](/security/trusted-root/participants-list) públicas. Actualmente, los emisores de certificados Authenticode [incluyen SSL.com](https://www.ssl.com/), [Digicert,](https://www.digicert.com/) [Sectigo(Comodo)](https://www.sectigo.com/)y [GlobalSign](https://www.globalsign.com/).

## <a name="about-cryptographic-time-stamping"></a>Acerca de la marca de tiempo criptográfica

En el pasado, se han propuesto diversos métodos de marca de tiempo criptográficos. Vea, por ejemplo, Haber y Storncentral "How to Time-Stamp a Digital Document" (Cómo Time-Stamp un documento digital) en *Journal of Cryptology* (1991) y Benalgrama y DeGrama "One-Way Accumulators: ACentraled Alternative to Digital Signatures" (Acumuladores unicidad: una alternativa descentralizada a las firmas digitales) en *Springer-Ver malware Lecture Notes in Computer Science* vol. 765 (EUROCRYPT '93). Hay disponible un resumen extendido de este artículo en [Microsoft Research.](https://research.microsoft.com/research/pubs/view.aspx?id=233&type=Publication&0sr=a) (Es posible que estos recursos no estén disponibles en algunos idiomas y países o regiones). Dado que el tiempo es una cantidad física, en lugar de matemática, estos métodos generalmente se refieren a cómo vincular objetos para que se pueda determinar su orden de creación o cómo agrupar eficazmente objetos que se pueden describir como creados simultáneamente.

Los sistemas que pretenden autenticar el tiempo como una cantidad siempre requieren algún tipo de confianza. En una configuración fuertemente adversaria, se pueden usar protocolos complejos para garantizar cierto grado de sincronía. Sin embargo, estos protocolos requieren una interacción extensa entre las partes afectadas. En la práctica, si solo se necesita la certificación de tiempo de un origen de confianza, el origen puede actuar simplemente como notario proporcionando una instrucción firmada (certificación) que indica que el objeto se presentó para la firma en el momento indicado.

El método de contrafirma de marca de tiempo implementado a continuación permite comprobar las firmas incluso después de que el certificado de firma haya expirado o se haya revocado. La marca de tiempo permite al comprobador saber de forma confiable la hora a la que se afijo la firma y, por tanto, confiar en la firma si era válida en ese momento. El stamper de hora debe tener un origen de hora confiable y protegido.

## <a name="pkcs-7-signed-documents-and-countersignatures"></a>Documentos y contrafirmas firmados de PKCS \# 7

PKCS 7 es un formato estándar para los datos criptográficos, incluidos los datos firmados, los certificados y las listas de \# [*revocación*](../secgloss/c-gly.md) de certificados (CRL). El tipo de interés PKCS 7 concreto en el contexto de la marca de tiempo son los datos firmados, correspondientes al tipo de contenido SignedData definido por \# PKCS \# 7. [](signeddata.md)

El paquete PKCS 7 consta de SignedData que identifica el contenido real y cierta información sobre él y los bloques de \# firma SignerInfo. [](signeddata.md) Un signerInfo puede contener una contrasignación, que de forma recursiva es otro SignerInfo. En principio, puede haber una secuencia de estas contrasignatures. La contrasignature es un atributo no autenticado con respecto a la firma en SignerInfo; es decir, se puede fijar posteriormente a la firma original. En forma de esquema:

[**SignedData**](signeddata.md) (PKCS \# 7)

-   Versión (de PKCS \# 7, por lo general, versión 1)
-   DigestAlgorithms (colección de todos los algoritmos usados por los bloques de firma SignerInfo, para un procesamiento optimizado)
-   ContentInfo (contentType es igual [**a SignedData,**](signeddata.md)más contenido o referencia al contenido)
-   Certificados OPCIONALes (colección de todos los certificados usados)
-   CRL OPCIONALes (colección de todas las CRL)
-   Bloques de firma signerInfo (la firma real, compuesta de uno o varios bloques de firma SignerInfo)

SignerInfo (el bloque de firma)

-   Versión (de PKCS \# 7, por lo general, versión 1)
-   Certificado (emisor y número de serie para identificar de forma única el certificado del firmante en [**SignedData**](signeddata.md))
-   DigestAlgorithm más DigestEncryptionAlgorithm más digest (hash), más EncryptedDigest (firma real)
-   OPCIONAL AuthenticatedAttributes (por ejemplo, firmado por este firmante)
-   OPCIONAL UnauthenticatedAttributes (por ejemplo, no firmado por este firmante)

Un ejemplo de un atributo autenticado es la hora de firma (OID 1.2.840.113549.1.9.5) porque forma parte de lo que firma el servicio de marca de tiempo. Un ejemplo de atributo no autenticado es la contrasignature (OID 1.2.840.113549.1.9.6) porque se puede fijar después de firmar. En este caso, el propio SignerInfo contiene signerInfo (la contrasignature).

> [!Note]  
> El objeto que está firmado en la contrafirma es la firma original (es decir, encryptedDigest del signerInfo original).

 

## <a name="signtool-and-the-authenticode-process"></a>SignTool y el proceso authenticode

[SignTool](signtool.md) está disponible para la firma Authenticode y los datos binarios de marca de tiempo. La herramienta se instala en la carpeta Bin de la ruta de \\ instalación de Microsoft Kit de desarrollo de software de Windows (SDK).

Los datos binarios de firma y marca de tiempo son relativamente sencillos mediante [SignTool](signtool.md). El publicador debe obtener un certificado de firma de código de una ENTIDAD de certificación de firma de código comercial. Para mayor comodidad, Microsoft publica y actualiza una lista de CA públicas, incluidas las que emiten certificados Authenticode. Cuando esté listo para publicarse, los archivos de objeto se firman y marcan de tiempo mediante los parámetros de línea de comandos adecuados con la herramienta SignTool. El resultado de cualquier operación SignTool siempre es un formato PKCS \# 7 [**SignedData**](signeddata.md).

SignTool acepta como entrada los datos binarios sin procesar que se firmarán y marcarán de tiempo, o bien los datos binarios firmados previamente para su marca de tiempo. Los datos que se han firmado previamente se pueden marcar de tiempo mediante el **comando signtool timestamp.**



| Argumento             | Descripción                                                                                                                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **/t** *HTTPAddress* | Indica que se va a marcar el tiempo del archivo. Se debe proporcionar una dirección URL que especifique una dirección de un servidor de marca de tiempo. **/t se** puede usar con los comandos **signtool sign y** **signtool timestamp.** |



 

Para obtener más información sobre las herramientas que pueden ser útiles en este contexto, vea [Herramientas de criptografía](cryptography-tools.md) y [SignTool](signtool.md).

## <a name="implementation-details-and-wire-format"></a>Detalles de implementación y formato de conexión

[SignTool](signtool.md) se basa en la implementación de Windows Authenticode para crear y firmas de marca de tiempo. [*Authenticode*](../secgloss/a-gly.md) funciona en archivos binarios, como .cab, .exe, .dll o .ocx. Authenticode crea primero la firma y genera un elemento PKCS \# 7 [**SignedData**](signeddata.md). Se trata de **SignedData** que se debe contrafirmar, como se describe en PKCS \# 9.

El proceso de contrasignación tiene lugar en cuatro pasos:

1.  Copie la firma (es decir, encryptedDigest) de SignerInfo de PKCS \# 7 [**SignedData**](signeddata.md).
2.  Cree una solicitud de marca de tiempo cuyo contenido sea la firma original. Envíelo al servidor de marca de tiempo [*Abstract Syntax Notation One*](../secgloss/a-gly.md) (ASN.1) codificado como TimeStampRequest.
3.  Reciba una marca de tiempo, con el formato de segundo PKCS \# 7 [**SignedData**](signeddata.md), devuelto desde el servidor de marca de tiempo.
4.  Copie signerInfo de la marca de tiempo directamente en el elemento Original PKCS \# 7 [**SignedData**](signeddata.md)como contrafirma PKCS 9 (es decir, un atributo no autenticado en \# signerInfo del original).

## <a name="time-stamp-request"></a>Solicitud de marca de tiempo

La solicitud de marca de tiempo se envía dentro de un mensaje HTTP 1.1 POST. En el encabezado HTTP, la directiva CacheControl se establece en no-cache y la directiva Content-Type se establece en application/octet-stream. El cuerpo del mensaje HTTP es una [](../secgloss/d-gly.md) codificación base64 de reglas de codificación distinguida (DER) de la solicitud de marca de tiempo.

Aunque no se usa actualmente, la directiva Content-Length también debe usarse para construir el mensaje HTTP, ya que ayuda al servidor de marca de tiempo a localizar dónde se encuentra la solicitud en HTTP POST.

También pueden estar presentes otros encabezados HTTP y deben omitirse si el solicitante o el servidor de marca de tiempo no los entiende.

La solicitud de marca de tiempo es un mensaje codificado asn.1. El formato de la solicitud es el siguiente.

``` syntax
TimeStampRequest ::= SEQUENCE {
   countersignatureType OBJECT IDENTIFIER,
   attributes Attributes OPTIONAL, 
   content  ContentInfo
}
```

CountersignatureType es [](../secgloss/o-gly.md) el identificador de objeto (OID) que lo identifica como contrasignación de marca de tiempo y debe ser el OID exacto 1.3.6.1.4.1.311.3.2.1.

Actualmente no se incluye ningún atributo en la solicitud de marca de tiempo.

El contenido es contentinfo tal como se define en PKCS \# 7. El contenido son los datos que se firmarán. Para la marca de tiempo de firma, ContentType debe ser Data y el contenido debe ser encryptedDigest (signerInfo) del contenido PKCS 7 que se va a marcar \# de tiempo.

## <a name="time-stamp-response"></a>Respuesta de marca de tiempo

La respuesta de marca de tiempo también se envía dentro de un mensaje HTTP 1.1. En el encabezado HTTP, la directiva Content-Type también se establece en application/octet-stream. El cuerpo del mensaje HTTP es una codificación base64 de codificación DER de la respuesta de marca de tiempo.

La respuesta de marca de tiempo es un mensaje firmado pkcs \# 7 firmado por el marca de tiempo. ContentInfo del mensaje PKCS \# 7 es idéntico al ContenidoInfo recibido en la marca de tiempo. El contenido pkcs 7 contiene el atributo autenticado de tiempo de firma (definido en \# PKCS \# 99, OID 1.2.840.113549.9.5).

Una vez que Authenticode recibe la marca de tiempo del servidor, Authenticode incorpora la marca de tiempo en el elemento SignedData de PKCS 7 original como \# contrafirma. [](signeddata.md) Para ello, se descarta contentinfo de los datos firmados de PKCS 7 devueltos y el elemento SignerInfo de la marca de tiempo devuelta se copia como contrafirma en \# signerInfo del elemento SignedData de PKCS  \# 7 original.  La cadena de certificados del autor de la marca de tiempo también se copia en Certificates in the original PKCS 7 SignedData como un atributo no autenticado del \# firmante original. 

Para obtener más información sobre PKCS y otros temas de seguridad, consulte la biblioteca [de contenido del sitio web de RSA.](https://www.rsa.com/content_library.aspx)

 

 
