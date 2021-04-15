---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4fb1fe6cdf6f667011eb048625349f6905913a16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418773"
---
# <a name="iagentpropertysheetgetpage"></a><span data-ttu-id="2430c-103">IAgentPropertySheet::GetPage</span><span class="sxs-lookup"><span data-stu-id="2430c-103">IAgentPropertySheet::GetPage</span></span>

<span data-ttu-id="2430c-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede que no esté disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2430c-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

<span data-ttu-id="2430c-105">Recupera la página actual de la hoja de propiedades del agente de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="2430c-105">Retrieves the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="2430c-106">Devuelve S \_ OK para indicar que la operación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="2430c-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2430c-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span><span class="sxs-lookup"><span data-stu-id="2430c-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span></span>
</dt> <dd>

<span data-ttu-id="2430c-108">Dirección de una variable que recibe la página actual de la hoja de propiedades (última página que se vio si la ventana no está abierta).</span><span class="sxs-lookup"><span data-stu-id="2430c-108">Address of a variable that receives the current page of the property sheet (last viewed page if the window is not open).</span></span> <span data-ttu-id="2430c-109">El parámetro puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2430c-109">The parameter can be one of the following:</span></span>



|                 |                        |
|-----------------|------------------------|
| <span data-ttu-id="2430c-110">**Gramatical**</span><span class="sxs-lookup"><span data-stu-id="2430c-110">**"Speech"**</span></span>    | <span data-ttu-id="2430c-111">La página de entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="2430c-111">The Speech Input page.</span></span> |
| <span data-ttu-id="2430c-112">**Genere**</span><span class="sxs-lookup"><span data-stu-id="2430c-112">**"Output"**</span></span>    | <span data-ttu-id="2430c-113">La página de salida.</span><span class="sxs-lookup"><span data-stu-id="2430c-113">The Output page.</span></span>       |
| <span data-ttu-id="2430c-114">**SSoftware**</span><span class="sxs-lookup"><span data-stu-id="2430c-114">**"Copyright"**</span></span> | <span data-ttu-id="2430c-115">La página Copyright.</span><span class="sxs-lookup"><span data-stu-id="2430c-115">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="2430c-116">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2430c-116">See Also</span></span>

[<span data-ttu-id="2430c-117">**IAgentPropertySheet:: SetPage**</span><span class="sxs-lookup"><span data-stu-id="2430c-117">**IAgentPropertySheet::SetPage**</span></span>](iagentpropertysheet--setpage.md)


 

 




