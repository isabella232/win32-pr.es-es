---
description: Enumera los objetos proporcionados por CryptoAPI.
ms.assetid: 4ab16355-1341-4c7a-b570-bd33f11dde00
title: Objetos criptografía
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ea3476e7edad1d32fe1e11635bd65622d2a8375
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127271087"
---
# <a name="cryptography-objects"></a>Objetos criptografía

Los objetos criptografía se clasifican según el uso como se muestra a continuación:

-   [Objetos de almacén de certificados](#certificate-store-objects)
-   [Objetos de firma digital](#digital-signature-objects)
-   [Objetos de datos sobreados](#enveloped-data-objects)
-   [Objetos de cifrado de datos](#data-encryption-objects)
-   [Objetos auxiliares](#auxiliary-objects)
-   [Objetos de inscripción de certificados](#certificate-enrollment-objects)

## <a name="certificate-store-objects"></a>Objetos de almacén de certificados

Los siguientes objetos funcionan con [*almacenes de certificados*](../secgloss/c-gly.md) y los certificados de esos almacenes. CAPICOM admite el uso de usuarios actuales, máquinas locales, memoria Active Directory almacenes de certificados.



| Object                                             | Descripción                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [**Certificado**](certificate.md)                 | Un único certificado digital.                                                                                           |
| [**CertificatePolicies**](certificatepolicies.md) | Colección de objetos [**PolicyInformation.**](policyinformation.md)                                                 |
| [**Certificados**](certificates.md)               | Colección de [**objetos Certificate.**](certificate.md)                                                               |
| [**CertificateStatus**](certificatestatus.md)     | Proporciona información de estado sobre un certificado.                                                                           |
| [**Cadena**](chain.md)                             | Crea y comprueba una cadena de validación de certificados basada en un certificado digital.                                       |
| [**ExtendedProperties**](extendedproperties.md)   | Representa una colección de [**objetos ExtendedProperty.**](extendedproperty.md)                                        |
| [**ExtendedProperty**](extendedproperties.md)     | Representa una propiedad extendida por Microsoft.                                                                               |
| [**Extensión**](extension.md)                     | Representa una extensión de certificado única.                                                                              |
| [**Extensiones**](extensions.md)                   | Representa una colección de [**objetos Extension.**](extension.md)                                                      |
| [**PrivateKey**](privatekey.md)                   | Representa una clave privada.                                                                                               |
| [**PublicKey**](publickey.md)                     | Representa una clave pública en un [**objeto Certificate.**](certificate.md)                                                 |
| [**Tienda**](store.md)                             | Proporciona las propiedades y los métodos para elegir, administrar y usar almacenes de certificados y los certificados de esos almacenes. |
| [**Plantilla**](template.md)                       | Representa la plantilla de extensión de certificado del certificado.                                                       |



 

## <a name="digital-signature-objects"></a>Objetos de firma digital

Los siguientes objetos se exportan para firmar digitalmente los datos y comprobar las firmas digitales.



| Object                           | Descripción                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| [**SignedCode**](signedcode.md) | Objeto que se usa para firmar código con una firma digital Authenticode y para comprobar la firma en el código firmado. |
| [**SignedData**](signeddata.md) | Objeto que se usa para firmar datos y comprobar la firma en los datos firmados.                                        |
| [**Firmante**](signer.md)         | Información sobre un firmante de datos único, incluido el certificado del firmante.                                    |
| [**Firmantes**](signers.md)       | Colección de [**objetos signer.**](signer.md)                                                             |



 

## <a name="enveloped-data-objects"></a>Objetos de datos sobreados

Los siguientes objetos se exportan para crear mensajes de datos en sobre para la privacidad y para descifrar datos en mensajes con sobres.



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
| [**NoticeNumbers**](noticenumbers.md)         | Representa una colección de [**objetos Extension.**](extension.md)                                                                              |
| [**OID**](oid.md)                             | Representa un identificador de objeto utilizado por varias propiedades CAPICOM.                                                                     |
| [**OID**](oids.md)                           | Representa una colección de [**objetos OID.**](oid.md)                                                                                          |
| [**PolicyInformation**](policyinformation.md) | Proporciona acceso a los edÍD de directiva de una extensión.                                                                                             |
| [**Calificador:**](qualifier.md)                 | Representa un puntero de instrucción de práctica de certificación (CPS) o un calificador de aviso de usuario.                                                           |
| [**Calificadores**](qualifiers.md)               | Representa una colección de calificadores.                                                                                                          |
| [**Configuración**](settings.md)                   | Habilita o deshabilita los cuadros de diálogo para solicitar la identidad del firmante o remitente si no se especifica esa identidad.                                     |
| [**Sectores públicos**](utilities.md)                 | Proporciona funcionalidad para tareas comunes.                                                                                                        |



 

## <a name="certificate-enrollment-objects"></a>Objetos de inscripción de certificados

El siguiente objeto se usa para la inscripción de certificados.



| Object                     | Descripción                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85)) | Objeto que representa el control de inscripción de certificados. Se usa principalmente al programar en Visual Basic u otro lenguaje de Automation. |



 

 

 
