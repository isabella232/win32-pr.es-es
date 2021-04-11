---
description: Un certificado X.509 versión 3 contiene los campos definidos en la versión 1 y la versión 2, y además agrega extensiones de certificado. En el ejemplo siguiente se muestra la sintaxis ASN. 1 de las extensiones de certificado.
ms.assetid: ca8df7a4-caa4-4fe7-81a8-8fce372454f4
title: Extensiones de la versión 3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee23ce35ba7031a1a9f7a2c9caa79fd955ccbe2d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276805"
---
# <a name="version-3-extensions"></a><span data-ttu-id="30b0d-104">Extensiones de la versión 3</span><span class="sxs-lookup"><span data-stu-id="30b0d-104">Version 3 Extensions</span></span>

<span data-ttu-id="30b0d-105">Un certificado X.509 versión 3 contiene los campos definidos en la versión 1 y la versión 2, y además agrega extensiones de certificado.</span><span class="sxs-lookup"><span data-stu-id="30b0d-105">An X.509 version 3 certificate contains the fields defined in version 1 and version 2 and adds certificate extensions.</span></span> <span data-ttu-id="30b0d-106">En el ejemplo siguiente se muestra la sintaxis ASN. 1 de las extensiones de certificado.</span><span class="sxs-lookup"><span data-stu-id="30b0d-106">The ASN.1 syntax of certificate extensions is shown in the following example.</span></span>

``` syntax
---------------------------------------------------------------------
-- Extensions (beginning with version 3).
---------------------------------------------------------------------
Extensions ::= SEQUENCE OF Extension

Extension ::= SEQUENCE 
{
  Id                  OBJECT IDENTIFIER,
  critical            BOOLEAN DEFAULT FALSE,
  extnValue           OCTET STRING
}
```

<span data-ttu-id="30b0d-107">En la tabla siguiente se enumeran las extensiones estándar de la versión 3 y sus identificadores de objeto (OID).</span><span class="sxs-lookup"><span data-stu-id="30b0d-107">The standard version 3 extensions and their object identifiers (OIDs) are listed in the following table.</span></span> <span data-ttu-id="30b0d-108">Microsoft los admite e incluye extensiones personalizadas adicionales.</span><span class="sxs-lookup"><span data-stu-id="30b0d-108">Microsoft supports these and includes additional custom extensions.</span></span> <span data-ttu-id="30b0d-109">Para obtener más información, vea [extensiones](extensions.md).</span><span class="sxs-lookup"><span data-stu-id="30b0d-109">For more information, see [Extensions](extensions.md).</span></span>

| <span data-ttu-id="30b0d-110">Extensión</span><span class="sxs-lookup"><span data-stu-id="30b0d-110">Extension</span></span>                                         | <span data-ttu-id="30b0d-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="30b0d-111">Description</span></span>                                                                                                                                                                                              |
|---------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30b0d-112">Identificador de clave de entidad (2.5.29.19)</span><span class="sxs-lookup"><span data-stu-id="30b0d-112">Authority Key Identifier(2.5.29.19)</span></span><br/>    | <span data-ttu-id="30b0d-113">Identifica la clave pública de la entidad de certificación (CA) correspondiente a la clave privada de CA utilizada para firmar el certificado.</span><span class="sxs-lookup"><span data-stu-id="30b0d-113">Identifies the certification authority (CA) public key that corresponds to the CA private key used to sign the certificate.</span></span>                                                                              |
| <span data-ttu-id="30b0d-114">Restricciones básicas (2.5.29.35)</span><span class="sxs-lookup"><span data-stu-id="30b0d-114">Basic Constraints(2.5.29.35)</span></span><br/>           | <span data-ttu-id="30b0d-115">Especifica si la entidad se puede utilizar como una CA y, en caso afirmativo, el número de CA subordinadas que pueden existir por debajo en la cadena de certificados.</span><span class="sxs-lookup"><span data-stu-id="30b0d-115">Specifies whether the entity can be used as a CA and, if so, the number of subordinate CAs that can exist beneath it in the certificate chain.</span></span>                                                           |
| <span data-ttu-id="30b0d-116">Directivas de certificado (2.5.29.32)</span><span class="sxs-lookup"><span data-stu-id="30b0d-116">Certificate Policies(2.5.29.32)</span></span><br/>        | <span data-ttu-id="30b0d-117">Especifica las directivas con las que se ha emitido el certificado y los fines para los que se puede utilizar.</span><span class="sxs-lookup"><span data-stu-id="30b0d-117">Specifies the policies under which the certificate has been issued and the purposes for which it can be used.</span></span>                                                                                            |
| <span data-ttu-id="30b0d-118">Puntos de distribución de CRL (2.5.29.31)</span><span class="sxs-lookup"><span data-stu-id="30b0d-118">CRL Distribution Points(2.5.29.31)</span></span><br/>     | <span data-ttu-id="30b0d-119">Contiene el URI de la [*lista de revocación de certificados*](/windows/desktop/SecGloss/c-gly) (CRL) base.</span><span class="sxs-lookup"><span data-stu-id="30b0d-119">Contains the URI of the base [*certificate revocation list*](/windows/desktop/SecGloss/c-gly) (CRL).</span></span>                                  |
| <span data-ttu-id="30b0d-120">Uso mejorado de clave (2.5.29.46)</span><span class="sxs-lookup"><span data-stu-id="30b0d-120">Enhanced Key Usage(2.5.29.46)</span></span><br/>          | <span data-ttu-id="30b0d-121">Especifica la manera en que se puede utilizar la clave pública contenida en el certificado.</span><span class="sxs-lookup"><span data-stu-id="30b0d-121">Specifies the manner in which the public key contained in the certificate can be used.</span></span>                                                                                                                   |
| <span data-ttu-id="30b0d-122">Nombre alternativo del emisor (2.5.29.8)</span><span class="sxs-lookup"><span data-stu-id="30b0d-122">Issuer Alternative Name(2.5.29.8)</span></span><br/>      | <span data-ttu-id="30b0d-123">Especifica una o más formas de nombre alternativas para el emisor de la solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="30b0d-123">Specifies one or more alternative name forms for the issuer of the certificate request.</span></span>                                                                                                                  |
| <span data-ttu-id="30b0d-124">Uso de la clave (2.5.29.15)</span><span class="sxs-lookup"><span data-stu-id="30b0d-124">Key Usage(2.5.29.15)</span></span><br/>                   | <span data-ttu-id="30b0d-125">Especifica restricciones en las operaciones que puede realizar la clave pública contenida en el certificado.</span><span class="sxs-lookup"><span data-stu-id="30b0d-125">Specifies restrictions on the operations that can be performed by the public key contained in the certificate.</span></span>                                                                                           |
| <span data-ttu-id="30b0d-126">Restricciones de nombres (2.5.29.30)</span><span class="sxs-lookup"><span data-stu-id="30b0d-126">Name Constraints(2.5.29.30)</span></span><br/>            | <span data-ttu-id="30b0d-127">Especifica el espacio de nombres en el que deben encontrarse todos los nombres de firmantes en una jerarquía de certificados.</span><span class="sxs-lookup"><span data-stu-id="30b0d-127">Specifies the namespace within which all subject names in a certificate hierarchy must be located.</span></span> <span data-ttu-id="30b0d-128">La extensión solo se utiliza en un certificado de CA.</span><span class="sxs-lookup"><span data-stu-id="30b0d-128">The extension is used only in a CA certificate.</span></span>                                                       |
| <span data-ttu-id="30b0d-129">Restricciones de directivas (2.5.29.36)</span><span class="sxs-lookup"><span data-stu-id="30b0d-129">Policy Constraints(2.5.29.36)</span></span><br/>          | <span data-ttu-id="30b0d-130">Restringen la validación de rutas prohibiendo la asignación de directivas o exigiendo que cada certificado de la jerarquía contenga un identificador de directiva aceptable.</span><span class="sxs-lookup"><span data-stu-id="30b0d-130">Constrains path validation by prohibiting policy mapping or by requiring that each certificate in the hierarchy contain an acceptable policy identifier.</span></span> <span data-ttu-id="30b0d-131">La extensión solo se utiliza en un certificado de CA.</span><span class="sxs-lookup"><span data-stu-id="30b0d-131">The extension is used only in a CA certificate.</span></span> |
| <span data-ttu-id="30b0d-132">Asignaciones de directivas (2.5.29.33)</span><span class="sxs-lookup"><span data-stu-id="30b0d-132">Policy Mappings(2.5.29.33)</span></span><br/>             | <span data-ttu-id="30b0d-133">Especifica las directivas de una CA subordinada correspondientes a directivas de la CA emisora.</span><span class="sxs-lookup"><span data-stu-id="30b0d-133">Specifies the policies in a subordinate CA that correspond to policies in the issuing CA.</span></span>                                                                                                                |
| <span data-ttu-id="30b0d-134">Período de uso de clave privada (2.5.29.16)</span><span class="sxs-lookup"><span data-stu-id="30b0d-134">Private Key Usage Period(2.5.29.16)</span></span><br/>    | <span data-ttu-id="30b0d-135">Especifica un período de validez distinto para la clave privada que para el certificado con el que la clave privada está asociada.</span><span class="sxs-lookup"><span data-stu-id="30b0d-135">Specifies a different validity period for the private key than for the certificate with which the private key is associated.</span></span>                                                                             |
| <span data-ttu-id="30b0d-136">Nombre alternativo del firmante (2.5.29.17)</span><span class="sxs-lookup"><span data-stu-id="30b0d-136">Subject Alternative Name(2.5.29.17)</span></span><br/>    | <span data-ttu-id="30b0d-137">Especifica una o más formas de nombre alternativas para el firmante de la solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="30b0d-137">Specifies one or more alternative name forms for the subject of the certificate request.</span></span> <span data-ttu-id="30b0d-138">Algunos ejemplos de formas alternativas son direcciones de correo electrónico, nombres DNS, direcciones IP y URI.</span><span class="sxs-lookup"><span data-stu-id="30b0d-138">Example alternative forms include email addresses, DNS names, IP addresses, and URIs.</span></span>                           |
| <span data-ttu-id="30b0d-139">Atributos de directorio de asunto (2.5.29.9)</span><span class="sxs-lookup"><span data-stu-id="30b0d-139">Subject Directory Attributes(2.5.29.9)</span></span><br/> | <span data-ttu-id="30b0d-140">Contiene atributos de identificación, como la nacionalidad del firmante del certificado.</span><span class="sxs-lookup"><span data-stu-id="30b0d-140">Conveys identification attributes such as the nationality of the certificate subject.</span></span> <span data-ttu-id="30b0d-141">El valor de extensión es una secuencia de pares de valores OID.</span><span class="sxs-lookup"><span data-stu-id="30b0d-141">The extension value is a sequence of OID-value pairs.</span></span>                                                              |
| <span data-ttu-id="30b0d-142">Identificador de clave de sujeto (2.5.29.14)</span><span class="sxs-lookup"><span data-stu-id="30b0d-142">Subject Key Identifier(2.5.29.14)</span></span><br/>      | <span data-ttu-id="30b0d-143">Diferencia entre varias claves públicas de las que el firmante del certificado es titular.</span><span class="sxs-lookup"><span data-stu-id="30b0d-143">Differentiates between multiple public keys held by the certificate subject.</span></span> <span data-ttu-id="30b0d-144">El valor de extensión suele ser un hash SHA-1 de la clave.</span><span class="sxs-lookup"><span data-stu-id="30b0d-144">The extension value is typically a SHA-1 hash of the key.</span></span>                                                                   |



 

## <a name="related-topics"></a><span data-ttu-id="30b0d-145">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="30b0d-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="30b0d-146">Campos básicos</span><span class="sxs-lookup"><span data-stu-id="30b0d-146">Basic Fields</span></span>](about-basic-fields.md)
</dt> <dt>

[<span data-ttu-id="30b0d-147">Campos de la versión 2</span><span class="sxs-lookup"><span data-stu-id="30b0d-147">Version 2 Fields</span></span>](about-version-2-fields.md)
</dt> <dt>

[<span data-ttu-id="30b0d-148">Certificados de clave pública X. 509</span><span class="sxs-lookup"><span data-stu-id="30b0d-148">X.509 Public Key Certificates</span></span>](about-x-509-public-key-certificates.md)
</dt> </dl>

 

