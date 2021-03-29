---
title: IAgentCharacterEx SetHelpContextID
description: IAgentCharacterEx SetHelpContextID
ms.assetid: 218e970e-825e-441d-8947-30ec6a2845bd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500187bf04babbecf7577ff933dd0adcc53609f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103774497"
---
# <a name="iagentcharacterexsethelpcontextid"></a><span data-ttu-id="e4690-103">IAgentCharacterEx::SetHelpContextID</span><span class="sxs-lookup"><span data-stu-id="e4690-103">IAgentCharacterEx::SetHelpContextID</span></span>

<span data-ttu-id="e4690-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e4690-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulHelpID  // ID for help topic
);
```

<span data-ttu-id="e4690-105">Establece [**HelpContextID**](helpcontextid-property.md) para el carácter.</span><span class="sxs-lookup"><span data-stu-id="e4690-105">Sets the [**HelpContextID**](helpcontextid-property.md) for the character.</span></span>

-   <span data-ttu-id="e4690-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e4690-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e4690-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span><span class="sxs-lookup"><span data-stu-id="e4690-107"><span id="ulHelpID"></span><span id="ulhelpid"></span><span id="ULHELPID"></span>*ulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="e4690-108">El número de contexto del tema de ayuda para asociado a un carácter; se utiliza para proporcionar ayuda contextual para el carácter.</span><span class="sxs-lookup"><span data-stu-id="e4690-108">The context number of the help topic for associated with a character; used to provide context-sensitive Help for the character.</span></span>

</dd> </dl>

<span data-ttu-id="e4690-109">Si ha creado un archivo de ayuda de Windows para la aplicación y lo ha establecido en la propiedad [**HelpFile**](helpfile-property.md) del carácter, el agente de Microsoft llama automáticamente a Help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **true** y el usuario selecciona el carácter.</span><span class="sxs-lookup"><span data-stu-id="e4690-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the character.</span></span> <span data-ttu-id="e4690-110">Si hay un número de contexto en el [**HelpContextID**](helpcontextid-property.md), el agente llama a help y busca el tema identificado por el número de contexto actual.</span><span class="sxs-lookup"><span data-stu-id="e4690-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="e4690-111">El número de contexto actual es el valor de **HelpContextID** para el carácter.</span><span class="sxs-lookup"><span data-stu-id="e4690-111">The current context number is the value of **HelpContextID** for the character.</span></span> <span data-ttu-id="e4690-112">Si hay un número de contexto en la propiedad **HelpContextID** , la ayuda muestra un tema correspondiente al contexto de ayuda actual. en caso contrario, se muestra "no hay ningún tema de ayuda asociado a este elemento".</span><span class="sxs-lookup"><span data-stu-id="e4690-112">If there is a context number in the **HelpContextID** property, Help displays a topic corresponding to the current Help context; otherwise it displays "No Help topic associated with this item."</span></span>

<span data-ttu-id="e4690-113">Esta configuración solo se aplica cuando la aplicación cliente es el cliente activo del carácter más alto.</span><span class="sxs-lookup"><span data-stu-id="e4690-113">This setting applies only when your client application is the active client of the topmost character.</span></span> <span data-ttu-id="e4690-114">No afecta a otros clientes del carácter u otros caracteres que usa la aplicación cliente.</span><span class="sxs-lookup"><span data-stu-id="e4690-114">It does not affect other clients of the character or other characters that your client application is using.</span></span>

> [!Note]  
> <span data-ttu-id="e4690-115">La compilación de un archivo de ayuda requiere el compilador de ayuda de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e4690-115">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="e4690-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e4690-116">See Also</span></span>

<span data-ttu-id="e4690-117">[**IAgentCharacterEx:: GetHelpContextID**](iagentcharacterex--gethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="e4690-117">[**IAgentCharacterEx::GetHelpContextID**](iagentcharacterex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




