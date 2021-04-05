---
title: IAgentNotifySinkEx HelpComplete
description: IAgentNotifySinkEx HelpComplete
ms.assetid: f8285d05-3b96-4046-a058-0e001e47b54b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3b7dbbdf272844242943d49ed86b303d220185
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104077624"
---
# <a name="iagentnotifysinkexhelpcomplete"></a><span data-ttu-id="cdc68-103">IAgentNotifySinkEx::HelpComplete</span><span class="sxs-lookup"><span data-stu-id="cdc68-103">IAgentNotifySinkEx::HelpComplete</span></span>

<span data-ttu-id="cdc68-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="cdc68-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT HelpComplete(
   long dwCharID,     // character ID
   long dwCommandID,  // command ID
   long dwCause       // cause 
);
```

<span data-ttu-id="cdc68-105">Notifica a una aplicación cliente cuando el usuario selecciona un comando o un carácter para completar el modo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="cdc68-105">Notifies a client application when the user selects a command or character to complete Help mode.</span></span>

-   <span data-ttu-id="cdc68-106">No de devuelve ningún valor.</span><span class="sxs-lookup"><span data-stu-id="cdc68-106">No return value.</span></span>

<dl> <dt>

<span data-ttu-id="cdc68-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span><span class="sxs-lookup"><span data-stu-id="cdc68-107"><span id="dwCharID"></span><span id="dwcharid"></span><span id="DWCHARID"></span>*dwCharID*</span></span>
</dt> <dd>

<span data-ttu-id="cdc68-108">Identificador del carácter para el que se ha completado el modo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="cdc68-108">Identifier of the character for which Help mode completed.</span></span>

</dd> <dt>

<span data-ttu-id="cdc68-109"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span><span class="sxs-lookup"><span data-stu-id="cdc68-109"><span id="dwCommandID"></span><span id="dwcommandid"></span><span id="DWCOMMANDID"></span>*dwCommandID*</span></span>
</dt> <dd>

<span data-ttu-id="cdc68-110">Identificador del comando seleccionado por el usuario.</span><span class="sxs-lookup"><span data-stu-id="cdc68-110">Identifier of the command the user selected.</span></span>

</dd> <dt>

<span data-ttu-id="cdc68-111"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span><span class="sxs-lookup"><span data-stu-id="cdc68-111"><span id="dwCause"></span><span id="dwcause"></span><span id="DWCAUSE"></span>*dwCause*</span></span>
</dt> <dd>

<span data-ttu-id="cdc68-112">La causa del evento, que puede ser los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="cdc68-112">The cause for the event, which may be the following values:</span></span>



| <span data-ttu-id="cdc68-113">Value</span><span class="sxs-lookup"><span data-stu-id="cdc68-113">Value</span></span>                                                                         | <span data-ttu-id="cdc68-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="cdc68-114">Description</span></span>                                                                          |
|-------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="cdc68-115">**const unsigned short** **CSHELPCAUSE \_ comando = 1;**</span><span class="sxs-lookup"><span data-stu-id="cdc68-115">**const unsigned short** **CSHELPCAUSE\_COMMAND = 1;**</span></span><br/>             | <span data-ttu-id="cdc68-116">El usuario seleccionó un comando proporcionado por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="cdc68-116">The user selected a command supplied by your application.</span></span>                            |
| <span data-ttu-id="cdc68-117">**const unsigned short** **CSHELPCAUSE \_ OTHERPROGRAM = 2;**</span><span class="sxs-lookup"><span data-stu-id="cdc68-117">**const unsigned short** **CSHELPCAUSE\_OTHERPROGRAM = 2;**</span></span><br/>        | <span data-ttu-id="cdc68-118">El usuario seleccionó el objeto [**Commands**](/windows/desktop/lwef/the-commands-collection-object) de otro cliente.</span><span class="sxs-lookup"><span data-stu-id="cdc68-118">The user selected the [**Commands**](/windows/desktop/lwef/the-commands-collection-object) object of another client.</span></span> |
| <span data-ttu-id="cdc68-119">**const unsigned short** **CSHELPCAUSE \_ OPENCOMMANDSWINDOW = 3;**</span><span class="sxs-lookup"><span data-stu-id="cdc68-119">**const unsigned short** **CSHELPCAUSE\_OPENCOMMANDSWINDOW = 3;**</span></span><br/>  | <span data-ttu-id="cdc68-120">El usuario seleccionó el comando abrir comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="cdc68-120">The user selected the Open Voice Commands command.</span></span>                                   |
| <span data-ttu-id="cdc68-121">**const unsigned short** **CSHELPCAUSE \_ CLOSECOMMANDSWINDOW = 4;**</span><span class="sxs-lookup"><span data-stu-id="cdc68-121">**const unsigned short** **CSHELPCAUSE\_CLOSECOMMANDSWINDOW = 4;**</span></span><br/> | <span data-ttu-id="cdc68-122">El usuario seleccionó el comando cerrar comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="cdc68-122">The user selected the Close Voice Commands command.</span></span>                                  |
| <span data-ttu-id="cdc68-123">**const unsigned short** **CSHELPCAUSE \_ SHOWCHARACTER = 5;**</span><span class="sxs-lookup"><span data-stu-id="cdc68-123">**const unsigned short** **CSHELPCAUSE\_SHOWCHARACTER = 5;**</span></span><br/>       | <span data-ttu-id="cdc68-124">El usuario seleccionó el comando show *nombredecarácter* .</span><span class="sxs-lookup"><span data-stu-id="cdc68-124">The user selected the Show *CharacterName* command.</span></span>                                  |
| <span data-ttu-id="cdc68-125">**const unsigned short** **CSHELPCAUSE \_ HIDECHARACTER = 6;**</span><span class="sxs-lookup"><span data-stu-id="cdc68-125">**const unsigned short** **CSHELPCAUSE\_HIDECHARACTER = 6;**</span></span><br/>       | <span data-ttu-id="cdc68-126">El usuario seleccionó el comando ocultar *nombredecarácter* .</span><span class="sxs-lookup"><span data-stu-id="cdc68-126">The user selected the Hide *CharacterName* command.</span></span>                                  |
| <span data-ttu-id="cdc68-127">**const unsigned short** **CSHELPCAUSE \_ carácter = 7;**</span><span class="sxs-lookup"><span data-stu-id="cdc68-127">**const unsigned short** **CSHELPCAUSE\_CHARACTER = 7;**</span></span><br/>           | <span data-ttu-id="cdc68-128">El usuario seleccionó (hizo clic en) el carácter.</span><span class="sxs-lookup"><span data-stu-id="cdc68-128">The user selected (clicked) the character.</span></span>                                           |



 

</dd> </dl>

<span data-ttu-id="cdc68-129">Normalmente, el modo de ayuda se completa cuando el usuario hace clic o arrastra el carácter o selecciona un comando en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="cdc68-129">Typically Help mode completes when the user clicks or drags the character or selects a command from the character's pop-up menu.</span></span> <span data-ttu-id="cdc68-130">Al hacer clic en otro carácter o en cualquier otro lugar de la pantalla, no se cancela el modo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="cdc68-130">Clicking on another character or elsewhere on the screen does not cancel Help mode.</span></span> <span data-ttu-id="cdc68-131">El cliente que establece el modo de ayuda para el carácter puede cancelar el modo de ayuda estableciendo [**IAgentCharacter:: HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) en **false**.</span><span class="sxs-lookup"><span data-stu-id="cdc68-131">The client that set Help mode for the character can cancel Help mode by setting [**IAgentCharacter::HelpModeOn**](https://www.bing.com/search?q=**IAgentCharacter::HelpModeOn**) to **False**.</span></span> <span data-ttu-id="cdc68-132">(Esto no desencadena el evento **IAgentNotifySinkEx:: HelpComplete** ).</span><span class="sxs-lookup"><span data-stu-id="cdc68-132">(This does not trigger the **IAgentNotifySinkEx::HelpComplete** event.)</span></span>

<span data-ttu-id="cdc68-133">Cuando el usuario selecciona un comando en el menú emergente del carácter en el modo de ayuda, el servidor quita el menú, llama a ayuda con el [**HelpContextID**](helpcontextid-property.md)especificado del comando y envía este evento.</span><span class="sxs-lookup"><span data-stu-id="cdc68-133">When the user selects a command from the character's pop-up menu in Help mode, the server removes the menu, calls Help with the command's specified [**HelpContextID**](helpcontextid-property.md), and sends this event.</span></span> <span data-ttu-id="cdc68-134">La información contextual (también conocida como esto?) La ventana de ayuda se muestra en la ubicación del puntero.</span><span class="sxs-lookup"><span data-stu-id="cdc68-134">The context-sensitive (also known as What's This?) Help window is displayed at the pointer location.</span></span> <span data-ttu-id="cdc68-135">Si el usuario selecciona el comando por entrada de voz, se muestra la ventana de ayuda sobre el carácter.</span><span class="sxs-lookup"><span data-stu-id="cdc68-135">If the user selects the command by voice input, the Help window is displayed over the character.</span></span> <span data-ttu-id="cdc68-136">Si el carácter está fuera de la pantalla, la ventana se muestra en la pantalla más cercana a la posición actual del carácter.</span><span class="sxs-lookup"><span data-stu-id="cdc68-136">If the character is off-screen, the window is displayed on-screen nearest to the character's current position.</span></span>

<span data-ttu-id="cdc68-137">Si el servidor devuelve *dwCommandID* como una cadena vacía (""), indica que el usuario seleccionó un comando proporcionado por el servidor.</span><span class="sxs-lookup"><span data-stu-id="cdc68-137">If the server returns *dwCommandID* as an empty string (""), it indicates that the user selected a server-supplied command.</span></span>

<span data-ttu-id="cdc68-138">Este evento solo se envía a la aplicación cliente que coloca el carácter en modo de ayuda.</span><span class="sxs-lookup"><span data-stu-id="cdc68-138">This event is sent only to the client application that places the character into Help mode.</span></span>

## <a name="see-also"></a><span data-ttu-id="cdc68-139">Consulte también</span><span class="sxs-lookup"><span data-stu-id="cdc68-139">See Also</span></span>

<span data-ttu-id="cdc68-140">[**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md), [**IAgentCharacterEx:: SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx:: SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span><span class="sxs-lookup"><span data-stu-id="cdc68-140">[**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md), [**IAgentCharacterEx::SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCommandsEx::SetHelpContextID**](iagentcommandsex--sethelpcontextid.md)</span></span>


 

