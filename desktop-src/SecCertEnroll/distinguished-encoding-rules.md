---
description: La notación de sintaxis abstracta uno (ASN. 1) define los siguientes conjuntos de reglas que rigen cómo se codifican y descodifican las estructuras de datos que se envían entre los equipos.
ms.assetid: 47735fa1-9d75-4c6b-b14c-6c7483f43a5d
title: reglas de codificación distinguida
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12429c7c2185fc4910abd00e4641e7cd9d2f2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104542694"
---
# <a name="distinguished-encoding-rules"></a><span data-ttu-id="82837-103">reglas de codificación distinguida</span><span class="sxs-lookup"><span data-stu-id="82837-103">Distinguished Encoding Rules</span></span>

<span data-ttu-id="82837-104">La notación de sintaxis abstracta uno (ASN. 1) define los siguientes conjuntos de reglas que rigen cómo se codifican y descodifican las estructuras de datos que se envían entre los equipos.</span><span class="sxs-lookup"><span data-stu-id="82837-104">Abstract Syntax Notation One (ASN.1) defines the following rule sets that govern how data structures that are being sent between computers are encoded and decoded.</span></span>

-   <span data-ttu-id="82837-105">Reglas de codificación básicas (BER)</span><span class="sxs-lookup"><span data-stu-id="82837-105">Basic Encoding Rules (BER)</span></span>
-   <span data-ttu-id="82837-106">Reglas de codificación canónica (CER)</span><span class="sxs-lookup"><span data-stu-id="82837-106">Canonical Encoding Rules (CER)</span></span>
-   <span data-ttu-id="82837-107">Reglas de codificación distinguida (DER)</span><span class="sxs-lookup"><span data-stu-id="82837-107">Distinguished Encoding Rules (DER)</span></span>
-   <span data-ttu-id="82837-108">Reglas de codificación empaquetadas (por)</span><span class="sxs-lookup"><span data-stu-id="82837-108">Packed Encoding Rules (PER)</span></span>

<span data-ttu-id="82837-109">El conjunto de reglas original se definió mediante la especificación BER.</span><span class="sxs-lookup"><span data-stu-id="82837-109">The original rule set was defined by the BER specification.</span></span> <span data-ttu-id="82837-110">CER y DER se desarrollaron más adelante como subconjuntos especializados de BER.</span><span class="sxs-lookup"><span data-stu-id="82837-110">CER and DER were developed later as specialized subsets of BER.</span></span> <span data-ttu-id="82837-111">POR se desarrolló en respuesta a críticas sobre la cantidad de ancho de banda necesario para transmitir datos mediante BER o sus variantes.</span><span class="sxs-lookup"><span data-stu-id="82837-111">PER was developed in response to criticisms about the amount of bandwidth required to transmit data using BER or its variants.</span></span> <span data-ttu-id="82837-112">POR proporciona un ahorro significativo.</span><span class="sxs-lookup"><span data-stu-id="82837-112">PER provides a significant savings.</span></span>

<span data-ttu-id="82837-113">Se creó DER para satisfacer los requisitos de la especificación X. 509 para la transferencia de datos segura.</span><span class="sxs-lookup"><span data-stu-id="82837-113">DER was created to satisfy the requirements of the X.509 specification for secure data transfer.</span></span> <span data-ttu-id="82837-114">La API de inscripción de certificados usa DER exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="82837-114">The Certificate Enrollment API uses DER exclusively.</span></span> <span data-ttu-id="82837-115">Para obtener más información, vea los siguientes temas.</span><span class="sxs-lookup"><span data-stu-id="82837-115">For more information, see the following topics.</span></span>

-   [<span data-ttu-id="82837-116">Sintaxis de transferencia DER</span><span class="sxs-lookup"><span data-stu-id="82837-116">DER Transfer Syntax</span></span>](about-der-transfer-syntax.md)
-   [<span data-ttu-id="82837-117">Codificación DER de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="82837-117">DER Encoding of ASN.1 Types</span></span>](about-der-encoding-of-asn-1-types.md)

## <a name="related-topics"></a><span data-ttu-id="82837-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="82837-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82837-119">Sistema de tipos ASN. 1</span><span class="sxs-lookup"><span data-stu-id="82837-119">ASN.1 Type System</span></span>](about-asn-1-type-system.md)
</dt> <dt>

[<span data-ttu-id="82837-120">Codificación de solicitud de certificado</span><span class="sxs-lookup"><span data-stu-id="82837-120">Certificate Request Encoding</span></span>](about-certificate-request-encoding.md)
</dt> <dt>

[<span data-ttu-id="82837-121">Introducción a la codificación y sintaxis de ASN. 1</span><span class="sxs-lookup"><span data-stu-id="82837-121">Introduction to ASN.1 Syntax and Encoding</span></span>](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



