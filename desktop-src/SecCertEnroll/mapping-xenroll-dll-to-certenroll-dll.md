---
description: La biblioteca de Xenroll.dll se ha quitado del sistema operativo y se ha reemplazado por CertEnroll.dll.
ms.assetid: ec28fbdc-9198-472a-8976-7b5db09069a6
title: Asignación Xenroll.dll a CertEnroll.dll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1fcaec56967f4c694b85d454bd21407c3af9029
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103815771"
---
# <a name="mapping-xenrolldll-to-certenrolldll"></a><span data-ttu-id="fd202-103">Asignación Xenroll.dll a CertEnroll.dll</span><span class="sxs-lookup"><span data-stu-id="fd202-103">Mapping Xenroll.dll to CertEnroll.dll</span></span>

<span data-ttu-id="fd202-104">Antes de Windows Vista, el control de inscripción de certificados se implementaba en Xenroll.dll.</span><span class="sxs-lookup"><span data-stu-id="fd202-104">Prior to Windows Vista, the Certificate Enrollment Control was implemented in Xenroll.dll.</span></span> <span data-ttu-id="fd202-105">La biblioteca de Xenroll.dll se ha quitado del sistema operativo y se ha reemplazado por CertEnroll.dll.</span><span class="sxs-lookup"><span data-stu-id="fd202-105">The Xenroll.dll library has been removed from the operating system and replaced by CertEnroll.dll.</span></span>

<span data-ttu-id="fd202-106">XENROLL intentó implementar dos conjuntos paralelos de interfaces.</span><span class="sxs-lookup"><span data-stu-id="fd202-106">Xenroll attempted to implement two parallel sets of interfaces.</span></span> <span data-ttu-id="fd202-107">[**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3)y [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) eran compatibles con la automatización y eran compatibles con los lenguajes de scripting.</span><span class="sxs-lookup"><span data-stu-id="fd202-107">[**ICEnroll**](/windows/desktop/api/xenroll/nn-xenroll-icenroll), [**ICEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-icenroll2), [**ICEnroll3**](/windows/desktop/api/xenroll/nn-xenroll-icenroll3), and [**ICEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-icenroll4) were Automation-compliant and compatible with scripting languages.</span></span> <span data-ttu-id="fd202-108">Las interfaces correspondientes ([**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2)y [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)) no se pudieron incluir en el script, pero eran más cómodas para los programadores de C++.</span><span class="sxs-lookup"><span data-stu-id="fd202-108">The corresponding interfaces—[**IEnroll**](/windows/desktop/api/xenroll/nn-xenroll-ienroll), [**IEnroll2**](/windows/desktop/api/xenroll/nn-xenroll-ienroll2), and [**IEnroll4**](/windows/desktop/api/xenroll/nn-xenroll-ienroll4)—could not be scripted but were more convenient for C++ programmers.</span></span> <span data-ttu-id="fd202-109">A medida que evolucionen, los dos conjuntos de interfaces no estaban sincronizados.</span><span class="sxs-lookup"><span data-stu-id="fd202-109">As they evolved, the two sets of interfaces did not remain synchronized.</span></span> <span data-ttu-id="fd202-110">En concreto, el conjunto de interfaces duales representadas más recientemente por **ICEnroll4** define solo un subconjunto de la funcionalidad definida por **IEnroll4**.</span><span class="sxs-lookup"><span data-stu-id="fd202-110">In particular, the set of dual interfaces represented most recently by **ICEnroll4** defines only a subset of the functionality defined by **IEnroll4**.</span></span>

<span data-ttu-id="fd202-111">CertEnroll.dll implementa un conjunto mayor y más estructurado de interfaces COM conformes a automatización.</span><span class="sxs-lookup"><span data-stu-id="fd202-111">CertEnroll.dll implements a larger and more structured set of Automation-compliant COM interfaces.</span></span> <span data-ttu-id="fd202-112">En los temas siguientes se describe cómo se asignan Xenroll.dll a CertEnroll.dll para distintos tipos de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="fd202-112">The following topics discuss how Xenroll.dll maps to CertEnroll.dll for different types of functionality.</span></span>

-   [<span data-ttu-id="fd202-113">Funciones de solicitud de certificado</span><span class="sxs-lookup"><span data-stu-id="fd202-113">Certificate Request Functions</span></span>](certificate-request-functions.md)
-   [<span data-ttu-id="fd202-114">Funciones de respuesta de certificado</span><span class="sxs-lookup"><span data-stu-id="fd202-114">Certificate Response Functions</span></span>](certificate-response-functions.md)
-   [<span data-ttu-id="fd202-115">Funciones de atributo</span><span class="sxs-lookup"><span data-stu-id="fd202-115">Attribute Functions</span></span>](attribute-functions.md)
-   [<span data-ttu-id="fd202-116">Funciones de extensión</span><span class="sxs-lookup"><span data-stu-id="fd202-116">Extension Functions</span></span>](extension-functions.md)
-   [<span data-ttu-id="fd202-117">Funciones de propiedad externa</span><span class="sxs-lookup"><span data-stu-id="fd202-117">External Property Functions</span></span>](external-property-functions.md)
-   [<span data-ttu-id="fd202-118">Funciones de clave pública y privada</span><span class="sxs-lookup"><span data-stu-id="fd202-118">Private and Public Key Functions</span></span>](private-and-public-key-functions.md)
-   [<span data-ttu-id="fd202-119">Funciones de proveedor de servicios criptográficos</span><span class="sxs-lookup"><span data-stu-id="fd202-119">Cryptographic Service Provider Functions</span></span>](cryptographic-service-provider-functions.md)
-   [<span data-ttu-id="fd202-120">Funciones del almacén de certificados</span><span class="sxs-lookup"><span data-stu-id="fd202-120">Certificate Store Functions</span></span>](certificate-store-functions.md)
-   [<span data-ttu-id="fd202-121">Funciones de intercambio de información personal</span><span class="sxs-lookup"><span data-stu-id="fd202-121">Personal Information Exchange Functions</span></span>](personal-information-exchange-functions.md)
-   [<span data-ttu-id="fd202-122">Funciones auxiliares</span><span class="sxs-lookup"><span data-stu-id="fd202-122">Helper Functions</span></span>](helper-functions.md)

## <a name="related-topics"></a><span data-ttu-id="fd202-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="fd202-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fd202-124">Uso de la API de inscripción de certificados</span><span class="sxs-lookup"><span data-stu-id="fd202-124">Using the Certificate Enrollment API</span></span>](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

 
