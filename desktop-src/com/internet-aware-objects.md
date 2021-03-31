---
title: Objetos Internet-Aware
description: Objetos Internet-Aware
ms.assetid: a8228431-5a07-4816-938d-c789ab6a8eaa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 806b8887309760417247cb176c84cda1605bd5aa
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/21/2020
ms.locfileid: "103995675"
---
# <a name="internet-aware-objects"></a><span data-ttu-id="43bbc-103">Objetos Internet-Aware</span><span class="sxs-lookup"><span data-stu-id="43bbc-103">Internet-Aware Objects</span></span>

<span data-ttu-id="43bbc-104">Existen ciertas categorías identificadas para cubrir las interfaces de persistencia; se han identificado como resultado de la definición del modo en que los controles funcionan a través de Internet.</span><span class="sxs-lookup"><span data-stu-id="43bbc-104">There are certain categories identified to cover the persistency interfaces; these have been identified as a result of defining how controls function across the Internet.</span></span> <span data-ttu-id="43bbc-105">Un contenedor que no admite el intervalo completo de interfaces persistencia debe asegurarse de que no hospeda un control que requiera una combinación de interfaces que no admita.</span><span class="sxs-lookup"><span data-stu-id="43bbc-105">A container that does not support the full range of persistency interfaces should ensure that it does not host a control that requires a combination of interfaces that it does not support.</span></span>

<span data-ttu-id="43bbc-106">En las tablas siguientes se describe el significado de varias categorías como categorías implementadas y necesarias.</span><span class="sxs-lookup"><span data-stu-id="43bbc-106">The following tables describe the meaning for various categories as both implemented and required categories.</span></span>



| <span data-ttu-id="43bbc-107">Categorías requeridas</span><span class="sxs-lookup"><span data-stu-id="43bbc-107">Required Categories</span></span>                                                                                                                                                                                | <span data-ttu-id="43bbc-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="43bbc-108">Description</span></span>                                                                                                                                                                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43bbc-109">CATId \_ PersistsToMoniker, CATID \_ PERSISTSTOSTREAMINIT, CATID \_ PersisitsToStream, CATID \_ PersistsToStorage, CATId \_ PersistsToMemory, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag</span><span class="sxs-lookup"><span data-stu-id="43bbc-109">CATID\_PersistsToMoniker, CATID\_PersistsToStreamInit, CATID\_PersisitsToStream, CATID\_PersistsToStorage, CATID\_PersistsToMemory, CATID\_PersistsToFile, CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="43bbc-110">Cada una de estas categorías es mutuamente excluyente y solo se usa cuando un objeto solo admite un mecanismo de persistencia en absoluto (por lo tanto, la exclusión mutua).</span><span class="sxs-lookup"><span data-stu-id="43bbc-110">Each of these categories is mutually exclusive and only used when an object supports only one persistence mechanism at all (hence the mutual exclusion).</span></span> <span data-ttu-id="43bbc-111">Los contenedores que no admiten el mecanismo de persistencia descrito por una de estas categorías deben evitar que se creen objetos de clases, por lo que se marcan como.</span><span class="sxs-lookup"><span data-stu-id="43bbc-111">Containers that do not support the persistence mechanism described by one of these categories should prevent themselves from creating any objects of classes so marked.</span></span><br/> |
| <span data-ttu-id="43bbc-112">CATId \_ RequiresDataPathHost</span><span class="sxs-lookup"><span data-stu-id="43bbc-112">CATID\_RequiresDataPathHost</span></span><br/>                                                                                                                                                             | <span data-ttu-id="43bbc-113">El objeto requiere la capacidad de guardar los datos en una o varias rutas de acceso y requiere la implicación del contenedor, por lo que se necesita compatibilidad con contenedores para [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="43bbc-113">The object requires the ability to save data to one or more paths and requires container involvement, therefore requiring container support for [**IBindHost**](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms775076(v=vs.85)).</span></span><br/>                                                                                                                                  |



 



| <span data-ttu-id="43bbc-114">Categorías implementadas</span><span class="sxs-lookup"><span data-stu-id="43bbc-114">Implemented Categories</span></span>                                                                                                                                                                            | <span data-ttu-id="43bbc-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="43bbc-115">Description</span></span>                                                                         |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="43bbc-116">CATId \_ PersistsToMoniker, CATID \_ PERSISTSTOSTREAMINIT, CATID \_ PersistsToStream, CATID \_ PersistsToStorage, CATId \_ PersistsToMemory, CATID \_ PersistsToFile, CATID \_ PersistsToPropertyBag</span><span class="sxs-lookup"><span data-stu-id="43bbc-116">CATID\_PersistsToMoniker, CATID\_PersistsToStreamInit, CATID\_PersistsToStream, CATID\_PersistsToStorage, CATID\_PersistsToMemory, CATID\_PersistsToFile, CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="43bbc-117">El objeto admite el mecanismo IPersist correspondiente \* para la categoría.</span><span class="sxs-lookup"><span data-stu-id="43bbc-117">Object supports the corresponding IPersist\* mechanism for the category.</span></span><br/> |



 

<span data-ttu-id="43bbc-118">En la tabla siguiente se proporcionan los CATID exactos asignados a cada categoría:</span><span class="sxs-lookup"><span data-stu-id="43bbc-118">The following table provides the exact CATIDs assigned to each category:</span></span>



| <span data-ttu-id="43bbc-119">Category</span><span class="sxs-lookup"><span data-stu-id="43bbc-119">Category</span></span>                                | <span data-ttu-id="43bbc-120">CATID</span><span class="sxs-lookup"><span data-stu-id="43bbc-120">CATID</span></span>                                           |
|-----------------------------------------|-------------------------------------------------|
| <span data-ttu-id="43bbc-121">CATId \_ RequiresDataPathHost</span><span class="sxs-lookup"><span data-stu-id="43bbc-121">CATID\_RequiresDataPathHost</span></span><br/>  | <span data-ttu-id="43bbc-122">0de86a50-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="43bbc-122">0de86a50-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="43bbc-123">CATId \_ PersistsToMoniker</span><span class="sxs-lookup"><span data-stu-id="43bbc-123">CATID\_PersistsToMoniker</span></span> <br/>    | <span data-ttu-id="43bbc-124">0de86a51-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="43bbc-124">0de86a51-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="43bbc-125">CATId \_ PersistsToStorage</span><span class="sxs-lookup"><span data-stu-id="43bbc-125">CATID\_PersistsToStorage</span></span> <br/>    | <span data-ttu-id="43bbc-126">0de86a52-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="43bbc-126">0de86a52-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="43bbc-127">CATId \_ PersistsToStreamInit</span><span class="sxs-lookup"><span data-stu-id="43bbc-127">CATID\_PersistsToStreamInit</span></span> <br/> | <span data-ttu-id="43bbc-128">0de86a53-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="43bbc-128">0de86a53-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="43bbc-129">CATId \_ PersistsToStream</span><span class="sxs-lookup"><span data-stu-id="43bbc-129">CATID\_PersistsToStream</span></span> <br/>     | <span data-ttu-id="43bbc-130">0de86a54-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="43bbc-130">0de86a54-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="43bbc-131">CATId \_ PersistsToMemory</span><span class="sxs-lookup"><span data-stu-id="43bbc-131">CATID\_PersistsToMemory</span></span> <br/>     | <span data-ttu-id="43bbc-132">0de86a55-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="43bbc-132">0de86a55-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="43bbc-133">CATId \_ PersistsToFile</span><span class="sxs-lookup"><span data-stu-id="43bbc-133">CATID\_PersistsToFile</span></span> <br/>       | <span data-ttu-id="43bbc-134">0de86a56-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="43bbc-134">0de86a56-2baa-11cf-a229-00aa003d7352</span></span><br/> |
| <span data-ttu-id="43bbc-135">CATId \_ PersistsToPropertyBag</span><span class="sxs-lookup"><span data-stu-id="43bbc-135">CATID\_PersistsToPropertyBag</span></span><br/> | <span data-ttu-id="43bbc-136">0de86a57-2baa-11cf-a229-00aa003d7352</span><span class="sxs-lookup"><span data-stu-id="43bbc-136">0de86a57-2baa-11cf-a229-00aa003d7352</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="43bbc-137">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="43bbc-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43bbc-138">Categorías del componente</span><span class="sxs-lookup"><span data-stu-id="43bbc-138">Component Categories</span></span>](component-categories.md)
</dt> </dl>

 

