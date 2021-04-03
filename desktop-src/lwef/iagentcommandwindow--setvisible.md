---
title: IAgentCommandWindow SetVisible
description: IAgentCommandWindow SetVisible
ms.assetid: 44f3fc2d-937a-4890-8dad-e0f29da4c6b5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a43ddff54f4869cbe36016f30d775eeea017ae6c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075918"
---
# <a name="iagentcommandwindowsetvisible"></a><span data-ttu-id="70ec5-103">IAgentCommandWindow:: SetVisible</span><span class="sxs-lookup"><span data-stu-id="70ec5-103">IAgentCommandWindow::SetVisible</span></span>

<span data-ttu-id="70ec5-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="70ec5-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetVisible(
   long bVisible  // Voice Commands Window Visible setting 
);
```

<span data-ttu-id="70ec5-105">Establezca la propiedad [**visible**](visible-property.md) para la ventana comandos de voz.</span><span class="sxs-lookup"><span data-stu-id="70ec5-105">Set the [**Visible**](visible-property.md) property for the Voice Commands Window.</span></span>

-   <span data-ttu-id="70ec5-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="70ec5-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="70ec5-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span><span class="sxs-lookup"><span data-stu-id="70ec5-107"><span id="bVisible"></span><span id="bvisible"></span><span id="BVISIBLE"></span>*bVisible*</span></span>
</dt> <dd>

<span data-ttu-id="70ec5-108">Configuración de la propiedad [**visible**](visible-property.md) .</span><span class="sxs-lookup"><span data-stu-id="70ec5-108">[**Visible**](visible-property.md) property setting.</span></span> <span data-ttu-id="70ec5-109">Un valor de **true** muestra la ventana comandos de voz. **False** lo oculta.</span><span class="sxs-lookup"><span data-stu-id="70ec5-109">A value of **True** displays the Voice Commands Window; **False** hides it.</span></span>

</dd> </dl>

<span data-ttu-id="70ec5-110">El usuario puede invalidar esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="70ec5-110">The user can override this property.</span></span>

## <a name="see-also"></a><span data-ttu-id="70ec5-111">Consulte también</span><span class="sxs-lookup"><span data-stu-id="70ec5-111">See Also</span></span>

[<span data-ttu-id="70ec5-112">**IAgentCommandWindow:: GetVisible**</span><span class="sxs-lookup"><span data-stu-id="70ec5-112">**IAgentCommandWindow::GetVisible**</span></span>](iagentcommandwindow--getvisible.md)


 

 




