---
description: CryptXML admite de forma nativa los URI que se enumeran a continuación.
ms.assetid: 012bad01-228a-4bb0-b883-0c2c7abd9271
title: Algoritmos criptográficos de firma digital XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 896348375d1d1a51288980aad3793dfffc69eb18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686791"
---
# <a name="xml-digital-signature-cryptographic-algorithms"></a><span data-ttu-id="9e4dc-103">Algoritmos criptográficos de firma digital XML</span><span class="sxs-lookup"><span data-stu-id="9e4dc-103">XML Digital Signature Cryptographic Algorithms</span></span>

<span data-ttu-id="9e4dc-104">CryptXML admite de forma nativa los URI que se enumeran a continuación.</span><span class="sxs-lookup"><span data-stu-id="9e4dc-104">CryptXML natively supports the URIs listed below.</span></span> <span data-ttu-id="9e4dc-105">Si es necesaria la compatibilidad con los algoritmos criptográficos y las transformaciones que no forman parte de la compatibilidad nativa, puede usar [las extensiones criptográficas](xml-digital-signature-cryptographic-extensions.md) [API: siguiente generación](../seccng/cng-portal.md) y firma digital XML para admitir nuevos algoritmos.</span><span class="sxs-lookup"><span data-stu-id="9e4dc-105">If support is required for cryptographic algorithms and transforms that are not part of the native support, you can use [Cryptography API: Next Generation](../seccng/cng-portal.md) and [XML Digital Signature Cryptographic Extensions](xml-digital-signature-cryptographic-extensions.md) to support new algorithms.</span></span>

## <a name="supported-uris"></a><span data-ttu-id="9e4dc-106">Uri admitidos</span><span class="sxs-lookup"><span data-stu-id="9e4dc-106">Supported URIs</span></span>

<span data-ttu-id="9e4dc-107">Métodos de síntesis</span><span class="sxs-lookup"><span data-stu-id="9e4dc-107">Digest Methods</span></span>



| <span data-ttu-id="9e4dc-108">Constante</span><span class="sxs-lookup"><span data-stu-id="9e4dc-108">Constant</span></span>                                 | <span data-ttu-id="9e4dc-109">Valor de URI</span><span class="sxs-lookup"><span data-stu-id="9e4dc-109">URI value</span></span>                                                   |
|------------------------------------------|-------------------------------------------------------------|
| <span data-ttu-id="9e4dc-110">wszURI \_ xmlns \_ DIGSIG \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="9e4dc-110">wszURI\_XMLNS\_DIGSIG\_SHA1</span></span><br/>   | <span data-ttu-id="9e4dc-111">"https://www.w3.org/2000/09/xmldsig\#sha1"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-111">"https://www.w3.org/2000/09/xmldsig\#sha1"</span></span><br/>        |
| <span data-ttu-id="9e4dc-112">wszURI \_ xmlns \_ DIGSIG \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="9e4dc-112">wszURI\_XMLNS\_DIGSIG\_SHA256</span></span><br/> | <span data-ttu-id="9e4dc-113">"https://www.w3.org/2001/04/xmlenc\#sha256"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-113">"https://www.w3.org/2001/04/xmlenc\#sha256"</span></span><br/>       |
| <span data-ttu-id="9e4dc-114">wszURI \_ xmlns \_ DIGSIG \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="9e4dc-114">wszURI\_XMLNS\_DIGSIG\_SHA384</span></span><br/> | <span data-ttu-id="9e4dc-115">"https://www.w3.org/2001/04/xmldsig-more\#sha384"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-115">"https://www.w3.org/2001/04/xmldsig-more\#sha384"</span></span><br/> |
| <span data-ttu-id="9e4dc-116">wszURI \_ xmlns \_ DIGSIG \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="9e4dc-116">wszURI\_XMLNS\_DIGSIG\_SHA512</span></span><br/> | <span data-ttu-id="9e4dc-117">"https://www.w3.org/2001/04/xmlenc\#sha512"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-117">"https://www.w3.org/2001/04/xmlenc\#sha512"</span></span><br/>       |



 

<span data-ttu-id="9e4dc-118">Métodos de firma</span><span class="sxs-lookup"><span data-stu-id="9e4dc-118">Signature Methods</span></span>



| <span data-ttu-id="9e4dc-119">Constante</span><span class="sxs-lookup"><span data-stu-id="9e4dc-119">Constant</span></span>                                        | <span data-ttu-id="9e4dc-120">Valor de URI</span><span class="sxs-lookup"><span data-stu-id="9e4dc-120">URI value</span></span>                                                         |
|-------------------------------------------------|-------------------------------------------------------------------|
| <span data-ttu-id="9e4dc-121">wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="9e4dc-121">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA1</span></span><br/>     | <span data-ttu-id="9e4dc-122">"https://www.w3.org/2000/09/xmldsig\#rsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-122">"https://www.w3.org/2000/09/xmldsig\#rsa-sha1"</span></span><br/>          |
| <span data-ttu-id="9e4dc-123">wszURI \_ xmlns \_ DIGSIG \_ DSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="9e4dc-123">wszURI\_XMLNS\_DIGSIG\_DSA\_SHA1</span></span><br/>     | <span data-ttu-id="9e4dc-124">"https://www.w3.org/2000/09/xmldsig\#dsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-124">"https://www.w3.org/2000/09/xmldsig\#dsa-sha1"</span></span><br/>          |
| <span data-ttu-id="9e4dc-125">wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="9e4dc-125">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA256</span></span><br/>   | <span data-ttu-id="9e4dc-126">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-126">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha256"</span></span><br/>   |
| <span data-ttu-id="9e4dc-127">wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="9e4dc-127">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA384</span></span><br/>   | <span data-ttu-id="9e4dc-128">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-128">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha384"</span></span><br/>   |
| <span data-ttu-id="9e4dc-129">wszURI \_ xmlns \_ DIGSIG \_ RSA \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="9e4dc-129">wszURI\_XMLNS\_DIGSIG\_RSA\_SHA512</span></span><br/>   | <span data-ttu-id="9e4dc-130">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-130">"https://www.w3.org/2001/04/xmldsig-more\#rsa-sha512"</span></span><br/>   |
| <span data-ttu-id="9e4dc-131">wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="9e4dc-131">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA1</span></span><br/>   | <span data-ttu-id="9e4dc-132">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-132">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha1"</span></span><br/>   |
| <span data-ttu-id="9e4dc-133">wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="9e4dc-133">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA256</span></span><br/> | <span data-ttu-id="9e4dc-134">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-134">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha256"</span></span><br/> |
| <span data-ttu-id="9e4dc-135">wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="9e4dc-135">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA384</span></span><br/> | <span data-ttu-id="9e4dc-136">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-136">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha384"</span></span><br/> |
| <span data-ttu-id="9e4dc-137">wszURI \_ xmlns \_ DIGSIG \_ ECDSA \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="9e4dc-137">wszURI\_XMLNS\_DIGSIG\_ECDSA\_SHA512</span></span><br/> | <span data-ttu-id="9e4dc-138">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-138">"https://www.w3.org/2001/04/xmldsig-more\#ecdsa-sha512"</span></span><br/> |
| <span data-ttu-id="9e4dc-139">wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA1</span><span class="sxs-lookup"><span data-stu-id="9e4dc-139">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA1</span></span><br/>    | <span data-ttu-id="9e4dc-140">"https://www.w3.org/2000/09/xmldsig\#hmac-sha1"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-140">"https://www.w3.org/2000/09/xmldsig\#hmac-sha1"</span></span><br/>         |
| <span data-ttu-id="9e4dc-141">wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA256</span><span class="sxs-lookup"><span data-stu-id="9e4dc-141">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA256</span></span><br/>  | <span data-ttu-id="9e4dc-142">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-142">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha256"</span></span><br/>  |
| <span data-ttu-id="9e4dc-143">wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA384</span><span class="sxs-lookup"><span data-stu-id="9e4dc-143">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA384</span></span><br/>  | <span data-ttu-id="9e4dc-144">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-144">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha384"</span></span><br/>  |
| <span data-ttu-id="9e4dc-145">wszURI \_ xmlns \_ DIGSIG \_ HMAC \_ SHA512</span><span class="sxs-lookup"><span data-stu-id="9e4dc-145">wszURI\_XMLNS\_DIGSIG\_HMAC\_SHA512</span></span><br/>  | <span data-ttu-id="9e4dc-146">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"</span><span class="sxs-lookup"><span data-stu-id="9e4dc-146">"https://www.w3.org/2001/04/xmldsig-more\#hmac-sha512"</span></span><br/>  |



 

 

 
