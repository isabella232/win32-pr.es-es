---
title: VarFileInfo BLOCK (instrucción)
description: Describe la forma del bloque de información variable.
ms.assetid: 81c7f5df-78fa-4571-9dad-a6c3e932471e
keywords:
- Menús de la instrucción de bloque VarFileInfo y otros recursos
topic_type:
- apiref
api_name:
- VarFileInfo BLOCK
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09645801618de130439bdf1998b92183e4791783
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/25/2019
ms.locfileid: "104076896"
---
# <a name="varfileinfo-block-statement"></a><span data-ttu-id="fff49-104">VarFileInfo BLOCK (instrucción)</span><span class="sxs-lookup"><span data-stu-id="fff49-104">VarFileInfo BLOCK statement</span></span>

<span data-ttu-id="fff49-105">Define un bloque de información variable.</span><span class="sxs-lookup"><span data-stu-id="fff49-105">Defines a variable information block.</span></span>

``` syntax
BLOCK "VarFileInfo" { VALUE "Translation", langID, charsetID . . . }
```

## <a name="parameters"></a><span data-ttu-id="fff49-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="fff49-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fff49-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*ididioma*</span><span class="sxs-lookup"><span data-stu-id="fff49-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="fff49-108">Uno de los identificadores de idioma especificados en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="fff49-108">One of the language identifiers specified in the Remarks section.</span></span>

</dd> <dt>

<span data-ttu-id="fff49-109"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span><span class="sxs-lookup"><span data-stu-id="fff49-109"><span id="charsetID"></span><span id="charsetid"></span><span id="CHARSETID"></span>*charsetID*</span></span>
</dt> <dd>

<span data-ttu-id="fff49-110">Uno de los identificadores de juegos de caracteres especificados en la sección Comentarios.</span><span class="sxs-lookup"><span data-stu-id="fff49-110">One of the character-set identifiers specified in the Remarks section.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="fff49-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="fff49-111">Remarks</span></span>

<span data-ttu-id="fff49-112">Se puede proporcionar más de un par de identificadores, pero cada par debe estar separado del par anterior con una coma.</span><span class="sxs-lookup"><span data-stu-id="fff49-112">More than one identifier pair can be given, but each pair must be separated from the preceding pair with a comma.</span></span>

<span data-ttu-id="fff49-113">El parámetro *langID* especifica uno de los siguientes códigos de idioma.</span><span class="sxs-lookup"><span data-stu-id="fff49-113">The *langID* parameter specifies one of the following language codes.</span></span>



| <span data-ttu-id="fff49-114">Código</span><span class="sxs-lookup"><span data-stu-id="fff49-114">Code</span></span>   | <span data-ttu-id="fff49-115">Idioma</span><span class="sxs-lookup"><span data-stu-id="fff49-115">Language</span></span>            | <span data-ttu-id="fff49-116">Código</span><span class="sxs-lookup"><span data-stu-id="fff49-116">Code</span></span>   | <span data-ttu-id="fff49-117">Idioma</span><span class="sxs-lookup"><span data-stu-id="fff49-117">Language</span></span>                  |
|--------|---------------------|--------|---------------------------|
| <span data-ttu-id="fff49-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="fff49-118">0x0401</span></span> | <span data-ttu-id="fff49-119">Árabe</span><span class="sxs-lookup"><span data-stu-id="fff49-119">Arabic</span></span>              | <span data-ttu-id="fff49-120">0x0415</span><span class="sxs-lookup"><span data-stu-id="fff49-120">0x0415</span></span> | <span data-ttu-id="fff49-121">Polaco</span><span class="sxs-lookup"><span data-stu-id="fff49-121">Polish</span></span>                    |
| <span data-ttu-id="fff49-122">0x0402</span><span class="sxs-lookup"><span data-stu-id="fff49-122">0x0402</span></span> | <span data-ttu-id="fff49-123">Búlgaro</span><span class="sxs-lookup"><span data-stu-id="fff49-123">Bulgarian</span></span>           | <span data-ttu-id="fff49-124">0x0416</span><span class="sxs-lookup"><span data-stu-id="fff49-124">0x0416</span></span> | <span data-ttu-id="fff49-125">Portugués (Brasil)</span><span class="sxs-lookup"><span data-stu-id="fff49-125">Portuguese (Brazil)</span></span>       |
| <span data-ttu-id="fff49-126">0x0403</span><span class="sxs-lookup"><span data-stu-id="fff49-126">0x0403</span></span> | <span data-ttu-id="fff49-127">Catalán</span><span class="sxs-lookup"><span data-stu-id="fff49-127">Catalan</span></span>             | <span data-ttu-id="fff49-128">0x0417</span><span class="sxs-lookup"><span data-stu-id="fff49-128">0x0417</span></span> | <span data-ttu-id="fff49-129">Rhaeto-Romanic</span><span class="sxs-lookup"><span data-stu-id="fff49-129">Rhaeto-Romanic</span></span>            |
| <span data-ttu-id="fff49-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="fff49-130">0x0404</span></span> | <span data-ttu-id="fff49-131">Chino tradicional</span><span class="sxs-lookup"><span data-stu-id="fff49-131">Traditional Chinese</span></span> | <span data-ttu-id="fff49-132">0x0418</span><span class="sxs-lookup"><span data-stu-id="fff49-132">0x0418</span></span> | <span data-ttu-id="fff49-133">Rumano</span><span class="sxs-lookup"><span data-stu-id="fff49-133">Romanian</span></span>                  |
| <span data-ttu-id="fff49-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="fff49-134">0x0405</span></span> | <span data-ttu-id="fff49-135">Checo</span><span class="sxs-lookup"><span data-stu-id="fff49-135">Czech</span></span>               | <span data-ttu-id="fff49-136">0x0419</span><span class="sxs-lookup"><span data-stu-id="fff49-136">0x0419</span></span> | <span data-ttu-id="fff49-137">Ruso</span><span class="sxs-lookup"><span data-stu-id="fff49-137">Russian</span></span>                   |
| <span data-ttu-id="fff49-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="fff49-138">0x0406</span></span> | <span data-ttu-id="fff49-139">Danés</span><span class="sxs-lookup"><span data-stu-id="fff49-139">Danish</span></span>              | <span data-ttu-id="fff49-140">0x041A</span><span class="sxs-lookup"><span data-stu-id="fff49-140">0x041A</span></span> | <span data-ttu-id="fff49-141">Croato-Serbian (Latín)</span><span class="sxs-lookup"><span data-stu-id="fff49-141">Croato-Serbian (Latin)</span></span>    |
| <span data-ttu-id="fff49-142">0x0407</span><span class="sxs-lookup"><span data-stu-id="fff49-142">0x0407</span></span> | <span data-ttu-id="fff49-143">Alemán</span><span class="sxs-lookup"><span data-stu-id="fff49-143">German</span></span>              | <span data-ttu-id="fff49-144">0x041B</span><span class="sxs-lookup"><span data-stu-id="fff49-144">0x041B</span></span> | <span data-ttu-id="fff49-145">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="fff49-145">Slovak</span></span>                    |
| <span data-ttu-id="fff49-146">0x0408</span><span class="sxs-lookup"><span data-stu-id="fff49-146">0x0408</span></span> | <span data-ttu-id="fff49-147">Griego</span><span class="sxs-lookup"><span data-stu-id="fff49-147">Greek</span></span>               | <span data-ttu-id="fff49-148">0x041C</span><span class="sxs-lookup"><span data-stu-id="fff49-148">0x041C</span></span> | <span data-ttu-id="fff49-149">Albanés</span><span class="sxs-lookup"><span data-stu-id="fff49-149">Albanian</span></span>                  |
| <span data-ttu-id="fff49-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="fff49-150">0x0409</span></span> | <span data-ttu-id="fff49-151">Inglés de EE. UU.</span><span class="sxs-lookup"><span data-stu-id="fff49-151">U.S. English</span></span>        | <span data-ttu-id="fff49-152">0x041D</span><span class="sxs-lookup"><span data-stu-id="fff49-152">0x041D</span></span> | <span data-ttu-id="fff49-153">Sueco</span><span class="sxs-lookup"><span data-stu-id="fff49-153">Swedish</span></span>                   |
| <span data-ttu-id="fff49-154">0x040A</span><span class="sxs-lookup"><span data-stu-id="fff49-154">0x040A</span></span> | <span data-ttu-id="fff49-155">Castilian Español</span><span class="sxs-lookup"><span data-stu-id="fff49-155">Castilian Spanish</span></span>   | <span data-ttu-id="fff49-156">0x041E</span><span class="sxs-lookup"><span data-stu-id="fff49-156">0x041E</span></span> | <span data-ttu-id="fff49-157">Tailandés</span><span class="sxs-lookup"><span data-stu-id="fff49-157">Thai</span></span>                      |
| <span data-ttu-id="fff49-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="fff49-158">0x040B</span></span> | <span data-ttu-id="fff49-159">Finés</span><span class="sxs-lookup"><span data-stu-id="fff49-159">Finnish</span></span>             | <span data-ttu-id="fff49-160">0x041F</span><span class="sxs-lookup"><span data-stu-id="fff49-160">0x041F</span></span> | <span data-ttu-id="fff49-161">Turco</span><span class="sxs-lookup"><span data-stu-id="fff49-161">Turkish</span></span>                   |
| <span data-ttu-id="fff49-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="fff49-162">0x040C</span></span> | <span data-ttu-id="fff49-163">Francés</span><span class="sxs-lookup"><span data-stu-id="fff49-163">French</span></span>              | <span data-ttu-id="fff49-164">0x0420</span><span class="sxs-lookup"><span data-stu-id="fff49-164">0x0420</span></span> | <span data-ttu-id="fff49-165">Urdu</span><span class="sxs-lookup"><span data-stu-id="fff49-165">Urdu</span></span>                      |
| <span data-ttu-id="fff49-166">0x040D</span><span class="sxs-lookup"><span data-stu-id="fff49-166">0x040D</span></span> | <span data-ttu-id="fff49-167">Hebreo</span><span class="sxs-lookup"><span data-stu-id="fff49-167">Hebrew</span></span>              | <span data-ttu-id="fff49-168">0x0421</span><span class="sxs-lookup"><span data-stu-id="fff49-168">0x0421</span></span> | <span data-ttu-id="fff49-169">Bahasa</span><span class="sxs-lookup"><span data-stu-id="fff49-169">Bahasa</span></span>                    |
| <span data-ttu-id="fff49-170">0x040E</span><span class="sxs-lookup"><span data-stu-id="fff49-170">0x040E</span></span> | <span data-ttu-id="fff49-171">Húngaro</span><span class="sxs-lookup"><span data-stu-id="fff49-171">Hungarian</span></span>           | <span data-ttu-id="fff49-172">0x0804</span><span class="sxs-lookup"><span data-stu-id="fff49-172">0x0804</span></span> | <span data-ttu-id="fff49-173">Chino simplificado</span><span class="sxs-lookup"><span data-stu-id="fff49-173">Simplified Chinese</span></span>        |
| <span data-ttu-id="fff49-174">0x040F</span><span class="sxs-lookup"><span data-stu-id="fff49-174">0x040F</span></span> | <span data-ttu-id="fff49-175">Islandés</span><span class="sxs-lookup"><span data-stu-id="fff49-175">Icelandic</span></span>           | <span data-ttu-id="fff49-176">0x0807</span><span class="sxs-lookup"><span data-stu-id="fff49-176">0x0807</span></span> | <span data-ttu-id="fff49-177">Alemán suizo</span><span class="sxs-lookup"><span data-stu-id="fff49-177">Swiss German</span></span>              |
| <span data-ttu-id="fff49-178">0x0410</span><span class="sxs-lookup"><span data-stu-id="fff49-178">0x0410</span></span> | <span data-ttu-id="fff49-179">Italiano</span><span class="sxs-lookup"><span data-stu-id="fff49-179">Italian</span></span>             | <span data-ttu-id="fff49-180">0x0809</span><span class="sxs-lookup"><span data-stu-id="fff49-180">0x0809</span></span> | <span data-ttu-id="fff49-181">Reino Unido</span><span class="sxs-lookup"><span data-stu-id="fff49-181">U.K.</span></span> <span data-ttu-id="fff49-182">Inglés</span><span class="sxs-lookup"><span data-stu-id="fff49-182">English</span></span>              |
| <span data-ttu-id="fff49-183">0x0411</span><span class="sxs-lookup"><span data-stu-id="fff49-183">0x0411</span></span> | <span data-ttu-id="fff49-184">Japonés</span><span class="sxs-lookup"><span data-stu-id="fff49-184">Japanese</span></span>            | <span data-ttu-id="fff49-185">0x080A</span><span class="sxs-lookup"><span data-stu-id="fff49-185">0x080A</span></span> | <span data-ttu-id="fff49-186">Español (México)</span><span class="sxs-lookup"><span data-stu-id="fff49-186">Spanish (Mexico)</span></span>          |
| <span data-ttu-id="fff49-187">0x0412</span><span class="sxs-lookup"><span data-stu-id="fff49-187">0x0412</span></span> | <span data-ttu-id="fff49-188">Coreano</span><span class="sxs-lookup"><span data-stu-id="fff49-188">Korean</span></span>              | <span data-ttu-id="fff49-189">0x080C</span><span class="sxs-lookup"><span data-stu-id="fff49-189">0x080C</span></span> | <span data-ttu-id="fff49-190">Francés belga</span><span class="sxs-lookup"><span data-stu-id="fff49-190">Belgian French</span></span>            |
| <span data-ttu-id="fff49-191">0x0413</span><span class="sxs-lookup"><span data-stu-id="fff49-191">0x0413</span></span> | <span data-ttu-id="fff49-192">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="fff49-192">Dutch</span></span>               | <span data-ttu-id="fff49-193">0x0C0C</span><span class="sxs-lookup"><span data-stu-id="fff49-193">0x0C0C</span></span> | <span data-ttu-id="fff49-194">Francés canadiense</span><span class="sxs-lookup"><span data-stu-id="fff49-194">Canadian French</span></span>           |
| <span data-ttu-id="fff49-195">0x0414</span><span class="sxs-lookup"><span data-stu-id="fff49-195">0x0414</span></span> | <span data-ttu-id="fff49-196">Noruego – Bokmal</span><span class="sxs-lookup"><span data-stu-id="fff49-196">Norwegian – Bokmal</span></span>  | <span data-ttu-id="fff49-197">0x100C</span><span class="sxs-lookup"><span data-stu-id="fff49-197">0x100C</span></span> | <span data-ttu-id="fff49-198">Francés suizo</span><span class="sxs-lookup"><span data-stu-id="fff49-198">Swiss French</span></span>              |
| <span data-ttu-id="fff49-199">0x0810</span><span class="sxs-lookup"><span data-stu-id="fff49-199">0x0810</span></span> | <span data-ttu-id="fff49-200">Italiano suizo</span><span class="sxs-lookup"><span data-stu-id="fff49-200">Swiss Italian</span></span>       | <span data-ttu-id="fff49-201">0x0816</span><span class="sxs-lookup"><span data-stu-id="fff49-201">0x0816</span></span> | <span data-ttu-id="fff49-202">Portugués (Portugal)</span><span class="sxs-lookup"><span data-stu-id="fff49-202">Portuguese (Portugal)</span></span>     |
| <span data-ttu-id="fff49-203">0x0813</span><span class="sxs-lookup"><span data-stu-id="fff49-203">0x0813</span></span> | <span data-ttu-id="fff49-204">Holandés belga</span><span class="sxs-lookup"><span data-stu-id="fff49-204">Belgian Dutch</span></span>       | <span data-ttu-id="fff49-205">0x081A</span><span class="sxs-lookup"><span data-stu-id="fff49-205">0x081A</span></span> | <span data-ttu-id="fff49-206">Serbo-Croatian (cirílico)</span><span class="sxs-lookup"><span data-stu-id="fff49-206">Serbo-Croatian (Cyrillic)</span></span> |
| <span data-ttu-id="fff49-207">0x0814</span><span class="sxs-lookup"><span data-stu-id="fff49-207">0x0814</span></span> | <span data-ttu-id="fff49-208">Noruego – nynorsk</span><span class="sxs-lookup"><span data-stu-id="fff49-208">Norwegian – Nynorsk</span></span> | <span data-ttu-id="fff49-209">?</span><span class="sxs-lookup"><span data-stu-id="fff49-209">?</span></span>      | <span data-ttu-id="fff49-210">?</span><span class="sxs-lookup"><span data-stu-id="fff49-210">?</span></span>                         |



 

<span data-ttu-id="fff49-211">El parámetro *charsetID* especifica uno de los siguientes identificadores de juego de caracteres:</span><span class="sxs-lookup"><span data-stu-id="fff49-211">The *charsetID* parameter specifies one of the following character-set identifiers:</span></span>



| <span data-ttu-id="fff49-212">Identificador</span><span class="sxs-lookup"><span data-stu-id="fff49-212">Identifier</span></span> | <span data-ttu-id="fff49-213">Juego de caracteres</span><span class="sxs-lookup"><span data-stu-id="fff49-213">Character Set</span></span>              |
|------------|----------------------------|
| <span data-ttu-id="fff49-214">0</span><span class="sxs-lookup"><span data-stu-id="fff49-214">0</span></span>          | <span data-ttu-id="fff49-215">ASCII de 7 bits</span><span class="sxs-lookup"><span data-stu-id="fff49-215">7-bit ASCII</span></span>                |
| <span data-ttu-id="fff49-216">932</span><span class="sxs-lookup"><span data-stu-id="fff49-216">932</span></span>        | <span data-ttu-id="fff49-217">Japón (Shift – JIS X-0208)</span><span class="sxs-lookup"><span data-stu-id="fff49-217">Japan (Shift – JIS X-0208)</span></span> |
| <span data-ttu-id="fff49-218">949</span><span class="sxs-lookup"><span data-stu-id="fff49-218">949</span></span>        | <span data-ttu-id="fff49-219">Corea (Shift – KSC 5601)</span><span class="sxs-lookup"><span data-stu-id="fff49-219">Korea (Shift – KSC 5601)</span></span>   |
| <span data-ttu-id="fff49-220">950</span><span class="sxs-lookup"><span data-stu-id="fff49-220">950</span></span>        | <span data-ttu-id="fff49-221">Taiwán (Big5)</span><span class="sxs-lookup"><span data-stu-id="fff49-221">Taiwan (Big5)</span></span>              |
| <span data-ttu-id="fff49-222">1200</span><span class="sxs-lookup"><span data-stu-id="fff49-222">1200</span></span>       | <span data-ttu-id="fff49-223">Unicode</span><span class="sxs-lookup"><span data-stu-id="fff49-223">Unicode</span></span>                    |
| <span data-ttu-id="fff49-224">1250</span><span class="sxs-lookup"><span data-stu-id="fff49-224">1250</span></span>       | <span data-ttu-id="fff49-225">Latín-2 (Europa Oriental)</span><span class="sxs-lookup"><span data-stu-id="fff49-225">Latin-2 (Eastern European)</span></span> |
| <span data-ttu-id="fff49-226">1251</span><span class="sxs-lookup"><span data-stu-id="fff49-226">1251</span></span>       | <span data-ttu-id="fff49-227">Cirílico</span><span class="sxs-lookup"><span data-stu-id="fff49-227">Cyrillic</span></span>                   |
| <span data-ttu-id="fff49-228">1252</span><span class="sxs-lookup"><span data-stu-id="fff49-228">1252</span></span>       | <span data-ttu-id="fff49-229">Entornos</span><span class="sxs-lookup"><span data-stu-id="fff49-229">Multilingual</span></span>               |
| <span data-ttu-id="fff49-230">1253</span><span class="sxs-lookup"><span data-stu-id="fff49-230">1253</span></span>       | <span data-ttu-id="fff49-231">Griego</span><span class="sxs-lookup"><span data-stu-id="fff49-231">Greek</span></span>                      |
| <span data-ttu-id="fff49-232">1254</span><span class="sxs-lookup"><span data-stu-id="fff49-232">1254</span></span>       | <span data-ttu-id="fff49-233">Turco</span><span class="sxs-lookup"><span data-stu-id="fff49-233">Turkish</span></span>                    |
| <span data-ttu-id="fff49-234">1255</span><span class="sxs-lookup"><span data-stu-id="fff49-234">1255</span></span>       | <span data-ttu-id="fff49-235">Hebreo</span><span class="sxs-lookup"><span data-stu-id="fff49-235">Hebrew</span></span>                     |
| <span data-ttu-id="fff49-236">1256</span><span class="sxs-lookup"><span data-stu-id="fff49-236">1256</span></span>       | <span data-ttu-id="fff49-237">Árabe</span><span class="sxs-lookup"><span data-stu-id="fff49-237">Arabic</span></span>                     |



 

 

 




