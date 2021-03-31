---
description: Enumera los objetos proporcionados por CryptoAPI.
ms.assetid: 4ab16355-1341-4c7a-b570-bd33f11dde00
title: Objetos de criptografía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea3476e7edad1d32fe1e11635bd65622d2a8375
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104423772"
---
# <a name="cryptography-objects"></a>Objetos de criptografía

Los objetos de criptografía se clasifican según el uso de la manera siguiente:

-   [Objetos de almacén de certificados](#certificate-store-objects)
-   [Objetos de firma digital](#digital-signature-objects)
-   [Objetos de datos con doble cifrado](#enveloped-data-objects)
-   [Objetos de cifrado de datos](#data-encryption-objects)
-   [Objetos auxiliares](#auxiliary-objects)
-   [Objetos de inscripción de certificados](#certificate-enrollment-objects)

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
| [**ExtendedProperty**](extendedproperties.md)     | Representa una propiedad extendida de Microsoft.                                                                               |
| [**Extensión**](extension.md)                     | Representa una única extensión de certificado.                                                                              |
| [**Extensiones**](extensions.md)                   | Representa una colección de objetos de [**extensión**](extension.md) .                                                      |
| [**PrivateKey**](privatekey.md)                   | Representa una clave privada.                                                                                               |
| [**PublicKey**](publickey.md)                     | Representa una clave pública en un objeto de [**certificado**](certificate.md) .                                                 |
| [**Store**](store.md)                             | Proporciona las propiedades y los métodos para elegir, administrar y usar almacenes de certificados y los certificados en esos almacenes. |
| [**Plantilla**](template.md)                       | Representa la plantilla de extensión de certificado del certificado.                                                       |



 

## <a name="digital-signature-objects"></a>Objetos de firma digital

Los objetos siguientes se exportan para firmar datos digitalmente y comprobar firmas digitales.



| Object                           | Descripción                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | Objeto que se usa para firmar código con una firma digital Authenticode y para comprobar la firma en código firmado. |
| [**SignedData**](signeddata.md) | Objeto que se usa para firmar datos y para comprobar la firma en los datos firmados.                                        |
| [**Firmante**](signer.md)         | Información sobre un único firmante de datos, incluido el certificado del firmante.                                    |
| [**Firmantes**](signers.md)       | Colección de objetos de [**firmante**](signer.md) .                                                             |



 

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
| [**NoticeNumbers**](noticenumbers.md)         | Representa una colección de objetos de [**extensión**](extension.md) .                                                                              |
| [**OID**](oid.md)                             | Representa un identificador de objeto que usan varias propiedades de CAPICOM.                                                                     |
| [**OID**](oids.md)                           | Representa una colección de objetos [**OID**](oid.md) .                                                                                          |
| [**PolicyInformation**](policyinformation.md) | Proporciona acceso a los OID de directiva de una extensión.                                                                                             |
| [**Qualifier**](qualifier.md)                 | Representa un puntero de informe de prácticas de certificación (CPS) o el calificador de aviso de usuario.                                                           |
| [**Calificadores**](qualifiers.md)               | Representa una colección de calificadores.                                                                                                          |
| [**Configuración**](settings.md)                   | Habilita o deshabilita los cuadros de diálogo para solicitar la identidad del remitente o del remitente si no se especifica esa identidad.                                     |
| [**Sectores públicos**](utilities.md)                 | Proporciona funcionalidad para las tareas comunes.                                                                                                        |



 

## <a name="certificate-enrollment-objects"></a>Objetos de inscripción de certificados

El siguiente objeto se usa para la inscripción de certificados.



| Object                     | Descripción                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)) | Objeto que representa el control de inscripción de certificados. Se utiliza principalmente al programar en Visual Basic u otro lenguaje de automatización. |



 

 

 
