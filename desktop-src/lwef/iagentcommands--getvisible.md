---
title: IAgentCommands GetVisible
description: IAgentCommands GetVisible
ms.assetid: 229a02c8-f0a1-4ee5-9bae-961b63792038
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 853a47f6136779415a08adc3c891d9b5cc95dcca
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "105695600"
---
# <a name="iagentcommandsgetvisible"></a><span data-ttu-id="d8c20-103">IAgentCommands:: GetVisible</span><span class="sxs-lookup"><span data-stu-id="d8c20-103">IAgentCommands::GetVisible</span></span>

<span data-ttu-id="d8c20-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="d8c20-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of Visible setting for Commands collection
);
```

<span data-ttu-id="d8c20-105">Recupera el valor de la propiedad [**visible**](visible-property.md) para una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="d8c20-105">Retrieves the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

-   <span data-ttu-id="d8c20-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="d8c20-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="d8c20-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="d8c20-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="d8c20-108">Dirección de una variable que recibe el valor de la propiedad [**visible**](visible-property.md) para una colección de [**comandos**](/windows/desktop/lwef/the-commands-collection-object) .</span><span class="sxs-lookup"><span data-stu-id="d8c20-108">The address of a variable that receives the value of the [**Visible**](visible-property.md) property for a [**Commands**](/windows/desktop/lwef/the-commands-collection-object) collection.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="d8c20-109">Consulte también</span><span class="sxs-lookup"><span data-stu-id="d8c20-109">See Also</span></span>

<span data-ttu-id="d8c20-110">[**IAgentCommands:: setVisible**](iagentcommands--setvisible.md), [ **IAgentCommands:: SetCaption**](iagentcommands--setcaption.md)</span><span class="sxs-lookup"><span data-stu-id="d8c20-110">[**IAgentCommands::SetVisible**](iagentcommands--setvisible.md), [**IAgentCommands::SetCaption**](iagentcommands--setcaption.md)</span></span>


 

 