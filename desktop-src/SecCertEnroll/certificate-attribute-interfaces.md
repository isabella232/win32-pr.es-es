---
description: Se pueden usar las siguientes interfaces para crear atributos de certificado.
ms.assetid: 3701f9b2-0857-45f0-b3ed-4f1b3db4d6d8
title: Interfaces de atributo de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 930f427ae6333084c8a180e5d227e4c24daa5426
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648197"
---
# <a name="certificate-attribute-interfaces"></a><span data-ttu-id="22210-103">Interfaces de atributo de certificado</span><span class="sxs-lookup"><span data-stu-id="22210-103">Certificate Attribute Interfaces</span></span>

<span data-ttu-id="22210-104">Se pueden usar las siguientes interfaces para crear atributos de certificado.</span><span class="sxs-lookup"><span data-stu-id="22210-104">The following interfaces can be used to create certificate attributes.</span></span>



| <span data-ttu-id="22210-105">Interfaz</span><span class="sxs-lookup"><span data-stu-id="22210-105">Interface</span></span>                                                                    | <span data-ttu-id="22210-106">Descripción</span><span class="sxs-lookup"><span data-stu-id="22210-106">Description</span></span>                                                                                                                                 |
|------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="22210-107">**ICryptAttribute**</span><span class="sxs-lookup"><span data-stu-id="22210-107">**ICryptAttribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute)                                   | <span data-ttu-id="22210-108">Representa un atributo criptográfico en una solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="22210-108">Represents a cryptographic attribute in a certificate request.</span></span>                                                                              |
| [<span data-ttu-id="22210-109">**ICryptAttributes**</span><span class="sxs-lookup"><span data-stu-id="22210-109">**ICryptAttributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattributes)                                 | <span data-ttu-id="22210-110">Administra una colección de objetos [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) .</span><span class="sxs-lookup"><span data-stu-id="22210-110">Manages a collection of [**ICryptAttribute**](/windows/desktop/api/CertEnroll/nn-certenroll-icryptattribute) objects.</span></span>                                                                 |
| [<span data-ttu-id="22210-111">**IX509Attribute**</span><span class="sxs-lookup"><span data-stu-id="22210-111">**IX509Attribute**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute)                                     | <span data-ttu-id="22210-112">Representa un atributo en una \# solicitud de certificado PKCS 7, PKCS \# 10 o CMC.</span><span class="sxs-lookup"><span data-stu-id="22210-112">Represents an attribute in a PKCS \#7, PKCS \#10, or CMC certificate request.</span></span>                                                               |
| [<span data-ttu-id="22210-113">**IX509AttributeClientId**</span><span class="sxs-lookup"><span data-stu-id="22210-113">**IX509AttributeClientId**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeclientid)                     | <span data-ttu-id="22210-114">Representa un atributo que se puede utilizar para identificar el cliente que generó una solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="22210-114">Represents an attribute that can be used to identify the client that generated a certificate request.</span></span>                                       |
| [<span data-ttu-id="22210-115">**IX509AttributeExtensions**</span><span class="sxs-lookup"><span data-stu-id="22210-115">**IX509AttributeExtensions**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeextensions)                 | <span data-ttu-id="22210-116">Representa las extensiones de certificado en una solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="22210-116">Represents the certificate extensions in a certificate request.</span></span>                                                                             |
| [<span data-ttu-id="22210-117">**IX509AttributeArchiveKey**</span><span class="sxs-lookup"><span data-stu-id="22210-117">**IX509AttributeArchiveKey**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekey)                 | <span data-ttu-id="22210-118">Representa un atributo que contiene una clave privada cifrada que va a ser archivada por una entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="22210-118">Represents an attribute that contains an encrypted private key to be archived by a certification authority.</span></span>                                 |
| [<span data-ttu-id="22210-119">**IX509AttributeArchiveKeyHash**</span><span class="sxs-lookup"><span data-stu-id="22210-119">**IX509AttributeArchiveKeyHash**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributearchivekeyhash)         | <span data-ttu-id="22210-120">Representa un atributo que contiene un hash SHA-1 de la clave privada cifrada que va a ser archivada por una entidad de certificación.</span><span class="sxs-lookup"><span data-stu-id="22210-120">Represents an attribute that contains a SHA-1 hash of the encrypted private key to be archived by a certification authority.</span></span>                |
| [<span data-ttu-id="22210-121">**IX509AttributeCspProvider**</span><span class="sxs-lookup"><span data-stu-id="22210-121">**IX509AttributeCspProvider**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributecspprovider)               | <span data-ttu-id="22210-122">Representa un atributo que identifica el proveedor de servicios criptográficos utilizado por la entidad que solicita el certificado.</span><span class="sxs-lookup"><span data-stu-id="22210-122">Represents an attribute that identifies the cryptographic provider used by the entity requesting the certificate.</span></span>                           |
| [<span data-ttu-id="22210-123">**IX509AttributeOSVersion**</span><span class="sxs-lookup"><span data-stu-id="22210-123">**IX509AttributeOSVersion**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributeosversion)                   | <span data-ttu-id="22210-124">Representa un atributo que contiene información de versión sobre el sistema operativo del cliente en el que se generó la solicitud de certificado.</span><span class="sxs-lookup"><span data-stu-id="22210-124">Represents an attribute that contains version information about the client operating system on which the certificate request was generated.</span></span> |
| [<span data-ttu-id="22210-125">**IX509AttributeRenewalCertificate**</span><span class="sxs-lookup"><span data-stu-id="22210-125">**IX509AttributeRenewalCertificate**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributerenewalcertificate) | <span data-ttu-id="22210-126">Representa un atributo que contiene el certificado que se va a renovar.</span><span class="sxs-lookup"><span data-stu-id="22210-126">Represents an attribute that contains the certificate being renewed.</span></span>                                                                        |
| [<span data-ttu-id="22210-127">**IX509Attributes**</span><span class="sxs-lookup"><span data-stu-id="22210-127">**IX509Attributes**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attributes)                                   | <span data-ttu-id="22210-128">Administra una colección de objetos [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) .</span><span class="sxs-lookup"><span data-stu-id="22210-128">Manages a collection of [**IX509Attribute**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509attribute) objects.</span></span>                                                                   |
| [<span data-ttu-id="22210-129">**IX509NameValuePair**</span><span class="sxs-lookup"><span data-stu-id="22210-129">**IX509NameValuePair**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair)                             | <span data-ttu-id="22210-130">Representa un par nombre-valor genérico.</span><span class="sxs-lookup"><span data-stu-id="22210-130">Represents a generic name-value pair.</span></span>                                                                                                       |
| [<span data-ttu-id="22210-131">**IX509NameValuePairs**</span><span class="sxs-lookup"><span data-stu-id="22210-131">**IX509NameValuePairs**</span></span>](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepairs)                           | <span data-ttu-id="22210-132">Administra una colección de objetos [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) .</span><span class="sxs-lookup"><span data-stu-id="22210-132">Manages a collection of [**IX509NameValuePair**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509namevaluepair) objects.</span></span>                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="22210-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="22210-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="22210-134">Interfaces CertEnroll</span><span class="sxs-lookup"><span data-stu-id="22210-134">CertEnroll Interfaces</span></span>](certenroll-interfaces.md)
</dt> </dl>

 

 



