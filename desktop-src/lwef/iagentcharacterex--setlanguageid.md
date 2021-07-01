---
title: IAgentCharacterEx SetLanguageID
description: IAgentCharacterEx SetLanguageID
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 036e1d41878adaae878a5961b45d190971d790af
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119010"
---
# <a name="iagentcharacterexsetlanguageid"></a><span data-ttu-id="3aafe-103">IAgentCharacterEx::SetLanguageID</span><span class="sxs-lookup"><span data-stu-id="3aafe-103">IAgentCharacterEx::SetLanguageID</span></span>

<span data-ttu-id="3aafe-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3aafe-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

<span data-ttu-id="3aafe-105">Establece el identificador de idioma establecido para el carácter.</span><span class="sxs-lookup"><span data-stu-id="3aafe-105">Sets the language ID set for the character.</span></span>

-   <span data-ttu-id="3aafe-106">Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="3aafe-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3aafe-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span><span class="sxs-lookup"><span data-stu-id="3aafe-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="3aafe-108">La configuración del identificador de idioma para el carácter.</span><span class="sxs-lookup"><span data-stu-id="3aafe-108">The language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="3aafe-109">Entero Long que especifica el identificador de idioma del carácter.</span><span class="sxs-lookup"><span data-stu-id="3aafe-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="3aafe-110">El identificador de idioma (LANGID) de un carácter es un valor de 16 bits definido por Windows, que consta de un identificador de idioma principal y un identificador de idioma secundario.</span><span class="sxs-lookup"><span data-stu-id="3aafe-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="3aafe-111">Puede usar los siguientes valores para los idiomas especificados.</span><span class="sxs-lookup"><span data-stu-id="3aafe-111">You can use the following values for the specified languages.</span></span> <span data-ttu-id="3aafe-112">Para más información, consulte la documentación del SDK de plataforma.</span><span class="sxs-lookup"><span data-stu-id="3aafe-112">For more information, see the Platform SDK documentation.</span></span>



| <span data-ttu-id="3aafe-113">Lenguaje</span><span class="sxs-lookup"><span data-stu-id="3aafe-113">Language</span></span>              | <span data-ttu-id="3aafe-114">ID</span><span class="sxs-lookup"><span data-stu-id="3aafe-114">ID</span></span>     |  <span data-ttu-id="3aafe-115">Lenguaje</span><span class="sxs-lookup"><span data-stu-id="3aafe-115">Language</span></span>             | <span data-ttu-id="3aafe-116">ID</span><span class="sxs-lookup"><span data-stu-id="3aafe-116">ID</span></span>     |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="3aafe-117">Árabe (Emiratos Árabes)</span><span class="sxs-lookup"><span data-stu-id="3aafe-117">Arabic (Saudi)</span></span>        | <span data-ttu-id="3aafe-118">0x0401</span><span class="sxs-lookup"><span data-stu-id="3aafe-118">0x0401</span></span> | <span data-ttu-id="3aafe-119">Italiano</span><span class="sxs-lookup"><span data-stu-id="3aafe-119">Italian</span></span>               | <span data-ttu-id="3aafe-120">0x0410</span><span class="sxs-lookup"><span data-stu-id="3aafe-120">0x0410</span></span> |
| <span data-ttu-id="3aafe-121">Vasco</span><span class="sxs-lookup"><span data-stu-id="3aafe-121">Basque</span></span>                | <span data-ttu-id="3aafe-122">0x042d</span><span class="sxs-lookup"><span data-stu-id="3aafe-122">0x042d</span></span> | <span data-ttu-id="3aafe-123">Japonés</span><span class="sxs-lookup"><span data-stu-id="3aafe-123">Japanese</span></span>              | <span data-ttu-id="3aafe-124">0x0411</span><span class="sxs-lookup"><span data-stu-id="3aafe-124">0x0411</span></span> |
| <span data-ttu-id="3aafe-125">Chino (simplificado)</span><span class="sxs-lookup"><span data-stu-id="3aafe-125">Chinese (Simplified)</span></span>  | <span data-ttu-id="3aafe-126">0x0804</span><span class="sxs-lookup"><span data-stu-id="3aafe-126">0x0804</span></span> | <span data-ttu-id="3aafe-127">Coreano</span><span class="sxs-lookup"><span data-stu-id="3aafe-127">Korean</span></span>                | <span data-ttu-id="3aafe-128">0x0412</span><span class="sxs-lookup"><span data-stu-id="3aafe-128">0x0412</span></span> |
| <span data-ttu-id="3aafe-129">Chino (tradicional)</span><span class="sxs-lookup"><span data-stu-id="3aafe-129">Chinese (Traditional)</span></span> | <span data-ttu-id="3aafe-130">0x0404</span><span class="sxs-lookup"><span data-stu-id="3aafe-130">0x0404</span></span> | <span data-ttu-id="3aafe-131">Noruego</span><span class="sxs-lookup"><span data-stu-id="3aafe-131">Norwegian</span></span>             | <span data-ttu-id="3aafe-132">0x0414</span><span class="sxs-lookup"><span data-stu-id="3aafe-132">0x0414</span></span> |
| <span data-ttu-id="3aafe-133">Croata</span><span class="sxs-lookup"><span data-stu-id="3aafe-133">Croatian</span></span>              | <span data-ttu-id="3aafe-134">0x041A</span><span class="sxs-lookup"><span data-stu-id="3aafe-134">0x041A</span></span> | <span data-ttu-id="3aafe-135">Polaco</span><span class="sxs-lookup"><span data-stu-id="3aafe-135">Polish</span></span>                | <span data-ttu-id="3aafe-136">0x0415</span><span class="sxs-lookup"><span data-stu-id="3aafe-136">0x0415</span></span> |
| <span data-ttu-id="3aafe-137">Checo</span><span class="sxs-lookup"><span data-stu-id="3aafe-137">Czech</span></span>                 | <span data-ttu-id="3aafe-138">0x0405</span><span class="sxs-lookup"><span data-stu-id="3aafe-138">0x0405</span></span> | <span data-ttu-id="3aafe-139">Portugués (Portugal)</span><span class="sxs-lookup"><span data-stu-id="3aafe-139">Portuguese (Portugal)</span></span> | <span data-ttu-id="3aafe-140">0x0816</span><span class="sxs-lookup"><span data-stu-id="3aafe-140">0x0816</span></span> |
| <span data-ttu-id="3aafe-141">Danés</span><span class="sxs-lookup"><span data-stu-id="3aafe-141">Danish</span></span>                | <span data-ttu-id="3aafe-142">0x0406</span><span class="sxs-lookup"><span data-stu-id="3aafe-142">0x0406</span></span> | <span data-ttu-id="3aafe-143">Portugués (Brasil)</span><span class="sxs-lookup"><span data-stu-id="3aafe-143">Portuguese (Brazil)</span></span>   | <span data-ttu-id="3aafe-144">0x0416</span><span class="sxs-lookup"><span data-stu-id="3aafe-144">0x0416</span></span> |
| <span data-ttu-id="3aafe-145">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="3aafe-145">Dutch</span></span>                 | <span data-ttu-id="3aafe-146">0x0413</span><span class="sxs-lookup"><span data-stu-id="3aafe-146">0x0413</span></span> | <span data-ttu-id="3aafe-147">Rumano</span><span class="sxs-lookup"><span data-stu-id="3aafe-147">Romanian</span></span>              | <span data-ttu-id="3aafe-148">0x0418</span><span class="sxs-lookup"><span data-stu-id="3aafe-148">0x0418</span></span> |
| <span data-ttu-id="3aafe-149">Inglés (Gran Bretaña)</span><span class="sxs-lookup"><span data-stu-id="3aafe-149">English (British)</span></span>     | <span data-ttu-id="3aafe-150">0x0809</span><span class="sxs-lookup"><span data-stu-id="3aafe-150">0x0809</span></span> | <span data-ttu-id="3aafe-151">Ruso</span><span class="sxs-lookup"><span data-stu-id="3aafe-151">Russian</span></span>               | <span data-ttu-id="3aafe-152">0x0419</span><span class="sxs-lookup"><span data-stu-id="3aafe-152">0x0419</span></span> |
| <span data-ttu-id="3aafe-153">Inglés (EE.UU.)</span><span class="sxs-lookup"><span data-stu-id="3aafe-153">English (US)</span></span>          | <span data-ttu-id="3aafe-154">0x0409</span><span class="sxs-lookup"><span data-stu-id="3aafe-154">0x0409</span></span> | <span data-ttu-id="3aafe-155">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="3aafe-155">Slovakian</span></span>             | <span data-ttu-id="3aafe-156">0x041B</span><span class="sxs-lookup"><span data-stu-id="3aafe-156">0x041B</span></span> |
| <span data-ttu-id="3aafe-157">Finlandés</span><span class="sxs-lookup"><span data-stu-id="3aafe-157">Finnish</span></span>               | <span data-ttu-id="3aafe-158">0x040B</span><span class="sxs-lookup"><span data-stu-id="3aafe-158">0x040B</span></span> | <span data-ttu-id="3aafe-159">Esloveno</span><span class="sxs-lookup"><span data-stu-id="3aafe-159">Slovenian</span></span>             | <span data-ttu-id="3aafe-160">0x0424</span><span class="sxs-lookup"><span data-stu-id="3aafe-160">0x0424</span></span> |
| <span data-ttu-id="3aafe-161">Francés</span><span class="sxs-lookup"><span data-stu-id="3aafe-161">French</span></span>                | <span data-ttu-id="3aafe-162">0x040C</span><span class="sxs-lookup"><span data-stu-id="3aafe-162">0x040C</span></span> | <span data-ttu-id="3aafe-163">Español</span><span class="sxs-lookup"><span data-stu-id="3aafe-163">Spanish</span></span>               | <span data-ttu-id="3aafe-164">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="3aafe-164">0x0C0A</span></span> |
| <span data-ttu-id="3aafe-165">Alemán</span><span class="sxs-lookup"><span data-stu-id="3aafe-165">German</span></span>                | <span data-ttu-id="3aafe-166">0x0407</span><span class="sxs-lookup"><span data-stu-id="3aafe-166">0x0407</span></span> | <span data-ttu-id="3aafe-167">Sueco</span><span class="sxs-lookup"><span data-stu-id="3aafe-167">Swedish</span></span>               | <span data-ttu-id="3aafe-168">0x041D</span><span class="sxs-lookup"><span data-stu-id="3aafe-168">0x041D</span></span> |
| <span data-ttu-id="3aafe-169">Griego</span><span class="sxs-lookup"><span data-stu-id="3aafe-169">Greek</span></span>                 | <span data-ttu-id="3aafe-170">0x0408</span><span class="sxs-lookup"><span data-stu-id="3aafe-170">0x0408</span></span> | <span data-ttu-id="3aafe-171">Tailandés</span><span class="sxs-lookup"><span data-stu-id="3aafe-171">Thai</span></span>                  | <span data-ttu-id="3aafe-172">0x041E</span><span class="sxs-lookup"><span data-stu-id="3aafe-172">0x041E</span></span> |
| <span data-ttu-id="3aafe-173">Hebreo</span><span class="sxs-lookup"><span data-stu-id="3aafe-173">Hebrew</span></span>                | <span data-ttu-id="3aafe-174">0x040D</span><span class="sxs-lookup"><span data-stu-id="3aafe-174">0x040D</span></span> | <span data-ttu-id="3aafe-175">Turco</span><span class="sxs-lookup"><span data-stu-id="3aafe-175">Turkish</span></span>               | <span data-ttu-id="3aafe-176">0x041F</span><span class="sxs-lookup"><span data-stu-id="3aafe-176">0x041F</span></span> |
| <span data-ttu-id="3aafe-177">Húngaro</span><span class="sxs-lookup"><span data-stu-id="3aafe-177">Hungarian</span></span>             | <span data-ttu-id="3aafe-178">0x040E</span><span class="sxs-lookup"><span data-stu-id="3aafe-178">0x040E</span></span> |                       |        |



 

<span data-ttu-id="3aafe-179">Si no establece el identificador de idioma para el carácter, su identificador de idioma será el identificador de idioma del sistema actual si está instalado el archivo DLL de idioma del Agente correspondiente; De lo contrario, el idioma del carácter será inglés (EE. UU.).</span><span class="sxs-lookup"><span data-stu-id="3aafe-179">If you do not set the language ID for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed; otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="3aafe-180">Esta propiedad también determina el idioma del texto del globo de palabras, los comandos del menú emergente del carácter y el motor de reconocimiento de voz.</span><span class="sxs-lookup"><span data-stu-id="3aafe-180">This property also determines the language for the word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="3aafe-181">También determina el idioma predeterminado para la salida de TTS.</span><span class="sxs-lookup"><span data-stu-id="3aafe-181">It also determines the default language for TTS output.</span></span> <span data-ttu-id="3aafe-182">Para determinar si hay un motor de voz compatible disponible para el lenguaje del carácter, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) o [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="3aafe-182">To determine if there is a compatible speech engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="3aafe-183">Si intenta establecer el identificador de idioma de un carácter y los recursos de lenguaje del Agente, la página de códigos o una fuente de presentación para el identificador de idioma no está disponible, el Agente devuelve un error y el identificador de idioma del carácter permanece en su última configuración.</span><span class="sxs-lookup"><span data-stu-id="3aafe-183">If you try to set the language ID for a character and the Agent language resources, the code page, or a display font for the language ID is not available, Agent returns an error and the character's language ID remains at its last setting.</span></span> <span data-ttu-id="3aafe-184">Al establecer esta propiedad no se devuelve un error si no hay motores de voz que coincidan con el idioma.</span><span class="sxs-lookup"><span data-stu-id="3aafe-184">Setting this property does not return an error if there are no matching speech engines for the language.</span></span>

<span data-ttu-id="3aafe-185">Esta propiedad solo se aplica al uso del carácter por parte de la aplicación cliente; la configuración no afecta a otros clientes del carácter ni a otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="3aafe-185">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="3aafe-186">Si establece el identificador de idioma del carácter en un idioma que admita texto bidireccional (como árabe o hebreo), pero el sistema que ejecuta la aplicación no tiene instalada compatibilidad bidireccional, el texto aparecerá en el globo de palabras en orden lógico en lugar de mostrar.</span><span class="sxs-lookup"><span data-stu-id="3aafe-186">If you set the character's language ID to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="3aafe-187">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3aafe-187">See Also</span></span>

<span data-ttu-id="3aafe-188">[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="3aafe-188">[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




