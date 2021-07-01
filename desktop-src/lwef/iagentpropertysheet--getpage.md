---
title: IAgentPropertySheet GetPage
description: IAgentPropertySheet GetPage
ms.assetid: 40d00e9b-dd81-4e23-907a-6ca24a28fa95
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7c08e564b5170d62cf5757536b9e11baec4883c
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119870"
---
# <a name="iagentpropertysheetgetpage"></a><span data-ttu-id="2ecb1-103">IAgentPropertySheet::GetPage</span><span class="sxs-lookup"><span data-stu-id="2ecb1-103">IAgentPropertySheet::GetPage</span></span>

<span data-ttu-id="2ecb1-104">\[Microsoft Agent está en desuso a partir de Windows 7 y puede no estar disponible en versiones posteriores de Windows.\]</span><span class="sxs-lookup"><span data-stu-id="2ecb1-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT GetPage(
BSTR * pbszPage  // address of variable for current property page
);
```

<span data-ttu-id="2ecb1-105">Recupera la página actual de la hoja de propiedades de Microsoft Agent.</span><span class="sxs-lookup"><span data-stu-id="2ecb1-105">Retrieves the current page of the Microsoft Agent property sheet.</span></span>

-   <span data-ttu-id="2ecb1-106">Devuelve S \_ OK para indicar que la operación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="2ecb1-106">Returns S\_OK to indicate the operation was successful.</span></span>

<dl> <dt>

<span data-ttu-id="2ecb1-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span><span class="sxs-lookup"><span data-stu-id="2ecb1-107"><span id="pbszPage"></span><span id="pbszpage"></span><span id="PBSZPAGE"></span>*pbszPage*</span></span>
</dt> <dd>

<span data-ttu-id="2ecb1-108">Dirección de una variable que recibe la página actual de la hoja de propiedades (última página vista si la ventana no está abierta).</span><span class="sxs-lookup"><span data-stu-id="2ecb1-108">Address of a variable that receives the current page of the property sheet (last viewed page if the window is not open).</span></span> <span data-ttu-id="2ecb1-109">El parámetro puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="2ecb1-109">The parameter can be one of the following:</span></span>



|                 | <span data-ttu-id="2ecb1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="2ecb1-110">Description</span></span>            |
|-----------------|------------------------|
| <span data-ttu-id="2ecb1-111">**"Voz"**</span><span class="sxs-lookup"><span data-stu-id="2ecb1-111">**"Speech"**</span></span>    | <span data-ttu-id="2ecb1-112">Página Entrada de voz.</span><span class="sxs-lookup"><span data-stu-id="2ecb1-112">The Speech Input page.</span></span> |
| <span data-ttu-id="2ecb1-113">**"Salida"**</span><span class="sxs-lookup"><span data-stu-id="2ecb1-113">**"Output"**</span></span>    | <span data-ttu-id="2ecb1-114">Página Salida.</span><span class="sxs-lookup"><span data-stu-id="2ecb1-114">The Output page.</span></span>       |
| <span data-ttu-id="2ecb1-115">**"Copyright"**</span><span class="sxs-lookup"><span data-stu-id="2ecb1-115">**"Copyright"**</span></span> | <span data-ttu-id="2ecb1-116">Página Copyright.</span><span class="sxs-lookup"><span data-stu-id="2ecb1-116">The Copyright page.</span></span>    |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="2ecb1-117">Consulte también</span><span class="sxs-lookup"><span data-stu-id="2ecb1-117">See Also</span></span>

[<span data-ttu-id="2ecb1-118">**IAgentPropertySheet::SetPage**</span><span class="sxs-lookup"><span data-stu-id="2ecb1-118">**IAgentPropertySheet::SetPage**</span></span>](iagentpropertysheet--setpage.md)


 

 




