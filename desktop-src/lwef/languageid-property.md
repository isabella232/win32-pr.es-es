---
title: LanguageID (propiedad)
description: LanguageID (propiedad)
ms.assetid: f57b0fa1-b3b8-49c8-b441-2a40e564d6ea
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a7a10e6b16f9e35b223bada728871d253685538
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357602"
---
# <a name="languageid-property"></a><span data-ttu-id="0910f-103">LanguageID (propiedad)</span><span class="sxs-lookup"><span data-stu-id="0910f-103">LanguageID Property</span></span>

<span data-ttu-id="0910f-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="0910f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

<dl> <dt>

<span data-ttu-id="0910f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Denominación**</span><span class="sxs-lookup"><span data-stu-id="0910f-105"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="0910f-106">Devuelve o establece el identificador de idioma del carácter.</span><span class="sxs-lookup"><span data-stu-id="0910f-106">Returns or sets the language ID for the character.</span></span>

</dd> <dt>

<span data-ttu-id="0910f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Sintáctica**</span><span class="sxs-lookup"><span data-stu-id="0910f-107"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="0910f-108">Caracteres del agente \*. \* \* \*\* \*  **("***CharacterID***"). LanguageID** \[  =  *LanguageID*\]</span><span class="sxs-lookup"><span data-stu-id="0910f-108">*agent.\*\*\*Characters*\* **("***CharacterID***").LanguageID** \[ = *LanguageID*\]</span></span>



<span data-ttu-id="0910f-109">Parte</span><span class="sxs-lookup"><span data-stu-id="0910f-109">Part</span></span>

<span data-ttu-id="0910f-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="0910f-110">Description</span></span>

<span data-ttu-id="0910f-111">LanguageID</span><span class="sxs-lookup"><span data-stu-id="0910f-111">LanguageID</span></span>

<span data-ttu-id="0910f-112">Entero largo que especifica el identificador de idioma del carácter.</span><span class="sxs-lookup"><span data-stu-id="0910f-112">A Long integer specifying the language ID for the character.</span></span> <span data-ttu-id="0910f-113">El identificador de idioma (LANGID) de un carácter es un valor de 16 bits definido por Windows, que consta de un identificador de idioma principal y un identificador de idioma secundario.</span><span class="sxs-lookup"><span data-stu-id="0910f-113">The language ID (LANGID) for a character is a 16-bit value defined by Windows, consisting of a primary language ID and a secondary language ID.</span></span> <span data-ttu-id="0910f-114">Los ejemplos siguientes son valores de idiomas admitidos por el agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="0910f-114">The following examples are values for languages supported by Microsoft Agent.</span></span> <span data-ttu-id="0910f-115">Para determinar el valor de otros lenguajes, consulte la *documentación del SDK* de la plataforma.</span><span class="sxs-lookup"><span data-stu-id="0910f-115">To determine the value for other languages, see the *Platform SDK documentation*.</span></span>

 

<span data-ttu-id="0910f-116">Árabe</span><span class="sxs-lookup"><span data-stu-id="0910f-116">Arabic</span></span>

<span data-ttu-id="0910f-117">&H0401</span><span class="sxs-lookup"><span data-stu-id="0910f-117">&H0401</span></span>

<span data-ttu-id="0910f-118">Italiano</span><span class="sxs-lookup"><span data-stu-id="0910f-118">Italian</span></span>

<span data-ttu-id="0910f-119">&H0410</span><span class="sxs-lookup"><span data-stu-id="0910f-119">&H0410</span></span>

 

<span data-ttu-id="0910f-120">Vasco</span><span class="sxs-lookup"><span data-stu-id="0910f-120">Basque</span></span>

<span data-ttu-id="0910f-121">&H042D</span><span class="sxs-lookup"><span data-stu-id="0910f-121">&H042D</span></span>

<span data-ttu-id="0910f-122">Japonés</span><span class="sxs-lookup"><span data-stu-id="0910f-122">Japanese</span></span>

<span data-ttu-id="0910f-123">&H0411</span><span class="sxs-lookup"><span data-stu-id="0910f-123">&H0411</span></span>

 

<span data-ttu-id="0910f-124">Chino (simplificado)</span><span class="sxs-lookup"><span data-stu-id="0910f-124">Chinese (Simplified)</span></span>

<span data-ttu-id="0910f-125">&H0804</span><span class="sxs-lookup"><span data-stu-id="0910f-125">&H0804</span></span>

<span data-ttu-id="0910f-126">Coreano</span><span class="sxs-lookup"><span data-stu-id="0910f-126">Korean</span></span>

<span data-ttu-id="0910f-127">&H0412</span><span class="sxs-lookup"><span data-stu-id="0910f-127">&H0412</span></span>

 

<span data-ttu-id="0910f-128">Chino (tradicional)</span><span class="sxs-lookup"><span data-stu-id="0910f-128">Chinese (Traditional)</span></span>

<span data-ttu-id="0910f-129">&H0404</span><span class="sxs-lookup"><span data-stu-id="0910f-129">&H0404</span></span>

<span data-ttu-id="0910f-130">Noruego</span><span class="sxs-lookup"><span data-stu-id="0910f-130">Norwegian</span></span>

<span data-ttu-id="0910f-131">&H0414</span><span class="sxs-lookup"><span data-stu-id="0910f-131">&H0414</span></span>

 

<span data-ttu-id="0910f-132">Croata</span><span class="sxs-lookup"><span data-stu-id="0910f-132">Croatian</span></span>

<span data-ttu-id="0910f-133">&H041A</span><span class="sxs-lookup"><span data-stu-id="0910f-133">&H041A</span></span>

<span data-ttu-id="0910f-134">Polaco</span><span class="sxs-lookup"><span data-stu-id="0910f-134">Polish</span></span>

<span data-ttu-id="0910f-135">&H0415</span><span class="sxs-lookup"><span data-stu-id="0910f-135">&H0415</span></span>

 

<span data-ttu-id="0910f-136">Checo</span><span class="sxs-lookup"><span data-stu-id="0910f-136">Czech</span></span>

<span data-ttu-id="0910f-137">&H0405</span><span class="sxs-lookup"><span data-stu-id="0910f-137">&H0405</span></span>

<span data-ttu-id="0910f-138">Portugués (Portugal)</span><span class="sxs-lookup"><span data-stu-id="0910f-138">Portuguese (Portugal)</span></span>

<span data-ttu-id="0910f-139">&H0816</span><span class="sxs-lookup"><span data-stu-id="0910f-139">&H0816</span></span>

 

<span data-ttu-id="0910f-140">Danés</span><span class="sxs-lookup"><span data-stu-id="0910f-140">Danish</span></span>

<span data-ttu-id="0910f-141">&H0406</span><span class="sxs-lookup"><span data-stu-id="0910f-141">&H0406</span></span>

<span data-ttu-id="0910f-142">Portugués (Brasil)</span><span class="sxs-lookup"><span data-stu-id="0910f-142">Portuguese (Brazil)</span></span>

<span data-ttu-id="0910f-143">&H0416</span><span class="sxs-lookup"><span data-stu-id="0910f-143">&H0416</span></span>

 

<span data-ttu-id="0910f-144">Neerlandés</span><span class="sxs-lookup"><span data-stu-id="0910f-144">Dutch</span></span>

<span data-ttu-id="0910f-145">&H0413</span><span class="sxs-lookup"><span data-stu-id="0910f-145">&H0413</span></span>

<span data-ttu-id="0910f-146">Rumano</span><span class="sxs-lookup"><span data-stu-id="0910f-146">Romanian</span></span>

<span data-ttu-id="0910f-147">&H0418</span><span class="sxs-lookup"><span data-stu-id="0910f-147">&H0418</span></span>

 

<span data-ttu-id="0910f-148">Inglés (Gran Bretaña)</span><span class="sxs-lookup"><span data-stu-id="0910f-148">English (British)</span></span>

<span data-ttu-id="0910f-149">&H0809</span><span class="sxs-lookup"><span data-stu-id="0910f-149">&H0809</span></span>

<span data-ttu-id="0910f-150">Ruso</span><span class="sxs-lookup"><span data-stu-id="0910f-150">Russian</span></span>

<span data-ttu-id="0910f-151">&H0419</span><span class="sxs-lookup"><span data-stu-id="0910f-151">&H0419</span></span>

 

<span data-ttu-id="0910f-152">Inglés (EE.UU.)</span><span class="sxs-lookup"><span data-stu-id="0910f-152">English (US)</span></span>

<span data-ttu-id="0910f-153">&H0409</span><span class="sxs-lookup"><span data-stu-id="0910f-153">&H0409</span></span>

<span data-ttu-id="0910f-154">Eslovaco</span><span class="sxs-lookup"><span data-stu-id="0910f-154">Slovakian</span></span>

<span data-ttu-id="0910f-155">&H041B</span><span class="sxs-lookup"><span data-stu-id="0910f-155">&H041B</span></span>

 

<span data-ttu-id="0910f-156">Finés</span><span class="sxs-lookup"><span data-stu-id="0910f-156">Finnish</span></span>

<span data-ttu-id="0910f-157">&H040B</span><span class="sxs-lookup"><span data-stu-id="0910f-157">&H040B</span></span>

<span data-ttu-id="0910f-158">Esloveno</span><span class="sxs-lookup"><span data-stu-id="0910f-158">Slovenian</span></span>

<span data-ttu-id="0910f-159">&H0424</span><span class="sxs-lookup"><span data-stu-id="0910f-159">&H0424</span></span>

 

<span data-ttu-id="0910f-160">Francés</span><span class="sxs-lookup"><span data-stu-id="0910f-160">French</span></span>

<span data-ttu-id="0910f-161">&H040C</span><span class="sxs-lookup"><span data-stu-id="0910f-161">&H040C</span></span>

<span data-ttu-id="0910f-162">Español</span><span class="sxs-lookup"><span data-stu-id="0910f-162">Spanish</span></span>

<span data-ttu-id="0910f-163">&H0C0A</span><span class="sxs-lookup"><span data-stu-id="0910f-163">&H0C0A</span></span>

 

<span data-ttu-id="0910f-164">Alemán</span><span class="sxs-lookup"><span data-stu-id="0910f-164">German</span></span>

<span data-ttu-id="0910f-165">&H0407</span><span class="sxs-lookup"><span data-stu-id="0910f-165">&H0407</span></span>

<span data-ttu-id="0910f-166">Sueco</span><span class="sxs-lookup"><span data-stu-id="0910f-166">Swedish</span></span>

<span data-ttu-id="0910f-167">&H041D</span><span class="sxs-lookup"><span data-stu-id="0910f-167">&H041D</span></span>

 

<span data-ttu-id="0910f-168">Griego</span><span class="sxs-lookup"><span data-stu-id="0910f-168">Greek</span></span>

<span data-ttu-id="0910f-169">&H0408</span><span class="sxs-lookup"><span data-stu-id="0910f-169">&H0408</span></span>

<span data-ttu-id="0910f-170">Tailandés</span><span class="sxs-lookup"><span data-stu-id="0910f-170">Thai</span></span>

<span data-ttu-id="0910f-171">&H041E</span><span class="sxs-lookup"><span data-stu-id="0910f-171">&H041E</span></span>

 

<span data-ttu-id="0910f-172">Hebreo</span><span class="sxs-lookup"><span data-stu-id="0910f-172">Hebrew</span></span>

<span data-ttu-id="0910f-173">&H040D</span><span class="sxs-lookup"><span data-stu-id="0910f-173">&H040D</span></span>

<span data-ttu-id="0910f-174">Turco</span><span class="sxs-lookup"><span data-stu-id="0910f-174">Turkish</span></span>

<span data-ttu-id="0910f-175">&H041F</span><span class="sxs-lookup"><span data-stu-id="0910f-175">&H041F</span></span>

 

<span data-ttu-id="0910f-176">Húngaro</span><span class="sxs-lookup"><span data-stu-id="0910f-176">Hungarian</span></span>

<span data-ttu-id="0910f-177">&H040E</span><span class="sxs-lookup"><span data-stu-id="0910f-177">&H040E</span></span>

 

 



 

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="0910f-178">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0910f-178">Remarks</span></span>

<span data-ttu-id="0910f-179">Si no establece el **iddeidioma** para el carácter, su identificador de idioma será el identificador de idioma del sistema actual si se instala la dll de idioma correspondiente del agente; de lo contrario, el idioma del carácter será inglés (EE. UU.).</span><span class="sxs-lookup"><span data-stu-id="0910f-179">If you do not set the **LanguageID** for the character, its language ID will be the current system language ID if the corresponding Agent language DLL is installed, otherwise, the character's language will be English (US).</span></span>

<span data-ttu-id="0910f-180">Esta propiedad también determina el idioma del texto del globo de palabras, los comandos del menú emergente del carácter y el motor de reconocimiento de voz.</span><span class="sxs-lookup"><span data-stu-id="0910f-180">This property also determines the language for word balloon text, the commands in the character's pop-up menu, and the speech recognition engine.</span></span> <span data-ttu-id="0910f-181">También determina el idioma predeterminado para la salida de TTS.</span><span class="sxs-lookup"><span data-stu-id="0910f-181">It also determines the default language for TTS output.</span></span>

<span data-ttu-id="0910f-182">Si intenta establecer el **LanguageID** para un carácter y el archivo DLL del idioma del agente para ese idioma no está instalado o si no hay disponible una fuente de presentación para el ID. de idioma, el agente genera un error y se mantiene el valor **LanguageID** en la última configuración.</span><span class="sxs-lookup"><span data-stu-id="0910f-182">If you try to set the **LanguageID** for a character and the Agent language DLL for that language is not installed or a display font for the language ID is not available, Agent raises an error and **LanguageID** remains at its last setting.</span></span>

<span data-ttu-id="0910f-183">Si se establece esta propiedad, no se produce un error si no hay ningún motor de voz coincidente para el idioma.</span><span class="sxs-lookup"><span data-stu-id="0910f-183">Setting this property does not raise an error if there are no matching speech engines for the language.</span></span> <span data-ttu-id="0910f-184">Para determinar si hay un motor de voz compatible disponible para el **iddeidioma**, consulte [**SRModeID**](srmodeid-property.md) o [**TTSModeID**](ttsmodeid-property.md).</span><span class="sxs-lookup"><span data-stu-id="0910f-184">To determine if there is a compatible speech engine available for the **LanguageID**, check [**SRModeID**](srmodeid-property.md) or [**TTSModeID**](ttsmodeid-property.md).</span></span> <span data-ttu-id="0910f-185">Si no establece **LanguageID**, se establecerá en la configuración de ID. de idioma predeterminado del usuario.</span><span class="sxs-lookup"><span data-stu-id="0910f-185">If you do not set **LanguageID**, it will be set to the user default language ID setting.</span></span>

<span data-ttu-id="0910f-186">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="0910f-186">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

> [!Note]  
> <span data-ttu-id="0910f-187">Si establece **LanguageID** en un idioma que admite texto bidireccional (como el árabe o el hebreo), pero el sistema que ejecuta la aplicación no tiene instalada la compatibilidad bidireccional, el texto del globo de palabras aparecerá en lugar lógico en lugar de mostrarse en orden.</span><span class="sxs-lookup"><span data-stu-id="0910f-187">If you set **LanguageID** to a language that supports bidirectional text (such as Arabic or Hebrew), but the system running your application does not have bidirectional support installed, text in the word balloon will appear in logical rather than display order.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="0910f-188">Consulte también</span><span class="sxs-lookup"><span data-stu-id="0910f-188">See Also</span></span>

<span data-ttu-id="0910f-189">[**Propiedad SRModeID**](srmodeid-property.md), [ **propiedad TTSModeID**](ttsmodeid-property.md)</span><span class="sxs-lookup"><span data-stu-id="0910f-189">[**SRModeID property**](srmodeid-property.md), [**TTSModeID property**](ttsmodeid-property.md)</span></span>


 

 




