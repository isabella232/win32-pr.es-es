---
description: Puede usar la interfaz IX509Extension para definir una extensión arbitraria.
ms.assetid: 025447f4-98d0-4cb8-b546-4797b7e60722
title: Extensiones admitidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd55886b03cdea5783f918182c84382910510918
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103810273"
---
# <a name="supported-extensions"></a><span data-ttu-id="9e0cd-103">Extensiones admitidas</span><span class="sxs-lookup"><span data-stu-id="9e0cd-103">Supported Extensions</span></span>

<span data-ttu-id="9e0cd-104">Puede usar la interfaz [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) para definir una extensión arbitraria.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-104">You can use the [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension) interface to define an arbitrary extension.</span></span> <span data-ttu-id="9e0cd-105">La API de inscripción de certificados también proporciona interfaces derivadas de **IX509Extension** para que pueda crear fácilmente cualquiera de las extensiones más comunes.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-105">The Certificate Enrollment API also provides interfaces derived from **IX509Extension** to enable you to easily create any of the most common extensions.</span></span> <span data-ttu-id="9e0cd-106">En la lista siguiente se identifican las extensiones comunes que admiten las entidades de certificación de Microsoft, así como los identificadores de objeto e interfaces que se pueden usar para crearlas.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-106">The following list identifies the common extensions supported by Microsoft certification authorities, and the object identifiers and interfaces that you can use to create them.</span></span>

## <a name="alternativenames"></a><span data-ttu-id="9e0cd-107">AlternativeNames</span><span class="sxs-lookup"><span data-stu-id="9e0cd-107">AlternativeNames</span></span>

<span data-ttu-id="9e0cd-108">La extensión de nombres alternativos se puede usar para definir una o varias formas de nombres alternativos para el sujeto de la solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-108">The alternative names extension can be used to define one or more alternative name forms for the subject of the certificate request.</span></span> <span data-ttu-id="9e0cd-109">Algunos ejemplos de formas alternativas son direcciones de correo electrónico, nombres DNS, direcciones IP y URI.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-109">Example alternative forms include email addresses, DNS names, IP addresses, and URIs.</span></span>

<span data-ttu-id="9e0cd-110">**Interfaz:** [ **IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-110">**Interface:** [**IX509ExtensionAlternativeNames**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionalternativenames)</span></span>

<span data-ttu-id="9e0cd-111">**OID:** XCN \_ OID \_ Subject \_ ALT \_ nombre2 (2.5.29.17)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-111">**OID:** XCN\_OID\_SUBJECT\_ALT\_NAME2 (2.5.29.17)</span></span>

## <a name="authorityinformationaccess"></a><span data-ttu-id="9e0cd-112">AuthorityInformationAccess</span><span class="sxs-lookup"><span data-stu-id="9e0cd-112">AuthorityInformationAccess</span></span>

<span data-ttu-id="9e0cd-113">La extensión de acceso a la información de entidad de certificación identifica cómo obtener acceso a la información y los servicios de CA.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-113">The authority information access extension identifies how to access CA information and services.</span></span> <span data-ttu-id="9e0cd-114">El valor de extensión contiene una secuencia de URI.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-114">The extension value contains a sequence of URIs.</span></span>

<span data-ttu-id="9e0cd-115">**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-115">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="9e0cd-116">**OID:** XCN \_ OID \_ Authority \_ \_ Access Info Access (1.3.6.1.5.5.7.1.1)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-116">**OID:** XCN\_OID\_AUTHORITY\_INFO\_ACCESS (1.3.6.1.5.5.7.1.1)</span></span>

## <a name="authoritykeyidentifier"></a><span data-ttu-id="9e0cd-117">AuthorityKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="9e0cd-117">AuthorityKeyIdentifier</span></span>

<span data-ttu-id="9e0cd-118">La extensión de identificador de clave de entidad de certificación habilita la identificación de la clave pública de CA correspondiente a la clave privada de CA que firmó un certificado emitido.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-118">The authority key identifier extension enables identification of the CA public key that corresponds to the CA private key that signed an issued certificate.</span></span> <span data-ttu-id="9e0cd-119">Lo usa la creación de rutas de acceso de certificado en un servidor de Windows para buscar el certificado de CA.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-119">It is used by certificate path building software on a Windows server to find the CA certificate.</span></span> <span data-ttu-id="9e0cd-120">Cuando una CA emite un certificado, el valor de la extensión se establece igual a la extensión **SubjectKeyIdentifier** en el certificado de firma de la entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-120">When a CA issues a certificate, the extension value is set equal to the **SubjectKeyIdentifier** extension in the CA signing certificate.</span></span> <span data-ttu-id="9e0cd-121">Normalmente, el valor es un hash SHA-1 de la clave pública.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-121">The value is typically a SHA-1 hash of the public key.</span></span>

<span data-ttu-id="9e0cd-122">**Interfaz:** [ **IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-122">**Interface:** [**IX509ExtensionAuthorityKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionauthoritykeyidentifier)</span></span>

<span data-ttu-id="9e0cd-123">**OID:** XCN \_ OID \_ Authority \_ key \_ identificador2 (2.5.29.35)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-123">**OID:** XCN\_OID\_AUTHORITY\_KEY\_IDENTIFIER2 (2.5.29.35)</span></span>

## <a name="basicconstraints"></a><span data-ttu-id="9e0cd-124">BasicConstraints</span><span class="sxs-lookup"><span data-stu-id="9e0cd-124">BasicConstraints</span></span>

<span data-ttu-id="9e0cd-125">La extensión de restricciones básicas se puede usar para identificar si la entidad se puede usar como entidad de certificación (CA) y, si es así, el número de CA subordinadas que pueden existir debajo de ella en la cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-125">The basic constraints extension can be used to identify whether the entity can be used as a certification authority (CA) and, if so, the number of subordinate CAs that can exist beneath it in the certificate chain.</span></span>

<span data-ttu-id="9e0cd-126">**Interfaz:** [ **IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-126">**Interface:** [**IX509ExtensionBasicConstraints**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionbasicconstraints)</span></span>

<span data-ttu-id="9e0cd-127">**OID:** XCN \_ OID \_ Basic \_ CONSTRAINTS2 (2.5.29.19)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-127">**OID:** XCN\_OID\_BASIC\_CONSTRAINTS2 (2.5.29.19)</span></span>

## <a name="certificatepolicies"></a><span data-ttu-id="9e0cd-128">CertificatePolicies</span><span class="sxs-lookup"><span data-stu-id="9e0cd-128">CertificatePolicies</span></span>

<span data-ttu-id="9e0cd-129">La extensión de directivas de certificados se puede usar para identificar las directivas en las que se ha emitido el certificado y se pueden usar los propósitos para ello.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-129">The certificate policies extension can be used to identify the policies under which the certificate has been issued and the purposes for it can be used.</span></span> <span data-ttu-id="9e0cd-130">Se identifican mediante una colección de identificadores de objeto (OID).</span><span class="sxs-lookup"><span data-stu-id="9e0cd-130">These are identified by a collection of object identifiers (OIDs).</span></span> <span data-ttu-id="9e0cd-131">Las directivas se personalizan para los requisitos de una organización.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-131">Policies are customized for the requirements of an organization.</span></span>

<span data-ttu-id="9e0cd-132">**Interfaz:** [ **IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-132">**Interface:** [**IX509ExtensionCertificatePolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensioncertificatepolicies)</span></span>

<span data-ttu-id="9e0cd-133">**OID:** XCN \_ \_ directivas de certificado OID \_ (2.5.29.32)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-133">**OID:** XCN\_OID\_CERT\_POLICIES (2.5.29.32)</span></span>

## <a name="crldistributionpoints"></a><span data-ttu-id="9e0cd-134">CrlDistributionPoints</span><span class="sxs-lookup"><span data-stu-id="9e0cd-134">CrlDistributionPoints</span></span>

<span data-ttu-id="9e0cd-135">La extensión de puntos de distribución de lista de revocación de certificados (CRL) contiene el URI de la lista de revocación de certificados (CRL) base.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-135">The certificate revocation list (CRL) distribution points extension contains the URI of the base certificate revocation list (CRL).</span></span>

<span data-ttu-id="9e0cd-136">**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-136">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="9e0cd-137">**OID:** Puntos de distribución de CRL de XCN \_ OID \_ \_ \_ (2.5.29.31)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-137">**OID:** XCN\_OID\_CRL\_DIST\_POINTS (2.5.29.31)</span></span>

## <a name="enhancedkeyusage"></a><span data-ttu-id="9e0cd-138">Campo EnhancedKeyUsage</span><span class="sxs-lookup"><span data-stu-id="9e0cd-138">EnhancedKeyUsage</span></span>

<span data-ttu-id="9e0cd-139">La extensión uso mejorado de clave se puede usar para definir uno o más usos de la clave pública incluida en el certificado.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-139">The enhanced key usage extension can be used to define one or more uses of the public key contained in the certificate.</span></span>

<span data-ttu-id="9e0cd-140">**Interfaz:** [ **IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-140">**Interface:** [**IX509ExtensionEnhancedKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionenhancedkeyusage)</span></span>

<span data-ttu-id="9e0cd-141">**OID:** \_Uso mejorado de clave de XCN OID \_ \_ \_ (2.5.29.37)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-141">**OID:** XCN\_OID\_ENHANCED\_KEY\_USAGE (2.5.29.37)</span></span>

## <a name="freshestcrl"></a><span data-ttu-id="9e0cd-142">FreshestCRL</span><span class="sxs-lookup"><span data-stu-id="9e0cd-142">FreshestCRL</span></span>

<span data-ttu-id="9e0cd-143">La extensión CRL más reciente contiene el URI de la CRL delta.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-143">The freshest CRL extension contains the URI of the delta CRL.</span></span> <span data-ttu-id="9e0cd-144">Se usa la misma sintaxis ASN. 1 para esta extensión y la extensión **CrlDistributionPoints** .</span><span class="sxs-lookup"><span data-stu-id="9e0cd-144">The same ASN.1 syntax is used for this extension and the **CrlDistributionPoints** extension.</span></span>

<span data-ttu-id="9e0cd-145">**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-145">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="9e0cd-146">**OID:** CRL más reciente de XCN \_ OID \_ \_ (2.5.29.46)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-146">**OID:** XCN\_OID\_FRESHEST\_CRL (2.5.29.46)</span></span>

## <a name="keyusage"></a><span data-ttu-id="9e0cd-147">KeyUsage</span><span class="sxs-lookup"><span data-stu-id="9e0cd-147">KeyUsage</span></span>

<span data-ttu-id="9e0cd-148">La extensión uso de clave se puede usar para definir restricciones en las operaciones que puede realizar la clave pública incluida en el certificado.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-148">The key usage extension can be used to define restrictions on the operations that can be performed by the public key contained in the certificate.</span></span> <span data-ttu-id="9e0cd-149">Por ejemplo, puede especificar que la clave pública se use solo para crear una firma digital, firmar una lista de revocación de certificados (CRL) o cifrar otra clave.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-149">For example, you can specify that the public key be used only to create a digital signature, sign a certificate revocation list (CRL), or encrypt another key.</span></span>

<span data-ttu-id="9e0cd-150">**Interfaz:** [ **IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-150">**Interface:** [**IX509ExtensionKeyUsage**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionkeyusage)</span></span>

<span data-ttu-id="9e0cd-151">**OID:** Uso de la \_ clave XCN OID \_ \_ (2.5.29.15)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-151">**OID:** XCN\_OID\_KEY\_USAGE (2.5.29.15)</span></span>

## <a name="msapplicationpolicies"></a><span data-ttu-id="9e0cd-152">MSApplicationPolicies</span><span class="sxs-lookup"><span data-stu-id="9e0cd-152">MSApplicationPolicies</span></span>

<span data-ttu-id="9e0cd-153">Una aplicación puede usar la extensión de directivas de aplicación de Microsoft para filtrar los certificados en función del uso permitido.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-153">The Microsoft application policies extension can be used by an application to filter certificates on the basis of permitted use.</span></span> <span data-ttu-id="9e0cd-154">Los usos permitidos se identifican mediante OID.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-154">Permitted uses are identified by OIDs.</span></span> <span data-ttu-id="9e0cd-155">Esta extensión es similar a la extensión **campo EnhancedKeyUsage** , pero con una semántica más estricta aplicada a la CA primaria.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-155">This extension is similar to the **EnhancedKeyUsage** extension but with stricter semantics applied to the parent CA.</span></span> <span data-ttu-id="9e0cd-156">La extensión es específica de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-156">The extension is Microsoft specific.</span></span>

<span data-ttu-id="9e0cd-157">**Interfaz:** [ **IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-157">**Interface:** [**IX509ExtensionMSApplicationPolicies**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionmsapplicationpolicies)</span></span>

<span data-ttu-id="9e0cd-158">**OID:** \_Directivas de certificados de aplicación XCN OID \_ \_ \_ (1.3.6.1.4.1.311.21.10)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-158">**OID:** XCN\_OID\_APPLICATION\_CERT\_POLICIES (1.3.6.1.4.1.311.21.10)</span></span>

## <a name="nameconstraints"></a><span data-ttu-id="9e0cd-159">NameConstraints</span><span class="sxs-lookup"><span data-stu-id="9e0cd-159">NameConstraints</span></span>

<span data-ttu-id="9e0cd-160">La extensión de restricciones de nombres se usa para identificar el espacio de nombres en el que se deben encontrar todos los nombres de asunto de los certificados en una jerarquía de certificados.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-160">The name constraints extension is used to identify the namespace within which all subject names of certificates in a certificate hierarchy must be located.</span></span> <span data-ttu-id="9e0cd-161">La extensión solo se utiliza en un certificado de CA.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-161">The extension is used only in a CA certificate.</span></span>

<span data-ttu-id="9e0cd-162">**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-162">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="9e0cd-163">**OID:** RESTRICCIONES de nombre de OID de XCN \_ \_ \_ (2.5.29.30)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-163">**OID:** XCN\_OID\_NAME\_CONSTRAINTS (2.5.29.30)</span></span>

## <a name="policyconstraints"></a><span data-ttu-id="9e0cd-164">PolicyConstraints</span><span class="sxs-lookup"><span data-stu-id="9e0cd-164">PolicyConstraints</span></span>

<span data-ttu-id="9e0cd-165">La extensión de restricciones de Directiva se agrega a los certificados de CA para restringir la validación de la ruta de acceso mediante la prohibición de la asignación de directivas o la exigencia de que cada certificado de la jerarquía contenga un identificador de directiva aceptable.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-165">The policy constraints extension is added to CA certificates to constrain path validation by prohibiting policy mapping or by requiring that each certificate in the hierarchy contain an acceptable policy identifier.</span></span>

<span data-ttu-id="9e0cd-166">**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-166">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="9e0cd-167">**OID:** RESTRICCIONES de la \_ Directiva XCN OID \_ \_ (2.5.29.36)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-167">**OID:** XCN\_OID\_POLICY\_CONSTRAINTS (2.5.29.36)</span></span>

## <a name="policymappings"></a><span data-ttu-id="9e0cd-168">PolicyMappings</span><span class="sxs-lookup"><span data-stu-id="9e0cd-168">PolicyMappings</span></span>

<span data-ttu-id="9e0cd-169">La extensión de asignaciones de directivas se usa para identificar las directivas de una CA subordinada que se corresponden con las directivas de la CA emisora.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-169">The policy mappings extension is used to identify the policies in a subordinate CA that correspond to policies in the issuing CA.</span></span> <span data-ttu-id="9e0cd-170">El valor de extensión contiene una secuencia de asignaciones de CA emisora y de directiva de CA subordinada representadas por identificadores de objeto.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-170">The extension value contains a sequence of issuing CA and subordinate CA policy mappings represented by object identifiers.</span></span>

<span data-ttu-id="9e0cd-171">**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-171">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="9e0cd-172">**OID:** Asignaciones de directivas de XCN \_ OID \_ \_ (2.5.29.33)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-172">**OID:** XCN\_OID\_POLICY\_MAPPINGS (2.5.29.33)</span></span>

## <a name="privatekeyusageperiod"></a><span data-ttu-id="9e0cd-173">PrivateKeyUsagePeriod</span><span class="sxs-lookup"><span data-stu-id="9e0cd-173">PrivateKeyUsagePeriod</span></span>

<span data-ttu-id="9e0cd-174">La extensión de período de uso de clave privada se utiliza para especificar un período de validez diferente para la clave privada que para el certificado al que está asociada la clave.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-174">The private key usage period extension is used to specify a different validity period for the private key than for the certificate with which the key is associated.</span></span>

<span data-ttu-id="9e0cd-175">**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-175">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="9e0cd-176">**OID:** XCN \_ OID \_ PRIVATEKEY \_ período de uso \_ (2.5.29.16)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-176">**OID:** XCN\_OID\_PRIVATEKEY\_USAGE\_PERIOD (2.5.29.16)</span></span>

## <a name="smimecapabilities"></a><span data-ttu-id="9e0cd-177">SmimeCapabilities</span><span class="sxs-lookup"><span data-stu-id="9e0cd-177">SmimeCapabilities</span></span>

<span data-ttu-id="9e0cd-178">La extensión de funciones de extensiones seguras multipropósito de correo Internet (S/MIME) se puede usar para notificar las funciones de descifrado de un destinatario de correo electrónico al remitente del mensaje de correo electrónico para que el remitente pueda elegir el algoritmo de cifrado más seguro compatible con ambas partes.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-178">The Secure/Multipurpose Internet Mail Extensions (S/MIME) capabilities extension can be used to report an email recipient's decryption capabilities to the sender of the email message so that the sender can choose the most secure encryption algorithm supported by both parties.</span></span> <span data-ttu-id="9e0cd-179">El valor de extensión contiene una colección de OID de algoritmo de cifrado simétrico y una seguridad de cifrado opcional para cada uno.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-179">The extension value contains a collection of symmetric encryption algorithm OIDs and an optional encryption strength for each.</span></span>

<span data-ttu-id="9e0cd-180">**Interfaz:** [ **IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-180">**Interface:** [**IX509ExtensionSmimeCapabilities**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsmimecapabilities)</span></span>

<span data-ttu-id="9e0cd-181">**OID:** XCN \_ OID \_ RSA \_ SMIMECapabilities (1.2.840.113549.1.9.15)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-181">**OID:** XCN\_OID\_RSA\_SMIMECapabilities (1.2.840.113549.1.9.15)</span></span>

## <a name="subjectdirectoryattributes"></a><span data-ttu-id="9e0cd-182">SubjectDirectoryAttributes</span><span class="sxs-lookup"><span data-stu-id="9e0cd-182">SubjectDirectoryAttributes</span></span>

<span data-ttu-id="9e0cd-183">La extensión de atributos de directorio de asunto se puede usar para transmitir atributos de identificación, como la nacionalidad del firmante del certificado.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-183">The subject directory attributes extension can be used to convey identification attributes such as the nationality of the certificate subject.</span></span> <span data-ttu-id="9e0cd-184">El valor de extensión es una secuencia de pares de valores OID.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-184">The extension value is a sequence of OID-value pairs.</span></span>

<span data-ttu-id="9e0cd-185">**Interfaz:** [ **IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-185">**Interface:** [**IX509Extension**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extension)</span></span>

<span data-ttu-id="9e0cd-186">**OID:** XCN \_ OID de \_ objeto de firmante \_ \_ (2.5.29.9)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-186">**OID:** XCN\_OID\_SUBJECT\_DIR\_ATTRS (2.5.29.9)</span></span>

## <a name="subjectkeyidentifier"></a><span data-ttu-id="9e0cd-187">SubjectKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="9e0cd-187">SubjectKeyIdentifier</span></span>

<span data-ttu-id="9e0cd-188">La extensión del identificador de clave de sujeto se puede usar para diferenciar entre varias claves públicas retenidas por el sujeto del certificado.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-188">The subject key identifier extension can be used to differentiate between multiple public keys held by the certificate subject.</span></span> <span data-ttu-id="9e0cd-189">El valor de extensión suele ser un hash SHA-1 de la clave.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-189">The extension value is typically a SHA-1 hash of the key.</span></span>

<span data-ttu-id="9e0cd-190">**Interfaz:** [ **IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-190">**Interface:** [**IX509ExtensionSubjectKeyIdentifier**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensionsubjectkeyidentifier)</span></span>

<span data-ttu-id="9e0cd-191">**OID:** Identificador de clave de sujeto de XCN \_ OID \_ \_ \_ (2.5.29.14)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-191">**OID:** XCN\_OID\_SUBJECT\_KEY\_IDENTIFIER (2.5.29.14)</span></span>

## <a name="template"></a><span data-ttu-id="9e0cd-192">Plantilla</span><span class="sxs-lookup"><span data-stu-id="9e0cd-192">Template</span></span>

<span data-ttu-id="9e0cd-193">La extensión de plantilla se puede usar para identificar la plantilla de la versión 2 que se va a usar al emitir o renovar un certificado.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-193">The template extension can be used to identify the version 2 template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="9e0cd-194">El valor de la extensión contiene el OID de la plantilla y la información de versión opcional.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-194">The extension value contains the template OID and optional version information.</span></span> <span data-ttu-id="9e0cd-195">La extensión es específica de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-195">The extension is Microsoft specific.</span></span>

<span data-ttu-id="9e0cd-196">**Interfaz:** [ **IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-196">**Interface:** [**IX509ExtensionTemplate**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplate)</span></span>

<span data-ttu-id="9e0cd-197">**OID:** XCN \_ \_ plantilla de certificado OID \_ (1.3.6.1.4.1.311.21.7)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-197">**OID:** XCN\_OID\_CERTIFICATE\_TEMPLATE (1.3.6.1.4.1.311.21.7)</span></span>

## <a name="templatename"></a><span data-ttu-id="9e0cd-198">TemplateName</span><span class="sxs-lookup"><span data-stu-id="9e0cd-198">TemplateName</span></span>

<span data-ttu-id="9e0cd-199">La extensión de nombre de plantilla se puede usar para identificar la plantilla de la versión 1 que se va a usar al emitir o renovar un certificado.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-199">The template name extension can be used to identify the version 1 template to use when issuing or renewing a certificate.</span></span> <span data-ttu-id="9e0cd-200">El valor de la extensión contiene el nombre de la plantilla.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-200">The extension value contains the name of the template.</span></span> <span data-ttu-id="9e0cd-201">La extensión es específica de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="9e0cd-201">The extension is Microsoft specific.</span></span>

<span data-ttu-id="9e0cd-202">**Interfaz:** [ **IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-202">**Interface:** [**IX509ExtensionTemplateName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509extensiontemplatename)</span></span>

<span data-ttu-id="9e0cd-203">**OID:** XCN \_ OID \_ ENROLL \_ CERTTYPE \_ Extension (1.3.6.1.4.1.311.20.2)</span><span class="sxs-lookup"><span data-stu-id="9e0cd-203">**OID:** XCN\_OID\_ENROLL\_CERTTYPE\_EXTENSION (1.3.6.1.4.1.311.20.2)</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e0cd-204">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9e0cd-204">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e0cd-205">Extensiones</span><span class="sxs-lookup"><span data-stu-id="9e0cd-205">Extensions</span></span>](extensions.md)
</dt> </dl>

 

 



