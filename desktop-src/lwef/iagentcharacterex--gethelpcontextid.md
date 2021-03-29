---
title: IAgentCharacterEx GetHelpContextID
description: IAgentCharacterEx GetHelpContextID
ms.assetid: 9dec5b0c-4758-4859-9aa6-6db3ef0d6b56
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfec03a217745838b88a592433defae01529ed50
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103778715"
---
# <a name="iagentcharacterexgethelpcontextid"></a><span data-ttu-id="61e1d-103">IAgentCharacterEx::GetHelpContextID</span><span class="sxs-lookup"><span data-stu-id="61e1d-103">IAgentCharacterEx::GetHelpContextID</span></span>

<span data-ttu-id="61e1d-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="61e1d-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetHelpContextID(
   long * pulHelpID  // address of character's help topic ID
);
```

<span data-ttu-id="61e1d-105">Recupera [**HelpContextID**](helpcontextid-property.md) para el carácter.</span><span class="sxs-lookup"><span data-stu-id="61e1d-105">Retrieves the [**HelpContextID**](helpcontextid-property.md) for the character.</span></span>

-   <span data-ttu-id="61e1d-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="61e1d-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="61e1d-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span><span class="sxs-lookup"><span data-stu-id="61e1d-107"><span id="pulHelpID"></span><span id="pulhelpid"></span><span id="PULHELPID"></span>*pulHelpID*</span></span>
</dt> <dd>

<span data-ttu-id="61e1d-108">Dirección de una variable que recibe el número de contexto del tema de ayuda para el carácter.</span><span class="sxs-lookup"><span data-stu-id="61e1d-108">Address of a variable that receives the context number of the help topic for the character.</span></span>

</dd> </dl>

<span data-ttu-id="61e1d-109">Si ha creado un archivo de ayuda de Windows para la aplicación y ha establecido la propiedad [**HelpFile**](helpfile-property.md) del carácter, el agente de Microsoft llama automáticamente a Help cuando [**HelpModeOn**](helpmodeon-property.md) está establecido en **true** y el usuario selecciona el carácter.</span><span class="sxs-lookup"><span data-stu-id="61e1d-109">If you've created a Windows Help file for your application and set the character's [**HelpFile**](helpfile-property.md) property, Microsoft Agent automatically calls Help when [**HelpModeOn**](helpmodeon-property.md) is set to **True** and the user selects the character.</span></span> <span data-ttu-id="61e1d-110">Si hay un número de contexto en el [**HelpContextID**](helpcontextid-property.md), el agente llama a help y busca el tema identificado por el número de contexto actual.</span><span class="sxs-lookup"><span data-stu-id="61e1d-110">If there is a context number in the [**HelpContextID**](helpcontextid-property.md), Agent calls Help and searches for the topic identified by the current context number.</span></span> <span data-ttu-id="61e1d-111">El número de contexto actual es el valor de **HelpContextID** para el carácter.</span><span class="sxs-lookup"><span data-stu-id="61e1d-111">The current context number is the value of **HelpContextID** for the character.</span></span>

<span data-ttu-id="61e1d-112">**IAgentCharacterEx:: GetHelpContextID** devuelve el [**HelpContextID**](helpcontextid-property.md) que estableció para el carácter.</span><span class="sxs-lookup"><span data-stu-id="61e1d-112">**IAgentCharacterEx::GetHelpContextID** returns the [**HelpContextID**](helpcontextid-property.md) you set for the character.</span></span> <span data-ttu-id="61e1d-113">No devuelve el valor de **HelpContextID** establecido por otros clientes.</span><span class="sxs-lookup"><span data-stu-id="61e1d-113">It does not return the **HelpContextID** set by other clients.</span></span>

> [!Note]  
> <span data-ttu-id="61e1d-114">La compilación de un archivo de ayuda requiere el compilador de ayuda de Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="61e1d-114">Building a Help file requires the Microsoft Windows Help Compiler.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="61e1d-115">Consulte también</span><span class="sxs-lookup"><span data-stu-id="61e1d-115">See Also</span></span>

<span data-ttu-id="61e1d-116">[**IAgentCharacterEx:: SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCharacterEx:: SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx:: SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span><span class="sxs-lookup"><span data-stu-id="61e1d-116">[**IAgentCharacterEx::SetHelpContextID**](iagentcharacterex--sethelpcontextid.md), [**IAgentCharacterEx::SetHelpModeOn**](iagentcharacterex--sethelpmodeon.md), [**IAgentCharacterEx::SetHelpFileName**](iagentcharacterex--sethelpfilename.md)</span></span>


 

 




