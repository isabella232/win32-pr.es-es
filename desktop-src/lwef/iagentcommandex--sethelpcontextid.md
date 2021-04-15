---
title: IAgentCommandEx SetHelpContextID
description: IAgentCommandEx SetHelpContextID
ms.assetid: 861d55dc-f584-495c-a148-016af8f7a3e2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1a7539cef8e986db40ef94a8fd3d47073fbe489d
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105695602"
---
# <a name="iagentcommandexsethelpcontextid"></a><span data-ttu-id="b4b7e-103">IAgentCommandEx::SetHelpContextID</span><span class="sxs-lookup"><span data-stu-id="b4b7e-103">IAgentCommandEx::SetHelpContextID</span></span>

<span data-ttu-id="b4b7e-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="b4b7e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetHelpContextID(
   long ulID  //  ID for help topic
);
```

<span data-ttu-id="b4b7e-105">Establece [**HelpContextID**](helpcontextid-property-com.md) para un objeto [**Command**](/windows/desktop/lwef/the-command-object) .</span><span class="sxs-lookup"><span data-stu-id="b4b7e-105">Sets the [**HelpContextID**](helpcontextid-property-com.md) for a [**Command**](/windows/desktop/lwef/the-command-object) object.</span></span>

-   <span data-ttu-id="b4b7e-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="b4b7e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="b4b7e-107"><span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*</span><span class="sxs-lookup"><span data-stu-id="b4b7e-107"><span id="ulID"></span><span id="ulid"></span><span id="ULID"></span>*ulID*</span></span>
</dt> <dd>

<span data-ttu-id="b4b7e-108">El número de contexto del tema de ayuda asociado al objeto de [**comando**](/windows/desktop/lwef/the-command-object) ; se utiliza para proporcionar ayuda contextual para el comando.</span><span class="sxs-lookup"><span data-stu-id="b4b7e-108">The context number of the help topic associated with the [**Command**](/windows/desktop/lwef/the-command-object) object; used to provide context-sensitive Help for the command.</span></span>

</dd> </dl>

<span data-ttu-id="b4b7e-109">Si ha creado un archivo de ayuda de Windows para la aplicación y lo ha establecido en la propiedad [**HelpFile**](helpfile-property.md) del carácter.</span><span class="sxs-lookup"><span data-stu-id="b4b7e-109">If you've created a Windows Help file for your application and set this in the character's [**HelpFile**](helpfile-property.md) property.</span></span> <span data-ttu-id="b4b7e-110">El agente de Microsoft llama automáticamente a la ayuda cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **true** y el usuario selecciona el comando.</span><span class="sxs-lookup"><span data-stu-id="b4b7e-110">Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the command.</span></span> <span data-ttu-id="b4b7e-111">Si hay un número de contexto en el [**HelpContextID**](helpcontextid-property-com.md), el agente llama a help y busca el tema identificado por el número de contexto actual.</span><span class="sxs-lookup"><span data-stu-id="b4b7e-111">If there is a context number in the [**HelpContextID**](helpcontextid-property-com.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="b4b7e-112">El número de contexto actual es el valor de **HelpContextID** para el comando.</span><span class="sxs-lookup"><span data-stu-id="b4b7e-112">The current context number is the value of **HelpContextID** for the command.</span></span>

> [!Note]  
> <span data-ttu-id="b4b7e-113">La compilación de un archivo de ayuda requiere el compilador de ayuda de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b4b7e-113">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="b4b7e-114">Consulte también</span><span class="sxs-lookup"><span data-stu-id="b4b7e-114">See Also</span></span>

<span data-ttu-id="b4b7e-115">[**IAgentCommandEx:: GetHelpContextID**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="b4b7e-115">[**IAgentCommandEx::GetHelpContextID**](iagentcommandex--gethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 