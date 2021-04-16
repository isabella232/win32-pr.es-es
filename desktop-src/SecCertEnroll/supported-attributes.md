---
description: La API de inscripción de certificados admite los siguientes atributos. Puede crear un atributo individual mediante la interfaz correspondiente identificada en cada una de las secciones siguientes.
ms.assetid: e14fd472-1974-4ad2-b35a-3ab58ba0d707
title: Atributos compatibles
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3bfff5785a0b891e98e6d78d59b4688e2d5c11a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686876"
---
# <a name="supported-attributes"></a><span data-ttu-id="6ae0e-104">Atributos compatibles</span><span class="sxs-lookup"><span data-stu-id="6ae0e-104">Supported Attributes</span></span>

<span data-ttu-id="6ae0e-105">La API de inscripción de certificados admite los siguientes atributos.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-105">The Certificate Enrollment API supports the following attributes.</span></span> <span data-ttu-id="6ae0e-106">Puede crear un atributo individual mediante la interfaz correspondiente identificada en cada una de las secciones siguientes.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-106">You can create an individual attribute by using the corresponding interface identified in each of the following sections.</span></span>

## <a name="clientid"></a><span data-ttu-id="6ae0e-107">ClientId</span><span class="sxs-lookup"><span data-stu-id="6ae0e-107">ClientId</span></span>

<span data-ttu-id="6ae0e-108">La interfaz [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) se puede utilizar para definir un atributo que contiene información sobre el equipo cliente que envió la solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-108">The [**IX509AttributeClientId**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid) interface can be used to define an attribute that contains information about the client computer that sent the certificate request.</span></span> <span data-ttu-id="6ae0e-109">La información se puede usar para el diagnóstico.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-109">The information can be used for diagnostics.</span></span>

<span data-ttu-id="6ae0e-110">**Se aplica a:** \#Solicitud PKCS 10 o CMC.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-110">**Applies To:** PKCS \#10 or CMC request.</span></span>

<span data-ttu-id="6ae0e-111">**OID:** \_ \_ Información del cliente de solicitud XCN OID \_ \_ (1.3.6.1.4.1.311.21.20)</span><span class="sxs-lookup"><span data-stu-id="6ae0e-111">**OID:** XCN\_OID\_REQUEST\_CLIENT\_INFO (1.3.6.1.4.1.311.21.20)</span></span>

## <a name="extensions"></a><span data-ttu-id="6ae0e-112">Extensiones</span><span class="sxs-lookup"><span data-stu-id="6ae0e-112">Extensions</span></span>

<span data-ttu-id="6ae0e-113">La interfaz [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) se puede usar para definir un conjunto de extensiones de certificado X. 509 versión 3.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-113">The [**IX509AttributeExtensions**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions) interface can be used to define a set of X.509 version 3 certificate extensions.</span></span> <span data-ttu-id="6ae0e-114">Se admiten las siguientes extensiones.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-114">The following extensions are supported.</span></span> <span data-ttu-id="6ae0e-115">Para obtener más información, vea el tema interfaces de extensión.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-115">For more information, see the Extension Interfaces topic.</span></span>



| <span data-ttu-id="6ae0e-116">Extensión</span><span class="sxs-lookup"><span data-stu-id="6ae0e-116">Extension</span></span>              | <span data-ttu-id="6ae0e-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="6ae0e-117">Description</span></span>                                                                                                                                                                                                                      |
|------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6ae0e-118">AlternativeNames</span><span class="sxs-lookup"><span data-stu-id="6ae0e-118">AlternativeNames</span></span>       | <span data-ttu-id="6ae0e-119">Contiene una o varias formas de nombre alternativo del emisor asociado al certificado.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-119">Contains one or more alternative name forms of the issuer associated with the certificate.</span></span>                                                                                                                                       |
| <span data-ttu-id="6ae0e-120">AuthorityKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="6ae0e-120">AuthorityKeyIdentifier</span></span> | <span data-ttu-id="6ae0e-121">Contiene un identificador de clave único para diferenciar entre varias claves de firma de certificado de la entidad de [*certificación*](/windows/desktop/SecGloss/c-gly) (CA).</span><span class="sxs-lookup"><span data-stu-id="6ae0e-121">Contains a unique key identifier to differentiate between multiple certificate signing keys of the [*certification authority*](/windows/desktop/SecGloss/c-gly) (CA).</span></span> |
| <span data-ttu-id="6ae0e-122">BasicConstraints</span><span class="sxs-lookup"><span data-stu-id="6ae0e-122">BasicConstraints</span></span>       | <span data-ttu-id="6ae0e-123">Indica si el sujeto puede actuar como CA.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-123">Indicates whether the subject can act as a CA.</span></span>                                                                                                                                                                                   |
| <span data-ttu-id="6ae0e-124">CertificatePolicies</span><span class="sxs-lookup"><span data-stu-id="6ae0e-124">CertificatePolicies</span></span>    | <span data-ttu-id="6ae0e-125">Identifica las directivas y la información opcional del calificador asociada con el certificado.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-125">Identifies the policies and optional qualifier information associated with the certificate.</span></span>                                                                                                                                      |
| <span data-ttu-id="6ae0e-126">MSApplicationPolicies</span><span class="sxs-lookup"><span data-stu-id="6ae0e-126">MSApplicationPolicies</span></span>  | <span data-ttu-id="6ae0e-127">Identifica uno o más usos para el certificado.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-127">Identifies one or more uses for the certificate.</span></span> <span data-ttu-id="6ae0e-128">Esta extensión es similar a la extensión campo EnhancedKeyUsage, pero está definida por Microsoft.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-128">This extension is similar to the EnhancedKeyUsage extension but is Microsoft-defined.</span></span>                                                                                           |
| <span data-ttu-id="6ae0e-129">Campo EnhancedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="6ae0e-129">EnhancedKeyUsage</span></span>       | <span data-ttu-id="6ae0e-130">Identifica uno o más usos de la clave pública incluida en el certificado.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-130">Identifies one or more uses of the public key contained in the certificate.</span></span> <span data-ttu-id="6ae0e-131">La extensión uso mejorado de clave se puede usar además o en lugar de la extensión uso de clave.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-131">The enhanced key usage extension can be used in addition to or in place of the key usage extension.</span></span>                                                  |
| <span data-ttu-id="6ae0e-132">KeyUsage</span><span class="sxs-lookup"><span data-stu-id="6ae0e-132">KeyUsage</span></span>               | <span data-ttu-id="6ae0e-133">Identifica las restricciones de las operaciones que puede realizar la clave pública incluida en el certificado.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-133">Identifies restrictions on the operations that can be performed by the public key contained in the certificate.</span></span>                                                                                                                  |
| <span data-ttu-id="6ae0e-134">SmimeCapabilities</span><span class="sxs-lookup"><span data-stu-id="6ae0e-134">SmimeCapabilities</span></span>      | <span data-ttu-id="6ae0e-135">Notifica las capacidades de descifrado de un destinatario de correo electrónico al remitente de correo electrónico para que el remitente pueda elegir el algoritmo simétrico más seguro compatible con ambas partes.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-135">Reports the decryption capabilities of an email recipient to the email sender to enable the sender to choose the most secure symmetric algorithm supported by both parties.</span></span>                                                      |
| <span data-ttu-id="6ae0e-136">SubjectKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="6ae0e-136">SubjectKeyIdentifier</span></span>   | <span data-ttu-id="6ae0e-137">Contiene un identificador de clave único que se puede utilizar para diferenciar entre varias claves de firma asociadas al propietario del certificado.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-137">Contains a unique key identifier that can be used to differentiate between multiple signing keys associated with the certificate owner.</span></span>                                                                                          |
| <span data-ttu-id="6ae0e-138">Plantilla</span><span class="sxs-lookup"><span data-stu-id="6ae0e-138">Template</span></span>               | <span data-ttu-id="6ae0e-139">Identifica la plantilla que se va a usar al emitir o renovar un certificado.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-139">Identifies the template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="6ae0e-140">La extensión contiene el identificador de objeto (OID) de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-140">The extension contains the object identifier (OID) of the template.</span></span>                                                                                       |
| <span data-ttu-id="6ae0e-141">TemplateName</span><span class="sxs-lookup"><span data-stu-id="6ae0e-141">TemplateName</span></span>           | <span data-ttu-id="6ae0e-142">Identifica la plantilla que se va a usar al emitir o renovar un certificado.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-142">Identifies the template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="6ae0e-143">La extensión contiene el nombre de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-143">The extension contains the name of the template.</span></span>                                                                                                          |



 

<span data-ttu-id="6ae0e-144">**Se aplica a:** \#Solicitud PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-144">**Applies To:** PKCS \#10 request.</span></span>

<span data-ttu-id="6ae0e-145">**OID:** XCN \_ OID \_ RSA \_ certExtensions (1.2.840.113549.1.9.14)</span><span class="sxs-lookup"><span data-stu-id="6ae0e-145">**OID:** XCN\_OID\_RSA\_certExtensions (1.2.840.113549.1.9.14)</span></span>

## <a name="archivekey"></a><span data-ttu-id="6ae0e-146">ArchiveKey</span><span class="sxs-lookup"><span data-stu-id="6ae0e-146">ArchiveKey</span></span>

<span data-ttu-id="6ae0e-147">La interfaz [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) se puede usar para definir un atributo que contenga una clave privada cifrada enviada a una CA para su archivado.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-147">The [**IX509AttributeArchiveKey**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey) interface can be used to define an attribute that contains an encrypted private key submitted to a CA for archiving.</span></span>

<span data-ttu-id="6ae0e-148">**Se aplica a:** Solicitud de CMC.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-148">**Applies To:** CMC request.</span></span>

<span data-ttu-id="6ae0e-149">**OID:** \_Atributo de \_ clave archivada XCN OID \_ \_ (1.3.6.1.4.1.311.21.13)</span><span class="sxs-lookup"><span data-stu-id="6ae0e-149">**OID:** XCN\_OID\_ARCHIVED\_KEY\_ATTR (1.3.6.1.4.1.311.21.13)</span></span>

## <a name="archivekeyhash"></a><span data-ttu-id="6ae0e-150">ArchiveKeyHash</span><span class="sxs-lookup"><span data-stu-id="6ae0e-150">ArchiveKeyHash</span></span>

<span data-ttu-id="6ae0e-151">La interfaz [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) se puede usar para definir un hash de la clave privada contenida en el atributo **ArchiveKey** .</span><span class="sxs-lookup"><span data-stu-id="6ae0e-151">The [**IX509AttributeArchiveKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash) interface can be used to define a hash of the private key contained in the **ArchiveKey** attribute.</span></span>

<span data-ttu-id="6ae0e-152">**Se aplica a:** Solicitud de CMC.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-152">**Applies To:** CMC request.</span></span>

<span data-ttu-id="6ae0e-153">**OID:** \_Hash de \_ clave cifrada XCN OID \_ \_ (1.3.6.1.4.1.311.21.21)</span><span class="sxs-lookup"><span data-stu-id="6ae0e-153">**OID:** XCN\_OID\_ENCRYPTED\_KEY\_HASH (1.3.6.1.4.1.311.21.21)</span></span>

## <a name="cspprovider"></a><span data-ttu-id="6ae0e-154">CspProvider</span><span class="sxs-lookup"><span data-stu-id="6ae0e-154">CspProvider</span></span>

<span data-ttu-id="6ae0e-155">La interfaz [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider) se puede utilizar para definir un atributo que contenga información sobre el [*proveedor de servicios criptográficos*](/windows/desktop/SecGloss/c-gly) (CSP) utilizado por el solicitante para las operaciones criptográficas.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-155">The [**IX509AttributeCspProvider**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider) interface can be used to define an attribute that contains information about the [*cryptographic service provider*](/windows/desktop/SecGloss/c-gly) (CSP) used by the requester for cryptographic operations.</span></span>

<span data-ttu-id="6ae0e-156">**Se aplica a:** \#Solicitud PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-156">**Applies To:** PKCS \#10 request.</span></span> <span data-ttu-id="6ae0e-157">Este atributo se crea automáticamente cuando se crea un objeto [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) .</span><span class="sxs-lookup"><span data-stu-id="6ae0e-157">This attribute is automatically created when you create an [**IX509CertificateRequestPkcs10**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509certificaterequestpkcs10) object.</span></span>

<span data-ttu-id="6ae0e-158">**OID:** Proveedor de CSP de inscripción de XCN \_ OID \_ \_ \_ (1.3.6.1.4.1.311.13.2.2)</span><span class="sxs-lookup"><span data-stu-id="6ae0e-158">**OID:** XCN\_OID\_ENROLLMENT\_CSP\_PROVIDER (1.3.6.1.4.1.311.13.2.2)</span></span>

## <a name="osversion"></a><span data-ttu-id="6ae0e-159">OSVersion</span><span class="sxs-lookup"><span data-stu-id="6ae0e-159">OSVersion</span></span>

<span data-ttu-id="6ae0e-160">La interfaz [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) se puede usar para crear un atributo que contenga información de versión sobre el sistema operativo del cliente.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-160">The [**IX509AttributeOSVersion**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion) interface can be used to create an attribute that contains version information about the client operating system.</span></span> <span data-ttu-id="6ae0e-161">La entidad de certificación puede usar la información para determinar el tipo de procesamiento que se va a aplicar al crear el certificado.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-161">The information can be used by the CA to determine the type of processing to apply when creating the certificate.</span></span>

<span data-ttu-id="6ae0e-162">**Se aplica a:** \#Solicitud PKCS 10 o CMC.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-162">**Applies To:** PKCS \#10 or CMC request.</span></span>

<span data-ttu-id="6ae0e-163">**OID:** \_ \_ Versión del sistema operativo OID de XCN \_ (1.3.6.1.4.1.311.13.2.3)</span><span class="sxs-lookup"><span data-stu-id="6ae0e-163">**OID:** XCN\_OID\_OS\_VERSION (1.3.6.1.4.1.311.13.2.3)</span></span>

## <a name="renewalcertificate"></a><span data-ttu-id="6ae0e-164">RenewalCertificate</span><span class="sxs-lookup"><span data-stu-id="6ae0e-164">RenewalCertificate</span></span>

<span data-ttu-id="6ae0e-165">La interfaz [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) se puede usar para crear un atributo que contenga el certificado que se va a renovar.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-165">The [**IX509AttributeRenewalCertificate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) interface can be used to create an attribute that contains the certificate being renewed.</span></span>

<span data-ttu-id="6ae0e-166">**Se aplica a:** \#Solicitud PKCS 10.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-166">**Applies To:** PKCS \#10 request.</span></span> <span data-ttu-id="6ae0e-167">Este atributo se crea automáticamente si se crea una \# solicitud PKCS 10 al iniciarla con el certificado que se va a renovar.</span><span class="sxs-lookup"><span data-stu-id="6ae0e-167">This attribute is automatically created if you create a PKCS \#10 request by initiating it with the certificate being renewed.</span></span>

<span data-ttu-id="6ae0e-168">**OID:** Certificado de renovación de OID de XCN \_ \_ \_ (1.3.6.1.4.1.311.13.1)</span><span class="sxs-lookup"><span data-stu-id="6ae0e-168">**OID:** XCN\_OID\_RENEWAL\_CERTIFICATE (1.3.6.1.4.1.311.13.1)</span></span>

 

 
