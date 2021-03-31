---
title: IAgentCharacterEx GetTTSModeID
description: IAgentCharacterEx GetTTSModeID
ms.assetid: e7b3c576-dc3c-40de-8d09-8e7f4b79250b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62a77e78755345c0993ed5723080b0b3f4b8297a
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104077393"
---
# <a name="iagentcharacterexgetttsmodeid"></a><span data-ttu-id="99c50-103">IAgentCharacterEx::GetTTSModeID</span><span class="sxs-lookup"><span data-stu-id="99c50-103">IAgentCharacterEx::GetTTSModeID</span></span>

<span data-ttu-id="99c50-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="99c50-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetTTSModeID(
   BSTR * pbszModeID  // address of TTS engine ID
);
```

<span data-ttu-id="99c50-105">Recupera el identificador de modo del conjunto de motores TTS para el carácter.</span><span class="sxs-lookup"><span data-stu-id="99c50-105">Retrieves the mode ID of the TTS engine set for the character.</span></span>

-   <span data-ttu-id="99c50-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="99c50-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="99c50-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span><span class="sxs-lookup"><span data-stu-id="99c50-107"><span id="pbszModeID"></span><span id="pbszmodeid"></span><span id="PBSZMODEID"></span>*pbszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="99c50-108">Dirección de un BSTR que recibe la configuración de ID. de modo del motor TTS para el carácter.</span><span class="sxs-lookup"><span data-stu-id="99c50-108">Address of a BSTR that receives the mode ID setting of the TTS engine for the character.</span></span>

</dd> </dl>

<span data-ttu-id="99c50-109">Esta configuración devuelve el identificador del modo de motor de TTS (texto a voz) de la salida hablada de un carácter.</span><span class="sxs-lookup"><span data-stu-id="99c50-109">This setting returns the TTS (text-to-speech) engine mode ID for a character's spoken output.</span></span> <span data-ttu-id="99c50-110">El identificador de modo de un motor TTS es una representación de cadena del GUID (con formato con llaves y guiones) definida por el proveedor de voz que identifica de forma única al motor.</span><span class="sxs-lookup"><span data-stu-id="99c50-110">The mode ID for a TTS engine is a string representation of the GUID (formatted with braces and dashes) defined by the speech vendor uniquely identifying the engine.</span></span> <span data-ttu-id="99c50-111">Para obtener más información, consulte la [documentación del SDK de Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="99c50-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span> <span data-ttu-id="99c50-112">Si se consulta esta propiedad, se cargará el motor asociado si aún no está cargado.</span><span class="sxs-lookup"><span data-stu-id="99c50-112">Querying this property will load the associated engine if it is not already loaded.</span></span>

<span data-ttu-id="99c50-113">Si no establece un identificador de modo de motor TTS para el carácter, el servidor intenta devolver un motor que coincide con (mediante interfaces de Microsoft Speech API) la configuración de TTS compilada del carácter y la configuración de idioma actual del carácter.</span><span class="sxs-lookup"><span data-stu-id="99c50-113">If you do not set a TTS engine mode ID for the character, the server attempts to return an engine that matches (using Microsoft Speech API interfaces) the character's compiled TTS setting and the character's current language setting.</span></span> <span data-ttu-id="99c50-114">Si son diferentes, la configuración de idioma del carácter invalida la configuración de modo creado.</span><span class="sxs-lookup"><span data-stu-id="99c50-114">If these are different, then the character's language setting overrides its authored mode setting.</span></span> <span data-ttu-id="99c50-115">Si no ha establecido la configuración de idioma del carácter, el idioma del carácter es el ID. de idioma predeterminado del usuario y el servidor intenta la coincidencia en función de ese identificador de idioma.</span><span class="sxs-lookup"><span data-stu-id="99c50-115">If you have not set the character's language setting, the character's language is the user default language ID, and the server attempts the match based on that language ID.</span></span>

<span data-ttu-id="99c50-116">Esta función no genera un error si [**IAgentAudioObjectProperties:: GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) devuelve **false**.</span><span class="sxs-lookup"><span data-stu-id="99c50-116">This function does not fail if the [**IAgentAudioObjectProperties::GetEnabled**](https://www.bing.com/search?q=**IAgentAudioObjectProperties::GetEnabled**) returns **False**.</span></span>

<span data-ttu-id="99c50-117">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="99c50-117">This property applies only to your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="99c50-118">Los requisitos del motor de voz de Microsoft Agent se basan en Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="99c50-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="99c50-119">Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el agente.</span><span class="sxs-lookup"><span data-stu-id="99c50-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="99c50-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="99c50-120">See Also</span></span>

[<span data-ttu-id="99c50-121">**IAgentCharacterEx::SetTTSModeID**</span><span class="sxs-lookup"><span data-stu-id="99c50-121">**IAgentCharacterEx::SetTTSModeID**</span></span>](iagentcharacterex--setttsmodeid.md)


 

 




