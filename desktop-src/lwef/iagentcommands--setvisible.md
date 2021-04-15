---
title: IAgentCommands SetVisible
description: IAgentCommands SetVisible
ms.assetid: 4b99989a-29bb-4e0e-8155-cf734cc667fd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04a4bdb3c1a7f1e11c9548eb1e1af415d0f5d18f
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105714353"
---
# <a name="iagentcommandssetvisible"></a><span data-ttu-id="e2e75-103">IAgentCommands:: SetVisible</span><span class="sxs-lookup"><span data-stu-id="e2e75-103">IAgentCommands::SetVisible</span></span>

<span data-ttu-id="e2e75-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e2e75-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // the Visible setting for Commands collection
);
```

<span data-ttu-id="e2e75-105">Establece el valor de la propiedad [**visible**](visible-property.md) para una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="e2e75-105">Sets the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="e2e75-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e2e75-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e2e75-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="e2e75-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="e2e75-108">Valor booleano que determina la propiedad [**visible**](visible-property.md) de una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="e2e75-108">A Boolean value that determines the [**Visible**](visible-property.md) property of a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span> <span data-ttu-id="e2e75-109">**True** establece el [**título**](caption-property.md) de la colección de **comandos** para que esté visible cuando se muestre el menú emergente del carácter; *False* no la muestra.</span><span class="sxs-lookup"><span data-stu-id="e2e75-109">**True** sets the **Commands** collection's [**Caption**](caption-property.md) to be visible when the character's pop-up menu is displayed; *False* does not display it.</span></span>

</dd> </dl>

<span data-ttu-id="e2e75-110">Una colección [**Commands**](/windows/desktop/lwef/the-commands-collection-object) debe tener su propiedad [**Caption**](caption-property.md) establecida y su propiedad [**visible**](visible-property.md) establecida en **true** para que aparezca en el menú emergente del carácter.</span><span class="sxs-lookup"><span data-stu-id="e2e75-110">A [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection must have its [**Caption**](caption-property.md) property set and its [**Visible**](visible-property.md) property set to **True** to appear on the character's pop-up menu.</span></span> <span data-ttu-id="e2e75-111">La propiedad **visible** también se debe establecer en **true** para que los comandos de la colección aparezcan cuando la aplicación cliente sea de entrada.</span><span class="sxs-lookup"><span data-stu-id="e2e75-111">The **Visible** property must also be set to **True** for commands in the collection to appear when your client application is input-active.</span></span>

## <a name="see-also"></a><span data-ttu-id="e2e75-112">Consulte también</span><span class="sxs-lookup"><span data-stu-id="e2e75-112">See Also</span></span>

<span data-ttu-id="e2e75-113">[**IAgentCommands:: GetVisible**](iagentcommands--getvisible.md), [ **IAgentCommand:: SetCaption**](iagentcommand--setcaption.md)</span><span class="sxs-lookup"><span data-stu-id="e2e75-113">[**IAgentCommands::GetVisible**](iagentcommands--getvisible.md), [**IAgentCommand::SetCaption**](iagentcommand--setcaption.md)</span></span>


 

 