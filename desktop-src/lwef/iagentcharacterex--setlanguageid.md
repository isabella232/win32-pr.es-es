---
title: IAgentCharacterEx SetLanguageID
description: IAgentCharacterEx SetLanguageID
ms.assetid: 064f4c3c-1871-4372-9796-5b53f05c6d9a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9ec8a396c174fd251b1cc7ac8d7e9696c9b9f2d1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774413"
---
# <a name="iagentcharacterexsetlanguageid"></a><span data-ttu-id="259be-103">IAgentCharacterEx::SetLanguageID</span><span class="sxs-lookup"><span data-stu-id="259be-103">IAgentCharacterEx::SetLanguageID</span></span>

<span data-ttu-id="259be-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="259be-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetLanguageID(
   long langID  // language ID setting of character
); 
```

<span data-ttu-id="259be-105">Establece el identificador de idioma establecido para el carácter.</span><span class="sxs-lookup"><span data-stu-id="259be-105">Sets the language ID set for the character.</span></span>

-   <span data-ttu-id="259be-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="259be-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="259be-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*ididioma*</span><span class="sxs-lookup"><span data-stu-id="259be-107"><span id="langID"></span><span id="langid"></span><span id="LANGID"></span>*langID*</span></span>
</dt> <dd>

<span data-ttu-id="259be-108">La configuración del identificador de idioma para el carácter.</span><span class="sxs-lookup"><span data-stu-id="259be-108">The language ID setting for the character.</span></span>

</dd> </dl>

<span data-ttu-id="259be-109">Entero largo que especifica el identificador de idioma del carácter.</span><span class="sxs-lookup"><span data-stu-id="259be-109">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="259be-110">El identificador de idioma (LANGID) de un carácter es un valor de 16 bits definido por Windows, que consta de un identificador de idioma principal y un identificador de idioma secundario.</span><span class="sxs-lookup"><span data-stu-id="259be-110">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="259be-111">Puede usar los siguientes valores para los idiomas especificados.</span><span class="sxs-lookup"><span data-stu-id="259be-111">You can use the following values for the specified languages.</span></span> <span data-ttu-id="259be-112">Para obtener más información, consulte la documentación del SDK de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="259be-112">For more information, see the Platform SDK documentation.</span></span>



|                       |        |                       |        |
|-----------------------|--------|-----------------------|--------|
| <span data-ttu-id="259be-113">Árabe (Arabia Saudí)</span><span class="sxs-lookup"><span data-stu-id="259be-113">Arabic (Saudi)</span></span>        | <span data-ttu-id="259be-114">0x0401</span><span class="sxs-lookup"><span data-stu-id="259be-114">0x0401</span></span> | <span data-ttu-id="259be-115">Italiano</span><span class="sxs-lookup"><span data-stu-id="259be-115">Italian</span></span>               | <span data-ttu-id="259be-116">0x0410</span><span class="sxs-lookup"><span data-stu-id="259be-116">0x0410</span></span> |
| <span data-ttu-id="259be-117">Vasco</span><span class="sxs-lookup"><span data-stu-id="259be-117">Basque</span></span>                | <span data-ttu-id="259be-118">0x042d</span><span class="sxs-lookup"><span data-stu-id="259be-118">0x042d</span></span> | <span data-ttu-id="259be-119">Japonés</span><span class="sxs-lookup"><span data-stu-id="259be-119">Japanese</span></span>              | <span data-ttu-id="259be-120">0x0411</span><span class="sxs-lookup"><span data-stu-id="259be-120">0x0411</span></span> |
| <span data-ttu-id="259be-121">Chino (simplificado)</span><span class="sxs-lookup"><span data-stu-id="259be-121">Chinese (Simplified)</span></span>  | <span data-ttu-id="259be-122">0x0804</span><span class="sxs-lookup"><span data-stu-id="259be-122">0x0804</span></span> | <span data-ttu-id="259be-123">Coreano</span><span class="sxs-lookup"><span data-stu-id="259be-123">Korean</span></span>                | <span data-ttu-id="259be-124">0x0412</span><span class="sxs-lookup"><span data-stu-id="259be-124">0x0412</span></span> |
| <span data-ttu-id="259be-125">Chino (tradicional)</span><span class="sxs-lookup"><span data-stu-id="259be-125">Chinese (Traditional)</span></span> | <span data-ttu-id="259be-126">0x0404</span><span class="sxs-lookup"><span data-stu-id="259be-126">0x0404</span></span> | <span data-ttu-id="259be-127">Noruego</span><span class="sxs-lookup"><span data-stu-id="259be-127">Norwegian</span></span>             | <span data-ttu-id="259be-128">0x0414</span><span class="sxs-lookup"><span data-stu-id="259be-128">0x0414</span></span> |
| <span data-ttu-id="259be-129">Croata</span><span class="sxs-lookup"><span data-stu-id="259be-129">Croatian</span></span>              | <span data-ttu-id="259be-130">0x041A</span><span class="sxs-lookup"><span data-stu-id="259be-130">0x041A</span></span> | <span data-ttu-id="259be-131">Polaco</span><span class="sxs-lookup"><span data-stu-id="259be-131">Polish</span></span>                | <span data-ttu-id="259be-132">0x0415</span><span class="sxs-lookup"><span data-stu-id="259be-132">0x0415</span></span> |
| <span data-ttu-id="259be-133">Checo</span><span class="sxs-lookup"><span data-stu-id="259be-133">Czech</span></span>                 | <span data-ttu-id="259be-134">0x0405</span><span class="sxs-lookup"><span data-stu-id="259be-134">0x0405</span></span> | <span data-ttu-id="259be-135">Portugués (Portugal)</span><span class="sxs-lookup"><span data-stu-id="259be-135">Portuguese (Portugal)</span></span> | <span data-ttu-id="259be-136">0x0816</span><span class="sxs-lookup"><span data-stu-id="259be-136">0x0816</span></span> |
| <span data-ttu-id="259be-137">Danés</span><span class="sxs-lookup"><span data-stu-id="259be-137">Danish</span></span>                | <span data-ttu-id="259be-138">0x0406</span><span class="sxs-lookup"><span data-stu-id="259be-138">0x0406</span></span> | <span data-ttu-id="259be-139">Portugués (Brasil)</span><span class="sxs-lookup"><span data-stu-id="259be-139">Portuguese (Brazil)</span></span>   | <span data-ttu-id="259be-140">0x0416</span><span class="sxs-lookup"><span data-stu-id="259be-140">0x0416</span></span> |
| <span data-ttu-id="259be-141">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="259be-141">Dutch</span></span>                 | <span data-ttu-id="259be-142">0x0413</span><span class="sxs-lookup"><span data-stu-id="259be-142">0x0413</span></span> | <span data-ttu-id="259be-143">Rumano</span><span class="sxs-lookup"><span data-stu-id="259be-143">Romanian</span></span>              | <span data-ttu-id="259be-144">0x0418</span><span class="sxs-lookup"><span data-stu-id="259be-144">0x0418</span></span> |
| <span data-ttu-id="259be-145">Inglés (Gran Bretaña)</span><span class="sxs-lookup"><span data-stu-id="259be-145">English (British)</span></span>     | <span data-ttu-id="259be-146">0x0809</span><span class="sxs-lookup"><span data-stu-id="259be-146">0x0809</span></span> | <span data-ttu-id="259be-147">Ruso</span><span class="sxs-lookup"><span data-stu-id="259be-147">Russian</span></span>               | <span data-ttu-id="259be-148">0x0419</span><span class="sxs-lookup"><span data-stu-id="259be-148">0x0419</span></span> |
| <span data-ttu-id="259be-149">Inglés (EE.UU.)</span><span class="sxs-lookup"><span data-stu-id="259be-149">English (US)</span></span>          | <span data-ttu-id="259be-150">0x0409</span><span class="sxs-lookup"><span data-stu-id="259be-150">0x0409</span></span> | <span data-ttu-id="259be-151">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="259be-151">Slovakian</span></span>             | <span data-ttu-id="259be-152">0x041B</span><span class="sxs-lookup"><span data-stu-id="259be-152">0x041B</span></span> |
| <span data-ttu-id="259be-153">Finés</span><span class="sxs-lookup"><span data-stu-id="259be-153">Finnish</span></span>               | <span data-ttu-id="259be-154">0x040B</span><span class="sxs-lookup"><span data-stu-id="259be-154">0x040B</span></span> | <span data-ttu-id="259be-155">Esloveno</span><span class="sxs-lookup"><span data-stu-id="259be-155">Slovenian</span></span>             | <span data-ttu-id="259be-156">0x0424</span><span class="sxs-lookup"><span data-stu-id="259be-156">0x0424</span></span> |
| <span data-ttu-id="259be-157">Francés</span><span class="sxs-lookup"><span data-stu-id="259be-157">French</span></span>                | <span data-ttu-id="259be-158">0x040C</span><span class="sxs-lookup"><span data-stu-id="259be-158">0x040C</span></span> | <span data-ttu-id="259be-159">Español</span><span class="sxs-lookup"><span data-stu-id="259be-159">Spanish</span></span>               | <span data-ttu-id="259be-160">0x0C0A</span><span class="sxs-lookup"><span data-stu-id="259be-160">0x0C0A</span></span> |
| <span data-ttu-id="259be-161">Alemán</span><span class="sxs-lookup"><span data-stu-id="259be-161">German</span></span>                | <span data-ttu-id="259be-162">0x0407</span><span class="sxs-lookup"><span data-stu-id="259be-162">0x0407</span></span> | <span data-ttu-id="259be-163">Sueco</span><span class="sxs-lookup"><span data-stu-id="259be-163">Swedish</span></span>               | <span data-ttu-id="259be-164">0x041D</span><span class="sxs-lookup"><span data-stu-id="259be-164">0x041D</span></span> |
| <span data-ttu-id="259be-165">Griego</span><span class="sxs-lookup"><span data-stu-id="259be-165">Greek</span></span>                 | <span data-ttu-id="259be-166">0x0408</span><span class="sxs-lookup"><span data-stu-id="259be-166">0x0408</span></span> | <span data-ttu-id="259be-167">Tailandés</span><span class="sxs-lookup"><span data-stu-id="259be-167">Thai</span></span>                  | <span data-ttu-id="259be-168">0x041E</span><span class="sxs-lookup"><span data-stu-id="259be-168">0x041E</span></span> |
| <span data-ttu-id="259be-169">Hebreo</span><span class="sxs-lookup"><span data-stu-id="259be-169">Hebrew</span></span>                | <span data-ttu-id="259be-170">0x040D</span><span class="sxs-lookup"><span data-stu-id="259be-170">0x040D</span></span> | <span data-ttu-id="259be-171">Turco</span><span class="sxs-lookup"><span data-stu-id="259be-171">Turkish</span></span>               | <span data-ttu-id="259be-172">0x041F</span><span class="sxs-lookup"><span data-stu-id="259be-172">0x041F</span></span> |
| <span data-ttu-id="259be-173">Húngaro</span><span class="sxs-lookup"><span data-stu-id="259be-173">Hungarian</span></span>             | <span data-ttu-id="259be-174">0x040E</span><span class="sxs-lookup"><span data-stu-id="259be-174">0x040E</span></span> |                       |        |



 

<span data-ttu-id="259be-175">Si no establece el identificador de idioma para el carácter, su ID. de idioma será el ID. de idioma actual del sistema si está instalado el archivo DLL correspondiente del idioma del agente; de lo contrario, el idioma del carácter será inglés (EE. UU.).</span><span class="sxs-lookup"><span data-stu-id="259be-175">If you do not set the language ID for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed; otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="259be-176">Esta propiedad también determina el idioma del texto del globo de palabras, los comandos del menú emergente del carácter y el motor de reconocimiento de voz.</span><span class="sxs-lookup"><span data-stu-id="259be-176">This property also determines the language for the word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="259be-177">También determina el idioma predeterminado para la salida de TTS.</span><span class="sxs-lookup"><span data-stu-id="259be-177">It also determines the default language for TTS output.</span></span> <span data-ttu-id="259be-178">Para determinar si hay un motor de voz compatible disponible para el idioma del carácter, use [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md) o [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span><span class="sxs-lookup"><span data-stu-id="259be-178">To determine if there is a compatible speech engine available for the character's language, use [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md) or [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md).</span></span>

<span data-ttu-id="259be-179">Si intenta establecer el identificador de idioma para un carácter y los recursos de idioma del agente, la página de códigos o una fuente de presentación para el ID. de idioma no está disponible, el agente devuelve un error y el identificador de idioma del carácter permanece en su última configuración.</span><span class="sxs-lookup"><span data-stu-id="259be-179">If you try to set the language ID for a character and the Agent language resources, the code page, or a display font for the language ID is not available, Agent returns an error and the character's language ID remains at its last setting.</span></span> <span data-ttu-id="259be-180">Si se establece esta propiedad, no se devuelve un error si no hay ningún motor de voz coincidente para el idioma.</span><span class="sxs-lookup"><span data-stu-id="259be-180">Setting this property does not return an error if there are no matching speech engines for the language.</span></span>

<span data-ttu-id="259be-181">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="259be-181">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="259be-182">Si establece el identificador de idioma del carácter en un idioma que admite texto bidireccional (como el árabe o el hebreo), pero el sistema que ejecuta la aplicación no tiene instalada la compatibilidad bidireccional, el texto aparecerá en el globo de palabras en lugar de en el orden de presentación.</span><span class="sxs-lookup"><span data-stu-id="259be-182">If you set the character's language ID to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text will appear in the word balloon in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="259be-183">Consulte también</span><span class="sxs-lookup"><span data-stu-id="259be-183">See Also</span></span>

<span data-ttu-id="259be-184">[**IAgentCharacterEx: GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx:: GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx:: GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span><span class="sxs-lookup"><span data-stu-id="259be-184">[**IAgentCharacterEx:GetLanguageID**](iagentcharacterex--getlanguageid.md), [**IAgentCharacterEx::GetSRModeID**](iagentcharacterex--getsrmodeid.md), [**IAgentCharacterEx::GetTTSModeID**](iagentcharacterex--getttsmodeid.md)</span></span>


 

 




