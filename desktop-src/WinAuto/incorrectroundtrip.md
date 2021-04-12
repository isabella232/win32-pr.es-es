---
title: IncorrectRoundTrip
description: IncorrectRoundTrip
ms.assetid: 244537EB-E7DC-49E4-BEAF-CFE3ED25E0B2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1f154c0ccc0fff9bb654b94ef9d0807aa459d4b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104269146"
---
# <a name="incorrectroundtrip"></a><span data-ttu-id="7bbc7-103">IncorrectRoundTrip</span><span class="sxs-lookup"><span data-stu-id="7bbc7-103">IncorrectRoundTrip</span></span>

## <a name="text"></a><span data-ttu-id="7bbc7-104">Texto</span><span class="sxs-lookup"><span data-stu-id="7bbc7-104">Text</span></span>

<span data-ttu-id="7bbc7-105">Llame a accNavigate (haga clic en posponer para que se le vuelva a recordar en:), 1, NAVDIR \_ siguiente) y, después, accNavigate ((abierto), 2, NAVDIR \_ anterior), debe haber devuelto hacer clic en posponer para que se le vuelva a recordar en: (ChildId = 1), pero devolvió hacer clic en posponer para volver a tener en cuenta:</span><span class="sxs-lookup"><span data-stu-id="7bbc7-105">Call to accNavigate((Click Snooze to be reminded again in:), 1, NAVDIR\_NEXT), then accNavigate((Open), 2, NAVDIR\_PREVIOUS), should have returned Click Snooze to be reminded again in:(ChildId=1), but returned Click Snooze to be reminded again in:</span></span>

## <a name="type"></a><span data-ttu-id="7bbc7-106">Tipo</span><span class="sxs-lookup"><span data-stu-id="7bbc7-106">Type</span></span>

<span data-ttu-id="7bbc7-107">Error</span><span class="sxs-lookup"><span data-stu-id="7bbc7-107">Error</span></span>

## <a name="description"></a><span data-ttu-id="7bbc7-108">Descripción</span><span class="sxs-lookup"><span data-stu-id="7bbc7-108">Description</span></span>

<span data-ttu-id="7bbc7-109">el uso de [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) para recorrer el árbol de elementos del destino de la comprobación no devuelve el mismo elemento inicial cuando se invierte la dirección del recorrido.</span><span class="sxs-lookup"><span data-stu-id="7bbc7-109">using [**accNavigate**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate) to traverse the element tree of the verification target does not return the same starting element when the direction of traversal is reversed.</span></span>

![ejemplo de una implementación de MSAA no válida que causó una navegación de ida y vuelta incorrecta](images/accchecker-invalid-round-trip.png)

<span data-ttu-id="7bbc7-111">Este problema puede provocar problemas de navegación en herramientas automatizadas, ya que el recorrido de los elementos puede ser errático e imprevisible.</span><span class="sxs-lookup"><span data-stu-id="7bbc7-111">This issue can cause navigation problems for automated tools because traversing elements might be erratic and unpredictable.</span></span>

## <a name="possible-causes"></a><span data-ttu-id="7bbc7-112">Causas posibles</span><span class="sxs-lookup"><span data-stu-id="7bbc7-112">Possible causes</span></span>

<span data-ttu-id="7bbc7-113">Implementación de MSAA incorrecta o no válida.</span><span class="sxs-lookup"><span data-stu-id="7bbc7-113">An incorrect or invalid MSAA implementation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7bbc7-114">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7bbc7-114">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7bbc7-115">**IAccessible:: accNavigate**</span><span class="sxs-lookup"><span data-stu-id="7bbc7-115">**IAccessible::accNavigate**</span></span>](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-accnavigate)
</dt> </dl>

 

 




