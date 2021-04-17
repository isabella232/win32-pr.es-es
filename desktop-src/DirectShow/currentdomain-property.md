---
description: La propiedad CurrentDomain recupera el dominio de DVD en el que se encuentra el objeto MSWebDVD.
ms.assetid: 9d545438-9a3d-4c57-a3df-5e75af2e4d1b
title: Propiedad CurrentDomain
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ead6d61cd622fceac2a4d133a0297892992e763a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104495149"
---
# <a name="currentdomain-property"></a><span data-ttu-id="8d2d9-103">Propiedad CurrentDomain</span><span class="sxs-lookup"><span data-stu-id="8d2d9-103">CurrentDomain Property</span></span>

> [!Note]  
> <span data-ttu-id="8d2d9-104">Este componente está disponible para su uso en los sistemas operativos Microsoft Windows 2000, Windows XP y Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="8d2d9-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="8d2d9-105">En versiones posteriores podría modificarse o no estar disponible.</span><span class="sxs-lookup"><span data-stu-id="8d2d9-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="8d2d9-106">La `CurrentDomain` propiedad recupera el dominio de DVD en el que se encuentra el objeto MSWebDVD.</span><span class="sxs-lookup"><span data-stu-id="8d2d9-106">The `CurrentDomain` property retrieves the DVD domain that the MSWebDVD object is in.</span></span>

``` syntax
[ iDomain = ] MSWebDVD.CurrentDomain
```

## <a name="return-value"></a><span data-ttu-id="8d2d9-107">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8d2d9-107">Return Value</span></span>

<span data-ttu-id="8d2d9-108">Devuelve un valor entero que representa el dominio actual.</span><span class="sxs-lookup"><span data-stu-id="8d2d9-108">Returns an integer value representing the current domain.</span></span>

## <a name="remarks"></a><span data-ttu-id="8d2d9-109">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8d2d9-109">Remarks</span></span>

<span data-ttu-id="8d2d9-110">Los valores posibles de la propiedad son:</span><span class="sxs-lookup"><span data-stu-id="8d2d9-110">The possible values of the property are:</span></span>



| <span data-ttu-id="8d2d9-111">Value</span><span class="sxs-lookup"><span data-stu-id="8d2d9-111">Value</span></span> | <span data-ttu-id="8d2d9-112">Descripción</span><span class="sxs-lookup"><span data-stu-id="8d2d9-112">Description</span></span>          |
|-------|----------------------|
| <span data-ttu-id="8d2d9-113">1</span><span class="sxs-lookup"><span data-stu-id="8d2d9-113">1</span></span>     | <span data-ttu-id="8d2d9-114">Primer juego</span><span class="sxs-lookup"><span data-stu-id="8d2d9-114">First play</span></span>           |
| <span data-ttu-id="8d2d9-115">2</span><span class="sxs-lookup"><span data-stu-id="8d2d9-115">2</span></span>     | <span data-ttu-id="8d2d9-116">Menú del administrador de vídeos</span><span class="sxs-lookup"><span data-stu-id="8d2d9-116">Video Manager Menu</span></span>   |
| <span data-ttu-id="8d2d9-117">3</span><span class="sxs-lookup"><span data-stu-id="8d2d9-117">3</span></span>     | <span data-ttu-id="8d2d9-118">Menú de conjunto de títulos de vídeo</span><span class="sxs-lookup"><span data-stu-id="8d2d9-118">Video Title Set Menu</span></span> |
| <span data-ttu-id="8d2d9-119">4</span><span class="sxs-lookup"><span data-stu-id="8d2d9-119">4</span></span>     | <span data-ttu-id="8d2d9-120">Title</span><span class="sxs-lookup"><span data-stu-id="8d2d9-120">Title</span></span>                |
| <span data-ttu-id="8d2d9-121">5</span><span class="sxs-lookup"><span data-stu-id="8d2d9-121">5</span></span>     | <span data-ttu-id="8d2d9-122">Stop</span><span class="sxs-lookup"><span data-stu-id="8d2d9-122">Stop</span></span>                 |



 

<span data-ttu-id="8d2d9-123">Llame a este método para asegurarse de que el navegador de DVD se encuentre en un dominio válido para el método que va a llamar.</span><span class="sxs-lookup"><span data-stu-id="8d2d9-123">Call this method to ensure that the DVD Navigator is in a valid domain for the method you are about to call.</span></span> <span data-ttu-id="8d2d9-124">Por ejemplo, antes de llamar a [**PlayTitle**](playtitle-method.md), Compruebe la `CurrentDomain` propiedad para asegurarse de que el navegador de DVD no se encuentra en el dominio STOP o First Play.</span><span class="sxs-lookup"><span data-stu-id="8d2d9-124">For example, before calling [**PlayTitle**](playtitle-method.md), check the `CurrentDomain` property to make sure that the DVD Navigator is not in the Stop or First Play domain.</span></span>

 

 



