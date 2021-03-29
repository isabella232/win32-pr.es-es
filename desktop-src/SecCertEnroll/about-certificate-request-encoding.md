---
description: En una PKI de Microsoft, las solicitudes de certificado se envían desde los equipos cliente a las entidades de certificación (CA) como una cadena binaria que contiene una secuencia de estructuras de datos codificadas.
ms.assetid: 0b9fa1bc-b67e-4b50-abd5-cbc3663ff219
title: Codificación de solicitud de certificado
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3cd9dfedede4c7b10d4968242b1d27ad11e2b6f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103813750"
---
# <a name="certificate-request-encoding"></a><span data-ttu-id="9bd48-103">Codificación de solicitud de certificado</span><span class="sxs-lookup"><span data-stu-id="9bd48-103">Certificate Request Encoding</span></span>

<span data-ttu-id="9bd48-104">En una PKI de Microsoft, las solicitudes de certificado se envían desde los equipos cliente a las entidades de certificación (CA) como una cadena binaria que contiene una secuencia de estructuras de datos codificadas.</span><span class="sxs-lookup"><span data-stu-id="9bd48-104">In a Microsoft PKI, certificate requests are sent from client computers to certification authorities (CAs) as a binary string that contains a sequence of encoded data structures.</span></span> <span data-ttu-id="9bd48-105">La API de inscripción de certificados usa la notación de sintaxis abstracta uno (ASN. 1) para describir y codificar estas estructuras.</span><span class="sxs-lookup"><span data-stu-id="9bd48-105">The Certificate Enrollment API uses Abstract Syntax Notation One (ASN.1) to describe and encode these structures.</span></span> <span data-ttu-id="9bd48-106">Para los fines de esta documentación, ASN. 1 puede dividirse conceptualmente en las reglas de sintaxis (ISO 8824) que describen las estructuras de datos y las reglas de codificación (ISO 8825) que especifican cómo se van a codificar los datos para la transmisión de red.</span><span class="sxs-lookup"><span data-stu-id="9bd48-106">For the purposes of this documentation, ASN.1 can be conceptually divided into the syntax rules (ISO 8824) that describe the data structures and the encoding rules (ISO 8825) that specify how the data is to be encoded for network transmission.</span></span> <span data-ttu-id="9bd48-107">Para obtener más información, vea los temas siguientes:</span><span class="sxs-lookup"><span data-stu-id="9bd48-107">For more information, see the following topics:</span></span>

-   [<span data-ttu-id="9bd48-108">Introducción a la codificación y sintaxis de ASN. 1</span><span class="sxs-lookup"><span data-stu-id="9bd48-108">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
-   [<span data-ttu-id="9bd48-109">Sistema de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="9bd48-109">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
-   [<span data-ttu-id="9bd48-110">reglas de codificación distinguida</span><span class="sxs-lookup"><span data-stu-id="9bd48-110">Distinguished Encoding Rules</span></span>](distinguished-encoding-rules.md)

## <a name="related-topics"></a><span data-ttu-id="9bd48-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="9bd48-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9bd48-112">Acerca de la API de inscripción de certificados</span><span class="sxs-lookup"><span data-stu-id="9bd48-112">About the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 



