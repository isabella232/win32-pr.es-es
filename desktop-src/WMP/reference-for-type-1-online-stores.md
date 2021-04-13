---
title: Referencia de las tiendas en línea de tipo 1
description: Referencia de las tiendas en línea de tipo 1
ms.assetid: e6f45a50-029e-4347-9b25-10e9e32a56eb
keywords:
- Windows Media Player tiendas en línea, referencia
- tiendas en línea, referencia
- tipo 1 almacenes en línea, referencia
- referencia de las tiendas en línea de tipo 1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475f7dee43f2f6152c3b3ebd0e6090a1efb33a72
ms.sourcegitcommit: ad672d3a10192c5ccac619ad2524407109266e93
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/25/2020
ms.locfileid: "104420446"
---
# <a name="reference-for-type-1-online-stores"></a><span data-ttu-id="dc0bf-107">Referencia de las tiendas en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="dc0bf-107">Reference for Type 1 Online Stores</span></span>

> [!Note]  
> <span data-ttu-id="dc0bf-108">En esta sección se describe la funcionalidad diseñada para su uso en tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-108">This section describes functionality designed for use by online stores.</span></span> <span data-ttu-id="dc0bf-109">No se admite el uso de esta funcionalidad fuera del contexto de una tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-109">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="dc0bf-110">Windows Media Player 11 proporciona un compilador de catálogo, un objeto y varias interfaces que admiten las tiendas en línea de tipo 1.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-110">Windows Media Player 11 provides a catalog compiler, an object, and several interfaces that support type 1 online stores.</span></span> <span data-ttu-id="dc0bf-111">En las secciones siguientes se documentan en detalle.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-111">The following sections document these in detail.</span></span>



| <span data-ttu-id="dc0bf-112">Sección</span><span class="sxs-lookup"><span data-stu-id="dc0bf-112">Section</span></span>                                                                                    | <span data-ttu-id="dc0bf-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="dc0bf-113">Description</span></span>                                                                                                                                                                                                                        |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="dc0bf-114">Compilador de catálogo para las tiendas en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="dc0bf-114">Catalog Compiler for Type 1 Online Stores</span></span>](catalog-compiler-for-type-1-online-stores.md) | <span data-ttu-id="dc0bf-115">Proporciona material de referencia para el compilador que usa una tienda en línea para compilar su catálogo de música.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-115">Provides reference material for the compiler that an online store uses to compile its music catalog.</span></span>                                                                                                                               |
| [<span data-ttu-id="dc0bf-116">Interfaz IWMPContentContainer</span><span class="sxs-lookup"><span data-stu-id="dc0bf-116">IWMPContentContainer Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainer)                                 | <span data-ttu-id="dc0bf-117">Proporciona páginas de referencia para los métodos a los que llama el complemento de la tienda en línea para inspeccionar un contenedor de contenido.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-117">Provides reference pages for methods that the online store's plug-in calls to inspect a content container.</span></span> <span data-ttu-id="dc0bf-118">Un contenedor de contenido representa un conjunto de elementos multimedia que se van a descargar o comprar.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-118">A content container represents a set of media items to be downloaded or purchased.</span></span> <span data-ttu-id="dc0bf-119">Implementado por Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-119">Implemented by Windows Media Player.</span></span> |
| [<span data-ttu-id="dc0bf-120">Interfaz IWMPContentContainerList</span><span class="sxs-lookup"><span data-stu-id="dc0bf-120">IWMPContentContainerList Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentcontainerlist)                         | <span data-ttu-id="dc0bf-121">Proporciona páginas de referencia para los métodos a los que llama el complemento de la tienda en línea para inspeccionar una lista de contenedores de contenido.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-121">Provides reference pages for methods that the online store's plug-in calls to inspect a list of content containers.</span></span> <span data-ttu-id="dc0bf-122">Implementado por Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-122">Implemented by Windows Media Player.</span></span>                                                                           |
| [<span data-ttu-id="dc0bf-123">Interfaz IWMPContentPartner</span><span class="sxs-lookup"><span data-stu-id="dc0bf-123">IWMPContentPartner Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartner)                                     | <span data-ttu-id="dc0bf-124">Proporciona páginas de referencia para los métodos a los que Windows Media Player llama para obtener información de la tienda en línea y para notificar a la tienda en línea acerca de las acciones del usuario.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-124">Provides reference pages for methods that Windows Media Player calls to get information from the online store and to notify the online store about the user's actions.</span></span> <span data-ttu-id="dc0bf-125">Implementado por el complemento de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-125">Implemented by the online store's plug-in.</span></span>                  |
| [<span data-ttu-id="dc0bf-126">Interfaz IWMPContentPartnerCallback</span><span class="sxs-lookup"><span data-stu-id="dc0bf-126">IWMPContentPartnerCallback Interface</span></span>](/previous-versions/windows/desktop/api/contentpartner/nn-contentpartner-iwmpcontentpartnercallback)                     | <span data-ttu-id="dc0bf-127">Proporciona páginas de referencia para los métodos a los que llama el complemento de la tienda en línea para notificar a Windows Media Player sobre la finalización de las operaciones asincrónicas.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-127">Provides reference pages for methods that the online store's plug-in calls to notify Windows Media Player about the completion of asynchronous operations.</span></span> <span data-ttu-id="dc0bf-128">Implementado por Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-128">Implemented by Windows Media Player.</span></span>                                    |
| [<span data-ttu-id="dc0bf-129">Objeto externo para las tiendas en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="dc0bf-129">External Object for Type 1 Online Stores</span></span>](external-object-for-type-1-online-stores.md)   | <span data-ttu-id="dc0bf-130">Proporciona páginas de referencia para las propiedades, los métodos y los eventos usados por el script en páginas web proporcionadas por la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-130">Provides reference pages for properties, methods, and events used by script in webpages provided by the online store.</span></span>                                                                                                              |
| [<span data-ttu-id="dc0bf-131">Enumeraciones de las tiendas en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="dc0bf-131">Enumerations for Type 1 Online Stores</span></span>](enumerations-for-type-1-online-stores.md)         | <span data-ttu-id="dc0bf-132">Proporciona páginas de referencia para las enumeraciones utilizadas en la comunicación entre Media Player de Windows y el complemento de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-132">Provides reference pages for the enumerations used in the communication between Windows Media Player and the online store's plug-in.</span></span>                                                                                               |
| [<span data-ttu-id="dc0bf-133">Estructuras para tiendas en línea de tipo 1</span><span class="sxs-lookup"><span data-stu-id="dc0bf-133">Structures for Type 1 Online Stores</span></span>](structures-for-type-1-online-stores.md)             | <span data-ttu-id="dc0bf-134">Proporciona páginas de referencia para las estructuras utilizadas en la comunicación entre Media Player de Windows y el complemento de la tienda en línea.</span><span class="sxs-lookup"><span data-stu-id="dc0bf-134">Provides reference pages for the structures used in the communication between Windows Media Player and the online store's plug-in.</span></span>                                                                                                 |



 

## <a name="related-topics"></a><span data-ttu-id="dc0bf-135">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="dc0bf-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="dc0bf-136">**Tipo 1 tiendas en línea**</span><span class="sxs-lookup"><span data-stu-id="dc0bf-136">**Type 1 Online Stores**</span></span>](type-1-online-stores.md)
</dt> </dl>

 

 




