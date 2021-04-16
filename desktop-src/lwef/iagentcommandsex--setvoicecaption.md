---
title: IAgentCommandsEx SetVoiceCaption
description: IAgentCommandsEx SetVoiceCaption
ms.assetid: f13c9ca5-70c9-42d0-b53c-45dc8980a24c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19fcc0f3ce98ff0187b7ed2f01b7131cc8e101bd
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105714370"
---
# <a name="iagentcommandsexsetvoicecaption"></a><span data-ttu-id="28a7a-103">IAgentCommandsEx::SetVoiceCaption</span><span class="sxs-lookup"><span data-stu-id="28a7a-103">IAgentCommandsEx::SetVoiceCaption</span></span>

<span data-ttu-id="28a7a-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="28a7a-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVoiceCaption(
   BSTR bszVoiceCaption  // voice caption text
);
```

<span data-ttu-id="28a7a-105">Establece el texto [**VoiceCaption**](voicecaption-property.md) que se muestra para el objeto de [**comando**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="28a7a-105">Sets the [**VoiceCaption**](voicecaption-property.md) text displayed for the [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="28a7a-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="28a7a-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="28a7a-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span><span class="sxs-lookup"><span data-stu-id="28a7a-107"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="28a7a-108">BSTR que especifica el texto de la propiedad [**VoiceCaption**](voicecaption-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="28a7a-108">A BSTR that specifies the text for the [**VoiceCaption**](voicecaption-property.md) property for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="28a7a-109">Si define un objeto de [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) y establece su propiedad [**Voice**](voice-property.md) , normalmente también establecerá su propiedad [**VoiceCaption**](voicecaption-property.md) .</span><span class="sxs-lookup"><span data-stu-id="28a7a-109">If you define a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection and set its [**Voice**](voice-property.md) property, you will typically also set its [**VoiceCaption**](voicecaption-property.md) property.</span></span> <span data-ttu-id="28a7a-110">Este texto aparecerá en la ventana comandos de voz cuando la aplicación cliente sea de entrada-activa y el carácter esté visible.</span><span class="sxs-lookup"><span data-stu-id="28a7a-110">This text will appear in the Voice Commands Window when your client application is input-active and the character is visible.</span></span> <span data-ttu-id="28a7a-111">Si no se establece esta propiedad, el valor de la propiedad [**Caption**](caption-property.md) determina el texto que se muestra.</span><span class="sxs-lookup"><span data-stu-id="28a7a-111">If this property is not set, the setting for the [**Caption**](caption-property.md) property determines the text displayed.</span></span> <span data-ttu-id="28a7a-112">Cuando no se establece la propiedad **VoiceCaption** o **Caption** , el comando no aparece en la ventana comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="28a7a-112">When neither the **VoiceCaption** or **Caption** property is set, the command does not appear in the Voice Commands Window.</span></span>

## <a name="see-also"></a><span data-ttu-id="28a7a-113">Consulte también</span><span class="sxs-lookup"><span data-stu-id="28a7a-113">See Also</span></span>

[<span data-ttu-id="28a7a-114">**IAgentCommandsEx::GetVoiceCaption**</span><span class="sxs-lookup"><span data-stu-id="28a7a-114">**IAgentCommandsEx::GetVoiceCaption**</span></span>](iagentcommandsex--getvoicecaption.md)


 

 