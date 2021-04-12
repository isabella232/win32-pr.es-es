---
title: IAgentPropertySheet GetVisible
description: IAgentPropertySheet GetVisible
ms.assetid: 5e95c4da-28a3-4686-8699-ff7b16b3808f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bcda8be2a3ae3e4084087225e0d7ed79d33621a8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357190"
---
# <a name="iagentpropertysheetgetvisible"></a><span data-ttu-id="33dc6-103">IAgentPropertySheet:: GetVisible</span><span class="sxs-lookup"><span data-stu-id="33dc6-103">IAgentPropertySheet::GetVisible</span></span>

<span data-ttu-id="33dc6-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="33dc6-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetVisible(
   long * pbVisible  // address of variable for property sheet
);                   // Visible setting
```

<span data-ttu-id="33dc6-105">Determina si la hoja de propiedades de Microsoft Agent está visible u oculta.</span><span class="sxs-lookup"><span data-stu-id="33dc6-105">Determines whether the Microsoft Agent property sheet is visible or hidden.</span></span>

-   <span data-ttu-id="33dc6-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="33dc6-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="33dc6-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span><span class="sxs-lookup"><span data-stu-id="33dc6-107"><span id="pbVisible"></span><span id="pbvisible"></span><span id="PBVISIBLE"></span>*pbVisible*</span></span>
</dt> <dd>

<span data-ttu-id="33dc6-108">Dirección de una variable que recibe **true** si la hoja de propiedades es visible y **false** si está oculta.</span><span class="sxs-lookup"><span data-stu-id="33dc6-108">Address of a variable that receives **True** if the property sheet is visible and **False** if hidden.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="33dc6-109">Consulte también</span><span class="sxs-lookup"><span data-stu-id="33dc6-109">See Also</span></span>

[<span data-ttu-id="33dc6-110">**IAgentPropertySheet:: SetVisible**</span><span class="sxs-lookup"><span data-stu-id="33dc6-110">**IAgentPropertySheet::SetVisible**</span></span>](iagentpropertysheet--setvisible.md)


 

 




