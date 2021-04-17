---
description: XML es un estándar del sector para describir los datos estructurados. Una firma digital XML es una representación XML de una firma digital que proporciona la capacidad de comprobar el origen y la integridad del documento XML y los datos a los que se hace referencia externamente.
ms.assetid: 02ca8d9b-be08-4b15-895f-9c8c4b0ed536
title: Información general sobre la firma digital XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b41a1b748305ab26b686e126cd201ad9e7f34d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105687579"
---
# <a name="xml-digital-signature-overview"></a><span data-ttu-id="7c0f6-104">Información general sobre la firma digital XML</span><span class="sxs-lookup"><span data-stu-id="7c0f6-104">XML Digital Signature Overview</span></span>

<span data-ttu-id="7c0f6-105">XML es un estándar del sector para describir los datos estructurados.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-105">XML is an industry standard for describing structured data.</span></span> <span data-ttu-id="7c0f6-106">Una firma digital XML es una representación XML de una [*firma digital*](../secgloss/d-gly.md) que proporciona la capacidad de comprobar el origen y la integridad del documento XML y los datos a los que se hace referencia externamente.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-106">An XML Digital Signature is an XML representation of a [*digital signature*](../secgloss/d-gly.md) that provides the ability to verify the origin and integrity of XML document and externally referenced data.</span></span> <span data-ttu-id="7c0f6-107">Las firmas digitales XML se pueden usar para firmar datos arbitrarios, como un documento o fragmento XML, una página HTML, texto sin formato o datos codificados en binario, como un archivo JPEG.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-107">XML digital signatures can be used to sign arbitrary data, including an XML document or fragment, an HTML page, plain text, or binary-encoded data such as a JPEG file.</span></span>

<span data-ttu-id="7c0f6-108">El formato de firma digital XML admitido por la API de firma digital de CryptXML se especifica mediante la recomendación de XML Signature Syntax and Processing (Second Edition) W3C.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-108">The XML digital signature format supported by the CryptXML digital signature API is specified by the XML Signature Syntax and Processing (Second Edition) W3C recommendation.</span></span>

<span data-ttu-id="7c0f6-109">La firma digital de CryptXML implementa la compatibilidad con los tipos de firma, los algoritmos criptográficos, los algoritmos de canonización y la transformación protegida con envoltorio especificados.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-109">The CryptXML digital signature implements support for the required signature types, cryptographic algorithms, canonicalization algorithms, and the specified enveloped transform.</span></span>

<span data-ttu-id="7c0f6-110">Los desarrolladores pueden extender el conjunto predeterminado de algoritmos criptográficos compatibles con CryptXML mediante la creación de archivos dll de extensión criptográfica.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-110">Developers can extend the default set of cryptographic algorithms supported by CryptXML by creating cryptographic extension DLLs.</span></span> <span data-ttu-id="7c0f6-111">Los desarrolladores también pueden crear sus propias transformaciones y algoritmos de canonización personalizados sobre la API de CryptXML.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-111">Developers can also create their own custom transforms and canonicalization algorithms on top of CryptXML API.</span></span> <span data-ttu-id="7c0f6-112">Los desarrolladores pueden usar las API de CryptXML con las API de certificados de Windows.</span><span class="sxs-lookup"><span data-stu-id="7c0f6-112">Developers can use the CryptXML APIs with the Windows certificate APIs.</span></span>

 

 
