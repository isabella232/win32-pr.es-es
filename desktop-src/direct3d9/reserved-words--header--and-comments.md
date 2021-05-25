---
description: En la tabla siguiente se muestra qué palabras están reservadas y no se deben usar.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Palabras reservadas, encabezado y comentarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8879d0dbb518f92f0d8a6c38793ab315ae48b73e
ms.sourcegitcommit: b40a986d5ded926ae7617119cdd35d99b533bad9
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/24/2021
ms.locfileid: "110343660"
---
# <a name="reserved-words-header-and-comments"></a><span data-ttu-id="5c8ca-103">Palabras reservadas, encabezado y comentarios</span><span class="sxs-lookup"><span data-stu-id="5c8ca-103">Reserved Words, Header, and Comments</span></span>

<span data-ttu-id="5c8ca-104">En la tabla siguiente se muestra qué palabras están reservadas y no se deben usar.</span><span class="sxs-lookup"><span data-stu-id="5c8ca-104">The table below shows which words are reserved and must not be used.</span></span>

| <span data-ttu-id="5c8ca-105">Palabras reservadas</span><span class="sxs-lookup"><span data-stu-id="5c8ca-105">Reserved Words</span></span> | <span data-ttu-id="5c8ca-106">Palabras reservadas</span><span class="sxs-lookup"><span data-stu-id="5c8ca-106">Reserved Words</span></span> | <span data-ttu-id="5c8ca-107">Palabras reservadas</span><span class="sxs-lookup"><span data-stu-id="5c8ca-107">Reserved Words</span></span>|
|------------------|----------|-----------|
| <span data-ttu-id="5c8ca-108">ARRAY</span><span class="sxs-lookup"><span data-stu-id="5c8ca-108">ARRAY</span></span>            | <span data-ttu-id="5c8ca-109">DWORD</span><span class="sxs-lookup"><span data-stu-id="5c8ca-109">DWORD</span></span>    | <span data-ttu-id="5c8ca-110">UCHAR</span><span class="sxs-lookup"><span data-stu-id="5c8ca-110">UCHAR</span></span>     |
| <span data-ttu-id="5c8ca-111">BINARY</span><span class="sxs-lookup"><span data-stu-id="5c8ca-111">BINARY</span></span>           | <span data-ttu-id="5c8ca-112">FLOAT</span><span class="sxs-lookup"><span data-stu-id="5c8ca-112">FLOAT</span></span>    | <span data-ttu-id="5c8ca-113">ULONGLONG</span><span class="sxs-lookup"><span data-stu-id="5c8ca-113">ULONGLONG</span></span> |
| <span data-ttu-id="5c8ca-114">RECURSO \_ BINARIO</span><span class="sxs-lookup"><span data-stu-id="5c8ca-114">BINARY\_RESOURCE</span></span> | <span data-ttu-id="5c8ca-115">SDWORD</span><span class="sxs-lookup"><span data-stu-id="5c8ca-115">SDWORD</span></span>   | <span data-ttu-id="5c8ca-116">UNICODE</span><span class="sxs-lookup"><span data-stu-id="5c8ca-116">UNICODE</span></span>   |
| <span data-ttu-id="5c8ca-117">CHAR</span><span class="sxs-lookup"><span data-stu-id="5c8ca-117">CHAR</span></span>             | <span data-ttu-id="5c8ca-118">STRING</span><span class="sxs-lookup"><span data-stu-id="5c8ca-118">STRING</span></span>   | <span data-ttu-id="5c8ca-119">WORD</span><span class="sxs-lookup"><span data-stu-id="5c8ca-119">WORD</span></span>      |
| <span data-ttu-id="5c8ca-120">Cstring</span><span class="sxs-lookup"><span data-stu-id="5c8ca-120">CSTRING</span></span>          | <span data-ttu-id="5c8ca-121">SWORD</span><span class="sxs-lookup"><span data-stu-id="5c8ca-121">SWORD</span></span>    |           |
| <span data-ttu-id="5c8ca-122">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="5c8ca-122">DOUBLE</span></span>           | <span data-ttu-id="5c8ca-123">TEMPLATE</span><span class="sxs-lookup"><span data-stu-id="5c8ca-123">TEMPLATE</span></span> |           |



 

<span data-ttu-id="5c8ca-124">El encabezado de longitud variable es obligatorio y debe estar al principio del flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="5c8ca-124">The variable-length header is compulsory and must be at the beginning of the data stream.</span></span> <span data-ttu-id="5c8ca-125">El encabezado contiene los datos siguientes.</span><span class="sxs-lookup"><span data-stu-id="5c8ca-125">The header contains the following data.</span></span>



| <span data-ttu-id="5c8ca-126">Tipo</span><span class="sxs-lookup"><span data-stu-id="5c8ca-126">Type</span></span>           | <span data-ttu-id="5c8ca-127">Requerido</span><span class="sxs-lookup"><span data-stu-id="5c8ca-127">Required</span></span> | <span data-ttu-id="5c8ca-128">Tamaño (en bytes)</span><span class="sxs-lookup"><span data-stu-id="5c8ca-128">Size (in bytes)</span></span> | <span data-ttu-id="5c8ca-129">Valor</span><span class="sxs-lookup"><span data-stu-id="5c8ca-129">Value</span></span> | <span data-ttu-id="5c8ca-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="5c8ca-130">Description</span></span>                  |
|----------------|----------|-----------------|-------|------------------------------|
| <span data-ttu-id="5c8ca-131">Número mágico</span><span class="sxs-lookup"><span data-stu-id="5c8ca-131">Magic Number</span></span>   | <span data-ttu-id="5c8ca-132">x</span><span class="sxs-lookup"><span data-stu-id="5c8ca-132">x</span></span>        | <span data-ttu-id="5c8ca-133">4</span><span class="sxs-lookup"><span data-stu-id="5c8ca-133">4</span></span>               | <span data-ttu-id="5c8ca-134">Xof</span><span class="sxs-lookup"><span data-stu-id="5c8ca-134">xof</span></span>   |                              |
| <span data-ttu-id="5c8ca-135">Número de versión</span><span class="sxs-lookup"><span data-stu-id="5c8ca-135">Version Number</span></span> | <span data-ttu-id="5c8ca-136">x</span><span class="sxs-lookup"><span data-stu-id="5c8ca-136">x</span></span>        | <span data-ttu-id="5c8ca-137">2</span><span class="sxs-lookup"><span data-stu-id="5c8ca-137">2</span></span>               | <span data-ttu-id="5c8ca-138">03</span><span class="sxs-lookup"><span data-stu-id="5c8ca-138">03</span></span>    | <span data-ttu-id="5c8ca-139">Versión principal 3</span><span class="sxs-lookup"><span data-stu-id="5c8ca-139">Major version 3</span></span>              |
|                |          |                 | <span data-ttu-id="5c8ca-140">03</span><span class="sxs-lookup"><span data-stu-id="5c8ca-140">03</span></span>    | <span data-ttu-id="5c8ca-141">Versión secundaria 3</span><span class="sxs-lookup"><span data-stu-id="5c8ca-141">Minor version 3</span></span>              |
| <span data-ttu-id="5c8ca-142">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="5c8ca-142">Format Type</span></span>    | <span data-ttu-id="5c8ca-143">x</span><span class="sxs-lookup"><span data-stu-id="5c8ca-143">x</span></span>        | <span data-ttu-id="5c8ca-144">4</span><span class="sxs-lookup"><span data-stu-id="5c8ca-144">4</span></span>               | <span data-ttu-id="5c8ca-145">txt</span><span class="sxs-lookup"><span data-stu-id="5c8ca-145">txt</span></span>   | <span data-ttu-id="5c8ca-146">Archivo de texto</span><span class="sxs-lookup"><span data-stu-id="5c8ca-146">Text File</span></span>                    |
|                |          |                 | <span data-ttu-id="5c8ca-147">bin</span><span class="sxs-lookup"><span data-stu-id="5c8ca-147">bin</span></span>   | <span data-ttu-id="5c8ca-148">Archivo binario</span><span class="sxs-lookup"><span data-stu-id="5c8ca-148">Binary file</span></span>                  |
|                |          |                 | <span data-ttu-id="5c8ca-149">tzip</span><span class="sxs-lookup"><span data-stu-id="5c8ca-149">tzip</span></span>  | <span data-ttu-id="5c8ca-150">Archivo de texto comprimido MSZip</span><span class="sxs-lookup"><span data-stu-id="5c8ca-150">MSZip compressed text file</span></span>   |
|                |          |                 | <span data-ttu-id="5c8ca-151">bzip</span><span class="sxs-lookup"><span data-stu-id="5c8ca-151">bzip</span></span>  | <span data-ttu-id="5c8ca-152">Archivo binario comprimido de MSZip</span><span class="sxs-lookup"><span data-stu-id="5c8ca-152">MSZip compressed binary file</span></span> |
| <span data-ttu-id="5c8ca-153">Tamaño flotante</span><span class="sxs-lookup"><span data-stu-id="5c8ca-153">Float Size</span></span>     | <span data-ttu-id="5c8ca-154">x</span><span class="sxs-lookup"><span data-stu-id="5c8ca-154">x</span></span>        | <span data-ttu-id="5c8ca-155">0064</span><span class="sxs-lookup"><span data-stu-id="5c8ca-155">0064</span></span>            |       | <span data-ttu-id="5c8ca-156">Flotantes de 64 bits</span><span class="sxs-lookup"><span data-stu-id="5c8ca-156">64-bit floats</span></span>                |
|                | <span data-ttu-id="5c8ca-157">x</span><span class="sxs-lookup"><span data-stu-id="5c8ca-157">x</span></span>        | <span data-ttu-id="5c8ca-158">"0032"</span><span class="sxs-lookup"><span data-stu-id="5c8ca-158">"0032"</span></span>          |       | <span data-ttu-id="5c8ca-159">Flotantes de 32 bits</span><span class="sxs-lookup"><span data-stu-id="5c8ca-159">32-bit floats</span></span>                |



 

<span data-ttu-id="5c8ca-160">Los valores de la tabla se delimitan entre comillas para llamar la atención sobre el número de caracteres de cada valor.</span><span class="sxs-lookup"><span data-stu-id="5c8ca-160">The values in the table are delimited by quotes to call attention to the number of characters in each value.</span></span> <span data-ttu-id="5c8ca-161">Aquellos con 4 bytes contienen cuatro caracteres, los que tienen 2 bytes contienen dos caracteres.</span><span class="sxs-lookup"><span data-stu-id="5c8ca-161">Those with 4 bytes contain four characters, those with 2 bytes contain two characters.</span></span>

<span data-ttu-id="5c8ca-162">Los comentarios solo son aplicables en archivos de texto.</span><span class="sxs-lookup"><span data-stu-id="5c8ca-162">Comments are applicable only in text files.</span></span> <span data-ttu-id="5c8ca-163">Los comentarios pueden producirse en cualquier parte del flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="5c8ca-163">Comments can occur anywhere in the data stream.</span></span> <span data-ttu-id="5c8ca-164">Un comentario comienza con barras diagonales dobles de estilo C++ (//) o un signo de perd ( \# ).</span><span class="sxs-lookup"><span data-stu-id="5c8ca-164">A comment begins with either C++ style double-slashes (//), or a pound sign (\#).</span></span> <span data-ttu-id="5c8ca-165">El comentario se ejecuta hasta la siguiente línea nueva.</span><span class="sxs-lookup"><span data-stu-id="5c8ca-165">The comment runs to the next new line.</span></span> <span data-ttu-id="5c8ca-166">En el ejemplo siguiente se muestran comentarios válidos.</span><span class="sxs-lookup"><span data-stu-id="5c8ca-166">The following example shows valid comments.</span></span>


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a><span data-ttu-id="5c8ca-167">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="5c8ca-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5c8ca-168">Codificación de texto</span><span class="sxs-lookup"><span data-stu-id="5c8ca-168">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



