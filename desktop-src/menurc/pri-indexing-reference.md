---
title: Referencia de indexación de recursos de paquetes (PRI)
description: .
ms.assetid: 15f41d83-d729-45e4-a6bb-5f8c6b78293c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b75c0739b4e7673863a21223fbed749c27e65dc4
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103995257"
---
# <a name="package-resource-indexing-pri-reference"></a><span data-ttu-id="06982-103">Referencia de indexación de recursos de paquetes (PRI)</span><span class="sxs-lookup"><span data-stu-id="06982-103">Package resource indexing (PRI) reference</span></span>

<span data-ttu-id="06982-104">Un conjunto de API para trabajar con un indizador de recursos.</span><span class="sxs-lookup"><span data-stu-id="06982-104">A set of APIs for working with a resource indexer.</span></span> <span data-ttu-id="06982-105">Un indizador de recursos se usa para generar los archivos de índice de recursos del paquete (PRI) para una aplicación para UWP.</span><span class="sxs-lookup"><span data-stu-id="06982-105">A resource indexer is used to generate package resource index (PRI) files for a UWP app.</span></span> <span data-ttu-id="06982-106">Para obtener más información y tutoriales basados en escenarios sobre cómo usar estas API, vea [API de indexación de recursos de paquetes (PRI) y sistemas de compilación personalizados](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span><span class="sxs-lookup"><span data-stu-id="06982-106">For more info, and scenario-based walkthroughs of how to use these APIs, see [Package resource indexing (PRI) APIs and custom build systems](/windows/uwp/app-resources/pri-apis-custom-build-systems).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="06982-107">En esta sección</span><span class="sxs-lookup"><span data-stu-id="06982-107">In this section</span></span>

<span data-ttu-id="06982-108">**Funciones**</span><span class="sxs-lookup"><span data-stu-id="06982-108">**Functions**</span></span>

-   <span data-ttu-id="06982-109">[**MrmCreateConfig**](mrmcreateconfig.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-109">[**MrmCreateConfig**](mrmcreateconfig.md) function</span></span>
-   <span data-ttu-id="06982-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-110">[**MrmCreateConfigInMemory**](mrmcreateconfiginmemory.md) function</span></span>
-   <span data-ttu-id="06982-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-111">[**MrmCreateResourceFile**](mrmcreateresourcefile.md) function</span></span>
-   <span data-ttu-id="06982-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-112">[**MrmCreateResourceFileInMemory**](mrmcreateresourcefileinmemory.md) function</span></span>
-   <span data-ttu-id="06982-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-113">[**MrmCreateResourceIndexer**](mrmcreateresourceindexer.md) function</span></span>
-   <span data-ttu-id="06982-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-114">[**MrmCreateResourceIndexerFromPreviousPriData**](mrmcreateresourceindexerfrompreviouspridata-.md) function</span></span>
-   <span data-ttu-id="06982-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-115">[**MrmCreateResourceIndexerFromPreviousPriFile**](mrmcreateresourceindexerfrompreviousprifile.md) function</span></span>
-   <span data-ttu-id="06982-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-116">[**MrmCreateResourceIndexerFromPreviousSchemaData**](mrmcreateresourceindexerfrompreviousschemadata.md) function</span></span>
-   <span data-ttu-id="06982-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-117">[**MrmCreateResourceIndexerFromPreviousSchemaFile**](mrmcreateresourceindexerfrompreviousschemafile.md) function</span></span>
-   <span data-ttu-id="06982-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-118">[**MrmDestroyIndexerAndMessages**](mrmdestroyindexerandmessages.md) function</span></span>
-   <span data-ttu-id="06982-119">[**MrmDumpPriFile**](mrmdumpprifile.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-119">[**MrmDumpPriFile**](mrmdumpprifile.md) function</span></span>
-   <span data-ttu-id="06982-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-120">[**MrmDumpPriFileInMemory**](mrmdumpprifileinmemory.md) function</span></span>
-   <span data-ttu-id="06982-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-121">[**MrmDumpPriDataInMemory**](mrmdumppridatainmemory.md) function</span></span>
-   <span data-ttu-id="06982-122">[**MrmFreeMemory**](mrmfreememory.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-122">[**MrmFreeMemory**](mrmfreememory.md) function</span></span>
-   <span data-ttu-id="06982-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-123">[**MrmIndexEmbeddedData**](mrmindexembeddeddata.md) function</span></span>
-   <span data-ttu-id="06982-124">[**MrmIndexFile**](mrmindexfile.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-124">[**MrmIndexFile**](mrmindexfile.md) function</span></span>
-   <span data-ttu-id="06982-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-125">[**MrmIndexFileAutoQualifiers**](mrmindexfileautoqualifiers.md) function</span></span>
-   <span data-ttu-id="06982-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-126">[**MrmIndexResourceContainerAutoQualifiers**](mrmindexresourcecontainerautoqualifiers.md) function</span></span>
-   <span data-ttu-id="06982-127">[**MrmIndexString**](mrmindexstring.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-127">[**MrmIndexString**](mrmindexstring.md) function</span></span>
-   <span data-ttu-id="06982-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) función)</span><span class="sxs-lookup"><span data-stu-id="06982-128">[**MrmPeekResourceIndexerMessages**](mrmpeekresourceindexermessages.md) function</span></span>

<span data-ttu-id="06982-129">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="06982-129">**Structures**</span></span>

-   <span data-ttu-id="06982-130">Estructura [**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md)</span><span class="sxs-lookup"><span data-stu-id="06982-130">[**MrmResourceIndexerHandle**](mrmresourceindexerhandle.md) structure</span></span>
-   <span data-ttu-id="06982-131">Estructura [**MrmResourceIndexerMessage**](mrmresourceindexermessage.md)</span><span class="sxs-lookup"><span data-stu-id="06982-131">[**MrmResourceIndexerMessage**](mrmresourceindexermessage.md) structure</span></span>

<span data-ttu-id="06982-132">**Enumeraciones**</span><span class="sxs-lookup"><span data-stu-id="06982-132">**Enumerations**</span></span>

-   <span data-ttu-id="06982-133">Enumeración [**MrmDumpType**](mrmdumptype.md)</span><span class="sxs-lookup"><span data-stu-id="06982-133">[**MrmDumpType**](mrmdumptype.md) enumeration</span></span>
-   <span data-ttu-id="06982-134">Enumeración [**MrmPackagingMode**](mrmpackagingmode.md)</span><span class="sxs-lookup"><span data-stu-id="06982-134">[**MrmPackagingMode**](mrmpackagingmode.md) enumeration</span></span>
-   <span data-ttu-id="06982-135">Enumeración [**MrmPackagingOptions**](mrmpackagingoptions.md)</span><span class="sxs-lookup"><span data-stu-id="06982-135">[**MrmPackagingOptions**](mrmpackagingoptions.md) enumeration</span></span>
-   <span data-ttu-id="06982-136">Enumeración [**MrmPlatformVersion**](mrmplatformversion.md)</span><span class="sxs-lookup"><span data-stu-id="06982-136">[**MrmPlatformVersion**](mrmplatformversion.md) enumeration</span></span>
-   <span data-ttu-id="06982-137">Enumeración [**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md)</span><span class="sxs-lookup"><span data-stu-id="06982-137">[**MrmResourceIndexerMessageSeverity**](mrmresourceindexermessageseverity.md) enumeration</span></span>

 

 