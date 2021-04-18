---
title: Consideraciones para los mercados internacionales
description: Consideraciones para los mercados internacionales
ms.assetid: 890a280d-a4e0-4349-960d-ca8ac1872ee6
keywords:
- Windows Media Player tiendas en línea, mercados internacionales
- tiendas en línea, mercados internacionales
- tipo 1 tiendas en línea, mercados internacionales
- tipo 2 tiendas en línea, mercados internacionales
- mercados internacionales
- Windows Media Player tiendas en línea, documento de ServiceInfo
- tiendas en línea, documento de ServiceInfo
- tipo 1 tiendas en línea, documento de ServiceInfo
- tipo 2 tiendas en línea, documento de ServiceInfo
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1822e4f647c9967d50d40fa19331cd58565cf2eb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695368"
---
# <a name="considerations-for-international-markets"></a><span data-ttu-id="dbe22-113">Consideraciones para los mercados internacionales</span><span class="sxs-lookup"><span data-stu-id="dbe22-113">Considerations for International Markets</span></span>

<span data-ttu-id="dbe22-114">Si su empresa crea tiendas en línea para varios mercados, debe proporcionar a Microsoft la dirección URL de un documento de ServiceInfo para cada mercado.</span><span class="sxs-lookup"><span data-stu-id="dbe22-114">If your company creates online stores for multiple markets, you must provide Microsoft with the URL of a ServiceInfo document for each market.</span></span> <span data-ttu-id="dbe22-115">Puede hacer esto de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="dbe22-115">You can do this one of the following two ways:</span></span>

-   <span data-ttu-id="dbe22-116">Cree un documento ServiceInfo independiente para cada mercado.</span><span class="sxs-lookup"><span data-stu-id="dbe22-116">Create a separate ServiceInfo document for each market.</span></span> <span data-ttu-id="dbe22-117">En este caso, proporciona a Microsoft las direcciones URL que apuntan a documentos de ServiceInfo individuales para cada tienda en línea en cada mercado.</span><span class="sxs-lookup"><span data-stu-id="dbe22-117">In this case, you provide Microsoft with URLs that point to individual ServiceInfo documents for each online store in each market.</span></span>
-   <span data-ttu-id="dbe22-118">Cree un único documento ServiceInfo para todos los mercados.</span><span class="sxs-lookup"><span data-stu-id="dbe22-118">Create a single ServiceInfo document for all markets.</span></span> <span data-ttu-id="dbe22-119">Al hacerlo, proporciona a Microsoft la misma dirección URL para cada mercado.</span><span class="sxs-lookup"><span data-stu-id="dbe22-119">When you do this, you provide Microsoft with the same URL for each market.</span></span> <span data-ttu-id="dbe22-120">El documento ServiceInfo, creado como una página ASP, puede detectar dinámicamente la ubicación del usuario en función de los parámetros de la cadena de consulta.</span><span class="sxs-lookup"><span data-stu-id="dbe22-120">Your ServiceInfo document, created as an ASP page, can then dynamically detect the user's location based on query string parameters.</span></span>

<span data-ttu-id="dbe22-121">Windows Media Player anexa una cadena de consulta a la solicitud URL de ServiceInfo que proporciona información sobre la configuración regional y de ubicación del usuario.</span><span class="sxs-lookup"><span data-stu-id="dbe22-121">Windows Media Player appends a query string to the ServiceInfo URL request that provides information about the user's locale and location settings.</span></span> <span data-ttu-id="dbe22-122">Si la tienda en línea usa esta información para determinar el contenido que se va a mostrar, debe anexar dinámicamente estos valores a sus propias direcciones URL en el documento de ServiceInfo.</span><span class="sxs-lookup"><span data-stu-id="dbe22-122">If your online store uses this information to determine which content to display, you should dynamically append these values to your own URLs in your ServiceInfo document.</span></span> <span data-ttu-id="dbe22-123">Esta es la mejor manera de asegurarse de que las direcciones URL de la página web siempre contendrán los parámetros esperados.</span><span class="sxs-lookup"><span data-stu-id="dbe22-123">This is the best way to ensure that your webpage URLs will always contain the parameters you expect.</span></span>

<span data-ttu-id="dbe22-124">Una vez que haya determinado la ubicación del usuario y la preferencia de idioma, es posible que desee conservar esta información para futuras sesiones.</span><span class="sxs-lookup"><span data-stu-id="dbe22-124">Once you have determined the user's location and language preference, you may want to persist this information for future sessions.</span></span> <span data-ttu-id="dbe22-125">Para ello, puede usar cualquiera de las técnicas que usaría normalmente en una página web, como cookies, o mediante el objeto COM.</span><span class="sxs-lookup"><span data-stu-id="dbe22-125">You can do this using any of the techniques you would normally use in a webpage, such as cookies, or by using your COM object.</span></span>

## <a name="related-topics"></a><span data-ttu-id="dbe22-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dbe22-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dbe22-127">**Creación dinámica del documento ServiceInfo**</span><span class="sxs-lookup"><span data-stu-id="dbe22-127">**Creating the ServiceInfo Document Dynamically**</span></span>](creating-the-serviceinfo-document-dynamically.md)
</dt> <dt>

[<span data-ttu-id="dbe22-128">**Información común para las tiendas en línea de tipo 1 y 2**</span><span class="sxs-lookup"><span data-stu-id="dbe22-128">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> <dt>

[<span data-ttu-id="dbe22-129">**ServiceInfo, elemento**</span><span class="sxs-lookup"><span data-stu-id="dbe22-129">**ServiceInfo Element**</span></span>](serviceinfo-element.md)
</dt> </dl>

 

 




