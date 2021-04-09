---
title: IAgentCharacter GetVisible
description: IAgentCharacter GetVisible
ms.assetid: 6e8e3a68-a7bb-4afb-a753-836fe82a0b24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b0593b9b3a193b9d5910888b81b4ecba90469b1e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/19/2020
ms.locfileid: "104149196"
---
# <a name="iagentcharactergetvisible"></a><span data-ttu-id="e3dc4-103">IAgentCharacter:: GetVisible</span><span class="sxs-lookup"><span data-stu-id="e3dc4-103">IAgentCharacter::GetVisible</span></span>

<span data-ttu-id="e3dc4-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="e3dc4-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for character Visible setting
);
```

<span data-ttu-id="e3dc4-105">Determina si el marco de animación del carácter está actualmente visible.</span><span class="sxs-lookup"><span data-stu-id="e3dc4-105">Determines whether the character's animation frame is currently visible.</span></span>

-   <span data-ttu-id="e3dc4-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="e3dc4-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="e3dc4-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="e3dc4-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="e3dc4-108">Dirección de una variable que recibe **true** si el fotograma del carácter está visible y **false** si está oculto.</span><span class="sxs-lookup"><span data-stu-id="e3dc4-108">Address of a variable that receives **True** if the character's frame is visible and **False** if hidden.</span></span>

</dd> </dl>

<span data-ttu-id="e3dc4-109">Puede usar este método para determinar si el marco del carácter está visible actualmente.</span><span class="sxs-lookup"><span data-stu-id="e3dc4-109">You can use this method to determine whether the character's frame is currently visible.</span></span> <span data-ttu-id="e3dc4-110">Para hacer que un carácter esté visible, use el método [**Show**](/windows/desktop/lwef/iagentcharacter--show) .</span><span class="sxs-lookup"><span data-stu-id="e3dc4-110">To make a character visible, use the [**Show**](/windows/desktop/lwef/iagentcharacter--show) method.</span></span> <span data-ttu-id="e3dc4-111">Para ocultar un carácter, utilice el método [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) .</span><span class="sxs-lookup"><span data-stu-id="e3dc4-111">To hide a character, use the [**Hide**](/windows/desktop/lwef/iagentcharacter--hide) method.</span></span>

 

 