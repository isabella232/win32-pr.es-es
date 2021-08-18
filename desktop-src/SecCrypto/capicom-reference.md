---
description: Proporciona servicios que permiten a los desarrolladores de aplicaciones agregar seguridad basada en criptografía a las aplicaciones.
ms.assetid: 9a2add82-53f9-49ed-b20c-019f95e7d260
title: Referencia de CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c94bd7f8c2052f53b4dc1e244251ba76c1b10e349e0f43434a926db6dbeb9190
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772116"
---
# <a name="capicom-reference"></a>Referencia de CAPICOM

\[CAPICOM es un componente de solo 32 bits que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use el .NET Framework para implementar características de seguridad. Para obtener más información, [vea Alternativas al uso de CAPICOM.](alternatives-to-using-capicom.md)\]

El cliente COM CAPICOM proporciona servicios que permiten a los desarrolladores de aplicaciones agregar seguridad basada en [*criptografía a*](../secgloss/c-gly.md) las aplicaciones. CryptoAPI incluye funcionalidad para la autenticación mediante [*firmas digitales,*](../secgloss/d-gly.md)para envolver mensajes y para cifrar y descifrar datos.



| Category                    | Descripción                                                                                                                |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Objetos de almacén de certificados   | Objetos disponibles para usar almacenes de certificados y certificados en esos almacenes.                                       |
| Objetos de firma digital   | Objetos que se usan para firmar digitalmente los datos y comprobar las firmas digitales.                                                      |
| Objetos de datos sobreados      | Objetos que se usan para crear mensajes de datos en sobre para la privacidad y para descifrar los datos de los mensajes con sobres.                      |
| Objetos de cifrado de datos     | Objetos usados para cifrar datos y descifrar datos cifrados.                                                                |
| Objetos auxiliares           | Objetos que se usan para cambiar los comportamientos predeterminados y para administrar certificados, almacenes de certificados y mensajes de interfaz de usuario (UI). |
| Interfaces de interoperabilidad | Interfaces que permiten que las derivaciones de CryptoAPI funcionen junto con CAPICOM 2.0.                                          |
| Tipos de enumeración           | Tipos de enumeración usados con CAPICOM.                                                                                       |



 

## <a name="certificate-store-objects"></a>Objetos de almacén de certificados

Los siguientes objetos funcionan con [*almacenes de certificados*](../secgloss/c-gly.md) y los certificados de esos almacenes. CAPICOM admite el uso de usuarios actuales, máquinas locales, memoria y Active Directory almacenes de certificados.



| Object                                             | Descripción                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Certificado**](certificate.md)                 | Un único certificado digital.                                                                                           |
| [**CertificatePolicies**](certificatepolicies.md) | Colección de objetos [**PolicyInformation.**](policyinformation.md)                                                 |
| [**Certificados**](certificates.md)               | Colección de [**objetos Certificate.**](certificate.md)                                                               |
| [**CertificateStatus**](certificatestatus.md)     | Proporciona información de estado sobre un certificado.                                                                           |
| [**Cadena**](chain.md)                             | Crea y comprueba una cadena de validación de certificados basada en un certificado digital.                                       |
| [**ExtendedProperties**](extendedproperties.md)   | Representa una colección de [**objetos ExtendedProperty.**](extendedproperty.md)                                        |
| [**ExtendedProperty**](extendedproperty.md)       | Representa una propiedad extendida por Microsoft.                                                                               |
| [**Extensión**](extension.md)                     | Representa una extensión de certificado única.                                                                              |
| [**Extensiones**](extensions.md)                   | Representa una colección de [**objetos Extension.**](extension.md)                                                      |
| [**PrivateKey**](privatekey.md)                   | Representa una clave privada.                                                                                               |
| [**PublicKey**](publickey.md)                     | Representa una clave pública en un [**objeto Certificate.**](certificate.md)                                                 |
| [**Tienda**](store.md)                             | Proporciona las propiedades y los métodos para elegir, administrar y usar almacenes de certificados y los certificados de esos almacenes. |
| [**Plantilla**](template.md)                       | Representa la plantilla de extensión de certificado del certificado.                                                       |



 

## <a name="digital-signature-objects"></a>Objetos de firma digital

Los siguientes objetos se exportan para firmar digitalmente los datos y comprobar las firmas digitales.



| Object                           | Descripción                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | Proporciona funcionalidad para firmar contenido con una firma digital Authenticode. |
| [**SignedData**](signeddata.md) | Objeto que se usa para firmar datos y comprobar la firma en los datos firmados.               |
| [**Firmante**](signer.md)         | Información sobre un firmante de datos único, incluido el certificado del firmante.           |
| [**Firmantes**](signers.md)       | Colección de [**objetos Signer.**](signer.md)                                    |



 

## <a name="enveloped-data-objects"></a>Objetos de datos sobreados

Los objetos siguientes se exportan para crear mensajes de datos en sobre para la privacidad y para descifrar datos en mensajes con sobres.



| Object                                 | Descripción                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnvelopedData**](envelopeddata.md) | Objetos que se usan para crear, enviar y recibir datos sobres. Los datos sobres se cifran para que solo los destinatarios previstos puedan descifrarlo. |
| [**Recipients**](recipients.md)       | Colección de los [**objetos Certificate**](certificate.md) de los destinatarios previstos de un mensaje con sobres.                           |



 

## <a name="data-encryption-objects"></a>Objetos de cifrado de datos

El siguiente objeto se exporta para cifrar datos arbitrarios por privacidad y para descifrar los datos cifrados.



| Object                                 | Descripción                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**EncryptedData**](encrypteddata.md) | Objetos usados para cifrar datos. Los datos cifrados en [**un objeto EncryptedData**](encrypteddata.md) se pueden descifrar. |



 

## <a name="auxiliary-objects"></a>Objetos auxiliares

Los siguientes objetos se exportan para cambiar los comportamientos predeterminados de otros objetos y para administrar certificados, almacenes de certificados y mensajes.



| Object                                         | Descripción                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](algorithm.md)                 | Establece el algoritmo y [*la longitud de clave que*](../secgloss/k-gly.md) se usarán en las operaciones criptográficas. |
| [**Atributo**](attribute.md)                 | Proporciona una única parte de información agregada sobre una firma, como la hora de firma.                                                    |
| [**Atributos**](attributes.md)               | Colección de [**objetos Attribute.**](attribute.md)                                                                                           |
| [**BasicConstraints**](basicconstraints.md)   | Proporciona acceso de solo lectura a las restricciones básicas en los usos de un certificado.                                                                    |
| [**EKU**](eku.md)                             | Proporciona acceso a las propiedades EKU de los certificados.                                                                                              |
| [**EKUs**](ekus.md)                           | Colección de [**objetos EKU.**](eku.md)                                                                                                       |
| [**EncodedData**](encodeddata.md)             | Representa un bloque de datos codificados.                                                                                                             |
| [**ExtendedKeyUsage**](extendedkeyusage.md)   | Proporciona acceso de solo lectura a las propiedades de uso de claves extendidas de los certificados.                                                                 |
| [**HashedData**](hasheddata.md)               | Proporciona funcionalidad para aplicar un algoritmo hash a una cadena.                                                                               |
| [**KeyUsage**](keyusage.md)                   | Proporciona acceso de solo lectura a las propiedades de uso clave de los certificados.                                                                              |
| [**Oid**](oid.md)                             | Representa un identificador de objeto utilizado por varias propiedades CAPICOM.                                                                     |
| [**OID**](oids.md)                           | Representa una colección de [**objetos OID.**](oid.md)                                                                                          |
| [**PolicyInformation**](policyinformation.md) | Proporciona acceso a los ED de directiva de una extensión.                                                                                             |
| [**Qualifier**](qualifier.md)                 | Representa un puntero de instrucción de práctica de certificación (CPS) o un calificador de aviso de usuario.                                                           |
| [**Calificadores**](qualifiers.md)               | Representa una colección de calificadores.                                                                                                          |
| [**Configuración**](settings.md)                   | Habilita o deshabilita los cuadros de diálogo para solicitar la identidad del firmante o remitente si no se especifica esa identidad.                                     |
| [**Utilidades**](utilities.md)                 | Proporciona funcionalidad para tareas comunes.                                                                                                        |



 

## <a name="interoperability-interfaces"></a>Interfaces de interoperabilidad

Las interfaces siguientes permiten que las derivaciones de CryptoAPI funcionen junto con CAPICOM 2.0.



| Interfaz                              | Descripción                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertContext**](icertcontext.md)   | Proporciona acceso al contexto de un objeto de certificado [](certificate.md) CAPICOM X.509v3. Este contexto permite usar el certificado CAPICOM en otras derivaciones de CryptoAPI. |
| [**ICertStore**](icertstore.md)       | Proporciona acceso al contexto de un objeto de [**almacén**](store.md) CAPICOM. Este contexto permite que el almacén de certificados CAPICOM se utilice en otras derivaciones de CryptoAPI.               |
| [**IChainContext**](ichaincontext.md) | Proporciona acceso al contexto de [](chain.md) un objeto de cadena CAPICOM. Este contexto permite usar la cadena de confianza de certificados CAPICOM en otras derivaciones de CryptoAPI.         |



 

## <a name="enumeration-types"></a>Tipos de enumeración

CAPICOM define los siguientes tipos de enumeración:

-   [**CAPICOM \_ ACTIVE \_ DIRECTORY \_ SEARCH \_ LOCATION**](capicom-active-directory-search-location.md)
-   [**ATRIBUTO \_ CAPICOM**](capicom-attribute.md)
-   [**CAPICOM \_ CERT \_ INFO \_ TYPE**](capicom-cert-info-type.md)
-   [**CAPICOM \_ CERTIFICATE \_ FIND \_ TYPE**](capicom-certificate-find-type.md)
-   [**CAPICOM \_ CERTIFICATE \_ INCLUDE \_ OPTION**](capicom-certificate-include-option.md)
-   [**CERTIFICADO CAPICOM \_ \_ GUARDAR COMO \_ \_ TIPO**](capicom-certificate-save-as-type.md)
-   [**CERTIFICADOS CAPICOM \_ \_ GUARDADOS \_ COMO \_ TIPO**](capicom-certificates-save-as-type.md)
-   [**MARCA DE COMPROBACIÓN \_ CAPICOM \_**](capicom-check-flag.md)
-   [**CAPICOM \_ EKU**](capicom-eku.md)
-   [**TIPO DE \_ CODIFICACIÓN \_ CAPICOM**](capicom-encoding-type.md)
-   [**ALGORITMO DE CIFRADO \_ \_ CAPICOM**](capicom-encryption-algorithm.md)
-   [**LONGITUD DE CLAVE \_ DE CIFRADO \_ CAPICOM \_**](capicom-encryption-key-length.md)
-   [**CÓDIGO DE \_ ERROR DE CAPICOM \_**](capicom-error-code.md)
-   [**MARCA DE EXPORTACIÓN \_ CAPICOM \_**](capicom-export-flag.md)
-   [**ALGORITMO \_ HASH CAPICOM \_**](capicom-hash-algorithm.md)
-   [**CAPICOM \_ KEY \_ LOCATION**](capicom-key-location.md)
-   [**CAPICOM \_ KEY \_ SPEC**](capicom-key-spec.md)
-   [**MARCA DE ALMACENAMIENTO DE CLAVES CAPICOM \_ \_ \_**](capicom-key-storage-flag.md)
-   [**CAPICOM \_ OID**](capicom-oid.md)
-   [**CAPICOM \_ PROPID**](capicom-propid.md)
-   [**CAPICOM \_ PROV \_ TYPE**](capicom-prov-type.md)
-   [**TIPO DE SECRETO \_ CAPICOM \_**](capicom-secret-type.md)
-   [**MARCA DE COMPROBACIÓN \_ DE \_ DATOS FIRMADOS \_ DE \_ CAPICOM**](capicom-signed-data-verify-flag.md)
-   [**UBICACIÓN DE LA \_ TIENDA CAPICOM \_**](capicom-store-location.md)
-   [**CAPICOM \_ STORE \_ OPEN \_ MODE**](capicom-store-open-mode.md)
-   [**CAPICOM \_ STORE \_ SAVE \_ AS \_ TYPE**](capicom-store-save-as-type.md)

 

 
