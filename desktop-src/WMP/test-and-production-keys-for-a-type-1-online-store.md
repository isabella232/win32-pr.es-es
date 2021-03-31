---
title: Claves de prueba y de producción para una tienda en línea de tipo 1
description: Claves de prueba y de producción para una tienda en línea de tipo 1
ms.assetid: 1a975c0b-16b8-4da7-8594-316ae34257d0
keywords:
- Windows Media Player tiendas en línea, claves de prueba
- tiendas en línea, claves de prueba
- tipo 1 almacenes en línea, claves de prueba
- Windows Media Player tiendas en línea, claves de producción
- tiendas en línea, claves de producción
- tipo 1 almacenes en línea, claves de producción
- Windows Media Player tiendas en línea, documento de ServiceInfo
- tiendas en línea, documento de ServiceInfo
- tipo 1 tiendas en línea, documento de ServiceInfo
- claves de prueba
- claves de producción
- Documento ServiceInfo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0e8ce8d049df78f186d336079f76eb00eb8bb10
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419036"
---
# <a name="test-and-production-keys-for-a-type-1-online-store"></a><span data-ttu-id="ee49a-115">Claves de prueba y de producción para una tienda en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="ee49a-115">Test and Production Keys for a Type 1 Online Store</span></span>

<span data-ttu-id="ee49a-116">Al comenzar el desarrollo de la tienda en línea, Microsoft proporciona dos claves numéricas: una clave de prueba y una clave de producción.</span><span class="sxs-lookup"><span data-stu-id="ee49a-116">When you begin development of your online store, Microsoft provides you with two numeric keys: a test key and a production key.</span></span> <span data-ttu-id="ee49a-117">Al mismo tiempo, debe proporcionar a Microsoft dos direcciones URL: una que apunte al documento ServiceInfo de prueba y otra que apunte al documento ServiceInfo de producción.</span><span class="sxs-lookup"><span data-stu-id="ee49a-117">At the same time, you must provide Microsoft with two URLs: one that points to your test ServiceInfo document and one that points to your production ServiceInfo document.</span></span>

<span data-ttu-id="ee49a-118">Durante la fase de desarrollo y pruebas, la tienda en línea solo es visible en Windows Media Player si la clave de prueba o la clave de producción se encuentra en el registro del equipo del usuario.</span><span class="sxs-lookup"><span data-stu-id="ee49a-118">During the development and testing stage, your online store is visible in Windows Media Player only if your test key or your production key is in the registry on the user's computer.</span></span> <span data-ttu-id="ee49a-119">Si la clave de prueba está en el registro, Windows Media Player recupera el documento de la prueba ServiceInfo, que señala al complemento, las páginas web y las imágenes que pertenecen a su almacén de pruebas.</span><span class="sxs-lookup"><span data-stu-id="ee49a-119">If your test key is in the registry, Windows Media Player retrieves your test ServiceInfo document, which points to the plug-in, webpages, and images that belong to your test store.</span></span> <span data-ttu-id="ee49a-120">Si la clave de producción está en el registro, Windows Media Player recupera el documento ServiceInfo de producción, que señala el complemento, las páginas web y las imágenes que pertenecen a la tienda de producción.</span><span class="sxs-lookup"><span data-stu-id="ee49a-120">If your production key is in the registry, Windows Media Player retrieves your production ServiceInfo document, which points to the plug-in, webpages, and images that belong to your production store.</span></span>

<span data-ttu-id="ee49a-121">Puede usar sus almacenes de prueba y producción de la forma que le resulte útil.</span><span class="sxs-lookup"><span data-stu-id="ee49a-121">You can use your test and production stores in any way that you find useful.</span></span> <span data-ttu-id="ee49a-122">Sin embargo, normalmente, la distinción es la siguiente:</span><span class="sxs-lookup"><span data-stu-id="ee49a-122">Typically, however, the distinction is as follows:</span></span>

-   <span data-ttu-id="ee49a-123">El almacén de pruebas es el lugar donde se realizan los cambios diarios en el complemento, las páginas web, las imágenes y otros componentes del servicio.</span><span class="sxs-lookup"><span data-stu-id="ee49a-123">Your test store is the place where you make daily changes to your plug-in, webpages, images, and other components of your service.</span></span>
-   <span data-ttu-id="ee49a-124">La tienda de producción es el lugar donde se mantiene una versión estable del servicio, que incluye el complemento, las páginas web, las imágenes y otros componentes.</span><span class="sxs-lookup"><span data-stu-id="ee49a-124">Your production store is the place where you keep a stable release of your service, which includes your plug-in, webpages, images, and other components.</span></span>

<span data-ttu-id="ee49a-125">Antes de que la tienda en línea pueda publicarse en Windows Media Player, Microsoft debe validar que el servicio funciona correctamente.</span><span class="sxs-lookup"><span data-stu-id="ee49a-125">Before your online store can be published in Windows Media Player, Microsoft must validate that your service performs correctly.</span></span> <span data-ttu-id="ee49a-126">Durante la fase de validación, Microsoft utiliza su clave de producción.</span><span class="sxs-lookup"><span data-stu-id="ee49a-126">During the validation phase, Microsoft uses your production key.</span></span> <span data-ttu-id="ee49a-127">Microsoft no usa la clave de prueba durante la fase de validación.</span><span class="sxs-lookup"><span data-stu-id="ee49a-127">Microsoft does not use your test key during the validation phase.</span></span>

<span data-ttu-id="ee49a-128">Cuando la tienda en línea de producción completa correctamente el proceso de validación, Microsoft publica la tienda, lo que significa que la tienda de producción aparece en Windows Media Player para todos los usuarios, no solo en las que tienen la clave de producción en el registro.</span><span class="sxs-lookup"><span data-stu-id="ee49a-128">When your production online store successfully completes the validation process, Microsoft publishes your store, which means that your production store appears in Windows Media Player for all users, not just the ones who have your production key in the registry.</span></span> <span data-ttu-id="ee49a-129">Una vez publicada la tienda, ya no se necesitan las claves de prueba y de producción.</span><span class="sxs-lookup"><span data-stu-id="ee49a-129">After your store is published, the test and production keys are no longer needed.</span></span>

> [!Note]  
> <span data-ttu-id="ee49a-130">Es posible que los usuarios puedan adivinar la clave de prueba o de producción de la tienda en línea y ver la tienda mientras se desarrolla.</span><span class="sxs-lookup"><span data-stu-id="ee49a-130">Users might be able to guess the test or production key for your online store and view your store while it is being developed.</span></span> <span data-ttu-id="ee49a-131">Debe tener cuidado al exponer las características que desea mantener como secreto hasta la versión pública.</span><span class="sxs-lookup"><span data-stu-id="ee49a-131">You should be careful about exposing features that you want to keep secret until public release.</span></span>

 

<span data-ttu-id="ee49a-132">Para obtener información detallada sobre dónde colocar las claves de producción y prueba en el registro del usuario, consulte [claves del registro y entradas para una tienda en línea de tipo 1](registry-keys-and-entries-for-a-type-1-online-store.md).</span><span class="sxs-lookup"><span data-stu-id="ee49a-132">For detailed information about where to put your production and test keys in the user's registry, see [Registry Keys and Entries for a Type 1 Online Store](registry-keys-and-entries-for-a-type-1-online-store.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="ee49a-133">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="ee49a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ee49a-134">**Acerca de las tiendas en línea de tipo 1**</span><span class="sxs-lookup"><span data-stu-id="ee49a-134">**About Type 1 Online Stores**</span></span>](about-type-1-online-stores.md)
</dt> </dl>

 

 




