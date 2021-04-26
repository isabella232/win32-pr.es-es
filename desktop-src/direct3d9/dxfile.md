---
description: Las marcas siguientes se usan para especificar los canales de una textura en los que se va a operar. En desuso.
ms.assetid: 6e421a0a-7e82-4640-a96c-7ec648df970d
title: Constantes DXFILE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42b20ca9934b9a4203e05f477ea8c40853a0a836
ms.sourcegitcommit: b6fe9acffad983c14864b8fe0296f6025cb1f961
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/26/2021
ms.locfileid: "107997302"
---
# <a name="dxfile-constants"></a><span data-ttu-id="66924-104">Constantes DXFILE</span><span class="sxs-lookup"><span data-stu-id="66924-104">DXFILE Constants</span></span>

<span data-ttu-id="66924-105">Las marcas siguientes se usan para especificar los canales de una textura en los que se va a operar.</span><span class="sxs-lookup"><span data-stu-id="66924-105">The following flags are used to specify which channels in a texture to operate on.</span></span> <span data-ttu-id="66924-106">En desuso.</span><span class="sxs-lookup"><span data-stu-id="66924-106">Deprecated.</span></span>

## <a name="dxfileformat"></a><span data-ttu-id="66924-107">DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="66924-107">DXFILEFORMAT</span></span>



| <span data-ttu-id="66924-108">\#Definir</span><span class="sxs-lookup"><span data-stu-id="66924-108">\#define</span></span>                 | <span data-ttu-id="66924-109">Value</span><span class="sxs-lookup"><span data-stu-id="66924-109">Value</span></span> | <span data-ttu-id="66924-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="66924-110">Description</span></span>      |
|--------------------------|-------|------------------|
| <span data-ttu-id="66924-111">DXFILEFORMAT \_ BINARY</span><span class="sxs-lookup"><span data-stu-id="66924-111">DXFILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="66924-112">0</span><span class="sxs-lookup"><span data-stu-id="66924-112">0</span></span>     | <span data-ttu-id="66924-113">Archivo binario.</span><span class="sxs-lookup"><span data-stu-id="66924-113">Binary file.</span></span>     |
| <span data-ttu-id="66924-114">TEXTO \_ DXFILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="66924-114">DXFILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="66924-115">1</span><span class="sxs-lookup"><span data-stu-id="66924-115">1</span></span>     | <span data-ttu-id="66924-116">Archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="66924-116">Text file.</span></span>       |
| <span data-ttu-id="66924-117">DXFILEFORMAT \_ COMPRIMIDO</span><span class="sxs-lookup"><span data-stu-id="66924-117">DXFILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="66924-118">2</span><span class="sxs-lookup"><span data-stu-id="66924-118">2</span></span>     | <span data-ttu-id="66924-119">Archivo comprimido.</span><span class="sxs-lookup"><span data-stu-id="66924-119">Compressed file.</span></span> |



 

<span data-ttu-id="66924-120">Estas \# define se declaran en Dxfile.h.</span><span class="sxs-lookup"><span data-stu-id="66924-120">These \#defines are declared in Dxfile.h.</span></span>

## <a name="dxfileloadoptions"></a><span data-ttu-id="66924-121">DXFILELOADOPTIONS</span><span class="sxs-lookup"><span data-stu-id="66924-121">DXFILELOADOPTIONS</span></span>



| <span data-ttu-id="66924-122">\#Definir</span><span class="sxs-lookup"><span data-stu-id="66924-122">\#define</span></span>                 | <span data-ttu-id="66924-123">Value</span><span class="sxs-lookup"><span data-stu-id="66924-123">Value</span></span> | <span data-ttu-id="66924-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="66924-124">Description</span></span>                  |
|--------------------------|-------|------------------------------|
| <span data-ttu-id="66924-125">DXFILELOAD \_ FROMFILE</span><span class="sxs-lookup"><span data-stu-id="66924-125">DXFILELOAD\_FROMFILE</span></span>     | <span data-ttu-id="66924-126">0x00L</span><span class="sxs-lookup"><span data-stu-id="66924-126">0x00L</span></span> | <span data-ttu-id="66924-127">Cargar un archivo desde un archivo.</span><span class="sxs-lookup"><span data-stu-id="66924-127">Load a file from a file.</span></span>     |
| <span data-ttu-id="66924-128">DXFILELOAD \_ FROMRESOURCE</span><span class="sxs-lookup"><span data-stu-id="66924-128">DXFILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="66924-129">0x01L</span><span class="sxs-lookup"><span data-stu-id="66924-129">0x01L</span></span> | <span data-ttu-id="66924-130">Cargar un archivo desde un recurso.</span><span class="sxs-lookup"><span data-stu-id="66924-130">Load a file from a resource.</span></span> |
| <span data-ttu-id="66924-131">DXFILELOAD \_ FROMMEMORY</span><span class="sxs-lookup"><span data-stu-id="66924-131">DXFILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="66924-132">0x02L</span><span class="sxs-lookup"><span data-stu-id="66924-132">0x02L</span></span> | <span data-ttu-id="66924-133">Cargue un archivo desde la memoria.</span><span class="sxs-lookup"><span data-stu-id="66924-133">Load a file from memory.</span></span>     |
| <span data-ttu-id="66924-134">DXFILELOAD \_ FROMSTREAM</span><span class="sxs-lookup"><span data-stu-id="66924-134">DXFILELOAD\_FROMSTREAM</span></span>   | <span data-ttu-id="66924-135">0x04L</span><span class="sxs-lookup"><span data-stu-id="66924-135">0x04L</span></span> | <span data-ttu-id="66924-136">Cargue un archivo desde una secuencia.</span><span class="sxs-lookup"><span data-stu-id="66924-136">Load a file from a stream.</span></span>   |
| <span data-ttu-id="66924-137">DXFILELOAD \_ FROMURL</span><span class="sxs-lookup"><span data-stu-id="66924-137">DXFILELOAD\_FROMURL</span></span>      | <span data-ttu-id="66924-138">0x08L</span><span class="sxs-lookup"><span data-stu-id="66924-138">0x08L</span></span> | <span data-ttu-id="66924-139">Cargue un archivo desde una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="66924-139">Load a file from a URL.</span></span>      |



 

<span data-ttu-id="66924-140">Estas \# define se declaran en Dxfile.h.</span><span class="sxs-lookup"><span data-stu-id="66924-140">These \#defines are declared in Dxfile.h.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66924-141">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="66924-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66924-142">Referencia de archivo X (heredado)</span><span class="sxs-lookup"><span data-stu-id="66924-142">X File Reference (Legacy)</span></span>](dx9-graphics-reference-x-file.md)
</dt> </dl>

 

 



