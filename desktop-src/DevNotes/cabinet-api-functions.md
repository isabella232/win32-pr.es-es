---
description: 'Más información sobre: funciones de la API de archivos. cab'
ms.assetid: 43afef50-8fd2-49ec-9fb4-dafd8ebc009e
title: Funciones de la API de archivo. cab
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327490332d2fe0cb9384eeaaad11215d551f4f0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907121"
---
# <a name="cabinet-api-functions"></a><span data-ttu-id="89691-103">Funciones de la API de archivo. cab</span><span class="sxs-lookup"><span data-stu-id="89691-103">Cabinet API Functions</span></span>

<span data-ttu-id="89691-104">En esta sección se describen las siguientes funciones de la API de archivo. cab:</span><span class="sxs-lookup"><span data-stu-id="89691-104">This section describes the following Cabinet API functions:</span></span>

## <a name="fci-functions"></a><span data-ttu-id="89691-105">Características de FCI</span><span class="sxs-lookup"><span data-stu-id="89691-105">FCI Functions</span></span>

<span data-ttu-id="89691-106">La biblioteca FCI (interfaz de compresión de archivos) proporciona la capacidad de crear archivadores (también conocidos como "archivos. CAB").</span><span class="sxs-lookup"><span data-stu-id="89691-106">The FCI (File Compression Interface) library provides the ability to create cabinets (also known as "CAB files").</span></span> <span data-ttu-id="89691-107">Además, la biblioteca proporciona compresión para reducir el tamaño de los datos de archivo almacenados en los archivadores.</span><span class="sxs-lookup"><span data-stu-id="89691-107">Additionally, the library provides compression to reduce the size of the file data stored in cabinets.</span></span>



| <span data-ttu-id="89691-108">Función</span><span class="sxs-lookup"><span data-stu-id="89691-108">Function</span></span>                                   | <span data-ttu-id="89691-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="89691-109">Description</span></span>                                                                                                 |
|--------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89691-110">**FCIAddFile**</span><span class="sxs-lookup"><span data-stu-id="89691-110">**FCIAddFile**</span></span>](/windows/desktop/api/Fci/nf-fci-fciaddfile)           | <span data-ttu-id="89691-111">Agrega un archivo al archivo. cab que se está construye.</span><span class="sxs-lookup"><span data-stu-id="89691-111">Adds a file to the cabinet currently being contructed.</span></span><br/>                                           |
| [<span data-ttu-id="89691-112">**FCICreate**</span><span class="sxs-lookup"><span data-stu-id="89691-112">**FCICreate**</span></span>](/windows/desktop/api/Fci/nf-fci-fcicreate)             | <span data-ttu-id="89691-113">Crea un contexto de FCI.</span><span class="sxs-lookup"><span data-stu-id="89691-113">Creates an FCI context.</span></span><br/>                                                                          |
| [<span data-ttu-id="89691-114">**FCIDestroy**</span><span class="sxs-lookup"><span data-stu-id="89691-114">**FCIDestroy**</span></span>](/windows/desktop/api/Fci/nf-fci-fcidestroy)           | <span data-ttu-id="89691-115">Elimina un contexto de FCI abierto, liberando la memoria y los archivos temporales asociados al contexto.</span><span class="sxs-lookup"><span data-stu-id="89691-115">Deletes an open FCI context, freeing any memory and temporary files associated with the context.</span></span><br/> |
| [<span data-ttu-id="89691-116">**FCIFlushCabinet**</span><span class="sxs-lookup"><span data-stu-id="89691-116">**FCIFlushCabinet**</span></span>](/windows/desktop/api/Fci/nf-fci-fciflushcabinet) | <span data-ttu-id="89691-117">Completa el archivo. cab actual.</span><span class="sxs-lookup"><span data-stu-id="89691-117">Completes the current cabinet.</span></span><br/>                                                                   |
| [<span data-ttu-id="89691-118">**FCIFlushFolder**</span><span class="sxs-lookup"><span data-stu-id="89691-118">**FCIFlushFolder**</span></span>](/windows/desktop/api/Fci/nf-fci-fciflushfolder)   | <span data-ttu-id="89691-119">Fuerza la finalización inmediata de la carpeta actual en construcción.</span><span class="sxs-lookup"><span data-stu-id="89691-119">Forces the current folder under construction to be completed immediately.</span></span><br/>                        |



 

## <a name="fdi-functions"></a><span data-ttu-id="89691-120">Funciones FDI</span><span class="sxs-lookup"><span data-stu-id="89691-120">FDI Functions</span></span>

<span data-ttu-id="89691-121">La biblioteca FDI (interfaz de descompresión de archivos) proporciona la capacidad de extraer archivos de los archivadores.</span><span class="sxs-lookup"><span data-stu-id="89691-121">The FDI (File Decompression Interface) library provides the ability to extract files from cabinets.</span></span>



| <span data-ttu-id="89691-122">Función</span><span class="sxs-lookup"><span data-stu-id="89691-122">Function</span></span>                                         | <span data-ttu-id="89691-123">Descripción</span><span class="sxs-lookup"><span data-stu-id="89691-123">Description</span></span>                                                                                       |
|--------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="89691-124">**FDICopy**</span><span class="sxs-lookup"><span data-stu-id="89691-124">**FDICopy**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdicopy)                       | <span data-ttu-id="89691-125">Extrae archivos de los archivadores.</span><span class="sxs-lookup"><span data-stu-id="89691-125">Extracts files from cabinets.</span></span><br/>                                                          |
| [<span data-ttu-id="89691-126">**FDICreate**</span><span class="sxs-lookup"><span data-stu-id="89691-126">**FDICreate**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdicreate)                   | <span data-ttu-id="89691-127">Crea un contexto FDI.</span><span class="sxs-lookup"><span data-stu-id="89691-127">Creates an FDI context.</span></span><br/>                                                                |
| [<span data-ttu-id="89691-128">**FDIDestroy**</span><span class="sxs-lookup"><span data-stu-id="89691-128">**FDIDestroy**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdidestroy)                 | <span data-ttu-id="89691-129">Elimina un contexto FDI abierto.</span><span class="sxs-lookup"><span data-stu-id="89691-129">Deletes an open FDI context.</span></span><br/>                                                           |
| [<span data-ttu-id="89691-130">**FDIIsCabinet**</span><span class="sxs-lookup"><span data-stu-id="89691-130">**FDIIsCabinet**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fdiiscabinet)             | <span data-ttu-id="89691-131">Determina si un archivo es un contenedor y, si es así, devuelve información descriptiva.</span><span class="sxs-lookup"><span data-stu-id="89691-131">Determines whether a file is a cabinet and, if it is, returns descriptive information.</span></span><br/> |
| [<span data-ttu-id="89691-132">**FDITruncateCabinet**</span><span class="sxs-lookup"><span data-stu-id="89691-132">**FDITruncateCabinet**</span></span>](/windows/desktop/api/Fdi/nf-fdi-fditruncatecabinet) | <span data-ttu-id="89691-133">Trunca un archivo. cab a partir del número de carpeta especificado.</span><span class="sxs-lookup"><span data-stu-id="89691-133">Truncates a cabinet file starting at the specified folder number.</span></span><br/>                      |



 

## <a name="deprecated-functions"></a><span data-ttu-id="89691-134">Funciones en desuso</span><span class="sxs-lookup"><span data-stu-id="89691-134">Deprecated Functions</span></span>

-   [<span data-ttu-id="89691-135">**DeleteExtractedFiles**</span><span class="sxs-lookup"><span data-stu-id="89691-135">**DeleteExtractedFiles**</span></span>](deleteextractedfiles.md)
-   [<span data-ttu-id="89691-136">**DllGetVersion**</span><span class="sxs-lookup"><span data-stu-id="89691-136">**DllGetVersion**</span></span>](dllgetversion.md)
-   [<span data-ttu-id="89691-137">**Extracción**</span><span class="sxs-lookup"><span data-stu-id="89691-137">**Extract**</span></span>](extract.md)
-   [<span data-ttu-id="89691-138">**GetDllVersion**</span><span class="sxs-lookup"><span data-stu-id="89691-138">**GetDllVersion**</span></span>](getdllversion.md)

## <a name="related-topics"></a><span data-ttu-id="89691-139">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="89691-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="89691-140">Referencia de la API de contenedor</span><span class="sxs-lookup"><span data-stu-id="89691-140">Cabinet API Reference</span></span>](cabinet-api-reference.md)
</dt> <dt>

[<span data-ttu-id="89691-141">Uso de la API de archivo. cab</span><span class="sxs-lookup"><span data-stu-id="89691-141">Using the Cabinet API</span></span>](using-the-cabinet-api.md)
</dt> </dl>

 

 




