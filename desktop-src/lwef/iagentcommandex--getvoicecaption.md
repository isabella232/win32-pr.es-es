---
title: IAgentCommandEx GetVoiceCaption
description: IAgentCommandEx GetVoiceCaption
ms.assetid: a81accfd-c137-4347-8ead-4ed5e7148751
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6f367a7956d1029eae47064a0778264e3b77f5a
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104358839"
---
# <a name="iagentcommandexgetvoicecaption"></a><span data-ttu-id="b3ae8-103">IAgentCommandEx::GetVoiceCaption</span><span class="sxs-lookup"><span data-stu-id="b3ae8-103">IAgentCommandEx::GetVoiceCaption</span></span>

<span data-ttu-id="b3ae8-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b3ae8-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVoiceCaption(
   BSTR * pbszVoiceCaption  // address of command's voice caption text
);
```

<span data-ttu-id="b3ae8-105">Recupera el [**VoiceCaption**](voicecaption-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="b3ae8-105">Retrieves the [**VoiceCaption**](voicecaption-property.md) for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

-   <span data-ttu-id="b3ae8-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b3ae8-107"><span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*</span><span class="sxs-lookup"><span data-stu-id="b3ae8-107"><span id="pbszVoiceCaption"></span><span id="pbszvoicecaption"></span><span id="PBSZVOICECAPTION"></span>*pbszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="b3ae8-108">Dirección de un BSTR que recibe el valor del texto de [**título**](caption-property.md) que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="b3ae8-108">The address of a BSTR that receives the value of the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="b3ae8-109">[**VoiceCaption**](voicecaption-property.md) es el texto que aparece para un objeto de [**comando**](/windows/desktop/lwef/the-command-object) en la ventana comandos de voz cuando la aplicación cliente es de entrada-activa.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-109">The [**VoiceCaption**](voicecaption-property.md) is the text that appears for a [**Command**](/windows/desktop/lwef/the-command-object) object in the Voice Commands Window when your client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="b3ae8-110">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b3ae8-110">See Also</span></span>

<span data-ttu-id="b3ae8-111">[**IAgentCommandEx:: SetVoiceCaption**](iagentcommandex--setvoicecaption.md), [**IAgentCommand:: setEnabled**](iagentcommand--setenabled.md), [**IAgentCommand:: setVisible**](iagentcommand--setvisible.md), [**IAgentCommand:: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx:: Addex**](iagentcommandsex--addex.md), [**IAgentCommandsEx:: InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md)</span><span class="sxs-lookup"><span data-stu-id="b3ae8-111">[**IAgentCommandEx::SetVoiceCaption**](iagentcommandex--setvoicecaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Insert**](iagentcommands--insert.md)</span></span>


 

 