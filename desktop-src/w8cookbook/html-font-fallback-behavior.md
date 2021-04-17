---
title: Comportamiento de reserva de fuente HTML
description: Comportamiento de reserva de fuente HTML
ms.assetid: 5BDFBD58-0B34-4A58-BFAF-B8BB1DD569DB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8fc7da95c46190fd348dda72edc8283ee6438b00
ms.sourcegitcommit: 80bac5863880f1bd4c1c3e06db27c5d8fb5232b4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/08/2020
ms.locfileid: "105705061"
---
# <a name="html-font-fallback-behavior"></a><span data-ttu-id="f32e3-103">Comportamiento de reserva de fuente HTML</span><span class="sxs-lookup"><span data-stu-id="f32e3-103">HTML font fallback behavior</span></span>

## <a name="platform"></a><span data-ttu-id="f32e3-104">Plataforma</span><span class="sxs-lookup"><span data-stu-id="f32e3-104">Platform</span></span>

<span data-ttu-id="f32e3-105">Clientes-\* \* Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="f32e3-105">Clients -\*\* Windows 8.1</span></span>  
<span data-ttu-id="f32e3-106">**Servidores:** Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="f32e3-106">**Servers -** Windows Server 2012 R2</span></span>  


## <a name="description"></a><span data-ttu-id="f32e3-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="f32e3-107">Description</span></span>

<span data-ttu-id="f32e3-108">Microsoft está actualizando la lógica de las fuentes de interfaz de usuario para varios idiomas en aplicaciones de la tienda Windows con HTML.</span><span class="sxs-lookup"><span data-stu-id="f32e3-108">Microsoft is updating the logic for UI fonts for several languages in Windows Store apps using HTML.</span></span> <span data-ttu-id="f32e3-109">En lugar de usar una sola fuente para todos los idiomas, la fuente de la interfaz de usuario se determinará en función de cada idioma.</span><span class="sxs-lookup"><span data-stu-id="f32e3-109">Rather than using a single font for all languages, the UI font will now be determined on a per language basis.</span></span> <span data-ttu-id="f32e3-110">Por ejemplo, las fuentes de interfaz de usuario para japonés ahora serán la interfaz de usuario de Meiryo en aplicaciones que usan HTML.</span><span class="sxs-lookup"><span data-stu-id="f32e3-110">For example, UI fonts for Japanese will now be Meiryo UI in apps that use HTML.</span></span>

## <a name="manifestation"></a><span data-ttu-id="f32e3-111">Manifestación</span><span class="sxs-lookup"><span data-stu-id="f32e3-111">Manifestation</span></span>

<span data-ttu-id="f32e3-112">Las aplicaciones que dependen de una fuente antigua pueden tener un aspecto diferente. Aunque el aspecto de la aplicación se mejorará globalmente gracias a las fuentes más legibles, podría haber un problema con los diseños que dependen de tamaños de contenido con píxeles perfectos.</span><span class="sxs-lookup"><span data-stu-id="f32e3-112">Apps that depended on an old font may look different; while your app appearance will be improved overall thanks to more readable fonts, there could be an issue with layouts that depend on pixel-perfect content sizes.</span></span> <span data-ttu-id="f32e3-113">Por ejemplo, algunas líneas de contenido pueden ser mayores de lo anterior, lo que provoca saltos de línea inesperados y/o el cambio de tamaño de los elementos del contenedor.</span><span class="sxs-lookup"><span data-stu-id="f32e3-113">For example, some lines of content may be bigger than they were previously, causing unexpected line breaks and/or resizing of container elements.</span></span> <span data-ttu-id="f32e3-114">Sin embargo, en la práctica no hemos observado ningún problema con las aplicaciones existentes.</span><span class="sxs-lookup"><span data-stu-id="f32e3-114">However, in practice we haven’t noticed any issues with any existing apps.</span></span>

## <a name="solution"></a><span data-ttu-id="f32e3-115">Solución</span><span class="sxs-lookup"><span data-stu-id="f32e3-115">Solution</span></span>

<span data-ttu-id="f32e3-116">Las aplicaciones afectadas pueden mitigar este comportamiento mediante la especificación de una fuente determinada a través de CSS (por ejemplo, "font-family: Meiryo UI") en lugar de depender de las fuentes predeterminadas anteriores.</span><span class="sxs-lookup"><span data-stu-id="f32e3-116">Affected apps can mitigate this behavior by specifying a given font via CSS (for example, “font-family: Meiryo UI”) instead of relying on the old default fonts.</span></span> <span data-ttu-id="f32e3-117">En la tabla siguiente se proporciona la fuente de la interfaz de usuario para cada uno de los nombres de script.</span><span class="sxs-lookup"><span data-stu-id="f32e3-117">The following table provides the UI font for each of the script names.</span></span>



| <span data-ttu-id="f32e3-118">Nombre del script</span><span class="sxs-lookup"><span data-stu-id="f32e3-118">Script Name</span></span>        | <span data-ttu-id="f32e3-119">Fuente de la interfaz de usuario</span><span class="sxs-lookup"><span data-stu-id="f32e3-119">UI Font</span></span>               |
|--------------------|-----------------------|
| <span data-ttu-id="f32e3-120">Árabe</span><span class="sxs-lookup"><span data-stu-id="f32e3-120">Arabic</span></span>             | <span data-ttu-id="f32e3-121">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-121">Segoe UI</span></span>              |
| <span data-ttu-id="f32e3-122">Armenio</span><span class="sxs-lookup"><span data-stu-id="f32e3-122">Armenian</span></span>           | <span data-ttu-id="f32e3-123">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-123">Segoe UI</span></span>              |
| <span data-ttu-id="f32e3-124">Bengalí</span><span class="sxs-lookup"><span data-stu-id="f32e3-124">Bengali</span></span>            | <span data-ttu-id="f32e3-125">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-125">Nirmala UI</span></span>            |
| <span data-ttu-id="f32e3-126">Bopomofo</span><span class="sxs-lookup"><span data-stu-id="f32e3-126">Bopomofo</span></span>           | <span data-ttu-id="f32e3-127">Microsoft JhengHei UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-127">Microsoft JhengHei UI</span></span> |
| <span data-ttu-id="f32e3-128">Pantallas</span><span class="sxs-lookup"><span data-stu-id="f32e3-128">Braille</span></span>            | <span data-ttu-id="f32e3-129">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="f32e3-129">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="f32e3-130">Buginés</span><span class="sxs-lookup"><span data-stu-id="f32e3-130">Buginese</span></span>           | <span data-ttu-id="f32e3-131">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-131">Leelawadee UI</span></span>         |
| <span data-ttu-id="f32e3-132">Silábico canadiense</span><span class="sxs-lookup"><span data-stu-id="f32e3-132">Canadian Syllabics</span></span> | <span data-ttu-id="f32e3-133">Gadugi</span><span class="sxs-lookup"><span data-stu-id="f32e3-133">Gadugi</span></span>                |
| <span data-ttu-id="f32e3-134">Cheroqui</span><span class="sxs-lookup"><span data-stu-id="f32e3-134">Cherokee</span></span>           | <span data-ttu-id="f32e3-135">Gadugi</span><span class="sxs-lookup"><span data-stu-id="f32e3-135">Gadugi</span></span>                |
| <span data-ttu-id="f32e3-136">Copto</span><span class="sxs-lookup"><span data-stu-id="f32e3-136">Coptic</span></span>             | <span data-ttu-id="f32e3-137">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="f32e3-137">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="f32e3-138">Han (simplificado)</span><span class="sxs-lookup"><span data-stu-id="f32e3-138">Han (Simplified)</span></span>   | <span data-ttu-id="f32e3-139">Microsoft YaHei UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-139">Microsoft YaHei UI</span></span>    |
| <span data-ttu-id="f32e3-140">Han (tradicional)</span><span class="sxs-lookup"><span data-stu-id="f32e3-140">Han (Traditional)</span></span>  | <span data-ttu-id="f32e3-141">Microsoft JhengHei UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-141">Microsoft JhengHei UI</span></span> |
| <span data-ttu-id="f32e3-142">Cirílico</span><span class="sxs-lookup"><span data-stu-id="f32e3-142">Cyrillic</span></span>           | <span data-ttu-id="f32e3-143">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-143">Segoe UI</span></span>              |
| <span data-ttu-id="f32e3-144">Devanagari</span><span class="sxs-lookup"><span data-stu-id="f32e3-144">Devanagari</span></span>         | <span data-ttu-id="f32e3-145">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-145">Nirmala UI</span></span>            |
| <span data-ttu-id="f32e3-146">Deseret</span><span class="sxs-lookup"><span data-stu-id="f32e3-146">Deseret</span></span>            | <span data-ttu-id="f32e3-147">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="f32e3-147">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="f32e3-148">Dígito</span><span class="sxs-lookup"><span data-stu-id="f32e3-148">Ethiopic</span></span>           | <span data-ttu-id="f32e3-149">Ebrima</span><span class="sxs-lookup"><span data-stu-id="f32e3-149">Ebrima</span></span>                |
| <span data-ttu-id="f32e3-150">Georgiano</span><span class="sxs-lookup"><span data-stu-id="f32e3-150">Georgian</span></span>           | <span data-ttu-id="f32e3-151">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-151">Segoe UI</span></span>              |
| <span data-ttu-id="f32e3-152">Letra</span><span class="sxs-lookup"><span data-stu-id="f32e3-152">Glagolitic</span></span>         | <span data-ttu-id="f32e3-153">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="f32e3-153">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="f32e3-154">Gótico</span><span class="sxs-lookup"><span data-stu-id="f32e3-154">Gothic</span></span>             | <span data-ttu-id="f32e3-155">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="f32e3-155">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="f32e3-156">Griego</span><span class="sxs-lookup"><span data-stu-id="f32e3-156">Greek</span></span>              | <span data-ttu-id="f32e3-157">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-157">Segoe UI</span></span>              |
| <span data-ttu-id="f32e3-158">Gujarati</span><span class="sxs-lookup"><span data-stu-id="f32e3-158">Gujarati</span></span>           | <span data-ttu-id="f32e3-159">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-159">Nirmala UI</span></span>            |
| <span data-ttu-id="f32e3-160">Gurmukhi</span><span class="sxs-lookup"><span data-stu-id="f32e3-160">Gurmukhi</span></span>           | <span data-ttu-id="f32e3-161">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-161">Nirmala UI</span></span>            |
| <span data-ttu-id="f32e3-162">Hebreo</span><span class="sxs-lookup"><span data-stu-id="f32e3-162">Hebrew</span></span>             | <span data-ttu-id="f32e3-163">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-163">Segoe UI</span></span>              |
| <span data-ttu-id="f32e3-164">Cursiva antigua</span><span class="sxs-lookup"><span data-stu-id="f32e3-164">Old Italic</span></span>         | <span data-ttu-id="f32e3-165">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="f32e3-165">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="f32e3-166">Javanés</span><span class="sxs-lookup"><span data-stu-id="f32e3-166">Javanese</span></span>           | <span data-ttu-id="f32e3-167">Texto javanés</span><span class="sxs-lookup"><span data-stu-id="f32e3-167">Javanese Text</span></span>         |
| <span data-ttu-id="f32e3-168">Japonés</span><span class="sxs-lookup"><span data-stu-id="f32e3-168">Japanese</span></span>           | <span data-ttu-id="f32e3-169">Interfaz de usuario de Meiryo</span><span class="sxs-lookup"><span data-stu-id="f32e3-169">Meiryo UI</span></span>             |
| <span data-ttu-id="f32e3-170">Canarés</span><span class="sxs-lookup"><span data-stu-id="f32e3-170">Kannada</span></span>            | <span data-ttu-id="f32e3-171">Interfaz de usuario de Mirmala</span><span class="sxs-lookup"><span data-stu-id="f32e3-171">Mirmala UI</span></span>            |
| <span data-ttu-id="f32e3-172">Jemer</span><span class="sxs-lookup"><span data-stu-id="f32e3-172">Khmer</span></span>              | <span data-ttu-id="f32e3-173">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-173">Leelawadee UI</span></span>         |
| <span data-ttu-id="f32e3-174">Coreano</span><span class="sxs-lookup"><span data-stu-id="f32e3-174">Korean</span></span>             | <span data-ttu-id="f32e3-175">Malgun Gothic</span><span class="sxs-lookup"><span data-stu-id="f32e3-175">Malgun Gothic</span></span>         |
| <span data-ttu-id="f32e3-176">Lao</span><span class="sxs-lookup"><span data-stu-id="f32e3-176">Lao</span></span>                | <span data-ttu-id="f32e3-177">Leelawadee</span><span class="sxs-lookup"><span data-stu-id="f32e3-177">Leelawadee</span></span>            |
| <span data-ttu-id="f32e3-178">Latín</span><span class="sxs-lookup"><span data-stu-id="f32e3-178">Latin</span></span>              | <span data-ttu-id="f32e3-179">Segoe UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-179">Segoe UI</span></span>              |
| <span data-ttu-id="f32e3-180">Malayalam</span><span class="sxs-lookup"><span data-stu-id="f32e3-180">Malayalam</span></span>          | <span data-ttu-id="f32e3-181">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-181">Nirmala UI</span></span>            |
| <span data-ttu-id="f32e3-182">Mongol</span><span class="sxs-lookup"><span data-stu-id="f32e3-182">Mongolian</span></span>          | <span data-ttu-id="f32e3-183">Mongolian Baiti</span><span class="sxs-lookup"><span data-stu-id="f32e3-183">Mongolian Baiti</span></span>       |
| <span data-ttu-id="f32e3-184">Myanmar</span><span class="sxs-lookup"><span data-stu-id="f32e3-184">Myanmar</span></span>            | <span data-ttu-id="f32e3-185">Myanmar Text</span><span class="sxs-lookup"><span data-stu-id="f32e3-185">Myanmar Text</span></span>          |
| <span data-ttu-id="f32e3-186">N'Ko</span><span class="sxs-lookup"><span data-stu-id="f32e3-186">N'Ko</span></span>               | <span data-ttu-id="f32e3-187">Ebrima</span><span class="sxs-lookup"><span data-stu-id="f32e3-187">Ebrima</span></span>                |
| <span data-ttu-id="f32e3-188">Ogham</span><span class="sxs-lookup"><span data-stu-id="f32e3-188">Ogham</span></span>              | <span data-ttu-id="f32e3-189">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="f32e3-189">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="f32e3-190">OL Chiki</span><span class="sxs-lookup"><span data-stu-id="f32e3-190">Ol Chiki</span></span>           | <span data-ttu-id="f32e3-191">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-191">Nirmala UI</span></span>            |
| <span data-ttu-id="f32e3-192">Turca anterior</span><span class="sxs-lookup"><span data-stu-id="f32e3-192">Old Turkic</span></span>         | <span data-ttu-id="f32e3-193">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="f32e3-193">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="f32e3-194">Odia</span><span class="sxs-lookup"><span data-stu-id="f32e3-194">Oriya</span></span>              | <span data-ttu-id="f32e3-195">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-195">Nirmala UI</span></span>            |
| <span data-ttu-id="f32e3-196">Osmanya</span><span class="sxs-lookup"><span data-stu-id="f32e3-196">Osmanya</span></span>            | <span data-ttu-id="f32e3-197">Ebrima</span><span class="sxs-lookup"><span data-stu-id="f32e3-197">Ebrima</span></span>                |
| <span data-ttu-id="f32e3-198">Phags-pa</span><span class="sxs-lookup"><span data-stu-id="f32e3-198">Phags-pa</span></span>           | <span data-ttu-id="f32e3-199">Microsoft PhagsPa</span><span class="sxs-lookup"><span data-stu-id="f32e3-199">Microsoft PhagsPa</span></span>     |
| <span data-ttu-id="f32e3-200">Rúnica</span><span class="sxs-lookup"><span data-stu-id="f32e3-200">Runic</span></span>              | <span data-ttu-id="f32e3-201">Segoe UI Symbol</span><span class="sxs-lookup"><span data-stu-id="f32e3-201">Segoe UI Symbol</span></span>       |
| <span data-ttu-id="f32e3-202">Sora Sompeng</span><span class="sxs-lookup"><span data-stu-id="f32e3-202">Sora Sompeng</span></span>       | <span data-ttu-id="f32e3-203">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-203">Nirmala UI</span></span>            |
| <span data-ttu-id="f32e3-204">Cingalés</span><span class="sxs-lookup"><span data-stu-id="f32e3-204">Sinhala</span></span>            | <span data-ttu-id="f32e3-205">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-205">Nirmala UI</span></span>            |
| <span data-ttu-id="f32e3-206">Siríaco</span><span class="sxs-lookup"><span data-stu-id="f32e3-206">Syriac</span></span>             | <span data-ttu-id="f32e3-207">Estrangelo Edessa</span><span class="sxs-lookup"><span data-stu-id="f32e3-207">Estrangelo Edessa</span></span>     |
| <span data-ttu-id="f32e3-208">Tai le</span><span class="sxs-lookup"><span data-stu-id="f32e3-208">Tai Le</span></span>             | <span data-ttu-id="f32e3-209">Microsoft Tai Le</span><span class="sxs-lookup"><span data-stu-id="f32e3-209">Microsoft Tai Le</span></span>      |
| <span data-ttu-id="f32e3-210">Nuevo tai lue moderno</span><span class="sxs-lookup"><span data-stu-id="f32e3-210">New Tai Lue</span></span>        | <span data-ttu-id="f32e3-211">Microsoft New Tai Lue</span><span class="sxs-lookup"><span data-stu-id="f32e3-211">Microsoft New Tai Lue</span></span> |
| <span data-ttu-id="f32e3-212">Tamil</span><span class="sxs-lookup"><span data-stu-id="f32e3-212">Tamil</span></span>              | <span data-ttu-id="f32e3-213">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-213">Nirmala UI</span></span>            |
| <span data-ttu-id="f32e3-214">Telugu</span><span class="sxs-lookup"><span data-stu-id="f32e3-214">Telugu</span></span>             | <span data-ttu-id="f32e3-215">Nirmala UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-215">Nirmala UI</span></span>            |
| <span data-ttu-id="f32e3-216">Tifinagh</span><span class="sxs-lookup"><span data-stu-id="f32e3-216">Tifinagh</span></span>           | <span data-ttu-id="f32e3-217">Ebrima</span><span class="sxs-lookup"><span data-stu-id="f32e3-217">Ebrima</span></span>                |
| <span data-ttu-id="f32e3-218">Thaana</span><span class="sxs-lookup"><span data-stu-id="f32e3-218">Thaana</span></span>             | <span data-ttu-id="f32e3-219">MV Boli</span><span class="sxs-lookup"><span data-stu-id="f32e3-219">MV Boli</span></span>               |
| <span data-ttu-id="f32e3-220">Tailandés</span><span class="sxs-lookup"><span data-stu-id="f32e3-220">Thai</span></span>               | <span data-ttu-id="f32e3-221">Leelawadee UI</span><span class="sxs-lookup"><span data-stu-id="f32e3-221">Leelawadee UI</span></span>         |
| <span data-ttu-id="f32e3-222">Tibetano</span><span class="sxs-lookup"><span data-stu-id="f32e3-222">Tibetan</span></span>            | <span data-ttu-id="f32e3-223">Microsoft Himalaya</span><span class="sxs-lookup"><span data-stu-id="f32e3-223">Microsoft Himalaya</span></span>    |
| <span data-ttu-id="f32e3-224">Vai</span><span class="sxs-lookup"><span data-stu-id="f32e3-224">Vai</span></span>                | <span data-ttu-id="f32e3-225">Ebrima</span><span class="sxs-lookup"><span data-stu-id="f32e3-225">Ebrima</span></span>                |
| <span data-ttu-id="f32e3-226">Yi</span><span class="sxs-lookup"><span data-stu-id="f32e3-226">Yi</span></span>                 | <span data-ttu-id="f32e3-227">Microsoft Yi Baiti</span><span class="sxs-lookup"><span data-stu-id="f32e3-227">Microsoft Yi Baiti</span></span>    |



 

 

 




