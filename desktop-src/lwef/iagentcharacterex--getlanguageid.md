---
title: IAgentCharacterEx GetLanguageID
description: IAgentCharacterEx GetLanguageID
ms.assetid: 4e4e5342-edf9-480b-a9c3-e2626fd89e76
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9679538f93d779acc6272dccada824585c4449f5
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104076079"
---
# <a name="iagentcharacterexgetlanguageid"></a><span data-ttu-id="5fdee-103">IAgentCharacterEx::GetLanguageID</span><span class="sxs-lookup"><span data-stu-id="5fdee-103">IAgentCharacterEx::GetLanguageID</span></span>

<span data-ttu-id="5fdee-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5fdee-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetLanguageID(
   long * plangID  // address of language ID setting
);
```

<span data-ttu-id="5fdee-105">Recupera el conjunto de IDENTIFICADOres de idioma para el carácter.</span><span class="sxs-lookup"><span data-stu-id="5fdee-105">Retrieves the language ID set for the character.</span></span>

-   <span data-ttu-id="5fdee-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="5fdee-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5fdee-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span><span class="sxs-lookup"><span data-stu-id="5fdee-107"><span id="plangID"></span><span id="plangid"></span><span id="PLANGID"></span>*plangID*</span></span>
</dt> <dd>

<span data-ttu-id="5fdee-108">Dirección de una variable que recibe la configuración de identificador de idioma para el carácter.</span><span class="sxs-lookup"><span data-stu-id="5fdee-108">Address of a variable that receives the language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="5fdee-109">Entero largo que especifica el identificador de idioma del carácter.</span><span class="sxs-lookup"><span data-stu-id="5fdee-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="5fdee-110">El identificador de idioma (LANGID) de un carácter es un valor de 16 bits definido por Windows, que consta de un identificador de idioma principal y un identificador de idioma secundario.</span><span class="sxs-lookup"><span data-stu-id="5fdee-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="5fdee-111">Los ejemplos siguientes son valores para algunos idiomas.</span><span class="sxs-lookup"><span data-stu-id="5fdee-111">The following examples are values for some languages.</span></span> <span data-ttu-id="5fdee-112">Para determinar los valores otros lenguajes, consulte la documentación del SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="5fdee-112">To determine the values other languages, see the Platform SDK documentation.</span></span>



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="5fdee-113">Árabe (Arabia Saudí)</span><span class="sxs-lookup"><span data-stu-id="5fdee-113">Arabic (Saudi)</span></span>        | <span data-ttu-id="5fdee-114">0x0401</span><span class="sxs-lookup"><span data-stu-id="5fdee-114">0x0401</span></span> | <span data-ttu-id="5fdee-115">Italiano</span><span class="sxs-lookup"><span data-stu-id="5fdee-115">Italian</span></span>               | <span data-ttu-id="5fdee-116">0x0410</span><span class="sxs-lookup"><span data-stu-id="5fdee-116">0x0410</span></span> |
| <span data-ttu-id="5fdee-117">Vasco</span><span class="sxs-lookup"><span data-stu-id="5fdee-117">Basque</span></span>                | <span data-ttu-id="5fdee-118">0x042d</span><span class="sxs-lookup"><span data-stu-id="5fdee-118">0x042d</span></span> | <span data-ttu-id="5fdee-119">Japonés</span><span class="sxs-lookup"><span data-stu-id="5fdee-119">Japanese</span></span>              | <span data-ttu-id="5fdee-120">0x0411</span><span class="sxs-lookup"><span data-stu-id="5fdee-120">0x0411</span></span> |
| <span data-ttu-id="5fdee-121">Chino (simplificado)</span><span class="sxs-lookup"><span data-stu-id="5fdee-121">Chinese (Simplified)</span></span>  | <span data-ttu-id="5fdee-122">0x0804</span><span class="sxs-lookup"><span data-stu-id="5fdee-122">0x0804</span></span> | <span data-ttu-id="5fdee-123">Coreano</span><span class="sxs-lookup"><span data-stu-id="5fdee-123">Korean</span></span>                | <span data-ttu-id="5fdee-124">0x0412</span><span class="sxs-lookup"><span data-stu-id="5fdee-124">0x0412</span></span> |
| <span data-ttu-id="5fdee-125">Chino (tradicional)</span><span class="sxs-lookup"><span data-stu-id="5fdee-125">Chinese (Traditional)</span></span> | <span data-ttu-id="5fdee-126">0x0404</span><span class="sxs-lookup"><span data-stu-id="5fdee-126">0x0404</span></span> | <span data-ttu-id="5fdee-127">Noruego</span><span class="sxs-lookup"><span data-stu-id="5fdee-127">Norwegian</span></span>             | <span data-ttu-id="5fdee-128">0x0414</span><span class="sxs-lookup"><span data-stu-id="5fdee-128">0x0414</span></span> |
| <span data-ttu-id="5fdee-129">Croata</span><span class="sxs-lookup"><span data-stu-id="5fdee-129">Croatian</span></span>              | <span data-ttu-id="5fdee-130">0x041A</span><span class="sxs-lookup"><span data-stu-id="5fdee-130">0x041A</span></span> | <span data-ttu-id="5fdee-131">Polaco</span><span class="sxs-lookup"><span data-stu-id="5fdee-131">Polish</span></span>                | <span data-ttu-id="5fdee-132">0x0415</span><span class="sxs-lookup"><span data-stu-id="5fdee-132">0x0415</span></span> |
| <span data-ttu-id="5fdee-133">Checo</span><span class="sxs-lookup"><span data-stu-id="5fdee-133">Czech</span></span>                 | <span data-ttu-id="5fdee-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="5fdee-134">0x0405</span></span> | <span data-ttu-id="5fdee-135">Portugués (Portugal)</span><span class="sxs-lookup"><span data-stu-id="5fdee-135">Portuguese (Portugal)</span></span> | <span data-ttu-id="5fdee-136">0x0816</span><span class="sxs-lookup"><span data-stu-id="5fdee-136">0x0816</span></span> |
| <span data-ttu-id="5fdee-137">Danés</span><span class="sxs-lookup"><span data-stu-id="5fdee-137">Danish</span></span>                | <span data-ttu-id="5fdee-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="5fdee-138">0x0406</span></span> | <span data-ttu-id="5fdee-139">Portugués (Brasil)</span><span class="sxs-lookup"><span data-stu-id="5fdee-139">Portuguese (Brazil)</span></span>   | <span data-ttu-id="5fdee-140">0x0416</span><span class="sxs-lookup"><span data-stu-id="5fdee-140">0x0416</span></span> |
| <span data-ttu-id="5fdee-141">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="5fdee-141">Dutch</span></span>                 | <span data-ttu-id="5fdee-142">0x0413</span><span class="sxs-lookup"><span data-stu-id="5fdee-142">0x0413</span></span> | <span data-ttu-id="5fdee-143">Rumano</span><span class="sxs-lookup"><span data-stu-id="5fdee-143">Romanian</span></span>              | <span data-ttu-id="5fdee-144">0x0418</span><span class="sxs-lookup"><span data-stu-id="5fdee-144">0x0418</span></span> |
| <span data-ttu-id="5fdee-145">Inglés (Gran Bretaña)</span><span class="sxs-lookup"><span data-stu-id="5fdee-145">English (British)</span></span>     | <span data-ttu-id="5fdee-146">0x0809</span><span class="sxs-lookup"><span data-stu-id="5fdee-146">0x0809</span></span> | <span data-ttu-id="5fdee-147">Ruso</span><span class="sxs-lookup"><span data-stu-id="5fdee-147">Russian</span></span>               | <span data-ttu-id="5fdee-148">0x0419</span><span class="sxs-lookup"><span data-stu-id="5fdee-148">0x0419</span></span> |
| <span data-ttu-id="5fdee-149">Inglés (EE.UU.)</span><span class="sxs-lookup"><span data-stu-id="5fdee-149">English (US)</span></span>          | <span data-ttu-id="5fdee-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="5fdee-150">0x0409</span></span> | <span data-ttu-id="5fdee-151">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="5fdee-151">Slovakian</span></span>             | <span data-ttu-id="5fdee-152">0x041B</span><span class="sxs-lookup"><span data-stu-id="5fdee-152">0x041B</span></span> |
| <span data-ttu-id="5fdee-153">Finés</span><span class="sxs-lookup"><span data-stu-id="5fdee-153">Finnish</span></span>               | <span data-ttu-id="5fdee-154">0x040B</span><span class="sxs-lookup"><span data-stu-id="5fdee-154">0x040B</span></span> | <span data-ttu-id="5fdee-155">Esloveno</span><span class="sxs-lookup"><span data-stu-id="5fdee-155">Slovenian</span></span>             | <span data-ttu-id="5fdee-156">0x0424</span><span class="sxs-lookup"><span data-stu-id="5fdee-156">0x0424</span></span> |
| <span data-ttu-id="5fdee-157">Francés</span><span class="sxs-lookup"><span data-stu-id="5fdee-157">French</span></span>                | <span data-ttu-id="5fdee-158">0x040C</span><span class="sxs-lookup"><span data-stu-id="5fdee-158">0x040C</span></span> | <span data-ttu-id="5fdee-159">Español</span><span class="sxs-lookup"><span data-stu-id="5fdee-159">Spanish</span></span>               | <span data-ttu-id="5fdee-160">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="5fdee-160">0x0C0A</span></span> |
| <span data-ttu-id="5fdee-161">Alemán</span><span class="sxs-lookup"><span data-stu-id="5fdee-161">German</span></span>                | <span data-ttu-id="5fdee-162">0x0407</span><span class="sxs-lookup"><span data-stu-id="5fdee-162">0x0407</span></span> | <span data-ttu-id="5fdee-163">Sueco</span><span class="sxs-lookup"><span data-stu-id="5fdee-163">Swedish</span></span>               | <span data-ttu-id="5fdee-164">0x041D</span><span class="sxs-lookup"><span data-stu-id="5fdee-164">0x041D</span></span> |
| <span data-ttu-id="5fdee-165">Griego</span><span class="sxs-lookup"><span data-stu-id="5fdee-165">Greek</span></span>                 | <span data-ttu-id="5fdee-166">0x0408</span><span class="sxs-lookup"><span data-stu-id="5fdee-166">0x0408</span></span> | <span data-ttu-id="5fdee-167">Tailandés</span><span class="sxs-lookup"><span data-stu-id="5fdee-167">Thai</span></span>                  | <span data-ttu-id="5fdee-168">0x041E</span><span class="sxs-lookup"><span data-stu-id="5fdee-168">0x041E</span></span> |
| <span data-ttu-id="5fdee-169">Hebreo</span><span class="sxs-lookup"><span data-stu-id="5fdee-169">Hebrew</span></span>                | <span data-ttu-id="5fdee-170">0x040D</span><span class="sxs-lookup"><span data-stu-id="5fdee-170">0x040D</span></span> | <span data-ttu-id="5fdee-171">Turco</span><span class="sxs-lookup"><span data-stu-id="5fdee-171">Turkish</span></span>               | <span data-ttu-id="5fdee-172">0x041F</span><span class="sxs-lookup"><span data-stu-id="5fdee-172">0x041F</span></span> |
| <span data-ttu-id="5fdee-173">Húngaro</span><span class="sxs-lookup"><span data-stu-id="5fdee-173">Hungarian</span></span>             | <span data-ttu-id="5fdee-174">0x040E</span><span class="sxs-lookup"><span data-stu-id="5fdee-174">0x040E</span></span> |                       |        |



 

<span data-ttu-id="5fdee-175">Si no establece este identificador de idioma para el carácter, el ID. de idioma del carácter será el ID. de idioma del sistema actual.</span><span class="sxs-lookup"><span data-stu-id="5fdee-175">If you do not set this language ID for the character, the character's language ID will be the current system language ID.</span></span>

<span data-ttu-id="5fdee-176">Esta configuración también determina el idioma de la salida de TTS, el texto de globo de palabras, los comandos del menú emergente del carácter y el motor de reconocimiento de voz.</span><span class="sxs-lookup"><span data-stu-id="5fdee-176">This setting also determines the language for TTS output, word balloon text, the commands in the character's pop-up menu, and speech recognition engine.</span></span> <span data-ttu-id="5fdee-177">Para determinar si hay un motor de reconocimiento de voz compatible disponible para el idioma del carácter, use [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md) o [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="5fdee-177">To determine if there is a compatible speech recognition engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="5fdee-178">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="5fdee-178">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="5fdee-179">Si el identificador de idioma se establece en un idioma que admite texto bidireccional (como el árabe o el hebreo), pero el sistema que ejecuta la aplicación no tiene instalada la compatibilidad bidireccional, el texto aparecerá en el globo de palabras en lugar de en el orden de visualización.</span><span class="sxs-lookup"><span data-stu-id="5fdee-179">If the language ID is set to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="5fdee-180">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5fdee-180">See Also</span></span>

<span data-ttu-id="5fdee-181">[**IAgentCharacterEx: SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="5fdee-181">[**IAgentCharacterEx:SetLanguageID**](iagentcharacterex--setlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




