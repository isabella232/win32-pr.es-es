---
description: Opciones de formato de archivo X, cargar y guardar.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 073887c6cc93754ead01ce379310a9be09edc88f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105696066"
---
# <a name="d3dxf"></a><span data-ttu-id="eeeb7-103">D3DXF</span><span class="sxs-lookup"><span data-stu-id="eeeb7-103">D3DXF</span></span>

<span data-ttu-id="eeeb7-104">Opciones de formato de archivo X, cargar y guardar.</span><span class="sxs-lookup"><span data-stu-id="eeeb7-104">X file format, load, and save options.</span></span>

## <a name="file-formats"></a><span data-ttu-id="eeeb7-105">Formatos de archivo</span><span class="sxs-lookup"><span data-stu-id="eeeb7-105">File Formats</span></span>

<span data-ttu-id="eeeb7-106">En la tabla siguiente se especifica el tipo de datos de archivo:</span><span class="sxs-lookup"><span data-stu-id="eeeb7-106">The following table specifies the type of file data:</span></span>



| <span data-ttu-id="eeeb7-107">\#define el formato de archivo</span><span class="sxs-lookup"><span data-stu-id="eeeb7-107">\#defines for File Format</span></span>     | <span data-ttu-id="eeeb7-108">Value</span><span class="sxs-lookup"><span data-stu-id="eeeb7-108">Value</span></span> | <span data-ttu-id="eeeb7-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="eeeb7-109">Description</span></span>                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eeeb7-110">\_Binario de D3DXF FILEFORMAT \_</span><span class="sxs-lookup"><span data-stu-id="eeeb7-110">D3DXF\_FILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="eeeb7-111">0</span><span class="sxs-lookup"><span data-stu-id="eeeb7-111">0</span></span>     | <span data-ttu-id="eeeb7-112">Archivo binario de formato heredado.</span><span class="sxs-lookup"><span data-stu-id="eeeb7-112">Legacy-format binary file.</span></span> <span data-ttu-id="eeeb7-113">Consulte [referencia de archivo X (heredado)](dx9-graphics-reference-x-file.md).</span><span class="sxs-lookup"><span data-stu-id="eeeb7-113">See [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span> |
| <span data-ttu-id="eeeb7-114">D3DXF \_ \_ texto FILEFORMAT</span><span class="sxs-lookup"><span data-stu-id="eeeb7-114">D3DXF\_FILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="eeeb7-115">1</span><span class="sxs-lookup"><span data-stu-id="eeeb7-115">1</span></span>     | <span data-ttu-id="eeeb7-116">Archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="eeeb7-116">Text file.</span></span>                                                                                     |
| <span data-ttu-id="eeeb7-117">D3DXF \_ FILEFORMAT \_ comprimido</span><span class="sxs-lookup"><span data-stu-id="eeeb7-117">D3DXF\_FILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="eeeb7-118">2</span><span class="sxs-lookup"><span data-stu-id="eeeb7-118">2</span></span>     | <span data-ttu-id="eeeb7-119">Archivo comprimido.</span><span class="sxs-lookup"><span data-stu-id="eeeb7-119">Compressed file.</span></span> <span data-ttu-id="eeeb7-120">Con esta marca, también debe especificar el formato binario o el formato de texto.</span><span class="sxs-lookup"><span data-stu-id="eeeb7-120">With this flag, you must also specify the binary format or the text format.</span></span>   |



 

## <a name="file-load-options"></a><span data-ttu-id="eeeb7-121">Opciones de carga de archivos</span><span class="sxs-lookup"><span data-stu-id="eeeb7-121">File Load Options</span></span>

<span data-ttu-id="eeeb7-122">En la tabla siguiente se especifican las opciones de carga de archivos con archivos. x:</span><span class="sxs-lookup"><span data-stu-id="eeeb7-122">The following table specifies file load options with .x files:</span></span>



| <span data-ttu-id="eeeb7-123">\#define</span><span class="sxs-lookup"><span data-stu-id="eeeb7-123">\#define</span></span>                      | <span data-ttu-id="eeeb7-124">Value</span><span class="sxs-lookup"><span data-stu-id="eeeb7-124">Value</span></span> | <span data-ttu-id="eeeb7-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="eeeb7-125">Description</span></span>                |
|-------------------------------|-------|----------------------------|
| <span data-ttu-id="eeeb7-126">D3DXF \_ FILELOAD \_ FromFile</span><span class="sxs-lookup"><span data-stu-id="eeeb7-126">D3DXF\_FILELOAD\_FromFile</span></span>     | <span data-ttu-id="eeeb7-127">0</span><span class="sxs-lookup"><span data-stu-id="eeeb7-127">0</span></span>     | <span data-ttu-id="eeeb7-128">Cargar datos de un archivo.</span><span class="sxs-lookup"><span data-stu-id="eeeb7-128">Load data from a file.</span></span>     |
| <span data-ttu-id="eeeb7-129">D3DXF \_ FILELOAD \_ FROMWFILE</span><span class="sxs-lookup"><span data-stu-id="eeeb7-129">D3DXF\_FILELOAD\_FROMWFILE</span></span>    | <span data-ttu-id="eeeb7-130">1</span><span class="sxs-lookup"><span data-stu-id="eeeb7-130">1</span></span>     | <span data-ttu-id="eeeb7-131">Cargar datos de un archivo.</span><span class="sxs-lookup"><span data-stu-id="eeeb7-131">Load data from a file.</span></span>     |
| <span data-ttu-id="eeeb7-132">D3DXF \_ FILELOAD \_ FROMRESOURCE</span><span class="sxs-lookup"><span data-stu-id="eeeb7-132">D3DXF\_FILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="eeeb7-133">2</span><span class="sxs-lookup"><span data-stu-id="eeeb7-133">2</span></span>     | <span data-ttu-id="eeeb7-134">Cargar datos de un recurso.</span><span class="sxs-lookup"><span data-stu-id="eeeb7-134">Load data from a resource.</span></span> |
| <span data-ttu-id="eeeb7-135">D3DXF \_ FILELOAD \_ FROMMEMORY</span><span class="sxs-lookup"><span data-stu-id="eeeb7-135">D3DXF\_FILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="eeeb7-136">3</span><span class="sxs-lookup"><span data-stu-id="eeeb7-136">3</span></span>     | <span data-ttu-id="eeeb7-137">Cargar datos de la memoria.</span><span class="sxs-lookup"><span data-stu-id="eeeb7-137">Load data from memory.</span></span>     |



 

## <a name="file-save-options"></a><span data-ttu-id="eeeb7-138">Opciones para guardar archivos</span><span class="sxs-lookup"><span data-stu-id="eeeb7-138">File Save Options</span></span>

<span data-ttu-id="eeeb7-139">En la tabla siguiente se especifican las opciones de guardado y carga de archivos con archivos. x:</span><span class="sxs-lookup"><span data-stu-id="eeeb7-139">The following table specifies file save and load options with .x files:</span></span>



| <span data-ttu-id="eeeb7-140">\#define</span><span class="sxs-lookup"><span data-stu-id="eeeb7-140">\#define</span></span>                 | <span data-ttu-id="eeeb7-141">Value</span><span class="sxs-lookup"><span data-stu-id="eeeb7-141">Value</span></span> | <span data-ttu-id="eeeb7-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="eeeb7-142">Description</span></span>                    |
|--------------------------|-------|--------------------------------|
| <span data-ttu-id="eeeb7-143">D3DXF \_ ArchivoGuardar \_ TOFILE</span><span class="sxs-lookup"><span data-stu-id="eeeb7-143">D3DXF\_FILESAVE\_TOFILE</span></span>  | <span data-ttu-id="eeeb7-144">0</span><span class="sxs-lookup"><span data-stu-id="eeeb7-144">0</span></span>     | <span data-ttu-id="eeeb7-145">Guardar en un archivo.</span><span class="sxs-lookup"><span data-stu-id="eeeb7-145">Save to a file.</span></span>                |
| <span data-ttu-id="eeeb7-146">D3DXF \_ ArchivoGuardar \_ TOWFILE</span><span class="sxs-lookup"><span data-stu-id="eeeb7-146">D3DXF\_FILESAVE\_TOWFILE</span></span> | <span data-ttu-id="eeeb7-147">1</span><span class="sxs-lookup"><span data-stu-id="eeeb7-147">1</span></span>     | <span data-ttu-id="eeeb7-148">Guardar en un archivo de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="eeeb7-148">Save to a wide-character file.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="eeeb7-149">Información constante</span><span class="sxs-lookup"><span data-stu-id="eeeb7-149">Constant Information</span></span>



|                          |            |
|--------------------------|------------|
| <span data-ttu-id="eeeb7-150">Encabezado</span><span class="sxs-lookup"><span data-stu-id="eeeb7-150">Header</span></span>                   | <span data-ttu-id="eeeb7-151">d3dx9xof. h</span><span class="sxs-lookup"><span data-stu-id="eeeb7-151">d3dx9xof.h</span></span> |
| <span data-ttu-id="eeeb7-152">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="eeeb7-152">Minimum operating system</span></span> | <span data-ttu-id="eeeb7-153">Windows 98</span><span class="sxs-lookup"><span data-stu-id="eeeb7-153">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="eeeb7-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eeeb7-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eeeb7-155">Constantes de archivo de D3DX X</span><span class="sxs-lookup"><span data-stu-id="eeeb7-155">D3DX X File Constants</span></span>](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[<span data-ttu-id="eeeb7-156">**D3DXSaveMeshToX**</span><span class="sxs-lookup"><span data-stu-id="eeeb7-156">**D3DXSaveMeshToX**</span></span>](d3dxsavemeshtox.md)
</dt> </dl>

 

 



