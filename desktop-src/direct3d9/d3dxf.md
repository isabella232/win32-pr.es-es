---
description: Opciones de formato de archivo X, carga y guardado.
ms.assetid: 813a2b4b-6577-4cdf-a2e6-e06870638354
title: D3DXF
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e230fc08ac4d7f8713959f2025f67262046ecea5
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343650"
---
# <a name="d3dxf"></a><span data-ttu-id="70a54-103">D3DXF</span><span class="sxs-lookup"><span data-stu-id="70a54-103">D3DXF</span></span>

<span data-ttu-id="70a54-104">Opciones de formato de archivo X, carga y guardado.</span><span class="sxs-lookup"><span data-stu-id="70a54-104">X file format, load, and save options.</span></span>

## <a name="file-formats"></a><span data-ttu-id="70a54-105">Formatos de archivo</span><span class="sxs-lookup"><span data-stu-id="70a54-105">File Formats</span></span>

<span data-ttu-id="70a54-106">En la tabla siguiente se especifica el tipo de datos de archivo:</span><span class="sxs-lookup"><span data-stu-id="70a54-106">The following table specifies the type of file data:</span></span>



| <span data-ttu-id="70a54-107">\#define para el formato de archivo</span><span class="sxs-lookup"><span data-stu-id="70a54-107">\#defines for File Format</span></span>     | <span data-ttu-id="70a54-108">Valor</span><span class="sxs-lookup"><span data-stu-id="70a54-108">Value</span></span> | <span data-ttu-id="70a54-109">Descripción</span><span class="sxs-lookup"><span data-stu-id="70a54-109">Description</span></span>                                                                                    |
|-------------------------------|-------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="70a54-110">D3DXF \_ FILEFORMAT \_ BINARY</span><span class="sxs-lookup"><span data-stu-id="70a54-110">D3DXF\_FILEFORMAT\_BINARY</span></span>     | <span data-ttu-id="70a54-111">0</span><span class="sxs-lookup"><span data-stu-id="70a54-111">0</span></span>     | <span data-ttu-id="70a54-112">Archivo binario con formato heredado.</span><span class="sxs-lookup"><span data-stu-id="70a54-112">Legacy-format binary file.</span></span> <span data-ttu-id="70a54-113">Vea [X File Reference (Legacy) [Referencia de archivo X (heredado)].](dx9-graphics-reference-x-file.md)</span><span class="sxs-lookup"><span data-stu-id="70a54-113">See [X File Reference (Legacy)](dx9-graphics-reference-x-file.md).</span></span> |
| <span data-ttu-id="70a54-114">TEXTO DEL FORMATO DE \_ ARCHIVO D3DXF \_</span><span class="sxs-lookup"><span data-stu-id="70a54-114">D3DXF\_FILEFORMAT\_TEXT</span></span>       | <span data-ttu-id="70a54-115">1</span><span class="sxs-lookup"><span data-stu-id="70a54-115">1</span></span>     | <span data-ttu-id="70a54-116">Archivo de texto.</span><span class="sxs-lookup"><span data-stu-id="70a54-116">Text file.</span></span>                                                                                     |
| <span data-ttu-id="70a54-117">FORMATO DE ARCHIVO D3DXF \_ \_ COMPRIMIDO</span><span class="sxs-lookup"><span data-stu-id="70a54-117">D3DXF\_FILEFORMAT\_COMPRESSED</span></span> | <span data-ttu-id="70a54-118">2</span><span class="sxs-lookup"><span data-stu-id="70a54-118">2</span></span>     | <span data-ttu-id="70a54-119">Archivo comprimido.</span><span class="sxs-lookup"><span data-stu-id="70a54-119">Compressed file.</span></span> <span data-ttu-id="70a54-120">Con esta marca, también debe especificar el formato binario o el formato de texto.</span><span class="sxs-lookup"><span data-stu-id="70a54-120">With this flag, you must also specify the binary format or the text format.</span></span>   |



 

## <a name="file-load-options"></a><span data-ttu-id="70a54-121">Opciones de carga de archivos</span><span class="sxs-lookup"><span data-stu-id="70a54-121">File Load Options</span></span>

<span data-ttu-id="70a54-122">En la tabla siguiente se especifican las opciones de carga de archivos con archivos .x:</span><span class="sxs-lookup"><span data-stu-id="70a54-122">The following table specifies file load options with .x files:</span></span>



| <span data-ttu-id="70a54-123">\#Definir</span><span class="sxs-lookup"><span data-stu-id="70a54-123">\#define</span></span>                      | <span data-ttu-id="70a54-124">Valor</span><span class="sxs-lookup"><span data-stu-id="70a54-124">Value</span></span> | <span data-ttu-id="70a54-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="70a54-125">Description</span></span>                |
|-------------------------------|-------|----------------------------|
| <span data-ttu-id="70a54-126">D3DXF \_ FILELOAD \_ FromFile</span><span class="sxs-lookup"><span data-stu-id="70a54-126">D3DXF\_FILELOAD\_FromFile</span></span>     | <span data-ttu-id="70a54-127">0</span><span class="sxs-lookup"><span data-stu-id="70a54-127">0</span></span>     | <span data-ttu-id="70a54-128">Cargar datos desde un archivo.</span><span class="sxs-lookup"><span data-stu-id="70a54-128">Load data from a file.</span></span>     |
| <span data-ttu-id="70a54-129">D3DXF \_ FILELOAD \_ FROMWFILE</span><span class="sxs-lookup"><span data-stu-id="70a54-129">D3DXF\_FILELOAD\_FROMWFILE</span></span>    | <span data-ttu-id="70a54-130">1</span><span class="sxs-lookup"><span data-stu-id="70a54-130">1</span></span>     | <span data-ttu-id="70a54-131">Cargar datos desde un archivo.</span><span class="sxs-lookup"><span data-stu-id="70a54-131">Load data from a file.</span></span>     |
| <span data-ttu-id="70a54-132">D3DXF \_ FILELOAD \_ FROMRESOURCE</span><span class="sxs-lookup"><span data-stu-id="70a54-132">D3DXF\_FILELOAD\_FROMRESOURCE</span></span> | <span data-ttu-id="70a54-133">2</span><span class="sxs-lookup"><span data-stu-id="70a54-133">2</span></span>     | <span data-ttu-id="70a54-134">Carga de datos desde un recurso.</span><span class="sxs-lookup"><span data-stu-id="70a54-134">Load data from a resource.</span></span> |
| <span data-ttu-id="70a54-135">D3DXF \_ FILELOAD \_ FROMMEMORY</span><span class="sxs-lookup"><span data-stu-id="70a54-135">D3DXF\_FILELOAD\_FROMMEMORY</span></span>   | <span data-ttu-id="70a54-136">3</span><span class="sxs-lookup"><span data-stu-id="70a54-136">3</span></span>     | <span data-ttu-id="70a54-137">Cargar datos desde la memoria.</span><span class="sxs-lookup"><span data-stu-id="70a54-137">Load data from memory.</span></span>     |



 

## <a name="file-save-options"></a><span data-ttu-id="70a54-138">Opciones de guardado de archivos</span><span class="sxs-lookup"><span data-stu-id="70a54-138">File Save Options</span></span>

<span data-ttu-id="70a54-139">En la tabla siguiente se especifican las opciones de guardado y carga de archivos con archivos .x:</span><span class="sxs-lookup"><span data-stu-id="70a54-139">The following table specifies file save and load options with .x files:</span></span>



| <span data-ttu-id="70a54-140">\#Definir</span><span class="sxs-lookup"><span data-stu-id="70a54-140">\#define</span></span>                 | <span data-ttu-id="70a54-141">Valor</span><span class="sxs-lookup"><span data-stu-id="70a54-141">Value</span></span> | <span data-ttu-id="70a54-142">Descripción</span><span class="sxs-lookup"><span data-stu-id="70a54-142">Description</span></span>                    |
|--------------------------|-------|--------------------------------|
| <span data-ttu-id="70a54-143">D3DXF \_ FILESAVE \_ TOFILE</span><span class="sxs-lookup"><span data-stu-id="70a54-143">D3DXF\_FILESAVE\_TOFILE</span></span>  | <span data-ttu-id="70a54-144">0</span><span class="sxs-lookup"><span data-stu-id="70a54-144">0</span></span>     | <span data-ttu-id="70a54-145">Guarde en un archivo.</span><span class="sxs-lookup"><span data-stu-id="70a54-145">Save to a file.</span></span>                |
| <span data-ttu-id="70a54-146">D3DXF \_ FILESAVE \_ TOWFILE</span><span class="sxs-lookup"><span data-stu-id="70a54-146">D3DXF\_FILESAVE\_TOWFILE</span></span> | <span data-ttu-id="70a54-147">1</span><span class="sxs-lookup"><span data-stu-id="70a54-147">1</span></span>     | <span data-ttu-id="70a54-148">Guarde en un archivo de caracteres anchos.</span><span class="sxs-lookup"><span data-stu-id="70a54-148">Save to a wide-character file.</span></span> |



 

## <a name="constant-information"></a><span data-ttu-id="70a54-149">Información constante</span><span class="sxs-lookup"><span data-stu-id="70a54-149">Constant Information</span></span>



| <span data-ttu-id="70a54-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="70a54-150">Requirement</span></span>                         | <span data-ttu-id="70a54-151">Value</span><span class="sxs-lookup"><span data-stu-id="70a54-151">Value</span></span>           |
|--------------------------|------------|
| <span data-ttu-id="70a54-152">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70a54-152">Header</span></span>                   | <span data-ttu-id="70a54-153">d3dx9xof.h</span><span class="sxs-lookup"><span data-stu-id="70a54-153">d3dx9xof.h</span></span> |
| <span data-ttu-id="70a54-154">Sistema operativo mínimo</span><span class="sxs-lookup"><span data-stu-id="70a54-154">Minimum operating system</span></span> | <span data-ttu-id="70a54-155">Windows 98</span><span class="sxs-lookup"><span data-stu-id="70a54-155">Windows 98</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="70a54-156">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="70a54-156">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70a54-157">Constantes de archivo D3DX X</span><span class="sxs-lookup"><span data-stu-id="70a54-157">D3DX X File Constants</span></span>](dx9-graphics-reference-d3dx-x-file-constants.md)
</dt> <dt>

[<span data-ttu-id="70a54-158">**D3DXSaveMeshToX**</span><span class="sxs-lookup"><span data-stu-id="70a54-158">**D3DXSaveMeshToX**</span></span>](d3dxsavemeshtox.md)
</dt> </dl>

 

 



