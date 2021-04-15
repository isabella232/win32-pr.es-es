---
description: Proporciona servicios que permiten a los desarrolladores de aplicaciones agregar seguridad basada en la criptografía a aplicaciones.
ms.assetid: 9a2add82-53f9-49ed-b20c-019f95e7d260
title: Referencia de CAPICOM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 41b828f3b5b35e3e0ef799529f866c23416c8df8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669816"
---
# <a name="capicom-reference"></a>Referencia de CAPICOM

\[CAPICOM es un componente de solo bits de 32 que está disponible para su uso en los siguientes sistemas operativos: Windows Server 2008, Windows Vista y Windows XP. En su lugar, use la .NET Framework para implementar características de seguridad. Para obtener más información, vea [alternativas al uso de CAPICOM](alternatives-to-using-capicom.md).\]

El cliente de CAPICOM COM proporciona servicios que permiten a los desarrolladores de aplicaciones agregar seguridad basada en la [*Criptografía*](../secgloss/c-gly.md) a las aplicaciones. CryptoAPI incluye funcionalidad para la autenticación mediante [*firmas digitales*](../secgloss/d-gly.md), para la envoltura de mensajes y para el cifrado y descifrado de datos.



| Category                    | Descripción                                                                                                                |
|-----------------------------|----------------------------------------------------------------------------------------------------------------------------|
| Objetos de almacén de certificados   | Objetos disponibles para usar almacenes de certificados y los certificados de esas tiendas.                                       |
| Objetos de firma digital   | Objetos usados para firmar datos digitalmente y comprobar firmas digitales.                                                      |
| Objetos de datos con doble cifrado      | Objetos que se usan para crear mensajes de datos con doble cifrado para la privacidad y para descifrar datos en mensajes con doble cifrado.                      |
| Objetos de cifrado de datos     | Objetos usados para cifrar datos y descifrar datos cifrados.                                                                |
| Objetos auxiliares           | Objetos usados para cambiar los comportamientos predeterminados y administrar certificados, almacenes de certificados y mensajes de interfaz de usuario (IU). |
| Interfaces de interoperabilidad | Interfaces que permiten que las derivaciones de CryptoAPI funcionen conjuntamente con CAPICOM 2,0.                                          |
| Tipos de enumeración           | Tipos de enumeración usados con CAPICOM.                                                                                       |



 

## <a name="certificate-store-objects"></a>Objetos de almacén de certificados

Los siguientes objetos funcionan con los [*almacenes de certificados*](../secgloss/c-gly.md) y los certificados de dichos almacenes. CAPICOM admite el uso de almacenes de certificados del usuario actual, el equipo local, la memoria y el Active Directory.



| Object                                             | Descripción                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Certificado**](certificate.md)                 | Un único certificado digital.                                                                                           |
| [**CertificatePolicies**](certificatepolicies.md) | Colección de objetos [**PolicyInformation**](policyinformation.md) .                                                 |
| [**Certificados**](certificates.md)               | Colección de objetos de [**certificado**](certificate.md) .                                                               |
| [**CertificateStatus**](certificatestatus.md)     | Proporciona información de estado sobre un certificado.                                                                           |
| [**IAM**](chain.md)                             | Crea y comprueba una cadena de validación de certificados basada en un certificado digital.                                       |
| [**ExtendedProperties**](extendedproperties.md)   | Representa una colección de objetos [**ExtendedProperty**](extendedproperty.md) .                                        |
| [**ExtendedProperty**](extendedproperty.md)       | Representa una propiedad extendida de Microsoft.                                                                               |
| [**Extensión**](extension.md)                     | Representa una única extensión de certificado.                                                                              |
| [**Extensiones**](extensions.md)                   | Representa una colección de objetos de [**extensión**](extension.md) .                                                      |
| [**PrivateKey**](privatekey.md)                   | Representa una clave privada.                                                                                               |
| [**PublicKey**](publickey.md)                     | Representa una clave pública en un objeto de [**certificado**](certificate.md) .                                                 |
| [**Store**](store.md)                             | Proporciona las propiedades y los métodos para elegir, administrar y usar almacenes de certificados y los certificados en esos almacenes. |
| [**Plantilla**](template.md)                       | Representa la plantilla de extensión de certificado del certificado.                                                       |



 

## <a name="digital-signature-objects"></a>Objetos de firma digital

Los objetos siguientes se exportan para firmar datos digitalmente y comprobar firmas digitales.



| Object                           | Descripción                                                                        |
|----------------------------------|------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | Proporciona funcionalidad para firmar el contenido con una firma digital Authenticode. |
| [**SignedData**](signeddata.md) | Objeto que se usa para firmar datos y para comprobar la firma en los datos firmados.               |
| [**Firmante**](signer.md)         | Información sobre un único firmante de datos, incluido el certificado del firmante.           |
| [**Firmantes**](signers.md)       | Colección de objetos de [**firmante**](signer.md) .                                    |



 

## <a name="enveloped-data-objects"></a>Objetos de datos con doble cifrado

Los objetos siguientes se exportan para crear mensajes de datos con doble cifrado para la privacidad y para descifrar los datos de los mensajes con doble cifrado.



| Object                                 | Descripción                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnvelopedData**](envelopeddata.md) | Objetos usados para crear, enviar y recibir datos con doble cifrado. Los datos con doble cifrado están cifrados para que solo los destinatarios deseados puedan descifrarlos. |
| [**Recipients**](recipients.md)       | Colección de los objetos de [**certificado**](certificate.md) de los destinatarios previstos de un mensaje con doble cifrado.                           |



 

## <a name="data-encryption-objects"></a>Objetos de cifrado de datos

El siguiente objeto se exporta para cifrar los datos arbitrarios para la privacidad y para descifrar los datos cifrados.



| Object                                 | Descripción                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**EncryptedData**](encrypteddata.md) | Objetos que se utilizan para cifrar datos. Los datos cifrados de un objeto [**EncryptedData**](encrypteddata.md) se pueden descifrar. |



 

## <a name="auxiliary-objects"></a>Objetos auxiliares

Los objetos siguientes se exportan para cambiar los comportamientos predeterminados de otros objetos y administrar certificados, almacenes de certificados y mensajes.



| Object                                         | Descripción                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Algoritmo**](algorithm.md)                 | Establece el algoritmo y la [*longitud de clave*](../secgloss/k-gly.md) que se van a usar en las operaciones criptográficas. |
| [**Atributo**](attribute.md)                 | Proporciona una sola parte de la información agregada sobre una firma, como la hora de firma.                                                    |
| [**Atributos**](attributes.md)               | Colección de objetos de [**atributo**](attribute.md) .                                                                                           |
| [**BasicConstraints**](basicconstraints.md)   | Proporciona acceso de solo lectura a las restricciones básicas de los usos de un certificado.                                                                    |
| [**EKU**](eku.md)                             | Proporciona acceso a las propiedades EKU de los certificados.                                                                                              |
| [**EKU**](ekus.md)                           | Colección de objetos [**EKU**](eku.md) .                                                                                                       |
| [**EncodedData**](encodeddata.md)             | Representa un bloque de datos codificados.                                                                                                             |
| [**ExtendedKeyUsage**](extendedkeyusage.md)   | Proporciona acceso de solo lectura a las propiedades de uso mejorado de clave de los certificados.                                                                 |
| [**HashedData**](hasheddata.md)               | Proporciona funcionalidad para aplicar un algoritmo hash a una cadena.                                                                               |
| [**KeyUsage**](keyusage.md)                   | Proporciona acceso de solo lectura a las propiedades de uso de claves de los certificados.                                                                              |
| [**OID**](oid.md)                             | Representa un identificador de objeto que usan varias propiedades de CAPICOM.                                                                     |
| [**OID**](oids.md)                           | Representa una colección de objetos [**OID**](oid.md) .                                                                                          |
| [**PolicyInformation**](policyinformation.md) | Proporciona acceso a los OID de directiva de una extensión.                                                                                             |
| [**Qualifier**](qualifier.md)                 | Representa un puntero de informe de prácticas de certificación (CPS) o el calificador de aviso de usuario.                                                           |
| [**Calificadores**](qualifiers.md)               | Representa una colección de calificadores.                                                                                                          |
| [**Configuración**](settings.md)                   | Habilita o deshabilita los cuadros de diálogo para solicitar la identidad del remitente o del remitente si no se especifica esa identidad.                                     |
| [**Sectores públicos**](utilities.md)                 | Proporciona funcionalidad para las tareas comunes.                                                                                                        |



 

## <a name="interoperability-interfaces"></a>Interfaces de interoperabilidad

Las siguientes interfaces permiten que la derivación de CryptoAPI funcione junto con CAPICOM 2,0.



| Interfaz                              | Descripción                                                                                                                                                                              |
|----------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertContext**](icertcontext.md)   | Proporciona acceso al contexto de un objeto de [**certificado**](certificate.md) de CAPICOM X. 509v3. Este contexto permite usar el certificado de CAPICOM en otras derivaciones de CryptoAPI. |
| [**ICertStore**](icertstore.md)       | Proporciona acceso al contexto de un objeto de [**almacén**](store.md) de CAPICOM. Este contexto permite usar el almacén de certificados de CAPICOM en otras derivaciones de CryptoAPI.               |
| [**IChainContext**](ichaincontext.md) | Proporciona acceso al contexto de un objeto de [**cadena**](chain.md) CAPICOM. Este contexto permite usar la cadena de confianza de certificados de CAPICOM en otras derivaciones de CryptoAPI.         |



 

## <a name="enumeration-types"></a>Tipos de enumeración

CAPICOM define los siguientes tipos de enumeración:

-   [**la \_ \_ Ubicación de \_ búsqueda de Active \_ Directory de CAPICOM**](capicom-active-directory-search-location.md)
-   [**\_atributo CAPICOM**](capicom-attribute.md)
-   [**\_tipo de \_ información de certificado de CAPICOM \_**](capicom-cert-info-type.md)
-   [**\_tipo de \_ búsqueda de certificado de CAPICOM \_**](capicom-certificate-find-type.md)
-   [**\_opción de \_ inclusión de certificado de CAPICOM \_**](capicom-certificate-include-option.md)
-   [**\_ \_ \_ tipo de guardado de certificado de \_ CAPICOM**](capicom-certificate-save-as-type.md)
-   [**los \_ certificados \_ de CAPICOM se guardan \_ como \_ tipo**](capicom-certificates-save-as-type.md)
-   [**\_marca de comprobación de CAPICOM \_**](capicom-check-flag.md)
-   [**EKU de CAPICOM \_**](capicom-eku.md)
-   [**tipo de codificación de CAPICOM \_ \_**](capicom-encoding-type.md)
-   [**\_algoritmo de cifrado de CAPICOM \_**](capicom-encryption-algorithm.md)
-   [**longitud de la \_ clave de cifrado de CAPICOM \_ \_**](capicom-encryption-key-length.md)
-   [**\_código de error de CAPICOM \_**](capicom-error-code.md)
-   [**\_marca de exportación de CAPICOM \_**](capicom-export-flag.md)
-   [**\_algoritmo hash \_ CAPICOM**](capicom-hash-algorithm.md)
-   [**Ubicación de la \_ clave CAPICOM \_**](capicom-key-location.md)
-   [**\_especificación de tecla CAPICOM \_**](capicom-key-spec.md)
-   [**\_marca de \_ almacenamiento de claves de CAPICOM \_**](capicom-key-storage-flag.md)
-   [**OID de CAPICOM \_**](capicom-oid.md)
-   [**el \_ PROPID de CAPICOM**](capicom-propid.md)
-   [**\_tipo de Prov de CAPICOM \_**](capicom-prov-type.md)
-   [**\_tipo de secreto de CAPICOM \_**](capicom-secret-type.md)
-   [**\_marca de \_ comprobación de datos firmados de \_ CAPICOM \_**](capicom-signed-data-verify-flag.md)
-   [**\_Ubicación del almacén de CAPICOM \_**](capicom-store-location.md)
-   [**\_ \_ modo abierto de la tienda CAPICOM \_**](capicom-store-open-mode.md)
-   [**CAPICOM \_ Store \_ Guardar \_ como \_ tipo**](capicom-store-save-as-type.md)

 

 
