---
description: Identificación de las operaciones de DVD válidas
ms.assetid: d368b552-7ed3-4334-b97b-ff49d6c331c3
title: Identificación de las operaciones de DVD válidas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 444595e402dc73a3468946b820f031dabaecc2f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "104423036"
---
# <a name="identifying-valid-dvd-operations"></a><span data-ttu-id="c7e5d-103">Identificación de las operaciones de DVD válidas</span><span class="sxs-lookup"><span data-stu-id="c7e5d-103">Identifying Valid DVD Operations</span></span>

<span data-ttu-id="c7e5d-104">Algunos factores determinan si se puede realizar una operación de DVD determinada:</span><span class="sxs-lookup"><span data-stu-id="c7e5d-104">Several factors determine whether you can perform a given DVD operation:</span></span>

-   <span data-ttu-id="c7e5d-105">Dominio actual.</span><span class="sxs-lookup"><span data-stu-id="c7e5d-105">The current domain.</span></span> <span data-ttu-id="c7e5d-106">Algunos comandos solo son válidos en determinados dominios.</span><span class="sxs-lookup"><span data-stu-id="c7e5d-106">Some commands are only valid in certain domains.</span></span> <span data-ttu-id="c7e5d-107">Cuando el dominio cambia, el navegador envía un evento de cambio de dominio de DVD de EC \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="c7e5d-107">When the domain changes, the navigator sends an EC\_DVD\_DOMAIN\_CHANGE event.</span></span> <span data-ttu-id="c7e5d-108">También puede llamar a [**IDvdInfo2:: GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) para obtener el dominio actual.</span><span class="sxs-lookup"><span data-stu-id="c7e5d-108">You can also call [**IDvdInfo2::GetCurrentDomain**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentdomain) to get the current domain.</span></span>
-   <span data-ttu-id="c7e5d-109">Marcas de UOPS.</span><span class="sxs-lookup"><span data-stu-id="c7e5d-109">UOPS flags.</span></span> <span data-ttu-id="c7e5d-110">Se trata de marcas escritas en el disco que indican qué operaciones se permiten.</span><span class="sxs-lookup"><span data-stu-id="c7e5d-110">These are flags written onto the disc that indicate which operations are permitted.</span></span> <span data-ttu-id="c7e5d-111">Cada vez que cambian las marcas, el navegador envía \_ un \_ \_ evento de cambio UOPS válido de un DVD \_ con las nuevas marcas.</span><span class="sxs-lookup"><span data-stu-id="c7e5d-111">Whenever the flags change, the navigator sends a EC\_DVD\_VALID\_UOPS\_CHANGE event with the new flags.</span></span> <span data-ttu-id="c7e5d-112">También puede llamar a [**IDvdInfo2:: GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) para obtener las marcas UOPS actuales.</span><span class="sxs-lookup"><span data-stu-id="c7e5d-112">You can also call [**IDvdInfo2::GetCurrentUOPS**](/windows/desktop/api/Strmif/nf-strmif-idvdinfo2-getcurrentuops) to get the current UOPS flags.</span></span>
-   <span data-ttu-id="c7e5d-113">Contenido del DVD.</span><span class="sxs-lookup"><span data-stu-id="c7e5d-113">DVD content.</span></span> <span data-ttu-id="c7e5d-114">Es posible que algunos comandos no sean relevantes en función del contenido del DVD.</span><span class="sxs-lookup"><span data-stu-id="c7e5d-114">Some commands may not be relevant based on the content of the DVD.</span></span> <span data-ttu-id="c7e5d-115">Por ejemplo, el método [**IDvdControl2:: SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) podría estar permitido según el dominio actual y las marcas UOPS, pero el vídeo puede tener solo un ángulo.</span><span class="sxs-lookup"><span data-stu-id="c7e5d-115">For example, the [**IDvdControl2::SelectAngle**](/windows/desktop/api/Strmif/nf-strmif-idvdcontrol2-selectangle) method might be permitted according to the current domain and UOPS flags, yet the video might have only one angle.</span></span> <span data-ttu-id="c7e5d-116">En ese caso, se permite la llamada **SelectAngle** , pero no es una opción significativa.</span><span class="sxs-lookup"><span data-stu-id="c7e5d-116">In that case, the **SelectAngle** call is permitted but is not a meaningful option.</span></span>

<span data-ttu-id="c7e5d-117">En casos de duda, permita una acción.</span><span class="sxs-lookup"><span data-stu-id="c7e5d-117">When in doubt, permit an action.</span></span> <span data-ttu-id="c7e5d-118">En el peor de los demás, se producirá un error en el método [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) y podrá enviar comentarios al usuario.</span><span class="sxs-lookup"><span data-stu-id="c7e5d-118">At worst, the [**IDvdControl2**](/windows/desktop/api/Strmif/nn-strmif-idvdcontrol2) method will fail and you can give feedback to the user.</span></span> <span data-ttu-id="c7e5d-119">Los comentarios deben ser relativamente discretos.</span><span class="sxs-lookup"><span data-stu-id="c7e5d-119">The feedback should be relatively unobtrusive.</span></span> <span data-ttu-id="c7e5d-120">Por ejemplo, puede que parpadee una X roja pequeña para alertar al usuario.</span><span class="sxs-lookup"><span data-stu-id="c7e5d-120">For example, you might flash a small red X to alert the user.</span></span> <span data-ttu-id="c7e5d-121">El navegador de DVD devuelve VFW \_ e \_ DVD \_ invaliddomain le cuando el dominio prohíbe una operación y \_ la operación VFW e \_ DVD se \_ \_ impide cuando las marcas de UOPS prohíben una operación.</span><span class="sxs-lookup"><span data-stu-id="c7e5d-121">The DVD Navigator returns VFW\_E\_DVD\_INVALIDDOMAIN when the domain prohibits an operation, and VFW\_E\_DVD\_OPERATION\_INHIBITED when the UOPS flags prohibit an operation.</span></span>

## <a name="related-topics"></a><span data-ttu-id="c7e5d-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="c7e5d-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c7e5d-123">Aplicaciones de DVD</span><span class="sxs-lookup"><span data-stu-id="c7e5d-123">DVD Applications</span></span>](dvd-applications.md)
</dt> </dl>

 

 



