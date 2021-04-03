---
description: Las marcas siguientes se usan para especificar en qué canales de una textura se va a operar. En desuso.
ms.assetid: 6e421a0a-7e82-4640-a96c-7ec648df970d
title: Constantes de DXFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25f1651d17f5acb2ef24ff9dae2ef547c3df7c0a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104079999"
---
# <a name="dxfile-constants"></a><span data-ttu-id="974a6-104">Constantes de DXFILE</span><span class="sxs-lookup"><span data-stu-id="974a6-104">DXFILE Constants</span></span>

<span data-ttu-id="974a6-105">Las marcas siguientes se usan para especificar en qué canales de una textura se va a operar.</span><span class="sxs-lookup"><span data-stu-id="974a6-105">The following flags are used to specify which channels in a texture to operate on.</span></span> <span data-ttu-id="974a6-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="974a6-106">Deprecated.</span></span>

## <a name="dxfileformat"></a><span data-ttu-id="974a6-107">DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="974a6-107">DXFILEFORMAT</span></span>



|                          |       |                  |
|--------------------------|-------|------------------|
| <span data-ttu-id="974a6-108">\#define</span><span class="sxs-lookup"><span data-stu-id="974a6-108">\#define</span></span>                 | <span data-ttu-id="974a6-109">Value</span><span class="sxs-lookup"><span data-stu-id="974a6-109">Value</span></span> | <span data-ttu-id="974a6-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="974a6-110">Description</span></span>      |
| <span data-ttu-id="974a6-111">\_binario DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="974a6-111">DXFILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="974a6-112">0</span><span class="sxs-lookup"><span data-stu-id="974a6-112">0</span></span>     | <span data-ttu-id="974a6-113">Archivo binario.</span><span class="sxs-lookup"><span data-stu-id="974a6-113">Binary file.</span></span>     |
| <span data-ttu-id="974a6-114">\_texto DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="974a6-114">DXFILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="974a6-115">1</span><span class="sxs-lookup"><span data-stu-id="974a6-115">1</span></span>     | <span data-ttu-id="974a6-116">Archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="974a6-116">Text file.</span></span>       |
| <span data-ttu-id="974a6-117">DXFILEFORMAT \_ comprimido</span><span class="sxs-lookup"><span data-stu-id="974a6-117">DXFILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="974a6-118">2</span><span class="sxs-lookup"><span data-stu-id="974a6-118">2</span></span>     | <span data-ttu-id="974a6-119">Archivo comprimido.</span><span class="sxs-lookup"><span data-stu-id="974a6-119">Compressed file.</span></span> |



 

<span data-ttu-id="974a6-120">Estas \# definiciones se declaran en Dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="974a6-120">These \#defines are declared in Dxfile.h.</span></span>

## <a name="dxfileloadoptions"></a><span data-ttu-id="974a6-121">DXFILELOADOPTIONS</span><span class="sxs-lookup"><span data-stu-id="974a6-121">DXFILELOADOPTIONS</span></span>



|                          |       |                              |
|--------------------------|-------|------------------------------|
| <span data-ttu-id="974a6-122">\#define</span><span class="sxs-lookup"><span data-stu-id="974a6-122">\#define</span></span>                 | <span data-ttu-id="974a6-123">Value</span><span class="sxs-lookup"><span data-stu-id="974a6-123">Value</span></span> | <span data-ttu-id="974a6-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="974a6-124">Description</span></span>                  |
| <span data-ttu-id="974a6-125">DXFILELOAD \_ FROMFILE</span><span class="sxs-lookup"><span data-stu-id="974a6-125">DXFILELOAD\_FROMFILE</span></span>     | <span data-ttu-id="974a6-126">0x00L</span><span class="sxs-lookup"><span data-stu-id="974a6-126">0x00L</span></span> | <span data-ttu-id="974a6-127">Cargar un archivo de un archivo.</span><span class="sxs-lookup"><span data-stu-id="974a6-127">Load a file from a file.</span></span>     |
| <span data-ttu-id="974a6-128">DXFILELOAD \_ FROMRESOURCE</span><span class="sxs-lookup"><span data-stu-id="974a6-128">DXFILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="974a6-129">0x01L</span><span class="sxs-lookup"><span data-stu-id="974a6-129">0x01L</span></span> | <span data-ttu-id="974a6-130">Cargar un archivo desde un recurso.</span><span class="sxs-lookup"><span data-stu-id="974a6-130">Load a file from a resource.</span></span> |
| <span data-ttu-id="974a6-131">DXFILELOAD \_ FROMMEMORY</span><span class="sxs-lookup"><span data-stu-id="974a6-131">DXFILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="974a6-132">0x02L</span><span class="sxs-lookup"><span data-stu-id="974a6-132">0x02L</span></span> | <span data-ttu-id="974a6-133">Cargar un archivo de la memoria.</span><span class="sxs-lookup"><span data-stu-id="974a6-133">Load a file from memory.</span></span>     |
| <span data-ttu-id="974a6-134">DXFILELOAD \_ FROMSTREAM</span><span class="sxs-lookup"><span data-stu-id="974a6-134">DXFILELOAD\_FROMSTREAM</span></span>   | <span data-ttu-id="974a6-135">0x04L</span><span class="sxs-lookup"><span data-stu-id="974a6-135">0x04L</span></span> | <span data-ttu-id="974a6-136">Carga de un archivo desde una secuencia.</span><span class="sxs-lookup"><span data-stu-id="974a6-136">Load a file from a stream.</span></span>   |
| <span data-ttu-id="974a6-137">DXFILELOAD \_ FROMURL</span><span class="sxs-lookup"><span data-stu-id="974a6-137">DXFILELOAD\_FROMURL</span></span>      | <span data-ttu-id="974a6-138">0x08L</span><span class="sxs-lookup"><span data-stu-id="974a6-138">0x08L</span></span> | <span data-ttu-id="974a6-139">Cargar un archivo desde una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="974a6-139">Load a file from a URL.</span></span>      |



 

<span data-ttu-id="974a6-140">Estas \# definiciones se declaran en Dxfile. h.</span><span class="sxs-lookup"><span data-stu-id="974a6-140">These \#defines are declared in Dxfile.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="974a6-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="974a6-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="974a6-142">Referencia de archivo X (heredado)</span><span class="sxs-lookup"><span data-stu-id="974a6-142">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



