---
description: En la tabla siguiente se muestran las palabras que están reservadas y no se deben usar.
ms.assetid: 680211de-3f81-4ea7-b03e-741096b5dde0
title: Palabras reservadas, encabezado y comentarios
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2696aaf6e635f08124e28392d0a8faf63c39a85
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104536819"
---
# <a name="reserved-words-header-and-comments"></a><span data-ttu-id="43b13-103">Palabras reservadas, encabezado y comentarios</span><span class="sxs-lookup"><span data-stu-id="43b13-103">Reserved Words, Header, and Comments</span></span>

<span data-ttu-id="43b13-104">En la tabla siguiente se muestran las palabras que están reservadas y no se deben usar.</span><span class="sxs-lookup"><span data-stu-id="43b13-104">The table below shows which words are reserved and must not be used.</span></span>



|                  |          |           |
|------------------|----------|-----------|
| <span data-ttu-id="43b13-105">ARRAY</span><span class="sxs-lookup"><span data-stu-id="43b13-105">ARRAY</span></span>            | <span data-ttu-id="43b13-106">DWORD</span><span class="sxs-lookup"><span data-stu-id="43b13-106">DWORD</span></span>    | <span data-ttu-id="43b13-107">UCHAR</span><span class="sxs-lookup"><span data-stu-id="43b13-107">UCHAR</span></span>     |
| <span data-ttu-id="43b13-108">BINARY</span><span class="sxs-lookup"><span data-stu-id="43b13-108">BINARY</span></span>           | <span data-ttu-id="43b13-109">FLOAT</span><span class="sxs-lookup"><span data-stu-id="43b13-109">FLOAT</span></span>    | <span data-ttu-id="43b13-110">ULONGLONG</span><span class="sxs-lookup"><span data-stu-id="43b13-110">ULONGLONG</span></span> |
| <span data-ttu-id="43b13-111">recurso BINARIo \_</span><span class="sxs-lookup"><span data-stu-id="43b13-111">BINARY\_RESOURCE</span></span> | <span data-ttu-id="43b13-112">SDWORD</span><span class="sxs-lookup"><span data-stu-id="43b13-112">SDWORD</span></span>   | <span data-ttu-id="43b13-113">UNICODE</span><span class="sxs-lookup"><span data-stu-id="43b13-113">UNICODE</span></span>   |
| <span data-ttu-id="43b13-114">CHAR</span><span class="sxs-lookup"><span data-stu-id="43b13-114">CHAR</span></span>             | <span data-ttu-id="43b13-115">STRING</span><span class="sxs-lookup"><span data-stu-id="43b13-115">STRING</span></span>   | <span data-ttu-id="43b13-116">WORD</span><span class="sxs-lookup"><span data-stu-id="43b13-116">WORD</span></span>      |
| <span data-ttu-id="43b13-117">CSTRING</span><span class="sxs-lookup"><span data-stu-id="43b13-117">CSTRING</span></span>          | <span data-ttu-id="43b13-118">SWORD</span><span class="sxs-lookup"><span data-stu-id="43b13-118">SWORD</span></span>    |           |
| <span data-ttu-id="43b13-119">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="43b13-119">DOUBLE</span></span>           | <span data-ttu-id="43b13-120">TEMPLATE</span><span class="sxs-lookup"><span data-stu-id="43b13-120">TEMPLATE</span></span> |           |



 

<span data-ttu-id="43b13-121">El encabezado de longitud variable es obligatorio y debe estar al principio del flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="43b13-121">The variable-length header is compulsory and must be at the beginning of the data stream.</span></span> <span data-ttu-id="43b13-122">El encabezado contiene los datos siguientes.</span><span class="sxs-lookup"><span data-stu-id="43b13-122">The header contains the following data.</span></span>



| <span data-ttu-id="43b13-123">Tipo</span><span class="sxs-lookup"><span data-stu-id="43b13-123">Type</span></span>           | <span data-ttu-id="43b13-124">Obligatorio</span><span class="sxs-lookup"><span data-stu-id="43b13-124">Required</span></span> | <span data-ttu-id="43b13-125">Tamaño (en bytes)</span><span class="sxs-lookup"><span data-stu-id="43b13-125">Size (in bytes)</span></span> | <span data-ttu-id="43b13-126">Value</span><span class="sxs-lookup"><span data-stu-id="43b13-126">Value</span></span> | <span data-ttu-id="43b13-127">Descripción</span><span class="sxs-lookup"><span data-stu-id="43b13-127">Description</span></span>                  |
|----------------|----------|-----------------|-------|------------------------------|
| <span data-ttu-id="43b13-128">Número mágico</span><span class="sxs-lookup"><span data-stu-id="43b13-128">Magic Number</span></span>   | <span data-ttu-id="43b13-129">x</span><span class="sxs-lookup"><span data-stu-id="43b13-129">x</span></span>        | <span data-ttu-id="43b13-130">4</span><span class="sxs-lookup"><span data-stu-id="43b13-130">4</span></span>               | <span data-ttu-id="43b13-131">xof</span><span class="sxs-lookup"><span data-stu-id="43b13-131">xof</span></span>   |                              |
| <span data-ttu-id="43b13-132">Número de versión</span><span class="sxs-lookup"><span data-stu-id="43b13-132">Version Number</span></span> | <span data-ttu-id="43b13-133">x</span><span class="sxs-lookup"><span data-stu-id="43b13-133">x</span></span>        | <span data-ttu-id="43b13-134">2</span><span class="sxs-lookup"><span data-stu-id="43b13-134">2</span></span>               | <span data-ttu-id="43b13-135">03</span><span class="sxs-lookup"><span data-stu-id="43b13-135">03</span></span>    | <span data-ttu-id="43b13-136">Versión principal 3</span><span class="sxs-lookup"><span data-stu-id="43b13-136">Major version 3</span></span>              |
|                |          |                 | <span data-ttu-id="43b13-137">03</span><span class="sxs-lookup"><span data-stu-id="43b13-137">03</span></span>    | <span data-ttu-id="43b13-138">Versión secundaria 3</span><span class="sxs-lookup"><span data-stu-id="43b13-138">Minor version 3</span></span>              |
| <span data-ttu-id="43b13-139">Tipo de formato</span><span class="sxs-lookup"><span data-stu-id="43b13-139">Format Type</span></span>    | <span data-ttu-id="43b13-140">x</span><span class="sxs-lookup"><span data-stu-id="43b13-140">x</span></span>        | <span data-ttu-id="43b13-141">4</span><span class="sxs-lookup"><span data-stu-id="43b13-141">4</span></span>               | <span data-ttu-id="43b13-142">txt</span><span class="sxs-lookup"><span data-stu-id="43b13-142">txt</span></span>   | <span data-ttu-id="43b13-143">Archivo de texto</span><span class="sxs-lookup"><span data-stu-id="43b13-143">Text File</span></span>                    |
|                |          |                 | <span data-ttu-id="43b13-144">bin</span><span class="sxs-lookup"><span data-stu-id="43b13-144">bin</span></span>   | <span data-ttu-id="43b13-145">Archivo binario</span><span class="sxs-lookup"><span data-stu-id="43b13-145">Binary file</span></span>                  |
|                |          |                 | <span data-ttu-id="43b13-146">tzip</span><span class="sxs-lookup"><span data-stu-id="43b13-146">tzip</span></span>  | <span data-ttu-id="43b13-147">MSZip archivo de texto comprimido</span><span class="sxs-lookup"><span data-stu-id="43b13-147">MSZip compressed text file</span></span>   |
|                |          |                 | <span data-ttu-id="43b13-148">bzip</span><span class="sxs-lookup"><span data-stu-id="43b13-148">bzip</span></span>  | <span data-ttu-id="43b13-149">MSZip archivo binario comprimido</span><span class="sxs-lookup"><span data-stu-id="43b13-149">MSZip compressed binary file</span></span> |
| <span data-ttu-id="43b13-150">Tamaño de Float</span><span class="sxs-lookup"><span data-stu-id="43b13-150">Float Size</span></span>     | <span data-ttu-id="43b13-151">x</span><span class="sxs-lookup"><span data-stu-id="43b13-151">x</span></span>        | <span data-ttu-id="43b13-152">0064</span><span class="sxs-lookup"><span data-stu-id="43b13-152">0064</span></span>            |       | <span data-ttu-id="43b13-153">floats de 64 bits</span><span class="sxs-lookup"><span data-stu-id="43b13-153">64-bit floats</span></span>                |
|                | <span data-ttu-id="43b13-154">x</span><span class="sxs-lookup"><span data-stu-id="43b13-154">x</span></span>        | <span data-ttu-id="43b13-155">"0032"</span><span class="sxs-lookup"><span data-stu-id="43b13-155">"0032"</span></span>          |       | <span data-ttu-id="43b13-156">floats de 32 bits</span><span class="sxs-lookup"><span data-stu-id="43b13-156">32-bit floats</span></span>                |



 

<span data-ttu-id="43b13-157">Los valores de la tabla están delimitados por comillas para llamar la atención al número de caracteres de cada valor.</span><span class="sxs-lookup"><span data-stu-id="43b13-157">The values in the table are delimited by quotes to call attention to the number of characters in each value.</span></span> <span data-ttu-id="43b13-158">Aquellos con 4 bytes contienen cuatro caracteres, los cuales tienen 2 bytes y dos.</span><span class="sxs-lookup"><span data-stu-id="43b13-158">Those with 4 bytes contain four characters, those with 2 bytes contain two characters.</span></span>

<span data-ttu-id="43b13-159">Los comentarios solo se aplican en archivos de texto.</span><span class="sxs-lookup"><span data-stu-id="43b13-159">Comments are applicable only in text files.</span></span> <span data-ttu-id="43b13-160">Los comentarios pueden aparecer en cualquier parte del flujo de datos.</span><span class="sxs-lookup"><span data-stu-id="43b13-160">Comments can occur anywhere in the data stream.</span></span> <span data-ttu-id="43b13-161">Un comentario comienza con barras diagonales dobles de estilo de C++ (//) o con un signo de almohadilla ( \# ).</span><span class="sxs-lookup"><span data-stu-id="43b13-161">A comment begins with either C++ style double-slashes (//), or a pound sign (\#).</span></span> <span data-ttu-id="43b13-162">El comentario se ejecuta en la siguiente línea nueva.</span><span class="sxs-lookup"><span data-stu-id="43b13-162">The comment runs to the next new line.</span></span> <span data-ttu-id="43b13-163">En el ejemplo siguiente se muestran comentarios válidos.</span><span class="sxs-lookup"><span data-stu-id="43b13-163">The following example shows valid comments.</span></span>


```
#  This is a comment.
// This is another comment.
```



## <a name="related-topics"></a><span data-ttu-id="43b13-164">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="43b13-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43b13-165">Codificación de texto</span><span class="sxs-lookup"><span data-stu-id="43b13-165">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



