---
description: CryptXML proporciona un conjunto de bajo nivel de API que permiten a las aplicaciones crear y comprobar firmas con doble cifrado, envoltura y desconectadas. Puede usar CryptXML para crear y comprobar el contenido almacenado en los elementos del objeto Signature, incluidos los manifiestos.
ms.assetid: 962dffdb-caa6-4aa7-b5c6-3a9de8cfaf6c
title: Funcionalidad de la API de firma digital XML
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67ae330fdd8ba75ece885e8ed0b7e2c91e60fc39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667529"
---
# <a name="xml-digital-signature-api-functionality"></a><span data-ttu-id="7fbfa-104">Funcionalidad de la API de firma digital XML</span><span class="sxs-lookup"><span data-stu-id="7fbfa-104">XML Digital Signature API Functionality</span></span>

<span data-ttu-id="7fbfa-105">CryptXML proporciona un conjunto de bajo nivel de API que permiten a las aplicaciones crear y comprobar firmas con doble cifrado, envoltura y desconectadas.</span><span class="sxs-lookup"><span data-stu-id="7fbfa-105">CryptXML provides a low level set of APIs that allow applications to create and verify enveloped, enveloping, and detached signatures.</span></span> <span data-ttu-id="7fbfa-106">Puede usar CryptXML para crear y comprobar el contenido almacenado en los elementos del objeto Signature, incluidos los manifiestos.</span><span class="sxs-lookup"><span data-stu-id="7fbfa-106">You can use CryptXML to create and verify content stored in signature object elements, including manifests.</span></span> <span data-ttu-id="7fbfa-107">Se puede usar una clave pública o privada, una clave compartida o un certificado [*X. 509*](../secgloss/x-gly.md) o una cadena de certificados para firmar y comprobar la [*firma digital*](../secgloss/d-gly.md)XML.</span><span class="sxs-lookup"><span data-stu-id="7fbfa-107">A public/private, shared key, or an [*X.509*](../secgloss/x-gly.md) certificate or certificate chain can be used to sign and verify the XML [*digital signature*](../secgloss/d-gly.md).</span></span>

<span data-ttu-id="7fbfa-108">Las aplicaciones que usan CryptXML para comprobar las referencias externas (referencias destinadas a un documento o archivo externo fuera del contexto del documento) deben resolver los URI externos y recuperar los datos que se van a resumir.</span><span class="sxs-lookup"><span data-stu-id="7fbfa-108">Applications that use CryptXML to verify external references (references that target an external document or file outside of the document context) must resolve the external URIs and retrieve the data to be digested.</span></span>

<span data-ttu-id="7fbfa-109">Para obtener información sobre los algoritmos criptográficos admitidos por CryptXML, consulte [algoritmos criptográficos de la firma digital XML](xml-digital-signature-cryptographic-algorithms.md).</span><span class="sxs-lookup"><span data-stu-id="7fbfa-109">For information about the cryptographic algorithms supported by CryptXML, see [XML Digital Signature Cryptographic Algorithms](xml-digital-signature-cryptographic-algorithms.md).</span></span>

<span data-ttu-id="7fbfa-110">CryptXML proporciona compatibilidad con los algoritmos de canonización con los siguientes identificadores.</span><span class="sxs-lookup"><span data-stu-id="7fbfa-110">CryptXML provides support for the canonicalization algorithms with the following identifiers.</span></span>



| <span data-ttu-id="7fbfa-111">Constante</span><span class="sxs-lookup"><span data-stu-id="7fbfa-111">Constant</span></span>                                              | <span data-ttu-id="7fbfa-112">Valor de URI</span><span class="sxs-lookup"><span data-stu-id="7fbfa-112">URI value</span></span>                                                                  |
|-------------------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="7fbfa-113">wszURI \_ canonicalización de la canonización \_</span><span class="sxs-lookup"><span data-stu-id="7fbfa-113">wszURI\_CANONICALIZATION\_C14N</span></span><br/>             | <span data-ttu-id="7fbfa-114">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315"</span><span class="sxs-lookup"><span data-stu-id="7fbfa-114">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315"</span></span><br/>               |
| <span data-ttu-id="7fbfa-115">wszURI \_ canonización \_ C14NC</span><span class="sxs-lookup"><span data-stu-id="7fbfa-115">wszURI\_CANONICALIZATION\_C14NC</span></span><br/>            | <span data-ttu-id="7fbfa-116">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"</span><span class="sxs-lookup"><span data-stu-id="7fbfa-116">"https://www.w3.org/TR/2001/REC-xml-c14n-20010315\#WithComments"</span></span><br/> |
| <span data-ttu-id="7fbfa-117">wszURI \_ canonicalización \_ EXSLUSIVE \_ C14N</span><span class="sxs-lookup"><span data-stu-id="7fbfa-117">wszURI\_CANONICALIZATION\_EXSLUSIVE\_C14N</span></span><br/>  | <span data-ttu-id="7fbfa-118">"https://www.w3.org/2001/10/xml-exc-c14n\#"</span><span class="sxs-lookup"><span data-stu-id="7fbfa-118">"https://www.w3.org/2001/10/xml-exc-c14n\#"</span></span><br/>                      |
| <span data-ttu-id="7fbfa-119">wszURI \_ canonicalización \_ EXSLUSIVE \_ C14NC</span><span class="sxs-lookup"><span data-stu-id="7fbfa-119">wszURI\_CANONICALIZATION\_EXSLUSIVE\_C14NC</span></span><br/> | <span data-ttu-id="7fbfa-120">"https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"</span><span class="sxs-lookup"><span data-stu-id="7fbfa-120">"https://www.w3.org/2001/10/xml-exc-c14n\#WithComments"</span></span><br/>          |



 

<span data-ttu-id="7fbfa-121">CryptXML proporciona compatibilidad con la transformación de firma con doble cifrado.</span><span class="sxs-lookup"><span data-stu-id="7fbfa-121">CryptXML provides support for the enveloped signature transform.</span></span>



| <span data-ttu-id="7fbfa-122">Constante</span><span class="sxs-lookup"><span data-stu-id="7fbfa-122">Constant</span></span>                                       | <span data-ttu-id="7fbfa-123">Valor de URI</span><span class="sxs-lookup"><span data-stu-id="7fbfa-123">URI value</span></span>                                                           |
|------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="7fbfa-124">wszURI \_ xmlns \_ Transform \_ sobre</span><span class="sxs-lookup"><span data-stu-id="7fbfa-124">wszURI\_XMLNS\_TRANSFORM\_ENVELOPED</span></span><br/> | <span data-ttu-id="7fbfa-125">"https://www.w3.org/2000/09/xmldsig\#enveloped-signature"</span><span class="sxs-lookup"><span data-stu-id="7fbfa-125">"https://www.w3.org/2000/09/xmldsig\#enveloped-signature"</span></span><br/> |



 

<span data-ttu-id="7fbfa-126">De forma predeterminada, CryptXML no admite las transformaciones XPath o XSLT.</span><span class="sxs-lookup"><span data-stu-id="7fbfa-126">By default, CryptXML does not support XPath or XSLT transforms.</span></span> <span data-ttu-id="7fbfa-127">Si es necesario, las aplicaciones pueden implementar estas transformaciones en la parte superior de CryptXML.</span><span class="sxs-lookup"><span data-stu-id="7fbfa-127">If required, applications can implement these transforms on top of CryptXML.</span></span>

 

 
