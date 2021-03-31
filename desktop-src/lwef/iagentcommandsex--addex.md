---
title: IAgentCommandsEx AddEx
description: IAgentCommandsEx AddEx
ms.assetid: 54be4793-89ac-475b-8a6a-5b8c18bb4b38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7487bb7c7af0295d82355c7a1f7fb50e30aa6e1f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "103790600"
---
# <a name="iagentcommandsexaddex"></a><span data-ttu-id="08e17-103">IAgentCommandsEx:: AddEx</span><span class="sxs-lookup"><span data-stu-id="08e17-103">IAgentCommandsEx::AddEx</span></span>

<span data-ttu-id="08e17-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="08e17-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT AddEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long * pdwID           // address for variable for ID
);
```

<span data-ttu-id="08e17-105">Agrega un [**comando**](/windows/desktop/lwef/the-command-object) a una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="08e17-105">Adds a [**Command**](/windows/desktop/lwef/the-command-object) to a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="08e17-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="08e17-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="08e17-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span><span class="sxs-lookup"><span data-stu-id="08e17-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="08e17-108">BSTR que especifica el valor del texto de [**título**](caption-property.md) que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="08e17-108">A BSTR that specifies the value of the [**Caption**](caption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="08e17-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span><span class="sxs-lookup"><span data-stu-id="08e17-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="08e17-110">BSTR que especifica el valor de la configuración del texto de la [**voz**](voice-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="08e17-110">A BSTR that specifies the value of the [**Voice**](voice-property.md) text setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="08e17-111"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span><span class="sxs-lookup"><span data-stu-id="08e17-111"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="08e17-112">BSTR que especifica el valor del texto [**VoiceCaption**](voicecaption-property.md) que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="08e17-112">A BSTR that specifies the value of the [**VoiceCaption**](voicecaption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="08e17-113"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="08e17-113"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="08e17-114">Una expresión booleana que especifica el valor [**habilitado**](enabled-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="08e17-114">A Boolean expression that specifies the [**Enabled**](enabled-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="08e17-115">Si el parámetro es **true**, el **comando** está habilitado y se puede seleccionar; Si es **false**, el **comando** está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="08e17-115">If the parameter is **True**, the **Command** is enabled and can be selected; if **False**, the **Command** is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="08e17-116"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="08e17-116"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="08e17-117">Una expresión booleana que especifica el valor [**visible**](visible-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="08e17-117">A Boolean expression that specifies the [**Visible**](visible-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="08e17-118">Si el parámetro es **true**, el **comando** estará visible en el menú emergente del carácter (si también se establece la propiedad [**Caption**](caption-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="08e17-118">If the parameter is **True**, the **Command** will be visible in the character's pop-up menu (if the [**Caption**](caption-property.md) property is also set).</span></span>

</dd> <dt>

<span data-ttu-id="08e17-119"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span><span class="sxs-lookup"><span data-stu-id="08e17-119"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="08e17-120">El número de contexto del tema de ayuda asociado al objeto de [**comando**](/windows/desktop/lwef/the-command-object) ; se utiliza para proporcionar ayuda contextual para el comando.</span><span class="sxs-lookup"><span data-stu-id="08e17-120">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> <dt>

<span data-ttu-id="08e17-121"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span><span class="sxs-lookup"><span data-stu-id="08e17-121"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span></span> 
</dt> <dd>

<span data-ttu-id="08e17-122">Dirección de una variable que recibe el identificador del [**comando**](/windows/desktop/lwef/the-command-object)agregado.</span><span class="sxs-lookup"><span data-stu-id="08e17-122">Address of a variable that receives the ID for the added [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="08e17-123">[**IAgentCommandsEx:: Addex**](https://www.bing.com/search?q=**IAgentCommandsEx::AddEx**) extiende [**IAgentCommands:: Add**](iagentcommands--add.md) incluyendo la propiedad [**HelpContextID**](helpcontextid-property.md) .</span><span class="sxs-lookup"><span data-stu-id="08e17-123">[**IAgentCommandsEx::AddEx**](https://www.bing.com/search?q=**IAgentCommandsEx::AddEx**) extends [**IAgentCommands::Add**](iagentcommands--add.md) by including the [**HelpContextID**](helpcontextid-property.md) property.</span></span> <span data-ttu-id="08e17-124">También puede establecer la propiedad mediante [ **IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span><span class="sxs-lookup"><span data-stu-id="08e17-124">You can also set the property using [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="08e17-125">Consulte también</span><span class="sxs-lookup"><span data-stu-id="08e17-125">See Also</span></span>

<span data-ttu-id="08e17-126">[**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommand:: SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand:: setEnabled**](iagentcommand--setenabled.md), [**IAgentCommand:: setVisible**](iagentcommand--setvisible.md), [**IAgentCommand:: SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands:: Insert**](iagentcommands--insert.md), [**IAgentCommandsEx:: InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="08e17-126">[**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md), [**IAgentCommand::SetEnabled**](iagentcommand--setenabled.md), [**IAgentCommand::SetVisible**](iagentcommand--setvisible.md), [**IAgentCommand::SetVoice**](iagentcommand--setvoice.md), [**IAgentCommands::Insert**](iagentcommands--insert.md), [**IAgentCommandsEx::InsertEx**](iagentcommandsex--insertex.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 