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
# <a name="cryptography-objects"></a><span data-ttu-id="d78c4-103">Objetos de criptografía</span><span class="sxs-lookup"><span data-stu-id="d78c4-103">Cryptography Objects</span></span>

<span data-ttu-id="d78c4-104">Los objetos de criptografía se clasifican según el uso de la manera siguiente:</span><span class="sxs-lookup"><span data-stu-id="d78c4-104">Cryptography objects are categorized according to usage as follows:</span></span>

-   [<span data-ttu-id="d78c4-105">Objetos de almacén de certificados</span><span class="sxs-lookup"><span data-stu-id="d78c4-105">Certificate Store Objects</span></span>](#certificate-store-objects)
-   [<span data-ttu-id="d78c4-106">Objetos de firma digital</span><span class="sxs-lookup"><span data-stu-id="d78c4-106">Digital Signature Objects</span></span>](#digital-signature-objects)
-   [<span data-ttu-id="d78c4-107">Objetos de datos con doble cifrado</span><span class="sxs-lookup"><span data-stu-id="d78c4-107">Enveloped Data Objects</span></span>](#enveloped-data-objects)
-   [<span data-ttu-id="d78c4-108">Objetos de cifrado de datos</span><span class="sxs-lookup"><span data-stu-id="d78c4-108">Data Encryption Objects</span></span>](#data-encryption-objects)
-   [<span data-ttu-id="d78c4-109">Objetos auxiliares</span><span class="sxs-lookup"><span data-stu-id="d78c4-109">Auxiliary Objects</span></span>](#auxiliary-objects)
-   [<span data-ttu-id="d78c4-110">Objetos de inscripción de certificados</span><span class="sxs-lookup"><span data-stu-id="d78c4-110">Certificate Enrollment Objects</span></span>](#certificate-enrollment-objects)

## <a name="certificate-store-objects"></a><span data-ttu-id="d78c4-111">Objetos de almacén de certificados</span><span class="sxs-lookup"><span data-stu-id="d78c4-111">Certificate Store Objects</span></span>

<span data-ttu-id="d78c4-112">Los siguientes objetos funcionan con los [*almacenes de certificados*](../secgloss/c-gly.md) y los certificados de dichos almacenes.</span><span class="sxs-lookup"><span data-stu-id="d78c4-112">The following objects work with [*certificate stores*](../secgloss/c-gly.md) and the certificates in those stores.</span></span> <span data-ttu-id="d78c4-113">CAPICOM admite el uso de almacenes de certificados del usuario actual, el equipo local, la memoria y el Active Directory.</span><span class="sxs-lookup"><span data-stu-id="d78c4-113">CAPICOM supports the use of Current User, Local Machine, memory, and Active Directory certificate stores.</span></span>



| <span data-ttu-id="d78c4-114">Object</span><span class="sxs-lookup"><span data-stu-id="d78c4-114">Object</span></span>                                             | <span data-ttu-id="d78c4-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="d78c4-115">Description</span></span>                                                                                                             |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d78c4-116">**Certificado**</span><span class="sxs-lookup"><span data-stu-id="d78c4-116">**Certificate**</span></span>](certificate.md)                 | <span data-ttu-id="d78c4-117">Un único certificado digital.</span><span class="sxs-lookup"><span data-stu-id="d78c4-117">A single digital certificate.</span></span>                                                                                           |
| [<span data-ttu-id="d78c4-118">**CertificatePolicies**</span><span class="sxs-lookup"><span data-stu-id="d78c4-118">**CertificatePolicies**</span></span>](certificatepolicies.md) | <span data-ttu-id="d78c4-119">Colección de objetos [**PolicyInformation**](policyinformation.md) .</span><span class="sxs-lookup"><span data-stu-id="d78c4-119">A collection of [**PolicyInformation**](policyinformation.md) objects.</span></span>                                                 |
| [<span data-ttu-id="d78c4-120">**Certificados**</span><span class="sxs-lookup"><span data-stu-id="d78c4-120">**Certificates**</span></span>](certificates.md)               | <span data-ttu-id="d78c4-121">Colección de objetos de [**certificado**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="d78c4-121">Collection of [**Certificate**](certificate.md) objects.</span></span>                                                               |
| [<span data-ttu-id="d78c4-122">**CertificateStatus**</span><span class="sxs-lookup"><span data-stu-id="d78c4-122">**CertificateStatus**</span></span>](certificatestatus.md)     | <span data-ttu-id="d78c4-123">Proporciona información de estado sobre un certificado.</span><span class="sxs-lookup"><span data-stu-id="d78c4-123">Provides status information on a certificate.</span></span>                                                                           |
| [<span data-ttu-id="d78c4-124">**IAM**</span><span class="sxs-lookup"><span data-stu-id="d78c4-124">**Chain**</span></span>](chain.md)                             | <span data-ttu-id="d78c4-125">Crea y comprueba una cadena de validación de certificados basada en un certificado digital.</span><span class="sxs-lookup"><span data-stu-id="d78c4-125">Creates and checks a certificate validation chain based on a digital certificate.</span></span>                                       |
| [<span data-ttu-id="d78c4-126">**ExtendedProperties**</span><span class="sxs-lookup"><span data-stu-id="d78c4-126">**ExtendedProperties**</span></span>](extendedproperties.md)   | <span data-ttu-id="d78c4-127">Representa una colección de objetos [**ExtendedProperty**](extendedproperty.md) .</span><span class="sxs-lookup"><span data-stu-id="d78c4-127">Represents a collection of [**ExtendedProperty**](extendedproperty.md) objects.</span></span>                                        |
| [<span data-ttu-id="d78c4-128">**ExtendedProperty**</span><span class="sxs-lookup"><span data-stu-id="d78c4-128">**ExtendedProperty**</span></span>](extendedproperties.md)     | <span data-ttu-id="d78c4-129">Representa una propiedad extendida de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="d78c4-129">Represents a Microsoft-extended property.</span></span>                                                                               |
| [<span data-ttu-id="d78c4-130">**Extensión**</span><span class="sxs-lookup"><span data-stu-id="d78c4-130">**Extension**</span></span>](extension.md)                     | <span data-ttu-id="d78c4-131">Representa una única extensión de certificado.</span><span class="sxs-lookup"><span data-stu-id="d78c4-131">Represents a single certificate extension.</span></span>                                                                              |
| [<span data-ttu-id="d78c4-132">**Extensiones**</span><span class="sxs-lookup"><span data-stu-id="d78c4-132">**Extensions**</span></span>](extensions.md)                   | <span data-ttu-id="d78c4-133">Representa una colección de objetos de [**extensión**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="d78c4-133">Represents a collection of [**Extension**](extension.md) objects.</span></span>                                                      |
| [<span data-ttu-id="d78c4-134">**PrivateKey**</span><span class="sxs-lookup"><span data-stu-id="d78c4-134">**PrivateKey**</span></span>](privatekey.md)                   | <span data-ttu-id="d78c4-135">Representa una clave privada.</span><span class="sxs-lookup"><span data-stu-id="d78c4-135">Represents a private key.</span></span>                                                                                               |
| [<span data-ttu-id="d78c4-136">**PublicKey**</span><span class="sxs-lookup"><span data-stu-id="d78c4-136">**PublicKey**</span></span>](publickey.md)                     | <span data-ttu-id="d78c4-137">Representa una clave pública en un objeto de [**certificado**](certificate.md) .</span><span class="sxs-lookup"><span data-stu-id="d78c4-137">Represents a public key in a [**Certificate**](certificate.md) object.</span></span>                                                 |
| [<span data-ttu-id="d78c4-138">**Store**</span><span class="sxs-lookup"><span data-stu-id="d78c4-138">**Store**</span></span>](store.md)                             | <span data-ttu-id="d78c4-139">Proporciona las propiedades y los métodos para elegir, administrar y usar almacenes de certificados y los certificados en esos almacenes.</span><span class="sxs-lookup"><span data-stu-id="d78c4-139">Provides the properties and methods to choose, manage, and use certificate stores and the certificates in those stores.</span></span> |
| [<span data-ttu-id="d78c4-140">**Plantilla**</span><span class="sxs-lookup"><span data-stu-id="d78c4-140">**Template**</span></span>](template.md)                       | <span data-ttu-id="d78c4-141">Representa la plantilla de extensión de certificado del certificado.</span><span class="sxs-lookup"><span data-stu-id="d78c4-141">Represents the certificate extension template of the certificate.</span></span>                                                       |



 

## <a name="digital-signature-objects"></a><span data-ttu-id="d78c4-142">Objetos de firma digital</span><span class="sxs-lookup"><span data-stu-id="d78c4-142">Digital Signature Objects</span></span>

<span data-ttu-id="d78c4-143">Los objetos siguientes se exportan para firmar datos digitalmente y comprobar firmas digitales.</span><span class="sxs-lookup"><span data-stu-id="d78c4-143">The following objects are exported to digitally sign data and to verify digital signatures.</span></span>



| <span data-ttu-id="d78c4-144">Object</span><span class="sxs-lookup"><span data-stu-id="d78c4-144">Object</span></span>                           | <span data-ttu-id="d78c4-145">Descripción</span><span class="sxs-lookup"><span data-stu-id="d78c4-145">Description</span></span>                                                                                                 |
|----------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d78c4-146">**SignedCode**</span><span class="sxs-lookup"><span data-stu-id="d78c4-146">**SignedCode**</span></span>](signedcode.md) | <span data-ttu-id="d78c4-147">Objeto que se usa para firmar código con una firma digital Authenticode y para comprobar la firma en código firmado.</span><span class="sxs-lookup"><span data-stu-id="d78c4-147">Object used to sign code with an Authenticode digital signature and to verify the signature on signed code.</span></span> |
| [<span data-ttu-id="d78c4-148">**SignedData**</span><span class="sxs-lookup"><span data-stu-id="d78c4-148">**SignedData**</span></span>](signeddata.md) | <span data-ttu-id="d78c4-149">Objeto que se usa para firmar datos y para comprobar la firma en los datos firmados.</span><span class="sxs-lookup"><span data-stu-id="d78c4-149">Object used to sign data and to verify the signature on signed data.</span></span>                                        |
| [<span data-ttu-id="d78c4-150">**Firmante**</span><span class="sxs-lookup"><span data-stu-id="d78c4-150">**Signer**</span></span>](signer.md)         | <span data-ttu-id="d78c4-151">Información sobre un único firmante de datos, incluido el certificado del firmante.</span><span class="sxs-lookup"><span data-stu-id="d78c4-151">Information on a single data signer, including the signer's certificate.</span></span>                                    |
| [<span data-ttu-id="d78c4-152">**Firmantes**</span><span class="sxs-lookup"><span data-stu-id="d78c4-152">**Signers**</span></span>](signers.md)       | <span data-ttu-id="d78c4-153">Colección de objetos de [**firmante**](signer.md) .</span><span class="sxs-lookup"><span data-stu-id="d78c4-153">Collection of [**Signer**](signer.md) objects.</span></span>                                                             |



 

## <a name="enveloped-data-objects"></a><span data-ttu-id="d78c4-154">Objetos de datos con doble cifrado</span><span class="sxs-lookup"><span data-stu-id="d78c4-154">Enveloped Data Objects</span></span>

<span data-ttu-id="d78c4-155">Los objetos siguientes se exportan para crear mensajes de datos con doble cifrado para la privacidad y para descifrar los datos de los mensajes con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="d78c4-155">The following objects are exported to create enveloped data messages for privacy and to decrypt data in enveloped messages.</span></span>



| <span data-ttu-id="d78c4-156">Object</span><span class="sxs-lookup"><span data-stu-id="d78c4-156">Object</span></span>                                 | <span data-ttu-id="d78c4-157">Descripción</span><span class="sxs-lookup"><span data-stu-id="d78c4-157">Description</span></span>                                                                                                                                |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d78c4-158">**EnvelopedData**</span><span class="sxs-lookup"><span data-stu-id="d78c4-158">**EnvelopedData**</span></span>](envelopeddata.md) | <span data-ttu-id="d78c4-159">Objetos usados para crear, enviar y recibir datos con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="d78c4-159">Objects used to create, send, and receive enveloped data.</span></span> <span data-ttu-id="d78c4-160">Los datos con doble cifrado están cifrados para que solo los destinatarios deseados puedan descifrarlos.</span><span class="sxs-lookup"><span data-stu-id="d78c4-160">Enveloped data is encrypted so that only the intended recipients can decrypt it.</span></span> |
| [<span data-ttu-id="d78c4-161">**Recipients**</span><span class="sxs-lookup"><span data-stu-id="d78c4-161">**Recipients**</span></span>](recipients.md)       | <span data-ttu-id="d78c4-162">Colección de los objetos de [**certificado**](certificate.md) de los destinatarios previstos de un mensaje con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="d78c4-162">Collection of the [**Certificate**](certificate.md) objects of the intended recipients of an enveloped message.</span></span>                           |



 

## <a name="data-encryption-objects"></a><span data-ttu-id="d78c4-163">Objetos de cifrado de datos</span><span class="sxs-lookup"><span data-stu-id="d78c4-163">Data Encryption Objects</span></span>

<span data-ttu-id="d78c4-164">El siguiente objeto se exporta para cifrar los datos arbitrarios para la privacidad y para descifrar los datos cifrados.</span><span class="sxs-lookup"><span data-stu-id="d78c4-164">The following object is exported to encrypt arbitrary data for privacy and to decrypt encrypted data.</span></span>



| <span data-ttu-id="d78c4-165">Object</span><span class="sxs-lookup"><span data-stu-id="d78c4-165">Object</span></span>                                 | <span data-ttu-id="d78c4-166">Descripción</span><span class="sxs-lookup"><span data-stu-id="d78c4-166">Description</span></span>                                                                                                        |
|----------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d78c4-167">**EncryptedData**</span><span class="sxs-lookup"><span data-stu-id="d78c4-167">**EncryptedData**</span></span>](encrypteddata.md) | <span data-ttu-id="d78c4-168">Objetos que se utilizan para cifrar datos.</span><span class="sxs-lookup"><span data-stu-id="d78c4-168">Objects used to encrypt data.</span></span> <span data-ttu-id="d78c4-169">Los datos cifrados de un objeto [**EncryptedData**](encrypteddata.md) se pueden descifrar.</span><span class="sxs-lookup"><span data-stu-id="d78c4-169">Encrypted data in an [**EncryptedData**](encrypteddata.md) object can be decrypted.</span></span> |



 

## <a name="auxiliary-objects"></a><span data-ttu-id="d78c4-170">Objetos auxiliares</span><span class="sxs-lookup"><span data-stu-id="d78c4-170">Auxiliary Objects</span></span>

<span data-ttu-id="d78c4-171">Los objetos siguientes se exportan para cambiar los comportamientos predeterminados de otros objetos y administrar certificados, almacenes de certificados y mensajes.</span><span class="sxs-lookup"><span data-stu-id="d78c4-171">The following objects are exported to change default behaviors of other objects and to manage certificates, certificate stores, and messages.</span></span>



| <span data-ttu-id="d78c4-172">Object</span><span class="sxs-lookup"><span data-stu-id="d78c4-172">Object</span></span>                                         | <span data-ttu-id="d78c4-173">Descripción</span><span class="sxs-lookup"><span data-stu-id="d78c4-173">Description</span></span>                                                                                                                                     |
|------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d78c4-174">**Algoritmo**</span><span class="sxs-lookup"><span data-stu-id="d78c4-174">**Algorithm**</span></span>](algorithm.md)                 | <span data-ttu-id="d78c4-175">Establece el algoritmo y la [*longitud de clave*](../secgloss/k-gly.md) que se van a usar en las operaciones criptográficas.</span><span class="sxs-lookup"><span data-stu-id="d78c4-175">Sets the algorithm and [*key length*](../secgloss/k-gly.md) to be used in cryptographic operations.</span></span> |
| [<span data-ttu-id="d78c4-176">**Atributo**</span><span class="sxs-lookup"><span data-stu-id="d78c4-176">**Attribute**</span></span>](attribute.md)                 | <span data-ttu-id="d78c4-177">Proporciona una sola parte de la información agregada sobre una firma, como la hora de firma.</span><span class="sxs-lookup"><span data-stu-id="d78c4-177">Provides a single piece of added information about a signature, such as the time of signing.</span></span>                                                    |
| [<span data-ttu-id="d78c4-178">**Atributos**</span><span class="sxs-lookup"><span data-stu-id="d78c4-178">**Attributes**</span></span>](attributes.md)               | <span data-ttu-id="d78c4-179">Colección de objetos de [**atributo**](attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="d78c4-179">Collection of [**Attribute**](attribute.md) objects.</span></span>                                                                                           |
| [<span data-ttu-id="d78c4-180">**BasicConstraints**</span><span class="sxs-lookup"><span data-stu-id="d78c4-180">**BasicConstraints**</span></span>](basicconstraints.md)   | <span data-ttu-id="d78c4-181">Proporciona acceso de solo lectura a las restricciones básicas de los usos de un certificado.</span><span class="sxs-lookup"><span data-stu-id="d78c4-181">Provides read-only access to basic constraints on the uses of a certificate.</span></span>                                                                    |
| [<span data-ttu-id="d78c4-182">**EKU**</span><span class="sxs-lookup"><span data-stu-id="d78c4-182">**EKU**</span></span>](eku.md)                             | <span data-ttu-id="d78c4-183">Proporciona acceso a las propiedades EKU de los certificados.</span><span class="sxs-lookup"><span data-stu-id="d78c4-183">Provides access to EKU properties of certificates.</span></span>                                                                                              |
| [<span data-ttu-id="d78c4-184">**EKU**</span><span class="sxs-lookup"><span data-stu-id="d78c4-184">**EKUs**</span></span>](ekus.md)                           | <span data-ttu-id="d78c4-185">Colección de objetos [**EKU**](eku.md) .</span><span class="sxs-lookup"><span data-stu-id="d78c4-185">Collection of [**EKU**](eku.md) objects.</span></span>                                                                                                       |
| [<span data-ttu-id="d78c4-186">**EncodedData**</span><span class="sxs-lookup"><span data-stu-id="d78c4-186">**EncodedData**</span></span>](encodeddata.md)             | <span data-ttu-id="d78c4-187">Representa un bloque de datos codificados.</span><span class="sxs-lookup"><span data-stu-id="d78c4-187">Represents a block of encoded data.</span></span>                                                                                                             |
| [<span data-ttu-id="d78c4-188">**ExtendedKeyUsage**</span><span class="sxs-lookup"><span data-stu-id="d78c4-188">**ExtendedKeyUsage**</span></span>](extendedkeyusage.md)   | <span data-ttu-id="d78c4-189">Proporciona acceso de solo lectura a las propiedades de uso mejorado de clave de los certificados.</span><span class="sxs-lookup"><span data-stu-id="d78c4-189">Provides read-only access to the extended key usage properties of certificates.</span></span>                                                                 |
| [<span data-ttu-id="d78c4-190">**HashedData**</span><span class="sxs-lookup"><span data-stu-id="d78c4-190">**HashedData**</span></span>](hasheddata.md)               | <span data-ttu-id="d78c4-191">Proporciona funcionalidad para aplicar un algoritmo hash a una cadena.</span><span class="sxs-lookup"><span data-stu-id="d78c4-191">Provides functionality for applying a hash algorithm to a string.</span></span>                                                                               |
| [<span data-ttu-id="d78c4-192">**KeyUsage**</span><span class="sxs-lookup"><span data-stu-id="d78c4-192">**KeyUsage**</span></span>](keyusage.md)                   | <span data-ttu-id="d78c4-193">Proporciona acceso de solo lectura a las propiedades de uso de claves de los certificados.</span><span class="sxs-lookup"><span data-stu-id="d78c4-193">Provides read-only access to key usage properties of certificates.</span></span>                                                                              |
| [<span data-ttu-id="d78c4-194">**NoticeNumbers**</span><span class="sxs-lookup"><span data-stu-id="d78c4-194">**NoticeNumbers**</span></span>](noticenumbers.md)         | <span data-ttu-id="d78c4-195">Representa una colección de objetos de [**extensión**](extension.md) .</span><span class="sxs-lookup"><span data-stu-id="d78c4-195">Represents a collection of [**Extension**](extension.md) objects.</span></span>                                                                              |
| [<span data-ttu-id="d78c4-196">**OID**</span><span class="sxs-lookup"><span data-stu-id="d78c4-196">**OID**</span></span>](oid.md)                             | <span data-ttu-id="d78c4-197">Representa un identificador de objeto que usan varias propiedades de CAPICOM.</span><span class="sxs-lookup"><span data-stu-id="d78c4-197">Represents an object identifier that is used by several CAPICOM properties.</span></span>                                                                     |
| [<span data-ttu-id="d78c4-198">**OID**</span><span class="sxs-lookup"><span data-stu-id="d78c4-198">**OIDs**</span></span>](oids.md)                           | <span data-ttu-id="d78c4-199">Representa una colección de objetos [**OID**](oid.md) .</span><span class="sxs-lookup"><span data-stu-id="d78c4-199">Represents a collection of [**OID**](oid.md) objects.</span></span>                                                                                          |
| [<span data-ttu-id="d78c4-200">**PolicyInformation**</span><span class="sxs-lookup"><span data-stu-id="d78c4-200">**PolicyInformation**</span></span>](policyinformation.md) | <span data-ttu-id="d78c4-201">Proporciona acceso a los OID de directiva de una extensión.</span><span class="sxs-lookup"><span data-stu-id="d78c4-201">Provides access to the policy OIDs of an extension.</span></span>                                                                                             |
| [<span data-ttu-id="d78c4-202">**Qualifier**</span><span class="sxs-lookup"><span data-stu-id="d78c4-202">**Qualifier**</span></span>](qualifier.md)                 | <span data-ttu-id="d78c4-203">Representa un puntero de informe de prácticas de certificación (CPS) o el calificador de aviso de usuario.</span><span class="sxs-lookup"><span data-stu-id="d78c4-203">Represents a Certification Practice Statement (CPS) pointer or user notice qualifier.</span></span>                                                           |
| [<span data-ttu-id="d78c4-204">**Calificadores**</span><span class="sxs-lookup"><span data-stu-id="d78c4-204">**Qualifiers**</span></span>](qualifiers.md)               | <span data-ttu-id="d78c4-205">Representa una colección de calificadores.</span><span class="sxs-lookup"><span data-stu-id="d78c4-205">Represents a collection of qualifiers.</span></span>                                                                                                          |
| [<span data-ttu-id="d78c4-206">**Configuración**</span><span class="sxs-lookup"><span data-stu-id="d78c4-206">**Settings**</span></span>](settings.md)                   | <span data-ttu-id="d78c4-207">Habilita o deshabilita los cuadros de diálogo para solicitar la identidad del remitente o del remitente si no se especifica esa identidad.</span><span class="sxs-lookup"><span data-stu-id="d78c4-207">Enables or disables dialog boxes to prompt for signer or sender identity if that identity is not specified.</span></span>                                     |
| [<span data-ttu-id="d78c4-208">**Sectores públicos**</span><span class="sxs-lookup"><span data-stu-id="d78c4-208">**Utilities**</span></span>](utilities.md)                 | <span data-ttu-id="d78c4-209">Proporciona funcionalidad para las tareas comunes.</span><span class="sxs-lookup"><span data-stu-id="d78c4-209">Provides functionality for common tasks.</span></span>                                                                                                        |



 

## <a name="certificate-enrollment-objects"></a><span data-ttu-id="d78c4-210">Objetos de inscripción de certificados</span><span class="sxs-lookup"><span data-stu-id="d78c4-210">Certificate Enrollment Objects</span></span>

<span data-ttu-id="d78c4-211">El siguiente objeto se usa para la inscripción de certificados.</span><span class="sxs-lookup"><span data-stu-id="d78c4-211">The following object is used for certificate enrollment.</span></span>



| <span data-ttu-id="d78c4-212">Object</span><span class="sxs-lookup"><span data-stu-id="d78c4-212">Object</span></span>                     | <span data-ttu-id="d78c4-213">Descripción</span><span class="sxs-lookup"><span data-stu-id="d78c4-213">Description</span></span>                                                                                                                                      |
|----------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d78c4-214">[**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="d78c4-214">[**CEnroll**](/previous-versions/windows/desktop/legacy/aa376007(v=vs.85))</span></span> | <span data-ttu-id="d78c4-215">Objeto que representa el control de inscripción de certificados.</span><span class="sxs-lookup"><span data-stu-id="d78c4-215">Object that represents the Certificate Enrollment Control.</span></span> <span data-ttu-id="d78c4-216">Se utiliza principalmente al programar en Visual Basic u otro lenguaje de automatización.</span><span class="sxs-lookup"><span data-stu-id="d78c4-216">It is primarily used when programming in Visual Basic or another Automation language.</span></span> |



 

 

 
