---
title: IAgentCharacterEx SetTTSModeID
description: IAgentCharacterEx SetTTSModeID
ms.assetid: 66ed792a-1693-45dc-b9a8-eebe772c5af9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34392e65fcb8f3a46db6251f01f59ad76aba278d
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/20/2020
ms.locfileid: "104420371"
---
# <a name="iagentcharacterexsetttsmodeid"></a><span data-ttu-id="3cd5b-103">IAgentCharacterEx::SetTTSModeID</span><span class="sxs-lookup"><span data-stu-id="3cd5b-103">IAgentCharacterEx::SetTTSModeID</span></span>

<span data-ttu-id="3cd5b-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="3cd5b-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetTTSModeID(
   BSTR bszModeID  // TTS engine ID
);
```

<span data-ttu-id="3cd5b-105">Establece el identificador de modo del conjunto de motores TTS para el carácter.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-105">Sets the mode ID of the TTS engine set for the character.</span></span>

-   <span data-ttu-id="3cd5b-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="3cd5b-107"><span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*</span><span class="sxs-lookup"><span data-stu-id="3cd5b-107"><span id="bszModeID"></span><span id="bszmodeid"></span><span id="BSZMODEID"></span>*bszModeID*</span></span>
</dt> <dd>

<span data-ttu-id="3cd5b-108">La configuración del identificador de modo del motor TTS para el carácter.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-108">The mode ID setting of the TTS engine for the character.</span></span>

> [!Note]  
> <span data-ttu-id="3cd5b-109">**IAgentCharacterEx: SetTTSModeID** puede producir un error si Speech.dll no está instalado y el motor especificado no coincide con la configuración de modo TTS compilado del carácter.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-109">**IAgentCharacterEx:SetTTSModeID** can fail if Speech.dll is not installed and the engine you specify does not match the character's compiled TTS mode setting.</span></span>

 

</dd> </dl>

<span data-ttu-id="3cd5b-110">Esta configuración determina el modo de motor preferido para la salida de voz oral de un carácter.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-110">This setting determines the preferred engine mode for a character's spoken TTS output.</span></span> <span data-ttu-id="3cd5b-111">El identificador de modo de un motor de conversión de texto a voz es el GUID definido por el proveedor de voz que identifica de forma única el modo del motor (con formato de llaves y guiones).</span><span class="sxs-lookup"><span data-stu-id="3cd5b-111">The mode ID for a TTS (text-to-speech) engine is the GUID defined by the speech vendor that uniquely identifies the mode of the engine (formatted with braces and dashes).</span></span> <span data-ttu-id="3cd5b-112">Para obtener más información, consulte la [documentación del SDK de Microsoft Speech](https://msdn.microsoft.com/library/ee705648.aspx).</span><span class="sxs-lookup"><span data-stu-id="3cd5b-112">For more information, see the [Microsoft Speech SDK documentation](https://msdn.microsoft.com/library/ee705648.aspx).</span></span>

<span data-ttu-id="3cd5b-113">Si establece un identificador de modo TTS, invalida el intento del servidor de hacer coincidir un motor de voz basado en el identificador del modo TTS compilado del carácter, el ID. de idioma actual del sistema y el ID. de idioma actual del carácter.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-113">If you set a TTS mode ID, it overrides the server attempt to match a speech engine based on the character's compiled TTS mode ID, the current system language ID, and the character's current language ID.</span></span> <span data-ttu-id="3cd5b-114">Sin embargo, si intenta establecer un identificador de modo cuando el usuario ha deshabilitado la salida de voz en la hoja de propiedades del agente de Microsoft o cuando el motor asociado no está instalado, se producirá un error en esta llamada.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-114">However, if you attempt to set a mode ID when the user has disabled speech output in the Microsoft Agent property sheet or when the associated engine is not installed, this call will fail.</span></span>

<span data-ttu-id="3cd5b-115">Si no establece un identificador de modo de motor TTS para el carácter, el servidor establece un motor que coincide con la configuración de idioma del carácter (mediante interfaces de Microsoft Speech API).</span><span class="sxs-lookup"><span data-stu-id="3cd5b-115">If you do not set a TTS engine mode ID for the character, the server sets an engine that matches the character's language setting (using Microsoft Speech API interfaces).</span></span> <span data-ttu-id="3cd5b-116">Al establecer esta propiedad, se cargará el motor asociado si aún no está cargado.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-116">Setting this property will load the associated engine if it is not already loaded.</span></span>

<span data-ttu-id="3cd5b-117">Esta propiedad solo se aplica al uso de la aplicación cliente del carácter; la configuración no afecta a otros clientes del carácter u otros caracteres de la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-117">This property applies to only your client application's use of the character; the setting does not affect other clients of the character or other characters of your client application.</span></span>

<span data-ttu-id="3cd5b-118">Los requisitos del motor de voz de Microsoft Agent se basan en Microsoft Speech API.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-118">Microsoft Agent's speech engine requirements are based on the Microsoft Speech API.</span></span> <span data-ttu-id="3cd5b-119">Los motores que admiten los requisitos de SAPI de Microsoft Agent se pueden instalar y usar con el agente.</span><span class="sxs-lookup"><span data-stu-id="3cd5b-119">Engines supporting Microsoft Agent's SAPI requirements can be installed and used with Agent.</span></span>

## <a name="see-also"></a><span data-ttu-id="3cd5b-120">Consulte también</span><span class="sxs-lookup"><span data-stu-id="3cd5b-120">See Also</span></span>

[<span data-ttu-id="3cd5b-121">**IAgentCharacterEx:GetTTSModeID**</span><span class="sxs-lookup"><span data-stu-id="3cd5b-121">**IAgentCharacterEx:GetTTSModeID**</span></span>](iagentcharacterex--getttsmodeid.md)


 

 




