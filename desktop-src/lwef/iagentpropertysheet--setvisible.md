---
title: IAgentPropertySheet SetVisible
description: IAgentPropertySheet SetVisible
ms.assetid: 53520a64-e99f-4d03-aa36-bcbb4547990c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26615f0e5282b399837726c980650abcf12fdb47
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704667"
---
# <a name="iagentpropertysheetsetvisible"></a><span data-ttu-id="5566e-103">IAgentPropertySheet:: SetVisible</span><span class="sxs-lookup"><span data-stu-id="5566e-103">IAgentPropertySheet::SetVisible</span></span>

<span data-ttu-id="5566e-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5566e-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // property sheet Visible setting 
);
```

<span data-ttu-id="5566e-105">Establece la propiedad [**visible**](visible-property.md) de la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="5566e-105">Sets the [**Visible**](visible-property.md) property for the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="5566e-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="5566e-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5566e-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="5566e-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="5566e-108">Configuración de la propiedad visible.</span><span class="sxs-lookup"><span data-stu-id="5566e-108">Visible property setting.</span></span> <span data-ttu-id="5566e-109">Un valor de **true** muestra la hoja de propiedades; un valor **false** lo oculta.</span><span class="sxs-lookup"><span data-stu-id="5566e-109">A value of **True** displays the property sheet; a value of **False** hides it.</span></span>

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="5566e-110">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5566e-110">See Also</span></span>

[<span data-ttu-id="5566e-111">**IAgentPropertySheet:: GetVisible**</span><span class="sxs-lookup"><span data-stu-id="5566e-111">**IAgentPropertySheet::GetVisible**</span></span>](iagentpropertysheet--getvisible.md)


 

 




