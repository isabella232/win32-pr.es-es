---
title: IAgentCharacterEx SetSRModeID
description: IAgentCharacterEx SetSRModeID
ms.assetid: 8f9072ec-1f64-4f5c-972d-cd6799ce028c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 390d7e0126fe5ef62273cf6d7d23ada25c26bbdb
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104487291"
---
# <a name="iagentcharacterexsetsrmodeid"></a><span data-ttu-id="a5e4f-103">IAgentCharacterEx::SetSRModeID</span><span class="sxs-lookup"><span data-stu-id="a5e4f-103">IAgentCharacterEx::SetSRModeID</span></span>

<span data-ttu-id="a5e4f-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="a5e4f-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetSRModeID(
   BSTR bszModeID  // speech recognition engine ID
);
```

<span data-ttu-id="a5e4f-105">Establece el identificador de modo del conjunto de motores de reconocimiento de voz para el carácter.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-105">Sets the mode ID of the speech recognition engine set for the character.</span></span>

-   <span data-ttu-id="a5e4f-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-106">Returns S\_OK to indicate the operation was successful.</span></span>

<span data-ttu-id="a5e4f-107">bszModeID</span><span class="sxs-lookup"><span data-stu-id="a5e4f-107">bszModeID</span></span>

<span data-ttu-id="a5e4f-108">La configuración del identificador de modo del motor de reconocimiento de voz para el carácter.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-108">The mode ID setting of the speech recognition engine for the character.</span></span>

<span data-ttu-id="a5e4f-109">Esta configuración establece el motor para la entrada de voz de un carácter.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-109">This setting sets the engine for a character's speech input.</span></span> <span data-ttu-id="a5e4f-110">El identificador de modo de un motor de reconocimiento de voz es el GUID definido por el proveedor de voz que identifica de forma única el modo del motor (con formato de llaves y guiones).</span><span class="sxs-lookup"><span data-stu-id="a5e4f-110">The mode ID for a speech recognition engine is the GUID defined by the speech vendor that uniquely identifies the engine's mode (formatted with braces and dashes).</span></span> <span data-ttu-id="a5e4f-111">Para obtener más información, consulte la [documentación del SDK de Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="a5e4f-111">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="a5e4f-112">Si especifica un identificador de modo que no coincide con la configuración de idioma del carácter, si el usuario ha deshabilitado el reconocimiento de voz (en la hoja de propiedades del agente de Microsoft) o si el motor no está instalado, se producirá un error en esta llamada.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-112">If you specify a mode ID that does not match the character's language setting, if the user has disabled speech recognition (in the Microsoft Agent property sheet), or the engine is not installed, this call will fail.</span></span> <span data-ttu-id="a5e4f-113">Si no establece un identificador de modo de motor de reconocimiento de voz para el carácter, el servidor establece uno que coincida con la configuración de idioma del carácter (mediante interfaces de Microsoft Speech API).</span><span class="sxs-lookup"><span data-stu-id="a5e4f-113">If you do not set a speech recognition engine mode ID for the character, the server sets one that matches the character's language setting (using Microsoft Speech API interfaces).</span></span>

<span data-ttu-id="a5e4f-114">Cuando la entrada de voz está habilitada en la hoja de propiedades del agente (opciones avanzadas de caracteres), al establecer esta propiedad se cargará el motor asociado (si aún no está cargado) e iniciará servicios de voz.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-114">When speech input is enabled in the Agent property sheet (Advanced Character Options), setting this property will load the associated engine (if it is not already loaded), and start speech services.</span></span> <span data-ttu-id="a5e4f-115">Es decir, la clave de escucha está disponible y la sugerencia de escucha es visible.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-115">That is, the Listening key is available, and the Listening Tip is displayable.</span></span> <span data-ttu-id="a5e4f-116">(La clave de escucha y la sugerencia de escucha solo están habilitadas si también están habilitadas en opciones de caracteres avanzadas). Sin embargo, si consulta la propiedad cuando la voz está deshabilitada, el servidor no inicia Speech Services.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-116">(The Listening key and Listening tip are enabled only if they are also enabled in Advanced Character Options.) However, if you query the property when speech is disabled, the server does not start speech services.</span></span>

<span data-ttu-id="a5e4f-117">Esta propiedad solo se aplica al cliente del carácter; la configuración no refleja la configuración de otros clientes del carácter u otros caracteres del cliente.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-117">This property applies to only the client of the character; the setting does not reflect the setting for other clients of the character or other characters of the client.</span></span>

<span data-ttu-id="a5e4f-118">Los requisitos del motor de voz de Microsoft Agent se basan en Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="a5e4f-119">Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el agente.</span><span class="sxs-lookup"><span data-stu-id="a5e4f-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="a5e4f-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="a5e4f-120">See Also</span></span>

[<span data-ttu-id="a5e4f-121">**IAgentCharacterEx::GetSRModeID**</span><span class="sxs-lookup"><span data-stu-id="a5e4f-121">**IAgentCharacterEx::GetSRModeID**</span></span>](iagentcharacterex--getsrmodeid.md)


 

 




