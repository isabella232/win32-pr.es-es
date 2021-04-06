---
description: Los atributos se pueden agregar a una solicitud de certificado para proporcionar a una entidad de certificación (CA) información adicional que puede utilizar al crear y emitir un certificado.
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
ms.openlocfilehash: e7a00c30be8bacf5593d78e21fb420c8a899dc7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103811263"
---
# <a name="attributes-certificate-enrollment-api"></a><span data-ttu-id="52a28-103">Atributos (API de inscripción de certificados)</span><span class="sxs-lookup"><span data-stu-id="52a28-103">Attributes (Certificate Enrollment API)</span></span>

<span data-ttu-id="52a28-104">Los atributos se pueden agregar a una solicitud de certificado para proporcionar a una entidad de certificación (CA) información adicional que puede utilizar al crear y emitir un certificado.</span><span class="sxs-lookup"><span data-stu-id="52a28-104">Attributes can be added to a certificate request to provide a certification authority (CA) with additional information that it can use when creating and issuing a certificate.</span></span> <span data-ttu-id="52a28-105">Cada atributo es una estructura de [*notación de sintaxis abstracta*](/windows/desktop/SecGloss/a-gly) (ASN. 1) codificada en [*reglas de codificación distinguida*](/windows/desktop/SecGloss/d-gly) (der) que contiene un identificador de objeto (OID) y cero o más valores.</span><span class="sxs-lookup"><span data-stu-id="52a28-105">Each attribute is a [*Distinguished Encoding Rules*](/windows/desktop/SecGloss/d-gly) (DER) encoded [*Abstract Syntax Notation One*](/windows/desktop/SecGloss/a-gly) (ASN.1) structure that contains an object identifier (OID) and zero or more values.</span></span> <span data-ttu-id="52a28-106">Los atributos se definen mediante interfaces que se incluyen con la API de inscripción de certificados.</span><span class="sxs-lookup"><span data-stu-id="52a28-106">Attributes are defined by using interfaces included with the Certificate Enrollment API.</span></span> <span data-ttu-id="52a28-107">En los temas siguientes se describen los atributos con más detalle:</span><span class="sxs-lookup"><span data-stu-id="52a28-107">The following topics discuss attributes in more detail:</span></span>

-   [<span data-ttu-id="52a28-108">Atributos compatibles</span><span class="sxs-lookup"><span data-stu-id="52a28-108">Supported Attributes</span></span>](supported-attributes.md)
-   [<span data-ttu-id="52a28-109">Arquitectura de atributo</span><span class="sxs-lookup"><span data-stu-id="52a28-109">Attribute Architecture</span></span>](attribute-architecture.md)
-   [<span data-ttu-id="52a28-110">\#Atributos PKCS 7</span><span class="sxs-lookup"><span data-stu-id="52a28-110">PKCS \#7 Attributes</span></span>](pkcs--7-attributes.md)
-   [<span data-ttu-id="52a28-111">\#Atributos PKCS 10</span><span class="sxs-lookup"><span data-stu-id="52a28-111">PKCS \#10 Attributes</span></span>](pkcs--10-attributes.md)
-   [<span data-ttu-id="52a28-112">Atributos de CMC</span><span class="sxs-lookup"><span data-stu-id="52a28-112">CMC Attributes</span></span>](cmc-attributes.md)

 

 
