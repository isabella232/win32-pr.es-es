---
description: Los campos de códigos de subconjuntos Unicode (USBs) se usan en las estructuras FONTSIGNATURE y LOCALESIGNATURE.
ms.assetid: f897dfc7-3e78-48dc-8d3d-6929e2f4ec4d
title: Campos de códigos de subconjunto Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fced251b1bf8e04dd4c0d7d7cb0dca15c8bdfa6b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105652865"
---
# <a name="unicode-subset-bitfields"></a><span data-ttu-id="84105-103">Campos de códigos de subconjunto Unicode</span><span class="sxs-lookup"><span data-stu-id="84105-103">Unicode Subset Bitfields</span></span>

<span data-ttu-id="84105-104">Los campos de códigos de subconjuntos Unicode (USBs) se usan en las estructuras [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) y [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) .</span><span class="sxs-lookup"><span data-stu-id="84105-104">The Unicode subset bitfields (USBs) are used in the [**FONTSIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-fontsignature) and [**LOCALESIGNATURE**](/windows/win32/api/wingdi/ns-wingdi-localesignature) structures.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="84105-105">bit</span><span class="sxs-lookup"><span data-stu-id="84105-105">Bit</span></span></th>
<th><span data-ttu-id="84105-106">Subintervalo Unicode</span><span class="sxs-lookup"><span data-stu-id="84105-106">Unicode subrange</span></span></th>
<th><span data-ttu-id="84105-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="84105-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="84105-108">0</span><span class="sxs-lookup"><span data-stu-id="84105-108">0</span></span></td>
<td><span data-ttu-id="84105-109">0000 - 007F</span><span class="sxs-lookup"><span data-stu-id="84105-109">0000 - 007F</span></span></td>
<td><span data-ttu-id="84105-110">Latín básico</span><span class="sxs-lookup"><span data-stu-id="84105-110">Basic Latin</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-111">1</span><span class="sxs-lookup"><span data-stu-id="84105-111">1</span></span></td>
<td><span data-ttu-id="84105-112">0080 - 00FF</span><span class="sxs-lookup"><span data-stu-id="84105-112">0080 - 00FF</span></span></td>
<td><span data-ttu-id="84105-113">Suplemento Latín-1</span><span class="sxs-lookup"><span data-stu-id="84105-113">Latin-1 Supplement</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-114">2</span><span class="sxs-lookup"><span data-stu-id="84105-114">2</span></span></td>
<td><span data-ttu-id="84105-115">0100 - 017F</span><span class="sxs-lookup"><span data-stu-id="84105-115">0100 - 017F</span></span></td>
<td><span data-ttu-id="84105-116">Latín extendido-A</span><span class="sxs-lookup"><span data-stu-id="84105-116">Latin Extended-A</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-117">3</span><span class="sxs-lookup"><span data-stu-id="84105-117">3</span></span></td>
<td><span data-ttu-id="84105-118">0180 - 024F</span><span class="sxs-lookup"><span data-stu-id="84105-118">0180 - 024F</span></span></td>
<td><span data-ttu-id="84105-119">Latín extendido-B</span><span class="sxs-lookup"><span data-stu-id="84105-119">Latin Extended-B</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="84105-120">4 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-120">4${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-121">0250 - 02AF</span><span class="sxs-lookup"><span data-stu-id="84105-121">0250 - 02AF</span></span></td>
<td><span data-ttu-id="84105-122">Extensiones IPA</span><span class="sxs-lookup"><span data-stu-id="84105-122">IPA Extensions</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-123">1D00 - 1D7F</span><span class="sxs-lookup"><span data-stu-id="84105-123">1D00 - 1D7F</span></span></td>
<td><span data-ttu-id="84105-124">Extensiones fonéticas</span><span class="sxs-lookup"><span data-stu-id="84105-124">Phonetic Extensions</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-125">1D80 - 1DBF</span><span class="sxs-lookup"><span data-stu-id="84105-125">1D80 - 1DBF</span></span></td>
<td><span data-ttu-id="84105-126">Suplemento de extensiones fonéticas</span><span class="sxs-lookup"><span data-stu-id="84105-126">Phonetic Extensions Supplement</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="84105-127">5 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-127">5${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-128">02B0 - 02FF</span><span class="sxs-lookup"><span data-stu-id="84105-128">02B0 - 02FF</span></span></td>
<td><span data-ttu-id="84105-129">Letras modificadoras de espaciado</span><span class="sxs-lookup"><span data-stu-id="84105-129">Spacing Modifier Letters</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-130">A700 - A71F</span><span class="sxs-lookup"><span data-stu-id="84105-130">A700 - A71F</span></span></td>
<td><span data-ttu-id="84105-131">Letras de tono modificador</span><span class="sxs-lookup"><span data-stu-id="84105-131">Modifier Tone Letters</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="84105-132">6 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-132">6${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-133">0300 - 036F</span><span class="sxs-lookup"><span data-stu-id="84105-133">0300 - 036F</span></span></td>
<td><span data-ttu-id="84105-134">Combinación de marcas diacríticas</span><span class="sxs-lookup"><span data-stu-id="84105-134">Combining Diacritical Marks</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-135">1DC0 - 1DFF</span><span class="sxs-lookup"><span data-stu-id="84105-135">1DC0 - 1DFF</span></span></td>
<td><span data-ttu-id="84105-136">Suplemento de combinación de marcas diacríticas</span><span class="sxs-lookup"><span data-stu-id="84105-136">Combining Diacritical Marks Supplement</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-137">7</span><span class="sxs-lookup"><span data-stu-id="84105-137">7</span></span></td>
<td><span data-ttu-id="84105-138">0370 - 03FF</span><span class="sxs-lookup"><span data-stu-id="84105-138">0370 - 03FF</span></span></td>
<td><span data-ttu-id="84105-139">Griego y cóptico</span><span class="sxs-lookup"><span data-stu-id="84105-139">Greek and Coptic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-140">8</span><span class="sxs-lookup"><span data-stu-id="84105-140">8</span></span></td>
<td><span data-ttu-id="84105-141">2C80 - 2CFF</span><span class="sxs-lookup"><span data-stu-id="84105-141">2C80 - 2CFF</span></span></td>
<td><span data-ttu-id="84105-142">Copto</span><span class="sxs-lookup"><span data-stu-id="84105-142">Coptic</span></span></td>
</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="84105-143">9 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-143">9${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-144">0400 - 04FF</span><span class="sxs-lookup"><span data-stu-id="84105-144">0400 - 04FF</span></span></td>
<td><span data-ttu-id="84105-145">Cirílico</span><span class="sxs-lookup"><span data-stu-id="84105-145">Cyrillic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-146">0500 - 052F</span><span class="sxs-lookup"><span data-stu-id="84105-146">0500 - 052F</span></span></td>
<td><span data-ttu-id="84105-147">Suplemento cirílico</span><span class="sxs-lookup"><span data-stu-id="84105-147">Cyrillic Supplement</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-148">2DE0 - 2DFF</span><span class="sxs-lookup"><span data-stu-id="84105-148">2DE0 - 2DFF</span></span></td>
<td><span data-ttu-id="84105-149">Cirílico extendido-A</span><span class="sxs-lookup"><span data-stu-id="84105-149">Cyrillic Extended-A</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-150">A640 - A69F</span><span class="sxs-lookup"><span data-stu-id="84105-150">A640 - A69F</span></span></td>
<td><span data-ttu-id="84105-151">Cirílico extendido-B</span><span class="sxs-lookup"><span data-stu-id="84105-151">Cyrillic Extended-B</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-152">10</span><span class="sxs-lookup"><span data-stu-id="84105-152">10</span></span></td>
<td><span data-ttu-id="84105-153">0530 - 058F</span><span class="sxs-lookup"><span data-stu-id="84105-153">0530 - 058F</span></span></td>
<td><span data-ttu-id="84105-154">Armenio</span><span class="sxs-lookup"><span data-stu-id="84105-154">Armenian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-155">11</span><span class="sxs-lookup"><span data-stu-id="84105-155">11</span></span></td>
<td><span data-ttu-id="84105-156">0590 - 05FF</span><span class="sxs-lookup"><span data-stu-id="84105-156">0590 - 05FF</span></span></td>
<td><span data-ttu-id="84105-157">Hebreo</span><span class="sxs-lookup"><span data-stu-id="84105-157">Hebrew</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-158">12</span><span class="sxs-lookup"><span data-stu-id="84105-158">12</span></span></td>
<td><span data-ttu-id="84105-159">A500 - A63F</span><span class="sxs-lookup"><span data-stu-id="84105-159">A500 - A63F</span></span></td>
<td><span data-ttu-id="84105-160">Vai</span><span class="sxs-lookup"><span data-stu-id="84105-160">Vai</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="84105-161">13 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-161">13${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-162">0600 - 06FF</span><span class="sxs-lookup"><span data-stu-id="84105-162">0600 - 06FF</span></span></td>
<td><span data-ttu-id="84105-163">Árabe</span><span class="sxs-lookup"><span data-stu-id="84105-163">Arabic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-164">0750-077F</span><span class="sxs-lookup"><span data-stu-id="84105-164">0750 - 077F</span></span></td>
<td><span data-ttu-id="84105-165">Suplemento Árabe</span><span class="sxs-lookup"><span data-stu-id="84105-165">Arabic Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-166">14</span><span class="sxs-lookup"><span data-stu-id="84105-166">14</span></span></td>
<td><span data-ttu-id="84105-167">07C0 - 07FF</span><span class="sxs-lookup"><span data-stu-id="84105-167">07C0 - 07FF</span></span></td>
<td><span data-ttu-id="84105-168">Símbolo</span><span class="sxs-lookup"><span data-stu-id="84105-168">NKo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-169">15</span><span class="sxs-lookup"><span data-stu-id="84105-169">15</span></span></td>
<td><span data-ttu-id="84105-170">0900 - 097F</span><span class="sxs-lookup"><span data-stu-id="84105-170">0900 - 097F</span></span></td>
<td><span data-ttu-id="84105-171">Devanagari</span><span class="sxs-lookup"><span data-stu-id="84105-171">Devanagari</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-172">16</span><span class="sxs-lookup"><span data-stu-id="84105-172">16</span></span></td>
<td><span data-ttu-id="84105-173">0980 - 09FF</span><span class="sxs-lookup"><span data-stu-id="84105-173">0980 - 09FF</span></span></td>
<td><span data-ttu-id="84105-174">Bengalí</span><span class="sxs-lookup"><span data-stu-id="84105-174">Bangla</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-175">17</span><span class="sxs-lookup"><span data-stu-id="84105-175">17</span></span></td>
<td><span data-ttu-id="84105-176">0A00 - 0A7F</span><span class="sxs-lookup"><span data-stu-id="84105-176">0A00 - 0A7F</span></span></td>
<td><span data-ttu-id="84105-177">Gurmukhi</span><span class="sxs-lookup"><span data-stu-id="84105-177">Gurmukhi</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-178">18</span><span class="sxs-lookup"><span data-stu-id="84105-178">18</span></span></td>
<td><span data-ttu-id="84105-179">0A80 - 0AFF</span><span class="sxs-lookup"><span data-stu-id="84105-179">0A80 - 0AFF</span></span></td>
<td><span data-ttu-id="84105-180">Gujarati</span><span class="sxs-lookup"><span data-stu-id="84105-180">Gujarati</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-181">19</span><span class="sxs-lookup"><span data-stu-id="84105-181">19</span></span></td>
<td><span data-ttu-id="84105-182">0B00 - 0B7F</span><span class="sxs-lookup"><span data-stu-id="84105-182">0B00 - 0B7F</span></span></td>
<td><span data-ttu-id="84105-183">Odia</span><span class="sxs-lookup"><span data-stu-id="84105-183">Odia</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-184">20</span><span class="sxs-lookup"><span data-stu-id="84105-184">20</span></span></td>
<td><span data-ttu-id="84105-185">0B80 - 0BFF</span><span class="sxs-lookup"><span data-stu-id="84105-185">0B80 - 0BFF</span></span></td>
<td><span data-ttu-id="84105-186">Tamil</span><span class="sxs-lookup"><span data-stu-id="84105-186">Tamil</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-187">21</span><span class="sxs-lookup"><span data-stu-id="84105-187">21</span></span></td>
<td><span data-ttu-id="84105-188">0C00 - 0C7F</span><span class="sxs-lookup"><span data-stu-id="84105-188">0C00 - 0C7F</span></span></td>
<td><span data-ttu-id="84105-189">Telugu</span><span class="sxs-lookup"><span data-stu-id="84105-189">Telugu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-190">22</span><span class="sxs-lookup"><span data-stu-id="84105-190">22</span></span></td>
<td><span data-ttu-id="84105-191">0C80 - 0CFF</span><span class="sxs-lookup"><span data-stu-id="84105-191">0C80 - 0CFF</span></span></td>
<td><span data-ttu-id="84105-192">Canarés</span><span class="sxs-lookup"><span data-stu-id="84105-192">Kannada</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-193">23</span><span class="sxs-lookup"><span data-stu-id="84105-193">23</span></span></td>
<td><span data-ttu-id="84105-194">0D00 - 0D7F</span><span class="sxs-lookup"><span data-stu-id="84105-194">0D00 - 0D7F</span></span></td>
<td><span data-ttu-id="84105-195">Malayalam</span><span class="sxs-lookup"><span data-stu-id="84105-195">Malayalam</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-196">24</span><span class="sxs-lookup"><span data-stu-id="84105-196">24</span></span></td>
<td><span data-ttu-id="84105-197">0E00 - 0E7F</span><span class="sxs-lookup"><span data-stu-id="84105-197">0E00 - 0E7F</span></span></td>
<td><span data-ttu-id="84105-198">Tailandés</span><span class="sxs-lookup"><span data-stu-id="84105-198">Thai</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-199">25</span><span class="sxs-lookup"><span data-stu-id="84105-199">25</span></span></td>
<td><span data-ttu-id="84105-200">0E80 - 0EFF</span><span class="sxs-lookup"><span data-stu-id="84105-200">0E80 - 0EFF</span></span></td>
<td><span data-ttu-id="84105-201">Lao</span><span class="sxs-lookup"><span data-stu-id="84105-201">Lao</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="84105-202">26 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-202">26${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-203">10A0 - 10FF</span><span class="sxs-lookup"><span data-stu-id="84105-203">10A0 - 10FF</span></span></td>
<td><span data-ttu-id="84105-204">Georgiano</span><span class="sxs-lookup"><span data-stu-id="84105-204">Georgian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-205">2D00 - 2D2F</span><span class="sxs-lookup"><span data-stu-id="84105-205">2D00 - 2D2F</span></span></td>
<td><span data-ttu-id="84105-206">Suplemento georgiano</span><span class="sxs-lookup"><span data-stu-id="84105-206">Georgian Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-207">27</span><span class="sxs-lookup"><span data-stu-id="84105-207">27</span></span></td>
<td><span data-ttu-id="84105-208">1B00 - 1B7F</span><span class="sxs-lookup"><span data-stu-id="84105-208">1B00 - 1B7F</span></span></td>
<td><span data-ttu-id="84105-209">Balinés</span><span class="sxs-lookup"><span data-stu-id="84105-209">Balinese</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-210">28</span><span class="sxs-lookup"><span data-stu-id="84105-210">28</span></span></td>
<td><span data-ttu-id="84105-211">1100 - 11FF</span><span class="sxs-lookup"><span data-stu-id="84105-211">1100 - 11FF</span></span></td>
<td><span data-ttu-id="84105-212">Jamo hangul</span><span class="sxs-lookup"><span data-stu-id="84105-212">Hangul Jamo</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="84105-213">29 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-213">29${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-214">1E00 - 1EFF</span><span class="sxs-lookup"><span data-stu-id="84105-214">1E00 - 1EFF</span></span></td>
<td><span data-ttu-id="84105-215">Latín extendido adicional</span><span class="sxs-lookup"><span data-stu-id="84105-215">Latin Extended Additional</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-216">2C60 - 2C7F</span><span class="sxs-lookup"><span data-stu-id="84105-216">2C60 - 2C7F</span></span></td>
<td><span data-ttu-id="84105-217">Latín extendido-C</span><span class="sxs-lookup"><span data-stu-id="84105-217">Latin Extended-C</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-218">A720 - A7FF</span><span class="sxs-lookup"><span data-stu-id="84105-218">A720 - A7FF</span></span></td>
<td><span data-ttu-id="84105-219">Latín extendido-D</span><span class="sxs-lookup"><span data-stu-id="84105-219">Latin Extended-D</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-220">30</span><span class="sxs-lookup"><span data-stu-id="84105-220">30</span></span></td>
<td><span data-ttu-id="84105-221">1F00 - 1FFF</span><span class="sxs-lookup"><span data-stu-id="84105-221">1F00 - 1FFF</span></span></td>
<td><span data-ttu-id="84105-222">Griego extendido</span><span class="sxs-lookup"><span data-stu-id="84105-222">Greek Extended</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="84105-223">31 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-223">31${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-224">2000 - 206F</span><span class="sxs-lookup"><span data-stu-id="84105-224">2000 - 206F</span></span></td>
<td><span data-ttu-id="84105-225">Puntuación general</span><span class="sxs-lookup"><span data-stu-id="84105-225">General Punctuation</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-226">2E00 - 2E7F</span><span class="sxs-lookup"><span data-stu-id="84105-226">2E00 - 2E7F</span></span></td>
<td><span data-ttu-id="84105-227">Puntuación complementaria</span><span class="sxs-lookup"><span data-stu-id="84105-227">Supplemental Punctuation</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-228">32</span><span class="sxs-lookup"><span data-stu-id="84105-228">32</span></span></td>
<td><span data-ttu-id="84105-229">2070 - 209F</span><span class="sxs-lookup"><span data-stu-id="84105-229">2070 - 209F</span></span></td>
<td><span data-ttu-id="84105-230">Superíndices y subíndices</span><span class="sxs-lookup"><span data-stu-id="84105-230">Superscripts And Subscripts</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-231">33</span><span class="sxs-lookup"><span data-stu-id="84105-231">33</span></span></td>
<td><span data-ttu-id="84105-232">20A0 - 20CF</span><span class="sxs-lookup"><span data-stu-id="84105-232">20A0 - 20CF</span></span></td>
<td><span data-ttu-id="84105-233">Símbolos de moneda</span><span class="sxs-lookup"><span data-stu-id="84105-233">Currency Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-234">34</span><span class="sxs-lookup"><span data-stu-id="84105-234">34</span></span></td>
<td><span data-ttu-id="84105-235">20D0 - 20FF</span><span class="sxs-lookup"><span data-stu-id="84105-235">20D0 - 20FF</span></span></td>
<td><span data-ttu-id="84105-236">Combinación de marcas diacríticas para símbolos</span><span class="sxs-lookup"><span data-stu-id="84105-236">Combining Diacritical Marks For Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-237">35</span><span class="sxs-lookup"><span data-stu-id="84105-237">35</span></span></td>
<td><span data-ttu-id="84105-238">2100 - 214F</span><span class="sxs-lookup"><span data-stu-id="84105-238">2100 - 214F</span></span></td>
<td><span data-ttu-id="84105-239">Símbolos de Letterlike</span><span class="sxs-lookup"><span data-stu-id="84105-239">Letterlike Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-240">36</span><span class="sxs-lookup"><span data-stu-id="84105-240">36</span></span></td>
<td><span data-ttu-id="84105-241">2150 - 218F</span><span class="sxs-lookup"><span data-stu-id="84105-241">2150 - 218F</span></span></td>
<td><span data-ttu-id="84105-242">Formatos numéricos</span><span class="sxs-lookup"><span data-stu-id="84105-242">Number Forms</span></span></td>
</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="84105-243">37 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-243">37${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-244">2190 - 21FF</span><span class="sxs-lookup"><span data-stu-id="84105-244">2190 - 21FF</span></span></td>
<td><span data-ttu-id="84105-245">Flechas</span><span class="sxs-lookup"><span data-stu-id="84105-245">Arrows</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-246">27F0 - 27FF</span><span class="sxs-lookup"><span data-stu-id="84105-246">27F0 - 27FF</span></span></td>
<td><span data-ttu-id="84105-247">Flechas adicionales-A</span><span class="sxs-lookup"><span data-stu-id="84105-247">Supplemental Arrows-A</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-248">2900 - 297F</span><span class="sxs-lookup"><span data-stu-id="84105-248">2900 - 297F</span></span></td>
<td><span data-ttu-id="84105-249">Flechas adicionales-B</span><span class="sxs-lookup"><span data-stu-id="84105-249">Supplemental Arrows-B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-250">2B00 - 2BFF</span><span class="sxs-lookup"><span data-stu-id="84105-250">2B00 - 2BFF</span></span></td>
<td><span data-ttu-id="84105-251">Símbolos y flechas varios</span><span class="sxs-lookup"><span data-stu-id="84105-251">Miscellaneous Symbols and Arrows</span></span></td>

</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="84105-252">38 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-252">38${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-253">2200 - 22FF</span><span class="sxs-lookup"><span data-stu-id="84105-253">2200 - 22FF</span></span></td>
<td><span data-ttu-id="84105-254">Operadores matemáticos</span><span class="sxs-lookup"><span data-stu-id="84105-254">Mathematical Operators</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-255">27C0 - 27EF</span><span class="sxs-lookup"><span data-stu-id="84105-255">27C0 - 27EF</span></span></td>
<td><span data-ttu-id="84105-256">Símbolos matemáticos varios: A</span><span class="sxs-lookup"><span data-stu-id="84105-256">Miscellaneous Mathematical Symbols-A</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-257">2980 - 29FF</span><span class="sxs-lookup"><span data-stu-id="84105-257">2980 - 29FF</span></span></td>
<td><span data-ttu-id="84105-258">Símbolos matemáticos varios-B</span><span class="sxs-lookup"><span data-stu-id="84105-258">Miscellaneous Mathematical Symbols-B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-259">2A00 - 2AFF</span><span class="sxs-lookup"><span data-stu-id="84105-259">2A00 - 2AFF</span></span></td>
<td><span data-ttu-id="84105-260">Operadores matemáticos adicionales</span><span class="sxs-lookup"><span data-stu-id="84105-260">Supplemental Mathematical Operators</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-261">39</span><span class="sxs-lookup"><span data-stu-id="84105-261">39</span></span></td>
<td><span data-ttu-id="84105-262">2300 - 23FF</span><span class="sxs-lookup"><span data-stu-id="84105-262">2300 - 23FF</span></span></td>
<td><span data-ttu-id="84105-263">Aspectos técnicos diversos</span><span class="sxs-lookup"><span data-stu-id="84105-263">Miscellaneous Technical</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-264">40</span><span class="sxs-lookup"><span data-stu-id="84105-264">40</span></span></td>
<td><span data-ttu-id="84105-265">2400 - 243F</span><span class="sxs-lookup"><span data-stu-id="84105-265">2400 - 243F</span></span></td>
<td><span data-ttu-id="84105-266">Imágenes de control</span><span class="sxs-lookup"><span data-stu-id="84105-266">Control Pictures</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-267">41</span><span class="sxs-lookup"><span data-stu-id="84105-267">41</span></span></td>
<td><span data-ttu-id="84105-268">2440 - 245F</span><span class="sxs-lookup"><span data-stu-id="84105-268">2440 - 245F</span></span></td>
<td><span data-ttu-id="84105-269">Reconocimiento óptico de caracteres</span><span class="sxs-lookup"><span data-stu-id="84105-269">Optical Character Recognition</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-270">42</span><span class="sxs-lookup"><span data-stu-id="84105-270">42</span></span></td>
<td><span data-ttu-id="84105-271">2460 - 24FF</span><span class="sxs-lookup"><span data-stu-id="84105-271">2460 - 24FF</span></span></td>
<td><span data-ttu-id="84105-272">Alfanuméricos delimitados</span><span class="sxs-lookup"><span data-stu-id="84105-272">Enclosed Alphanumerics</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-273">43</span><span class="sxs-lookup"><span data-stu-id="84105-273">43</span></span></td>
<td><span data-ttu-id="84105-274">2500 - 257F</span><span class="sxs-lookup"><span data-stu-id="84105-274">2500 - 257F</span></span></td>
<td><span data-ttu-id="84105-275">Dibujo de caja</span><span class="sxs-lookup"><span data-stu-id="84105-275">Box Drawing</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-276">44</span><span class="sxs-lookup"><span data-stu-id="84105-276">44</span></span></td>
<td><span data-ttu-id="84105-277">2580 - 259F</span><span class="sxs-lookup"><span data-stu-id="84105-277">2580 - 259F</span></span></td>
<td><span data-ttu-id="84105-278">Elementos de bloque</span><span class="sxs-lookup"><span data-stu-id="84105-278">Block Elements</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-279">45</span><span class="sxs-lookup"><span data-stu-id="84105-279">45</span></span></td>
<td><span data-ttu-id="84105-280">25A0 - 25FF</span><span class="sxs-lookup"><span data-stu-id="84105-280">25A0 - 25FF</span></span></td>
<td><span data-ttu-id="84105-281">Formas geométricas</span><span class="sxs-lookup"><span data-stu-id="84105-281">Geometric Shapes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-282">46</span><span class="sxs-lookup"><span data-stu-id="84105-282">46</span></span></td>
<td><span data-ttu-id="84105-283">2600 - 26FF</span><span class="sxs-lookup"><span data-stu-id="84105-283">2600 - 26FF</span></span></td>
<td><span data-ttu-id="84105-284">Símbolos varios</span><span class="sxs-lookup"><span data-stu-id="84105-284">Miscellaneous Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-285">47</span><span class="sxs-lookup"><span data-stu-id="84105-285">47</span></span></td>
<td><span data-ttu-id="84105-286">2700 - 27BF</span><span class="sxs-lookup"><span data-stu-id="84105-286">2700 - 27BF</span></span></td>
<td><span data-ttu-id="84105-287">Dingbats</span><span class="sxs-lookup"><span data-stu-id="84105-287">Dingbats</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-288">48</span><span class="sxs-lookup"><span data-stu-id="84105-288">48</span></span></td>
<td><span data-ttu-id="84105-289">3000 - 303F</span><span class="sxs-lookup"><span data-stu-id="84105-289">3000 - 303F</span></span></td>
<td><span data-ttu-id="84105-290">Símbolos y puntuación CJK</span><span class="sxs-lookup"><span data-stu-id="84105-290">CJK Symbols And Punctuation</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-291">49</span><span class="sxs-lookup"><span data-stu-id="84105-291">49</span></span></td>
<td><span data-ttu-id="84105-292">3040 - 309F</span><span class="sxs-lookup"><span data-stu-id="84105-292">3040 - 309F</span></span></td>
<td><span data-ttu-id="84105-293">Hiragana</span><span class="sxs-lookup"><span data-stu-id="84105-293">Hiragana</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="84105-294">50 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-294">50${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-295">30A0 - 30FF</span><span class="sxs-lookup"><span data-stu-id="84105-295">30A0 - 30FF</span></span></td>
<td><span data-ttu-id="84105-296">Katakana</span><span class="sxs-lookup"><span data-stu-id="84105-296">Katakana</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-297">31F0 - 31FF</span><span class="sxs-lookup"><span data-stu-id="84105-297">31F0 - 31FF</span></span></td>
<td><span data-ttu-id="84105-298">Extensiones fonéticas katakana</span><span class="sxs-lookup"><span data-stu-id="84105-298">Katakana Phonetic Extensions</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="84105-299">51 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-299">51${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-300">3100 - 312F</span><span class="sxs-lookup"><span data-stu-id="84105-300">3100 - 312F</span></span></td>
<td><span data-ttu-id="84105-301">Bopomofo</span><span class="sxs-lookup"><span data-stu-id="84105-301">Bopomofo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-302">31A0 - 31BF</span><span class="sxs-lookup"><span data-stu-id="84105-302">31A0 - 31BF</span></span></td>
<td><span data-ttu-id="84105-303">Bopomofo extendido</span><span class="sxs-lookup"><span data-stu-id="84105-303">Bopomofo Extended</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-304">52</span><span class="sxs-lookup"><span data-stu-id="84105-304">52</span></span></td>
<td><span data-ttu-id="84105-305">3130 - 318F</span><span class="sxs-lookup"><span data-stu-id="84105-305">3130 - 318F</span></span></td>
<td><span data-ttu-id="84105-306">Compatibilidad con hangul Jamo</span><span class="sxs-lookup"><span data-stu-id="84105-306">Hangul Compatibility Jamo</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-307">53</span><span class="sxs-lookup"><span data-stu-id="84105-307">53</span></span></td>
<td><span data-ttu-id="84105-308">A840 - A87F</span><span class="sxs-lookup"><span data-stu-id="84105-308">A840 - A87F</span></span></td>
<td><span data-ttu-id="84105-309">Phags-pa</span><span class="sxs-lookup"><span data-stu-id="84105-309">Phags-pa</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-310">54</span><span class="sxs-lookup"><span data-stu-id="84105-310">54</span></span></td>
<td><span data-ttu-id="84105-311">3200 - 32FF</span><span class="sxs-lookup"><span data-stu-id="84105-311">3200 - 32FF</span></span></td>
<td><span data-ttu-id="84105-312">Letras y meses CJK delimitados</span><span class="sxs-lookup"><span data-stu-id="84105-312">Enclosed CJK Letters And Months</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-313">55</span><span class="sxs-lookup"><span data-stu-id="84105-313">55</span></span></td>
<td><span data-ttu-id="84105-314">3300 - 33FF</span><span class="sxs-lookup"><span data-stu-id="84105-314">3300 - 33FF</span></span></td>
<td><span data-ttu-id="84105-315">Compatibilidad con CJK</span><span class="sxs-lookup"><span data-stu-id="84105-315">CJK Compatibility</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-316">56</span><span class="sxs-lookup"><span data-stu-id="84105-316">56</span></span></td>
<td><span data-ttu-id="84105-317">AC00 - D7AF</span><span class="sxs-lookup"><span data-stu-id="84105-317">AC00 - D7AF</span></span></td>
<td><span data-ttu-id="84105-318">Sílabas hangul</span><span class="sxs-lookup"><span data-stu-id="84105-318">Hangul Syllables</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-319">57</span><span class="sxs-lookup"><span data-stu-id="84105-319">57</span></span></td>
<td><span data-ttu-id="84105-320">D800-DFFF</span><span class="sxs-lookup"><span data-stu-id="84105-320">D800 - DFFF</span></span></td>
<td><span data-ttu-id="84105-321">No plano 0.</span><span class="sxs-lookup"><span data-stu-id="84105-321">Non-Plane 0.</span></span> <span data-ttu-id="84105-322">Tenga en cuenta que establecer este bit implica que hay al menos un punto de código suplementario más allá del plano básico multilingüe (BMP) que es compatible con esta fuente.</span><span class="sxs-lookup"><span data-stu-id="84105-322">Note that setting this bit implies that there is at least one supplementary code point beyond the Basic Multilingual Plane (BMP) that is supported by this font.</span></span> <span data-ttu-id="84105-323">Vea <a href="surrogates-and-supplementary-characters.md">suplentes y caracteres adicionales</a>.</span><span class="sxs-lookup"><span data-stu-id="84105-323">See <a href="surrogates-and-supplementary-characters.md">Surrogates and Supplementary Characters</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-324">58</span><span class="sxs-lookup"><span data-stu-id="84105-324">58</span></span></td>
<td><span data-ttu-id="84105-325">10900-1091F</span><span class="sxs-lookup"><span data-stu-id="84105-325">10900 - 1091F</span></span></td>
<td><span data-ttu-id="84105-326">Phoenician</span><span class="sxs-lookup"><span data-stu-id="84105-326">Phoenician</span></span></td>
</tr>
<tr class="even">
<td rowspan="7"><span data-ttu-id="84105-327">59 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-327">59${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-328">2E80 - 2EFF</span><span class="sxs-lookup"><span data-stu-id="84105-328">2E80 - 2EFF</span></span></td>
<td><span data-ttu-id="84105-329">Suplemento de radicales CJK</span><span class="sxs-lookup"><span data-stu-id="84105-329">CJK Radicals Supplement</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-330">2F00 - 2FDF</span><span class="sxs-lookup"><span data-stu-id="84105-330">2F00 - 2FDF</span></span></td>
<td><span data-ttu-id="84105-331">Radicales kangxi</span><span class="sxs-lookup"><span data-stu-id="84105-331">Kangxi Radicals</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-332">2FF0 - 2FFF</span><span class="sxs-lookup"><span data-stu-id="84105-332">2FF0 - 2FFF</span></span></td>
<td><span data-ttu-id="84105-333">Caracteres de descripción ideográfica</span><span class="sxs-lookup"><span data-stu-id="84105-333">Ideographic Description Characters</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-334">3190 - 319F</span><span class="sxs-lookup"><span data-stu-id="84105-334">3190 - 319F</span></span></td>
<td><span data-ttu-id="84105-335">Kanbun</span><span class="sxs-lookup"><span data-stu-id="84105-335">Kanbun</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-336">3400 - 4DBF</span><span class="sxs-lookup"><span data-stu-id="84105-336">3400 - 4DBF</span></span></td>
<td><span data-ttu-id="84105-337">Extensión A de Ideogramas unificados CJK</span><span class="sxs-lookup"><span data-stu-id="84105-337">CJK Unified Ideographs Extension A</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-338">4E00 - 9FFF</span><span class="sxs-lookup"><span data-stu-id="84105-338">4E00 - 9FFF</span></span></td>
<td><span data-ttu-id="84105-339">Ideogramas unificados CJK</span><span class="sxs-lookup"><span data-stu-id="84105-339">CJK Unified Ideographs</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-340">20000-2A6DF</span><span class="sxs-lookup"><span data-stu-id="84105-340">20000 - 2A6DF</span></span></td>
<td><span data-ttu-id="84105-341">Extensión de ideogramas unificadas CJK B</span><span class="sxs-lookup"><span data-stu-id="84105-341">CJK Unified Ideographs Extension B</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-342">60</span><span class="sxs-lookup"><span data-stu-id="84105-342">60</span></span></td>
<td><span data-ttu-id="84105-343">E000 - F8FF</span><span class="sxs-lookup"><span data-stu-id="84105-343">E000 - F8FF</span></span></td>
<td><span data-ttu-id="84105-344">Área de uso privado</span><span class="sxs-lookup"><span data-stu-id="84105-344">Private Use Area</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="84105-345">61 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-345">61${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-346">31C0 - 31EF</span><span class="sxs-lookup"><span data-stu-id="84105-346">31C0 - 31EF</span></span></td>
<td><span data-ttu-id="84105-347">Trazos CJK</span><span class="sxs-lookup"><span data-stu-id="84105-347">CJK Strokes</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-348">F900 - FAFF</span><span class="sxs-lookup"><span data-stu-id="84105-348">F900 - FAFF</span></span></td>
<td><span data-ttu-id="84105-349">Ideogramas de compatibilidad CJK</span><span class="sxs-lookup"><span data-stu-id="84105-349">CJK Compatibility Ideographs</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-350">2F800 - 2FA1F</span><span class="sxs-lookup"><span data-stu-id="84105-350">2F800 - 2FA1F</span></span></td>
<td><span data-ttu-id="84105-351">Suplemento de los ideogramas de compatibilidad CJK</span><span class="sxs-lookup"><span data-stu-id="84105-351">CJK Compatibility Ideographs Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-352">62</span><span class="sxs-lookup"><span data-stu-id="84105-352">62</span></span></td>
<td><span data-ttu-id="84105-353">FB00 - FB4F</span><span class="sxs-lookup"><span data-stu-id="84105-353">FB00 - FB4F</span></span></td>
<td><span data-ttu-id="84105-354">Formularios de presentación alfabética</span><span class="sxs-lookup"><span data-stu-id="84105-354">Alphabetic Presentation Forms</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-355">63</span><span class="sxs-lookup"><span data-stu-id="84105-355">63</span></span></td>
<td><span data-ttu-id="84105-356">FB50 - FDFF</span><span class="sxs-lookup"><span data-stu-id="84105-356">FB50 - FDFF</span></span></td>
<td><span data-ttu-id="84105-357">Formularios de presentación árabe-A</span><span class="sxs-lookup"><span data-stu-id="84105-357">Arabic Presentation Forms-A</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-358">64</span><span class="sxs-lookup"><span data-stu-id="84105-358">64</span></span></td>
<td><span data-ttu-id="84105-359">FE20 - FE2F</span><span class="sxs-lookup"><span data-stu-id="84105-359">FE20 - FE2F</span></span></td>
<td><span data-ttu-id="84105-360">Combinación de medias marcas</span><span class="sxs-lookup"><span data-stu-id="84105-360">Combining Half Marks</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="84105-361">65 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-361">65${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-362">FE10 - FE1F</span><span class="sxs-lookup"><span data-stu-id="84105-362">FE10 - FE1F</span></span></td>
<td><span data-ttu-id="84105-363">Formularios verticales</span><span class="sxs-lookup"><span data-stu-id="84105-363">Vertical Forms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-364">FE30 - FE4F</span><span class="sxs-lookup"><span data-stu-id="84105-364">FE30 - FE4F</span></span></td>
<td><span data-ttu-id="84105-365">Formularios de compatibilidad CJK</span><span class="sxs-lookup"><span data-stu-id="84105-365">CJK Compatibility Forms</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-366">66</span><span class="sxs-lookup"><span data-stu-id="84105-366">66</span></span></td>
<td><span data-ttu-id="84105-367">FE50 - FE6F</span><span class="sxs-lookup"><span data-stu-id="84105-367">FE50 - FE6F</span></span></td>
<td><span data-ttu-id="84105-368">Variantes de formato pequeño</span><span class="sxs-lookup"><span data-stu-id="84105-368">Small Form Variants</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-369">67</span><span class="sxs-lookup"><span data-stu-id="84105-369">67</span></span></td>
<td><span data-ttu-id="84105-370">FE70 - FEFF</span><span class="sxs-lookup"><span data-stu-id="84105-370">FE70 - FEFF</span></span></td>
<td><span data-ttu-id="84105-371">Formularios de presentación árabes-B</span><span class="sxs-lookup"><span data-stu-id="84105-371">Arabic Presentation Forms-B</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-372">68</span><span class="sxs-lookup"><span data-stu-id="84105-372">68</span></span></td>
<td><span data-ttu-id="84105-373">FF00 - FFEF</span><span class="sxs-lookup"><span data-stu-id="84105-373">FF00 - FFEF</span></span></td>
<td><span data-ttu-id="84105-374">Formatos de ancho de ancho y de ancho completo</span><span class="sxs-lookup"><span data-stu-id="84105-374">Halfwidth And Fullwidth Forms</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-375">69</span><span class="sxs-lookup"><span data-stu-id="84105-375">69</span></span></td>
<td><span data-ttu-id="84105-376">FFF0 - FFFF</span><span class="sxs-lookup"><span data-stu-id="84105-376">FFF0 - FFFF</span></span></td>
<td><span data-ttu-id="84105-377">Especiales</span><span class="sxs-lookup"><span data-stu-id="84105-377">Specials</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-378">70</span><span class="sxs-lookup"><span data-stu-id="84105-378">70</span></span></td>
<td><span data-ttu-id="84105-379">0F00 - 0FFF</span><span class="sxs-lookup"><span data-stu-id="84105-379">0F00 - 0FFF</span></span></td>
<td><span data-ttu-id="84105-380">Tibetano</span><span class="sxs-lookup"><span data-stu-id="84105-380">Tibetan</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-381">71</span><span class="sxs-lookup"><span data-stu-id="84105-381">71</span></span></td>
<td><span data-ttu-id="84105-382">0700 - 074F</span><span class="sxs-lookup"><span data-stu-id="84105-382">0700 - 074F</span></span></td>
<td><span data-ttu-id="84105-383">Siríaco</span><span class="sxs-lookup"><span data-stu-id="84105-383">Syriac</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-384">72</span><span class="sxs-lookup"><span data-stu-id="84105-384">72</span></span></td>
<td><span data-ttu-id="84105-385">0780 - 07BF</span><span class="sxs-lookup"><span data-stu-id="84105-385">0780 - 07BF</span></span></td>
<td><span data-ttu-id="84105-386">Thaana</span><span class="sxs-lookup"><span data-stu-id="84105-386">Thaana</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-387">73</span><span class="sxs-lookup"><span data-stu-id="84105-387">73</span></span></td>
<td><span data-ttu-id="84105-388">0D80 - 0DFF</span><span class="sxs-lookup"><span data-stu-id="84105-388">0D80 - 0DFF</span></span></td>
<td><span data-ttu-id="84105-389">Cingalés</span><span class="sxs-lookup"><span data-stu-id="84105-389">Sinhala</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-390">74</span><span class="sxs-lookup"><span data-stu-id="84105-390">74</span></span></td>
<td><span data-ttu-id="84105-391">1000 - 109F</span><span class="sxs-lookup"><span data-stu-id="84105-391">1000 - 109F</span></span></td>
<td><span data-ttu-id="84105-392">Myanmar</span><span class="sxs-lookup"><span data-stu-id="84105-392">Myanmar</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="84105-393">75 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-393">75${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-394">1200 - 137F</span><span class="sxs-lookup"><span data-stu-id="84105-394">1200 - 137F</span></span></td>
<td><span data-ttu-id="84105-395">Dígito</span><span class="sxs-lookup"><span data-stu-id="84105-395">Ethiopic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-396">1380-139F</span><span class="sxs-lookup"><span data-stu-id="84105-396">1380 - 139F</span></span></td>
<td><span data-ttu-id="84105-397">Suplemento etíope</span><span class="sxs-lookup"><span data-stu-id="84105-397">Ethiopic Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-398">2D80 - 2DDF</span><span class="sxs-lookup"><span data-stu-id="84105-398">2D80 - 2DDF</span></span></td>
<td><span data-ttu-id="84105-399">Etíope extendido</span><span class="sxs-lookup"><span data-stu-id="84105-399">Ethiopic Extended</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-400">76</span><span class="sxs-lookup"><span data-stu-id="84105-400">76</span></span></td>
<td><span data-ttu-id="84105-401">13A0 - 13FF</span><span class="sxs-lookup"><span data-stu-id="84105-401">13A0 - 13FF</span></span></td>
<td><span data-ttu-id="84105-402">Cheroqui</span><span class="sxs-lookup"><span data-stu-id="84105-402">Cherokee</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-403">77</span><span class="sxs-lookup"><span data-stu-id="84105-403">77</span></span></td>
<td><span data-ttu-id="84105-404">1400 - 167F</span><span class="sxs-lookup"><span data-stu-id="84105-404">1400 - 167F</span></span></td>
<td><span data-ttu-id="84105-405">Silábico indígena canadiense unificada</span><span class="sxs-lookup"><span data-stu-id="84105-405">Unified Canadian Aboriginal Syllabics</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-406">78</span><span class="sxs-lookup"><span data-stu-id="84105-406">78</span></span></td>
<td><span data-ttu-id="84105-407">1680 - 169F</span><span class="sxs-lookup"><span data-stu-id="84105-407">1680 - 169F</span></span></td>
<td><span data-ttu-id="84105-408">Ogham</span><span class="sxs-lookup"><span data-stu-id="84105-408">Ogham</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-409">79</span><span class="sxs-lookup"><span data-stu-id="84105-409">79</span></span></td>
<td><span data-ttu-id="84105-410">16A0 - 16FF</span><span class="sxs-lookup"><span data-stu-id="84105-410">16A0 - 16FF</span></span></td>
<td><span data-ttu-id="84105-411">Rúnica</span><span class="sxs-lookup"><span data-stu-id="84105-411">Runic</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="84105-412">80 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-412">80${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-413">1780 - 17FF</span><span class="sxs-lookup"><span data-stu-id="84105-413">1780 - 17FF</span></span></td>
<td><span data-ttu-id="84105-414">Jemer</span><span class="sxs-lookup"><span data-stu-id="84105-414">Khmer</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-415">19E0 - 19FF</span><span class="sxs-lookup"><span data-stu-id="84105-415">19E0 - 19FF</span></span></td>
<td><span data-ttu-id="84105-416">Símbolos Khmer</span><span class="sxs-lookup"><span data-stu-id="84105-416">Khmer Symbols</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-417">81</span><span class="sxs-lookup"><span data-stu-id="84105-417">81</span></span></td>
<td><span data-ttu-id="84105-418">1800 - 18AF</span><span class="sxs-lookup"><span data-stu-id="84105-418">1800 - 18AF</span></span></td>
<td><span data-ttu-id="84105-419">Mongol</span><span class="sxs-lookup"><span data-stu-id="84105-419">Mongolian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-420">82</span><span class="sxs-lookup"><span data-stu-id="84105-420">82</span></span></td>
<td><span data-ttu-id="84105-421">2800 - 28FF</span><span class="sxs-lookup"><span data-stu-id="84105-421">2800 - 28FF</span></span></td>
<td><span data-ttu-id="84105-422">Patrones de Braille</span><span class="sxs-lookup"><span data-stu-id="84105-422">Braille Patterns</span></span></td>
</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="84105-423">83 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-423">83${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-424">A000 - A48F</span><span class="sxs-lookup"><span data-stu-id="84105-424">A000 - A48F</span></span></td>
<td><span data-ttu-id="84105-425">Sílabas Yi</span><span class="sxs-lookup"><span data-stu-id="84105-425">Yi Syllables</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-426">A490 - A4CF</span><span class="sxs-lookup"><span data-stu-id="84105-426">A490 - A4CF</span></span></td>
<td><span data-ttu-id="84105-427">Radicales Yi</span><span class="sxs-lookup"><span data-stu-id="84105-427">Yi Radicals</span></span></td>

</tr>
<tr class="even">
<td rowspan="4"><span data-ttu-id="84105-428">84 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-428">84${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-429">1700 - 171F</span><span class="sxs-lookup"><span data-stu-id="84105-429">1700 - 171F</span></span></td>
<td><span data-ttu-id="84105-430">Tagalo</span><span class="sxs-lookup"><span data-stu-id="84105-430">Tagalog</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-431">1720 - 173F</span><span class="sxs-lookup"><span data-stu-id="84105-431">1720 - 173F</span></span></td>
<td><span data-ttu-id="84105-432">Hanunno</span><span class="sxs-lookup"><span data-stu-id="84105-432">Hanunoo</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-433">1740 - 175F</span><span class="sxs-lookup"><span data-stu-id="84105-433">1740 - 175F</span></span></td>
<td><span data-ttu-id="84105-434">Buhid</span><span class="sxs-lookup"><span data-stu-id="84105-434">Buhid</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-435">1760 - 177F</span><span class="sxs-lookup"><span data-stu-id="84105-435">1760 - 177F</span></span></td>
<td><span data-ttu-id="84105-436">Tagbanwa</span><span class="sxs-lookup"><span data-stu-id="84105-436">Tagbanwa</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-437">85</span><span class="sxs-lookup"><span data-stu-id="84105-437">85</span></span></td>
<td><span data-ttu-id="84105-438">10300-1032F</span><span class="sxs-lookup"><span data-stu-id="84105-438">10300 - 1032F</span></span></td>
<td><span data-ttu-id="84105-439">Cursiva antigua</span><span class="sxs-lookup"><span data-stu-id="84105-439">Old Italic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-440">86</span><span class="sxs-lookup"><span data-stu-id="84105-440">86</span></span></td>
<td><span data-ttu-id="84105-441">10330-1034F</span><span class="sxs-lookup"><span data-stu-id="84105-441">10330 - 1034F</span></span></td>
<td><span data-ttu-id="84105-442">Gótico</span><span class="sxs-lookup"><span data-stu-id="84105-442">Gothic</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-443">87</span><span class="sxs-lookup"><span data-stu-id="84105-443">87</span></span></td>
<td><span data-ttu-id="84105-444">10400-1044F</span><span class="sxs-lookup"><span data-stu-id="84105-444">10400 - 1044F</span></span></td>
<td><span data-ttu-id="84105-445">Deseret</span><span class="sxs-lookup"><span data-stu-id="84105-445">Deseret</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="84105-446">88 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-446">88${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-447">1D000 - 1D0FF</span><span class="sxs-lookup"><span data-stu-id="84105-447">1D000 - 1D0FF</span></span></td>
<td><span data-ttu-id="84105-448">Símbolos musicales de Byzantine</span><span class="sxs-lookup"><span data-stu-id="84105-448">Byzantine Musical Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-449">1D100 - 1D1FF</span><span class="sxs-lookup"><span data-stu-id="84105-449">1D100 - 1D1FF</span></span></td>
<td><span data-ttu-id="84105-450">Símbolos musicales</span><span class="sxs-lookup"><span data-stu-id="84105-450">Musical Symbols</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-451">1D200 - 1D24F</span><span class="sxs-lookup"><span data-stu-id="84105-451">1D200 - 1D24F</span></span></td>
<td><span data-ttu-id="84105-452">Notación musical griega antigua</span><span class="sxs-lookup"><span data-stu-id="84105-452">Ancient Greek Musical Notation</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-453">89</span><span class="sxs-lookup"><span data-stu-id="84105-453">89</span></span></td>
<td><span data-ttu-id="84105-454">1D400 - 1D7FF</span><span class="sxs-lookup"><span data-stu-id="84105-454">1D400 - 1D7FF</span></span></td>
<td><span data-ttu-id="84105-455">Símbolos alfanuméricos matemáticos</span><span class="sxs-lookup"><span data-stu-id="84105-455">Mathematical Alphanumeric Symbols</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="84105-456">90 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-456">90${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-457">FF000 - FFFFD</span><span class="sxs-lookup"><span data-stu-id="84105-457">FF000 - FFFFD</span></span></td>
<td><span data-ttu-id="84105-458">Uso privado (plano 15)</span><span class="sxs-lookup"><span data-stu-id="84105-458">Private Use (plane 15)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-459">100000-10FFFD</span><span class="sxs-lookup"><span data-stu-id="84105-459">100000 - 10FFFD</span></span></td>
<td><span data-ttu-id="84105-460">Uso privado (plano 16)</span><span class="sxs-lookup"><span data-stu-id="84105-460">Private Use (plane 16)</span></span></td>

</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="84105-461">91 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-461">91${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-462">FE00 - FE0F</span><span class="sxs-lookup"><span data-stu-id="84105-462">FE00 - FE0F</span></span></td>
<td><span data-ttu-id="84105-463">Selectores de variación</span><span class="sxs-lookup"><span data-stu-id="84105-463">Variation Selectors</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-464">E0100 - E01EF</span><span class="sxs-lookup"><span data-stu-id="84105-464">E0100 - E01EF</span></span></td>
<td><span data-ttu-id="84105-465">Suplemento de selectores de variación</span><span class="sxs-lookup"><span data-stu-id="84105-465">Variation Selectors Supplement</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-466">92</span><span class="sxs-lookup"><span data-stu-id="84105-466">92</span></span></td>
<td><span data-ttu-id="84105-467">E0000 - E007F</span><span class="sxs-lookup"><span data-stu-id="84105-467">E0000 - E007F</span></span></td>
<td><span data-ttu-id="84105-468">Etiquetas</span><span class="sxs-lookup"><span data-stu-id="84105-468">Tags</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-469">93</span><span class="sxs-lookup"><span data-stu-id="84105-469">93</span></span></td>
<td><span data-ttu-id="84105-470">1900 - 194F</span><span class="sxs-lookup"><span data-stu-id="84105-470">1900 - 194F</span></span></td>
<td><span data-ttu-id="84105-471">Limbu</span><span class="sxs-lookup"><span data-stu-id="84105-471">Limbu</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-472">94</span><span class="sxs-lookup"><span data-stu-id="84105-472">94</span></span></td>
<td><span data-ttu-id="84105-473">1950 - 197F</span><span class="sxs-lookup"><span data-stu-id="84105-473">1950 - 197F</span></span></td>
<td><span data-ttu-id="84105-474">Tai le</span><span class="sxs-lookup"><span data-stu-id="84105-474">Tai Le</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-475">95</span><span class="sxs-lookup"><span data-stu-id="84105-475">95</span></span></td>
<td><span data-ttu-id="84105-476">1980-19DF</span><span class="sxs-lookup"><span data-stu-id="84105-476">1980 - 19DF</span></span></td>
<td><span data-ttu-id="84105-477">Nuevo tai lue moderno</span><span class="sxs-lookup"><span data-stu-id="84105-477">New Tai Lue</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-478">96</span><span class="sxs-lookup"><span data-stu-id="84105-478">96</span></span></td>
<td><span data-ttu-id="84105-479">1A00 - 1A1F</span><span class="sxs-lookup"><span data-stu-id="84105-479">1A00 - 1A1F</span></span></td>
<td><span data-ttu-id="84105-480">Buginés</span><span class="sxs-lookup"><span data-stu-id="84105-480">Buginese</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-481">97</span><span class="sxs-lookup"><span data-stu-id="84105-481">97</span></span></td>
<td><span data-ttu-id="84105-482">2C00 - 2C5F</span><span class="sxs-lookup"><span data-stu-id="84105-482">2C00 - 2C5F</span></span></td>
<td><span data-ttu-id="84105-483">Letra</span><span class="sxs-lookup"><span data-stu-id="84105-483">Glagolitic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-484">98</span><span class="sxs-lookup"><span data-stu-id="84105-484">98</span></span></td>
<td><span data-ttu-id="84105-485">2D30 - 2D7F</span><span class="sxs-lookup"><span data-stu-id="84105-485">2D30 - 2D7F</span></span></td>
<td><span data-ttu-id="84105-486">Tifinagh</span><span class="sxs-lookup"><span data-stu-id="84105-486">Tifinagh</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-487">99</span><span class="sxs-lookup"><span data-stu-id="84105-487">99</span></span></td>
<td><span data-ttu-id="84105-488">4DC0 - 4DFF</span><span class="sxs-lookup"><span data-stu-id="84105-488">4DC0 - 4DFF</span></span></td>
<td><span data-ttu-id="84105-489">Símbolos de Yijing Hexagrama</span><span class="sxs-lookup"><span data-stu-id="84105-489">Yijing Hexagram Symbols</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-490">100</span><span class="sxs-lookup"><span data-stu-id="84105-490">100</span></span></td>
<td><span data-ttu-id="84105-491">A800 - A82F</span><span class="sxs-lookup"><span data-stu-id="84105-491">A800 - A82F</span></span></td>
<td><span data-ttu-id="84105-492">Syloti Nagri</span><span class="sxs-lookup"><span data-stu-id="84105-492">Syloti Nagri</span></span></td>
</tr>
<tr class="even">
<td rowspan="3"><span data-ttu-id="84105-493">101 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-493">101${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-494">10000-1007F</span><span class="sxs-lookup"><span data-stu-id="84105-494">10000 - 1007F</span></span></td>
<td><span data-ttu-id="84105-495">Syllabary lineal B</span><span class="sxs-lookup"><span data-stu-id="84105-495">Linear B Syllabary</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-496">10080-100FF</span><span class="sxs-lookup"><span data-stu-id="84105-496">10080 - 100FF</span></span></td>
<td><span data-ttu-id="84105-497">Ideogramas mostrados lineal B</span><span class="sxs-lookup"><span data-stu-id="84105-497">Linear B Ideograms</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-498">10100-1013F</span><span class="sxs-lookup"><span data-stu-id="84105-498">10100 - 1013F</span></span></td>
<td><span data-ttu-id="84105-499">Números Egeo</span><span class="sxs-lookup"><span data-stu-id="84105-499">Aegean Numbers</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-500">102</span><span class="sxs-lookup"><span data-stu-id="84105-500">102</span></span></td>
<td><span data-ttu-id="84105-501">10140-1018F</span><span class="sxs-lookup"><span data-stu-id="84105-501">10140 - 1018F</span></span></td>
<td><span data-ttu-id="84105-502">Números griegos antiguos</span><span class="sxs-lookup"><span data-stu-id="84105-502">Ancient Greek Numbers</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-503">103</span><span class="sxs-lookup"><span data-stu-id="84105-503">103</span></span></td>
<td><span data-ttu-id="84105-504">10380-1039F</span><span class="sxs-lookup"><span data-stu-id="84105-504">10380 - 1039F</span></span></td>
<td><span data-ttu-id="84105-505">Ugarítico</span><span class="sxs-lookup"><span data-stu-id="84105-505">Ugaritic</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-506">104</span><span class="sxs-lookup"><span data-stu-id="84105-506">104</span></span></td>
<td><span data-ttu-id="84105-507">103A0 - 103DF</span><span class="sxs-lookup"><span data-stu-id="84105-507">103A0 - 103DF</span></span></td>
<td><span data-ttu-id="84105-508">Persa antiguo</span><span class="sxs-lookup"><span data-stu-id="84105-508">Old Persian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-509">105</span><span class="sxs-lookup"><span data-stu-id="84105-509">105</span></span></td>
<td><span data-ttu-id="84105-510">10450-1047F</span><span class="sxs-lookup"><span data-stu-id="84105-510">10450 - 1047F</span></span></td>
<td><span data-ttu-id="84105-511">Shavian</span><span class="sxs-lookup"><span data-stu-id="84105-511">Shavian</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-512">106</span><span class="sxs-lookup"><span data-stu-id="84105-512">106</span></span></td>
<td><span data-ttu-id="84105-513">10480-104AF</span><span class="sxs-lookup"><span data-stu-id="84105-513">10480 - 104AF</span></span></td>
<td><span data-ttu-id="84105-514">Osmanya</span><span class="sxs-lookup"><span data-stu-id="84105-514">Osmanya</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-515">107</span><span class="sxs-lookup"><span data-stu-id="84105-515">107</span></span></td>
<td><span data-ttu-id="84105-516">10800-1083F</span><span class="sxs-lookup"><span data-stu-id="84105-516">10800 - 1083F</span></span></td>
<td><span data-ttu-id="84105-517">Cypriot Syllabary</span><span class="sxs-lookup"><span data-stu-id="84105-517">Cypriot Syllabary</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-518">108</span><span class="sxs-lookup"><span data-stu-id="84105-518">108</span></span></td>
<td><span data-ttu-id="84105-519">10A00 - 10A5F</span><span class="sxs-lookup"><span data-stu-id="84105-519">10A00 - 10A5F</span></span></td>
<td><span data-ttu-id="84105-520">Kharoshthi</span><span class="sxs-lookup"><span data-stu-id="84105-520">Kharoshthi</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-521">109</span><span class="sxs-lookup"><span data-stu-id="84105-521">109</span></span></td>
<td><span data-ttu-id="84105-522">1D300 - 1D35F</span><span class="sxs-lookup"><span data-stu-id="84105-522">1D300 - 1D35F</span></span></td>
<td><span data-ttu-id="84105-523">Símbolos de Jing Tai Xuan</span><span class="sxs-lookup"><span data-stu-id="84105-523">Tai Xuan Jing Symbols</span></span></td>
</tr>
<tr class="odd">
<td rowspan="2"><span data-ttu-id="84105-524">110 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-524">110${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-525">12000-123FF</span><span class="sxs-lookup"><span data-stu-id="84105-525">12000 - 123FF</span></span></td>
<td><span data-ttu-id="84105-526">Cuneiform</span><span class="sxs-lookup"><span data-stu-id="84105-526">Cuneiform</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-527">12400-1247F</span><span class="sxs-lookup"><span data-stu-id="84105-527">12400 - 1247F</span></span></td>
<td><span data-ttu-id="84105-528">Cuneiform números y signos de puntuación</span><span class="sxs-lookup"><span data-stu-id="84105-528">Cuneiform Numbers and Punctuation</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-529">111</span><span class="sxs-lookup"><span data-stu-id="84105-529">111</span></span></td>
<td><span data-ttu-id="84105-530">1D360 - 1D37F</span><span class="sxs-lookup"><span data-stu-id="84105-530">1D360 - 1D37F</span></span></td>
<td><span data-ttu-id="84105-531">Números de la varilla de recuento</span><span class="sxs-lookup"><span data-stu-id="84105-531">Counting Rod Numerals</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-532">112</span><span class="sxs-lookup"><span data-stu-id="84105-532">112</span></span></td>
<td><span data-ttu-id="84105-533">1B80 - 1BBF</span><span class="sxs-lookup"><span data-stu-id="84105-533">1B80 - 1BBF</span></span></td>
<td><span data-ttu-id="84105-534">Sundanés</span><span class="sxs-lookup"><span data-stu-id="84105-534">Sundanese</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-535">113</span><span class="sxs-lookup"><span data-stu-id="84105-535">113</span></span></td>
<td><span data-ttu-id="84105-536">1C00 - 1C4F</span><span class="sxs-lookup"><span data-stu-id="84105-536">1C00 - 1C4F</span></span></td>
<td><span data-ttu-id="84105-537">Lepcha</span><span class="sxs-lookup"><span data-stu-id="84105-537">Lepcha</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-538">114</span><span class="sxs-lookup"><span data-stu-id="84105-538">114</span></span></td>
<td><span data-ttu-id="84105-539">1C50 - 1C7F</span><span class="sxs-lookup"><span data-stu-id="84105-539">1C50 - 1C7F</span></span></td>
<td><span data-ttu-id="84105-540">OL Chiki</span><span class="sxs-lookup"><span data-stu-id="84105-540">Ol Chiki</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-541">115</span><span class="sxs-lookup"><span data-stu-id="84105-541">115</span></span></td>
<td><span data-ttu-id="84105-542">A880 - A8DF</span><span class="sxs-lookup"><span data-stu-id="84105-542">A880 - A8DF</span></span></td>
<td><span data-ttu-id="84105-543">Saurashtra</span><span class="sxs-lookup"><span data-stu-id="84105-543">Saurashtra</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-544">116</span><span class="sxs-lookup"><span data-stu-id="84105-544">116</span></span></td>
<td><span data-ttu-id="84105-545">A900 - A92F</span><span class="sxs-lookup"><span data-stu-id="84105-545">A900 - A92F</span></span></td>
<td><span data-ttu-id="84105-546">Kayah Li</span><span class="sxs-lookup"><span data-stu-id="84105-546">Kayah Li</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-547">117</span><span class="sxs-lookup"><span data-stu-id="84105-547">117</span></span></td>
<td><span data-ttu-id="84105-548">A930 - A95F</span><span class="sxs-lookup"><span data-stu-id="84105-548">A930 - A95F</span></span></td>
<td><span data-ttu-id="84105-549">Rejang</span><span class="sxs-lookup"><span data-stu-id="84105-549">Rejang</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-550">118</span><span class="sxs-lookup"><span data-stu-id="84105-550">118</span></span></td>
<td><span data-ttu-id="84105-551">AA00 - AA5F</span><span class="sxs-lookup"><span data-stu-id="84105-551">AA00 - AA5F</span></span></td>
<td><span data-ttu-id="84105-552">Cham</span><span class="sxs-lookup"><span data-stu-id="84105-552">Cham</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-553">119</span><span class="sxs-lookup"><span data-stu-id="84105-553">119</span></span></td>
<td><span data-ttu-id="84105-554">10190-101CF</span><span class="sxs-lookup"><span data-stu-id="84105-554">10190 - 101CF</span></span></td>
<td><span data-ttu-id="84105-555">Antiguos símbolos</span><span class="sxs-lookup"><span data-stu-id="84105-555">Ancient Symbols</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-556">120</span><span class="sxs-lookup"><span data-stu-id="84105-556">120</span></span></td>
<td><span data-ttu-id="84105-557">101D0 - 101FF</span><span class="sxs-lookup"><span data-stu-id="84105-557">101D0 - 101FF</span></span></td>
<td><span data-ttu-id="84105-558">Disco Phaistos</span><span class="sxs-lookup"><span data-stu-id="84105-558">Phaistos Disc</span></span></td>
</tr>
<tr class="odd">
<td rowspan="3"><span data-ttu-id="84105-559">121 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-559">121${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-560">10280-1029F</span><span class="sxs-lookup"><span data-stu-id="84105-560">10280 - 1029F</span></span></td>
<td><span data-ttu-id="84105-561">Licio</span><span class="sxs-lookup"><span data-stu-id="84105-561">Lycian</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-562">102A0 - 102DF</span><span class="sxs-lookup"><span data-stu-id="84105-562">102A0 - 102DF</span></span></td>
<td><span data-ttu-id="84105-563">Cario</span><span class="sxs-lookup"><span data-stu-id="84105-563">Carian</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="84105-564">10920-1093F</span><span class="sxs-lookup"><span data-stu-id="84105-564">10920 - 1093F</span></span></td>
<td><span data-ttu-id="84105-565">Lidio</span><span class="sxs-lookup"><span data-stu-id="84105-565">Lydian</span></span></td>

</tr>
<tr class="even">
<td rowspan="2"><span data-ttu-id="84105-566">122 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="84105-566">122${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="84105-567">1F000 - 1F02F</span><span class="sxs-lookup"><span data-stu-id="84105-567">1F000 - 1F02F</span></span></td>
<td><span data-ttu-id="84105-568">Mosaicos de Mahjong</span><span class="sxs-lookup"><span data-stu-id="84105-568">Mahjong Tiles</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-569">1F030 - 1F09F</span><span class="sxs-lookup"><span data-stu-id="84105-569">1F030 - 1F09F</span></span></td>
<td><span data-ttu-id="84105-570">Iconos de Domino</span><span class="sxs-lookup"><span data-stu-id="84105-570">Domino Tiles</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="84105-571">123</span><span class="sxs-lookup"><span data-stu-id="84105-571">123</span></span></td>

<td><span data-ttu-id="84105-572"><strong>Windows 2000 y versiones posteriores:</strong> Progreso del diseño, horizontal de derecha a izquierda</span><span class="sxs-lookup"><span data-stu-id="84105-572"><strong>Windows 2000 and later:</strong> Layout progress, horizontal from right to left</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-573">124</span><span class="sxs-lookup"><span data-stu-id="84105-573">124</span></span></td>

<td><span data-ttu-id="84105-574"><strong>Windows 2000 y versiones posteriores:</strong> Progreso de diseño, vertical delante de horizontal</span><span class="sxs-lookup"><span data-stu-id="84105-574"><strong>Windows 2000 and later:</strong> Layout progress, vertical before horizontal</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="84105-575">125</span><span class="sxs-lookup"><span data-stu-id="84105-575">125</span></span></td>

<td><span data-ttu-id="84105-576"><strong>Windows 2000 y versiones posteriores:</strong> Progreso de diseño, vertical de abajo arriba</span><span class="sxs-lookup"><span data-stu-id="84105-576"><strong>Windows 2000 and later:</strong> Layout progress, vertical bottom to top</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="84105-577">126-127</span><span class="sxs-lookup"><span data-stu-id="84105-577">126-127</span></span></td>

<td><span data-ttu-id="84105-578">Reservado para uso interno del proceso</span><span class="sxs-lookup"><span data-stu-id="84105-578">Reserved for process-internal usage</span></span></td>
</tr>
</tbody>
</table>



 

 

 



