---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d86bbacfed445c5266a299495df5c07fd6166d9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776890"
---
# <a name="iagentpropertysheetsetpage"></a><span data-ttu-id="88ecf-103">IAgentPropertySheet:: SetPage</span><span class="sxs-lookup"><span data-stu-id="88ecf-103">IAgentPropertySheet::SetPage</span></span>

<span data-ttu-id="88ecf-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="88ecf-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

<span data-ttu-id="88ecf-105">Establece la página actual de la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="88ecf-105">Sets the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="88ecf-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="88ecf-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="88ecf-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span><span class="sxs-lookup"><span data-stu-id="88ecf-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span></span>
</dt> <dd>

<span data-ttu-id="88ecf-108">BSTR que establece la página actual de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="88ecf-108">A BSTR that sets the current page of the property.</span></span> <span data-ttu-id="88ecf-109">El parámetro puede ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="88ecf-109">The parameter can be one of the following.</span></span>



|                 |                        |
|-----------------|------------------------|
| <span data-ttu-id="88ecf-110">**Gramatical**</span><span class="sxs-lookup"><span data-stu-id="88ecf-110">**"Speech"**</span></span>    | <span data-ttu-id="88ecf-111">La página de entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="88ecf-111">The Speech Input page.</span></span> |
| <span data-ttu-id="88ecf-112">**Genere**</span><span class="sxs-lookup"><span data-stu-id="88ecf-112">**"Output"**</span></span>    | <span data-ttu-id="88ecf-113">La página de salida.</span><span class="sxs-lookup"><span data-stu-id="88ecf-113">The Output page.</span></span>       |
| <span data-ttu-id="88ecf-114">**SSoftware**</span><span class="sxs-lookup"><span data-stu-id="88ecf-114">**"Copyright"**</span></span> | <span data-ttu-id="88ecf-115">La página Copyright.</span><span class="sxs-lookup"><span data-stu-id="88ecf-115">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="88ecf-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="88ecf-116">See Also</span></span>

[<span data-ttu-id="88ecf-117">**IAgentPropertySheet::GetPage**</span><span class="sxs-lookup"><span data-stu-id="88ecf-117">**IAgentPropertySheet::GetPage**</span></span>](iagentpropertysheet--getpage.md)


 

 




