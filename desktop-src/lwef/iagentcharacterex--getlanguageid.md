---
title: IAgentCharacterEx GetLanguageID
description: IAgentCharacterEx GetLanguageID
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d847bf392709b2433b045a357a703173e2de454
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120651"
---
# <a name="iagentcharacterexgetlanguageid"></a><span data-ttu-id="2b458-103">IAgentCharacterEx::GetLanguageID</span><span class="sxs-lookup"><span data-stu-id="2b458-103">IAgentCharacterEx::GetLanguageID</span></span>

<span data-ttu-id="2b458-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2b458-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

<span data-ttu-id="2b458-105">Recupera el identificador de idioma establecido para el carácter.</span><span class="sxs-lookup"><span data-stu-id="2b458-105">Retrieves the language ID set for the character.</span></span>

-   <span data-ttu-id="2b458-106">Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2b458-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2b458-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span><span class="sxs-lookup"><span data-stu-id="2b458-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span></span>
</dt> <dd>

<span data-ttu-id="2b458-108">Dirección de una variable que recibe la configuración del identificador de idioma del carácter.</span><span class="sxs-lookup"><span data-stu-id="2b458-108">Address of a variable that receives the language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="2b458-109">Entero Long que especifica el identificador de idioma del carácter.</span><span class="sxs-lookup"><span data-stu-id="2b458-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="2b458-110">El identificador de idioma (LANGID) de un carácter es un valor de 16 bits definido por Windows, que consta de un identificador de idioma principal y un identificador de idioma secundario.</span><span class="sxs-lookup"><span data-stu-id="2b458-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="2b458-111">Los ejemplos siguientes son valores para algunos idiomas.</span><span class="sxs-lookup"><span data-stu-id="2b458-111">The following examples are values for some languages.</span></span> <span data-ttu-id="2b458-112">Para determinar los valores de otros lenguajes, consulte la documentación del SDK de plataforma.</span><span class="sxs-lookup"><span data-stu-id="2b458-112">To determine the values other languages, see the Platform SDK documentation.</span></span>



| <span data-ttu-id="2b458-113">Lenguaje</span><span class="sxs-lookup"><span data-stu-id="2b458-113">Language</span></span>              | <span data-ttu-id="2b458-114">ID</span><span class="sxs-lookup"><span data-stu-id="2b458-114">ID</span></span>     | <span data-ttu-id="2b458-115">Lenguaje</span><span class="sxs-lookup"><span data-stu-id="2b458-115">Language</span></span>              | <span data-ttu-id="2b458-116">ID</span><span class="sxs-lookup"><span data-stu-id="2b458-116">ID</span></span>     |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="2b458-117">Árabe (Emiratos Árabes)</span><span class="sxs-lookup"><span data-stu-id="2b458-117">Arabic (Saudi)</span></span>        | <span data-ttu-id="2b458-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="2b458-118">0x0401</span></span> | <span data-ttu-id="2b458-119">Italiano</span><span class="sxs-lookup"><span data-stu-id="2b458-119">Italian</span></span>               | <span data-ttu-id="2b458-120">0x0410</span><span class="sxs-lookup"><span data-stu-id="2b458-120">0x0410</span></span> |
| <span data-ttu-id="2b458-121">Vasco</span><span class="sxs-lookup"><span data-stu-id="2b458-121">Basque</span></span>                | <span data-ttu-id="2b458-122">0x042d</span><span class="sxs-lookup"><span data-stu-id="2b458-122">0x042d</span></span> | <span data-ttu-id="2b458-123">Japonés</span><span class="sxs-lookup"><span data-stu-id="2b458-123">Japanese</span></span>              | <span data-ttu-id="2b458-124">0x0411</span><span class="sxs-lookup"><span data-stu-id="2b458-124">0x0411</span></span> |
| <span data-ttu-id="2b458-125">Chino (simplificado)</span><span class="sxs-lookup"><span data-stu-id="2b458-125">Chinese (Simplified)</span></span>  | <span data-ttu-id="2b458-126">0x0804</span><span class="sxs-lookup"><span data-stu-id="2b458-126">0x0804</span></span> | <span data-ttu-id="2b458-127">Coreano</span><span class="sxs-lookup"><span data-stu-id="2b458-127">Korean</span></span>                | <span data-ttu-id="2b458-128">0x0412</span><span class="sxs-lookup"><span data-stu-id="2b458-128">0x0412</span></span> |
| <span data-ttu-id="2b458-129">Chino (tradicional)</span><span class="sxs-lookup"><span data-stu-id="2b458-129">Chinese (Traditional)</span></span> | <span data-ttu-id="2b458-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="2b458-130">0x0404</span></span> | <span data-ttu-id="2b458-131">Noruego</span><span class="sxs-lookup"><span data-stu-id="2b458-131">Norwegian</span></span>             | <span data-ttu-id="2b458-132">0x0414</span><span class="sxs-lookup"><span data-stu-id="2b458-132">0x0414</span></span> |
| <span data-ttu-id="2b458-133">Croata</span><span class="sxs-lookup"><span data-stu-id="2b458-133">Croatian</span></span>              | <span data-ttu-id="2b458-134">0x041A</span><span class="sxs-lookup"><span data-stu-id="2b458-134">0x041A</span></span> | <span data-ttu-id="2b458-135">Polaco</span><span class="sxs-lookup"><span data-stu-id="2b458-135">Polish</span></span>                | <span data-ttu-id="2b458-136">0x0415</span><span class="sxs-lookup"><span data-stu-id="2b458-136">0x0415</span></span> |
| <span data-ttu-id="2b458-137">Checo</span><span class="sxs-lookup"><span data-stu-id="2b458-137">Czech</span></span>                 | <span data-ttu-id="2b458-138">0x0405</span><span class="sxs-lookup"><span data-stu-id="2b458-138">0x0405</span></span> | <span data-ttu-id="2b458-139">Portugués (Portugal)</span><span class="sxs-lookup"><span data-stu-id="2b458-139">Portuguese (Portugal)</span></span> | <span data-ttu-id="2b458-140">0x0816</span><span class="sxs-lookup"><span data-stu-id="2b458-140">0x0816</span></span> |
| <span data-ttu-id="2b458-141">Danés</span><span class="sxs-lookup"><span data-stu-id="2b458-141">Danish</span></span>                | <span data-ttu-id="2b458-142">0x0406</span><span class="sxs-lookup"><span data-stu-id="2b458-142">0x0406</span></span> | <span data-ttu-id="2b458-143">Portugués (Brasil)</span><span class="sxs-lookup"><span data-stu-id="2b458-143">Portuguese (Brazil)</span></span>   | <span data-ttu-id="2b458-144">0x0416</span><span class="sxs-lookup"><span data-stu-id="2b458-144">0x0416</span></span> |
| <span data-ttu-id="2b458-145">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="2b458-145">Dutch</span></span>                 | <span data-ttu-id="2b458-146">0x0413</span><span class="sxs-lookup"><span data-stu-id="2b458-146">0x0413</span></span> | <span data-ttu-id="2b458-147">Rumano</span><span class="sxs-lookup"><span data-stu-id="2b458-147">Romanian</span></span>              | <span data-ttu-id="2b458-148">0x0418</span><span class="sxs-lookup"><span data-stu-id="2b458-148">0x0418</span></span> |
| <span data-ttu-id="2b458-149">Inglés (Gran Bretaña)</span><span class="sxs-lookup"><span data-stu-id="2b458-149">English (British)</span></span>     | <span data-ttu-id="2b458-150">0x0809</span><span class="sxs-lookup"><span data-stu-id="2b458-150">0x0809</span></span> | <span data-ttu-id="2b458-151">Ruso</span><span class="sxs-lookup"><span data-stu-id="2b458-151">Russian</span></span>               | <span data-ttu-id="2b458-152">0x0419</span><span class="sxs-lookup"><span data-stu-id="2b458-152">0x0419</span></span> |
| <span data-ttu-id="2b458-153">Inglés (EE.UU.)</span><span class="sxs-lookup"><span data-stu-id="2b458-153">English (US)</span></span>          | <span data-ttu-id="2b458-154">0x0409</span><span class="sxs-lookup"><span data-stu-id="2b458-154">0x0409</span></span> | <span data-ttu-id="2b458-155">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="2b458-155">Slovakian</span></span>             | <span data-ttu-id="2b458-156">0x041B</span><span class="sxs-lookup"><span data-stu-id="2b458-156">0x041B</span></span> |
| <span data-ttu-id="2b458-157">Finlandés</span><span class="sxs-lookup"><span data-stu-id="2b458-157">Finnish</span></span>               | <span data-ttu-id="2b458-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="2b458-158">0x040B</span></span> | <span data-ttu-id="2b458-159">Esloveno</span><span class="sxs-lookup"><span data-stu-id="2b458-159">Slovenian</span></span>             | <span data-ttu-id="2b458-160">0x0424</span><span class="sxs-lookup"><span data-stu-id="2b458-160">0x0424</span></span> |
| <span data-ttu-id="2b458-161">Francés</span><span class="sxs-lookup"><span data-stu-id="2b458-161">French</span></span>                | <span data-ttu-id="2b458-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="2b458-162">0x040C</span></span> | <span data-ttu-id="2b458-163">Español</span><span class="sxs-lookup"><span data-stu-id="2b458-163">Spanish</span></span>               | <span data-ttu-id="2b458-164">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="2b458-164">0x0C0A</span></span> |
| <span data-ttu-id="2b458-165">Alemán</span><span class="sxs-lookup"><span data-stu-id="2b458-165">German</span></span>                | <span data-ttu-id="2b458-166">0x0407</span><span class="sxs-lookup"><span data-stu-id="2b458-166">0x0407</span></span> | <span data-ttu-id="2b458-167">Sueco</span><span class="sxs-lookup"><span data-stu-id="2b458-167">Swedish</span></span>               | <span data-ttu-id="2b458-168">0x041D</span><span class="sxs-lookup"><span data-stu-id="2b458-168">0x041D</span></span> |
| <span data-ttu-id="2b458-169">Griego</span><span class="sxs-lookup"><span data-stu-id="2b458-169">Greek</span></span>                 | <span data-ttu-id="2b458-170">0x0408</span><span class="sxs-lookup"><span data-stu-id="2b458-170">0x0408</span></span> | <span data-ttu-id="2b458-171">Tailandés</span><span class="sxs-lookup"><span data-stu-id="2b458-171">Thai</span></span>                  | <span data-ttu-id="2b458-172">0x041E</span><span class="sxs-lookup"><span data-stu-id="2b458-172">0x041E</span></span> |
| <span data-ttu-id="2b458-173">Hebreo</span><span class="sxs-lookup"><span data-stu-id="2b458-173">Hebrew</span></span>                | <span data-ttu-id="2b458-174">0x040D</span><span class="sxs-lookup"><span data-stu-id="2b458-174">0x040D</span></span> | <span data-ttu-id="2b458-175">Turco</span><span class="sxs-lookup"><span data-stu-id="2b458-175">Turkish</span></span>               | <span data-ttu-id="2b458-176">0x041F</span><span class="sxs-lookup"><span data-stu-id="2b458-176">0x041F</span></span> |
| <span data-ttu-id="2b458-177">Húngaro</span><span class="sxs-lookup"><span data-stu-id="2b458-177">Hungarian</span></span>             | <span data-ttu-id="2b458-178">0x040E</span><span class="sxs-lookup"><span data-stu-id="2b458-178">0x040E</span></span> |                       |        |



 

<span data-ttu-id="2b458-179">Si no establece este identificador de idioma para el carácter, el identificador de idioma del carácter será el identificador de idioma del sistema actual.</span><span class="sxs-lookup"><span data-stu-id="2b458-179">If you do not set this language ID for the character, the character's language ID will be the current system language ID.</span></span>

<span data-ttu-id="2b458-180">Esta configuración también determina el idioma de la salida de TTS, el texto del globo de palabras, los comandos del menú emergente del carácter y el motor de reconocimiento de voz.</span><span class="sxs-lookup"><span data-stu-id="2b458-180">This setting also determines the language for TTS output, word balloon text, the commands in the character's pop-up menu, and speech recognition engine.</span></span> <span data-ttu-id="2b458-181">Para determinar si hay un motor de reconocimiento de voz compatible disponible para el lenguaje del carácter, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) o [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="2b458-181">To determine if there is a compatible speech recognition engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="2b458-182">Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="2b458-182">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="2b458-183">Si el identificador de idioma se establece en un idioma que admite texto bidireccional (como árabe o hebreo), pero el sistema que ejecuta la aplicación no tiene instalada la compatibilidad bidireccional, el texto aparecerá en el globo de palabras en orden lógico en lugar de mostrarse.</span><span class="sxs-lookup"><span data-stu-id="2b458-183">If the language ID is set to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="2b458-184">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2b458-184">See Also</span></span>

<span data-ttu-id="2b458-185">[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="2b458-185">[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




