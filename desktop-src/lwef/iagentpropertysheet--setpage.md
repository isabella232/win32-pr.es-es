---
title: IAgentPropertySheet SetPage
description: IAgentPropertySheet SetPage
ms.assetid: 52451a45-4f05-4209-ac3a-b4f2d90b3e74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b84f9b9d5f74170644488cc2049376ecf409997
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113120750"
---
# <a name="iagentpropertysheetsetpage"></a><span data-ttu-id="5eb46-103">IAgentPropertySheet::SetPage</span><span class="sxs-lookup"><span data-stu-id="5eb46-103">IAgentPropertySheet::SetPage</span></span>

<span data-ttu-id="5eb46-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="5eb46-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT SetPage(
   BSTR bszPage  // current property page
);
```

<span data-ttu-id="5eb46-105">Establece la página actual de la hoja de propiedades de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="5eb46-105">Sets the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="5eb46-106">Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="5eb46-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="5eb46-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span><span class="sxs-lookup"><span data-stu-id="5eb46-107"><span id="bszPage"></span><span id="bszpage"></span><span id="BSZPAGE"></span>*bszPage*</span></span>
</dt> <dd>

<span data-ttu-id="5eb46-108">BSTR que establece la página actual de la propiedad.</span><span class="sxs-lookup"><span data-stu-id="5eb46-108">A BSTR that sets the current page of the property.</span></span> <span data-ttu-id="5eb46-109">El parámetro puede ser uno de los siguientes.</span><span class="sxs-lookup"><span data-stu-id="5eb46-109">The parameter can be one of the following.</span></span>



|                 | <span data-ttu-id="5eb46-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="5eb46-110">Description</span></span>            |
|-----------------|------------------------|
| <span data-ttu-id="5eb46-111">**"Voz"**</span><span class="sxs-lookup"><span data-stu-id="5eb46-111">**"Speech"**</span></span>    | <span data-ttu-id="5eb46-112">Página Entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="5eb46-112">The Speech Input page.</span></span> |
| <span data-ttu-id="5eb46-113">**"Salida"**</span><span class="sxs-lookup"><span data-stu-id="5eb46-113">**"Output"**</span></span>    | <span data-ttu-id="5eb46-114">Página Salida.</span><span class="sxs-lookup"><span data-stu-id="5eb46-114">The Output page.</span></span>       |
| <span data-ttu-id="5eb46-115">**"Copyright"**</span><span class="sxs-lookup"><span data-stu-id="5eb46-115">**"Copyright"**</span></span> | <span data-ttu-id="5eb46-116">Página Copyright.</span><span class="sxs-lookup"><span data-stu-id="5eb46-116">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="5eb46-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="5eb46-117">See Also</span></span>

[<span data-ttu-id="5eb46-118">**IAgentPropertySheet::GetPage**</span><span class="sxs-lookup"><span data-stu-id="5eb46-118">**IAgentPropertySheet::GetPage**</span></span>](iagentpropertysheet--getpage.md)


 

 




