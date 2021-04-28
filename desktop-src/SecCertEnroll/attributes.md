---
description: 'Atributos (API de inscripción de certificados): se pueden agregar atributos a una solicitud de certificado para proporcionar una entidad de certificación (CA) con información adicional que puede usar al crear y emitir un certificado.'
ms.assetid: 6116e61e-3ec5-4992-90ab-e3c7ced291b6
title: Atributos (API de inscripción de certificados)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Attributes
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 93414156c7fa6e46fe80995d8d01eadc28796ec2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118433"
---
# <a name="attributes-certificate-enrollment-api"></a><span data-ttu-id="b85f6-103">Atributos (API de inscripción de certificados)</span><span class="sxs-lookup"><span data-stu-id="b85f6-103">Attributes (Certificate Enrollment API)</span></span>

<span data-ttu-id="b85f6-104">Los atributos se pueden agregar a una solicitud de certificado para proporcionar una entidad de certificación (CA) con información adicional que puede usar al crear y emitir un certificado.</span><span class="sxs-lookup"><span data-stu-id="b85f6-104">Attributes can be added to a certificate request to provide a certification authority (CA) with additional information that it can use when creating and issuing a certificate.</span></span> <span data-ttu-id="b85f6-105">Cada atributo es una [*estructura*](/windows/desktop/SecGloss/d-gly) de notación [](/windows/desktop/SecGloss/a-gly) de sintaxis abstracta (ASN.1) codificada por reglas de codificación distinguida (DER) que contiene un identificador de objeto (OID) y cero o más valores.</span><span class="sxs-lookup"><span data-stu-id="b85f6-105">Each attribute is a [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) encoded [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) structure that contains an object identifier (OID) and zero or more values.</span></span> <span data-ttu-id="b85f6-106">Los atributos se definen mediante interfaces incluidas con la API de inscripción de certificados.</span><span class="sxs-lookup"><span data-stu-id="b85f6-106">Attributes are defined by using interfaces included with the Certificate Enrollment API.</span></span> <span data-ttu-id="b85f6-107">En los temas siguientes se tratan los atributos con más detalle:</span><span class="sxs-lookup"><span data-stu-id="b85f6-107">The following topics discuss attributes in more detail:</span></span>

-   [<span data-ttu-id="b85f6-108">Atributos compatibles</span><span class="sxs-lookup"><span data-stu-id="b85f6-108">Supported Attributes</span></span>](supported-attributes.md)
-   [<span data-ttu-id="b85f6-109">Arquitectura de atributos</span><span class="sxs-lookup"><span data-stu-id="b85f6-109">Attribute Architecture</span></span>](attribute-architecture.md)
-   [<span data-ttu-id="b85f6-110">Atributos PKCS \# 7</span><span class="sxs-lookup"><span data-stu-id="b85f6-110">PKCS \#7 Attributes</span></span>](pkcs--7-attributes.md)
-   [<span data-ttu-id="b85f6-111">Atributos PKCS \# 10</span><span class="sxs-lookup"><span data-stu-id="b85f6-111">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
-   [<span data-ttu-id="b85f6-112">Atributos de CMC</span><span class="sxs-lookup"><span data-stu-id="b85f6-112">CMC Attributes</span></span>](cmc-attributes.md)

 

 
