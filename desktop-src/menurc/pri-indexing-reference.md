---
title: Referencia de indexación de recursos de paquetes (PRI)
description: Referencia de indexación de recursos de paquetes (PRI)
ms.assetid: 15f41d83-d729-45e4-a6bb-5f8c6b78293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef99acafe4fbdadef26c5947145ad734ec44b7bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108117553"
---
# <a name="package-resource-indexing-pri-reference"></a><span data-ttu-id="33cc5-103">Referencia de indexación de recursos de paquetes (PRI)</span><span class="sxs-lookup"><span data-stu-id="33cc5-103">Package resource indexing (PRI) reference</span></span>

<span data-ttu-id="33cc5-104">Conjunto de API para trabajar con un indexador de recursos.</span><span class="sxs-lookup"><span data-stu-id="33cc5-104">A set of APIs for working with a resource indexer.</span></span> <span data-ttu-id="33cc5-105">Un indexador de recursos se usa para generar archivos de índice de recursos de paquete (PRI) para una aplicación para UWP.</span><span class="sxs-lookup"><span data-stu-id="33cc5-105">A resource indexer is used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="33cc5-106">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, consulte API de indexación de recursos de paquetes (PRI) y sistemas [de compilación personalizados.](/windows/uwp/app-resources/pri-apis-custom-build-systems)</span><span class="sxs-lookup"><span data-stu-id="33cc5-106">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="33cc5-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="33cc5-107">In this section</span></span>

<span data-ttu-id="33cc5-108">**Funciones**</span><span class="sxs-lookup"><span data-stu-id="33cc5-108">**Functions**</span></span>

-   <span data-ttu-id="33cc5-109">[**Función MrmCreateConfig**](mrmcreateconfig.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-109">[**MrmCreateConfig**](mrmcreateconfig.md) function</span></span>
-   <span data-ttu-id="33cc5-110">[**Función MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) function</span></span>
-   <span data-ttu-id="33cc5-111">[**Función MrmCreateResourceFile**](mrmcreateresourcefile.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) function</span></span>
-   <span data-ttu-id="33cc5-112">[**Función MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) function</span></span>
-   <span data-ttu-id="33cc5-113">[**Función MrmCreateResourceIndexer**](mrmcreateresourceindexer.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) function</span></span>
-   <span data-ttu-id="33cc5-114">[**Función MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) function</span></span>
-   <span data-ttu-id="33cc5-115">[**Función MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) function</span></span>
-   <span data-ttu-id="33cc5-116">[**Función MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) function</span></span>
-   <span data-ttu-id="33cc5-117">[**Función MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) function</span></span>
-   <span data-ttu-id="33cc5-118">[**Función MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) function</span></span>
-   <span data-ttu-id="33cc5-119">[**Función MrmDumpPriFile**](mrmdumpprifile.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-119">[**MrmDumpPriFile**](mrmdumpprifile.md) function</span></span>
-   <span data-ttu-id="33cc5-120">[**Función MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) function</span></span>
-   <span data-ttu-id="33cc5-121">[**Función MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) function</span></span>
-   <span data-ttu-id="33cc5-122">[**Función MrmFreeMemory**](mrmfreememory.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-122">[**MrmFreeMemory**](mrmfreememory.md) function</span></span>
-   <span data-ttu-id="33cc5-123">[**Función MrmIndexEmbeddedData**](mrmindexembeddeddata.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) function</span></span>
-   <span data-ttu-id="33cc5-124">[**Función MrmIndexFile**](mrmindexfile.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-124">[**MrmIndexFile**](mrmindexfile.md) function</span></span>
-   <span data-ttu-id="33cc5-125">[**Función MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) function</span></span>
-   <span data-ttu-id="33cc5-126">[**Función MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) function</span></span>
-   <span data-ttu-id="33cc5-127">[**Función MrmIndexString**](mrmindexstring.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-127">[**MrmIndexString**](mrmindexstring.md) function</span></span>
-   <span data-ttu-id="33cc5-128">[**Función MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) function</span></span>

<span data-ttu-id="33cc5-129">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="33cc5-129">**Structures**</span></span>

-   <span data-ttu-id="33cc5-130">[**MrmResourceIndexerHandle (estructura)**](mrmresourceindexerhandle.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-130">[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) structure</span></span>
-   <span data-ttu-id="33cc5-131">[**Estructura MrmResourceIndexerMessage**](mrmresourceindexermessage.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-131">[**MrmResourceIndexerMessage**](mrmresourceindexermessage.md) structure</span></span>

<span data-ttu-id="33cc5-132">**Enumeraciones**</span><span class="sxs-lookup"><span data-stu-id="33cc5-132">**Enumerations**</span></span>

-   <span data-ttu-id="33cc5-133">[**Enumeración MrmDumpType**](mrmdumptype.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-133">[**MrmDumpType**](mrmdumptype.md) enumeration</span></span>
-   <span data-ttu-id="33cc5-134">[**Enumeración MrmPackagingMode**](mrmpackagingmode.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-134">[**MrmPackagingMode**](mrmpackagingmode.md) enumeration</span></span>
-   <span data-ttu-id="33cc5-135">[**Enumeración MrmPackagingOptions**](mrmpackagingoptions.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-135">[**MrmPackagingOptions**](mrmpackagingoptions.md) enumeration</span></span>
-   <span data-ttu-id="33cc5-136">[**Enumeración MrmPlatformVersion**](mrmplatformversion.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-136">[**MrmPlatformVersion**](mrmplatformversion.md) enumeration</span></span>
-   <span data-ttu-id="33cc5-137">[**MrmResourceIndexerMessageSeverity (enumeración)**](mrmresourceindexermessageseverity.md)</span><span class="sxs-lookup"><span data-stu-id="33cc5-137">[**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md) enumeration</span></span>

 

 
