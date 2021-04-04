---
title: IAgentCommandsEx InsertEx
description: IAgentCommandsEx InsertEx
ms.assetid: 037c47df-f026-42dc-8c37-2704518d3fd2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6d59b504cfa475c3ac63888796d7df8d800bfd72
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077669"
---
# <a name="iagentcommandsexinsertex"></a><span data-ttu-id="ee806-103">IAgentCommandsEx::InsertEx</span><span class="sxs-lookup"><span data-stu-id="ee806-103">IAgentCommandsEx::InsertEx</span></span>

<span data-ttu-id="ee806-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="ee806-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT InsertEx(
   BSTR bszCaption,       // Caption setting for Command
   BSTR bszVoice,         // Voice setting for Command
   BSTR bszVoiceCaption,  // VoiceCaption setting for Command
   long bEnabled,         // Enabled setting for Command
   long bVisible,         // Visible setting for Command
   long ulHelpID,         // HelpContextID setting for Command
   long dwRefID,          // reference Command for insertion
   long dBefore,          // insertion position flag
   long * pdwID           // address for variable for Command ID
);
```

<span data-ttu-id="ee806-105">Inserta un objeto [**Command**](/windows/desktop/lwef/the-command-object) en una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="ee806-105">Inserts a [**Command**](/windows/desktop/lwef/the-command-object) object in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="ee806-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="ee806-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="ee806-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span><span class="sxs-lookup"><span data-stu-id="ee806-107"><span id="bszCaption"></span><span id="bszcaption"></span><span id="BSZCAPTION"></span>*bszCaption*</span></span>
</dt> <dd>

<span data-ttu-id="ee806-108">BSTR que especifica el valor del texto de [**título**](caption-property.md) que se muestra para el [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="ee806-108">A BSTR that specifies the value of the [**Caption**](caption-property.md) text displayed for the [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> <dt>

<span data-ttu-id="ee806-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span><span class="sxs-lookup"><span data-stu-id="ee806-109"><span id="bszVoice"></span><span id="bszvoice"></span><span id="BSZVOICE"></span>*bszVoice*</span></span>
</dt> <dd>

<span data-ttu-id="ee806-110">BSTR que especifica el valor de la configuración del texto de la [**voz**](voice-property.md) de un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="ee806-110">A BSTR that specifies the value of the [**Voice**](voice-property.md) text setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> <dt>

<span data-ttu-id="ee806-111"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span><span class="sxs-lookup"><span data-stu-id="ee806-111"><span id="bszVoiceCaption"></span><span id="bszvoicecaption"></span><span id="BSZVOICECAPTION"></span>*bszVoiceCaption*</span></span>
</dt> <dd>

<span data-ttu-id="ee806-112">BSTR que especifica el valor del texto [**VoiceCaption**](voicecaption-property.md) que se muestra para un [**comando**](/windows/desktop/lwef/the-command-object) en una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="ee806-112">A BSTR that specifies the value of the [**VoiceCaption**](voicecaption-property.md) text displayed for a [**Command**](/windows/desktop/lwef/the-command-object) in a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> <dt>

<span data-ttu-id="ee806-113"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span><span class="sxs-lookup"><span data-stu-id="ee806-113"><span id="bEnabled"></span><span id="benabled"></span><span id="BENABLED"></span>*bEnabled*</span></span>
</dt> <dd>

<span data-ttu-id="ee806-114">Una expresión booleana que especifica el valor [**habilitado**](enabled-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="ee806-114">A Boolean expression that specifies the [**Enabled**](enabled-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="ee806-115">Si el parámetro es **true**, el **comando** está habilitado y se puede seleccionar; Si es **false**, el **comando** está deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="ee806-115">If the parameter is **True**, the **Command** is enabled and can be selected; if **False**, the **Command** is disabled.</span></span>

</dd> <dt>

<span data-ttu-id="ee806-116"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="ee806-116"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="ee806-117">Una expresión booleana que especifica el valor [**visible**](visible-property.md) para un [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="ee806-117">A Boolean expression that specifies the [**Visible**](visible-property.md) setting for a [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="ee806-118">Si el parámetro es **true**, el **comando** estará visible en el menú emergente del carácter (si también se establece la propiedad [**Caption**](caption-property.md) ).</span><span class="sxs-lookup"><span data-stu-id="ee806-118">If the parameter is **True**, the **Command** will be visible in the character's pop-up menu (if the [**Caption**](caption-property.md) property is also set).</span></span>

</dd> <dt>

<span data-ttu-id="ee806-119"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span><span class="sxs-lookup"><span data-stu-id="ee806-119"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="ee806-120">El número de contexto del tema de ayuda asociado al objeto de [**comando**](/windows/desktop/lwef/the-command-object) ; se utiliza para proporcionar ayuda contextual para el comando.</span><span class="sxs-lookup"><span data-stu-id="ee806-120">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> <dt>

<span data-ttu-id="ee806-121"><span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*</span><span class="sxs-lookup"><span data-stu-id="ee806-121"><span id="dwRefID"></span><span id="dwrefid"></span><span id="DWREFID"></span>*dwRefID*</span></span>
</dt> <dd>

<span data-ttu-id="ee806-122">IDENTIFICADOR de un [**comando**](/windows/desktop/lwef/the-command-object) que se usa como referencia para la inserción relativa del nuevo **comando**.</span><span class="sxs-lookup"><span data-stu-id="ee806-122">The ID of a [**Command**](/windows/desktop/lwef/the-command-object) used as a reference for the relative insertion of the new **Command**.</span></span>

</dd> <dt>

<span data-ttu-id="ee806-123"><span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*</span><span class="sxs-lookup"><span data-stu-id="ee806-123"><span id="dBefore"></span><span id="dbefore"></span><span id="DBEFORE"></span>*dBefore*</span></span>
</dt> <dd>

<span data-ttu-id="ee806-124">Expresión booleana que especifica dónde se debe colocar el [**comando**](/windows/desktop/lwef/the-command-object).</span><span class="sxs-lookup"><span data-stu-id="ee806-124">A Boolean expression that specifies where to place the [**Command**](/windows/desktop/lwef/the-command-object).</span></span> <span data-ttu-id="ee806-125">Si este parámetro es **true**, el nuevo **comando** se inserta antes del **comando** al que se hace referencia; Si es **false**, el nuevo **comando** se coloca después del **comando** al que se hace referencia.</span><span class="sxs-lookup"><span data-stu-id="ee806-125">If this parameter is **True**, the new **Command** is inserted before the referenced **Command**; if **False**, the new **Command** is placed after the referenced **Command**.</span></span>

</dd> <dt>

<span data-ttu-id="ee806-126"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span><span class="sxs-lookup"><span data-stu-id="ee806-126"><span id="pdwID_"></span><span id="pdwid_"></span><span id="PDWID_"></span>*pdwID*</span></span> 
</dt> <dd>

<span data-ttu-id="ee806-127">Dirección de una variable que recibe el identificador del [**comando**](/windows/desktop/lwef/the-command-object)insertado.</span><span class="sxs-lookup"><span data-stu-id="ee806-127">Address of a variable that receives the ID for the inserted [**Command**](/windows/desktop/lwef/the-command-object).</span></span>

</dd> </dl>

<span data-ttu-id="ee806-128">[**IAgentCommandsEx:: InsertEx**](https://www.bing.com/search?q=**IAgentCommandsEx::InsertEx**) extiende [**IAgentCommands:: Insert**](iagentcommands--insert.md) incluyendo la propiedad [**HelpContextID**](helpcontextid-property.md) .</span><span class="sxs-lookup"><span data-stu-id="ee806-128">[**IAgentCommandsEx::InsertEx**](https://www.bing.com/search?q=**IAgentCommandsEx::InsertEx**) extends [**IAgentCommands::Insert**](iagentcommands--insert.md) by including the [**HelpContextID**](helpcontextid-property.md) property.</span></span> <span data-ttu-id="ee806-129">También puede establecer la propiedad mediante [ **IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span><span class="sxs-lookup"><span data-stu-id="ee806-129">You can also set the property using [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span></span>

## <a name="see-also"></a><span data-ttu-id="ee806-130">Consulte también</span><span class="sxs-lookup"><span data-stu-id="ee806-130">See Also</span></span>

<span data-ttu-id="ee806-131">[**IAgentCommandsEx:: Addex**](iagentcommandsex--addex.md), [**IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommands:: Add**](iagentcommands--add.md), [**IAgentCommands:: Remove**](iagentcommands--remove.md), [**IAgentCommands:: RemoveAll**](iagentcommands--removeall.md)</span><span class="sxs-lookup"><span data-stu-id="ee806-131">[**IAgentCommandsEx::AddEx**](iagentcommandsex--addex.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md), [**IAgentCommands::Add**](iagentcommands--add.md), [**IAgentCommands::Remove**](iagentcommands--remove.md), [**IAgentCommands::RemoveAll**](iagentcommands--removeall.md)</span></span>


 

 