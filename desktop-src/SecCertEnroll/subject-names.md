---
description: El campo de asunto de una \# solicitud de certificado PKCS 10 contiene el nombre distintivo de la entidad que solicita el certificado.
ms.assetid: 6c35ce42-07be-4d47-a14e-ed5a361dbe33
title: Nombres de sujeto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 226c294e75477a3960cd0ad824a98b3556c34322
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667720"
---
# <a name="subject-names"></a><span data-ttu-id="cf89c-103">Nombres de sujeto</span><span class="sxs-lookup"><span data-stu-id="cf89c-103">Subject Names</span></span>

<span data-ttu-id="cf89c-104">El campo de **asunto** de una \# solicitud de certificado PKCS 10 contiene el nombre distintivo de la entidad que solicita el certificado.</span><span class="sxs-lookup"><span data-stu-id="cf89c-104">The **subject** field of a PKCS \#10 certificate request contains the distinguished name of the entity requesting the certificate.</span></span>

``` syntax
CertificationRequestInfo ::= SEQUENCE 
{
   version                 CertificationRequestInfoVersion,
   subject                 Name,
   subjectPublicKeyInfo    SubjectPublicKeyInfo,
   attributes              [0] IMPLICIT Attributes
}
```

<span data-ttu-id="cf89c-105">El nombre distintivo consta de una secuencia de nombres distintivos relativos (RDN).</span><span class="sxs-lookup"><span data-stu-id="cf89c-105">The distinguished name consists of a sequence of relative distinguished names (RDNs).</span></span> <span data-ttu-id="cf89c-106">Cada RDN está compuesto de un conjunto de atributos y cada atributo consta de un identificador de objeto y un valor.</span><span class="sxs-lookup"><span data-stu-id="cf89c-106">Each RDN consists of a set of attributes, and each attribute consists of an object identifier and a value.</span></span> <span data-ttu-id="cf89c-107">El tipo de datos del valor se identifica mediante la estructura **DirectoryString** .</span><span class="sxs-lookup"><span data-stu-id="cf89c-107">The data type of the value is identified by the **DirectoryString** structure.</span></span>

``` syntax
Name ::= SEQUENCE OF RelativeDistinguishedName

RelativeDistinguishedName ::= SET OF AttributeTypeValue

AttributeTypeValue ::= SEQUENCE 
{
   type       EncodedObjectID,
   value      ANY 
}

DirectoryString ::= CHOICE 
{
   teletexString           TeletexString (SIZE (1..MAX)),
   printableString         PrintableString (SIZE (1..MAX)),
   universalString         UniversalString (SIZE (1..MAX)),
   utf8String              UTF8String (SIZE (1..MAX)),
   bmpString               BMPString (SIZE (1..MAX)) 
}
```

<span data-ttu-id="cf89c-108">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="cf89c-108">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="cf89c-109">Crear un nombre de sujeto</span><span class="sxs-lookup"><span data-stu-id="cf89c-109">Creating a Subject Name</span></span>](creating-a-subject-name.md)
-   [<span data-ttu-id="cf89c-110">Codificar un nombre de sujeto</span><span class="sxs-lookup"><span data-stu-id="cf89c-110">Encoding a Subject Name</span></span>](encoding-a-subject-name.md)

## <a name="related-topics"></a><span data-ttu-id="cf89c-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="cf89c-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf89c-112">Solicitudes</span><span class="sxs-lookup"><span data-stu-id="cf89c-112">Requests</span></span>](/windows/desktop/SecCrypto/requests)
</dt> </dl>

 

 
