---
description: Las nubes, humo y rastros de vapor se pueden crear mediante una extensión de la técnica de la cartelera.
ms.assetid: c5607327-de46-4241-a01a-4adfe0bbf6fb
title: Nubes, humo y rastros de vapor (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f60bce89e23b2b2aab7affbb6947cab4d11c33ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104564331"
---
# <a name="clouds-smoke-and-vapor-trails-direct3d-9"></a><span data-ttu-id="7df3b-103">Nubes, humo y rastros de vapor (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="7df3b-103">Clouds, Smoke, and Vapor Trails (Direct3D 9)</span></span>

<span data-ttu-id="7df3b-104">Las nubes, humo y rastros de vapor se pueden crear mediante una extensión de la técnica de la cartelera.</span><span class="sxs-lookup"><span data-stu-id="7df3b-104">Clouds, smoke, and vapor trails can all be created by an extension of the billboarding technique.</span></span> <span data-ttu-id="7df3b-105">Vea la [cartelera (Direct3D 9)](billboarding.md).</span><span class="sxs-lookup"><span data-stu-id="7df3b-105">See [Billboarding (Direct3D 9)](billboarding.md).</span></span> <span data-ttu-id="7df3b-106">Al girar la cartelera en dos ejes en lugar de uno, la aplicación puede permitir al usuario ver una cartelera desde cualquier ángulo.</span><span class="sxs-lookup"><span data-stu-id="7df3b-106">By rotating the billboard on two axes instead of one, your application can enable the user to view a billboard from any angle.</span></span> <span data-ttu-id="7df3b-107">Normalmente, una aplicación gira la cartelera en los ejes horizontal y vertical.</span><span class="sxs-lookup"><span data-stu-id="7df3b-107">Typically, an application rotates the billboard on the horizontal and vertical axes.</span></span>

<span data-ttu-id="7df3b-108">Para crear una nube sencilla, la aplicación puede girar un primitivo rectangular en uno o dos ejes para que el primitivo enfrente al usuario.</span><span class="sxs-lookup"><span data-stu-id="7df3b-108">To make a simple cloud, your application can rotate a rectangular primitive on one or two axes so that the primitive faces the user.</span></span> <span data-ttu-id="7df3b-109">Una textura similar a la nube se puede aplicar a la primitiva con transparencia.</span><span class="sxs-lookup"><span data-stu-id="7df3b-109">A cloud-like texture can then be applied to the primitive with transparency.</span></span> <span data-ttu-id="7df3b-110">Para obtener más información sobre cómo aplicar texturas transparentes a primitivos, vea [Texture blending (Direct3D 9)](texture-blending.md).</span><span class="sxs-lookup"><span data-stu-id="7df3b-110">For details on applying transparent textures to primitives, see [Texture Blending (Direct3D 9)](texture-blending.md).</span></span> <span data-ttu-id="7df3b-111">Puede animar la nube aplicando una serie de texturas a lo largo del tiempo.</span><span class="sxs-lookup"><span data-stu-id="7df3b-111">You can animate the cloud by applying a series of textures over time.</span></span>

<span data-ttu-id="7df3b-112">Una aplicación puede crear nubes más complejas formando un grupo de primitivas.</span><span class="sxs-lookup"><span data-stu-id="7df3b-112">An application can create more complex clouds by forming them from a group of primitives.</span></span> <span data-ttu-id="7df3b-113">Cada parte de la nube es un primitivo rectangular.</span><span class="sxs-lookup"><span data-stu-id="7df3b-113">Each part of the cloud is a rectangular primitive.</span></span> <span data-ttu-id="7df3b-114">Los primitivos se pueden moverse de forma independiente a lo largo del tiempo para dar la apariencia de una niebla dinámica.</span><span class="sxs-lookup"><span data-stu-id="7df3b-114">The primitives can be moved independently over time to give the appearance of a dynamic mist.</span></span> <span data-ttu-id="7df3b-115">En la ilustración siguiente se muestra este concepto.</span><span class="sxs-lookup"><span data-stu-id="7df3b-115">The following illustration shows this concept.</span></span>

![Ilustración de primitivas que forman nubes más complejas](images/cloud.png)

<span data-ttu-id="7df3b-117">La apariencia del humo se muestra de manera similar a las nubes.</span><span class="sxs-lookup"><span data-stu-id="7df3b-117">The appearance of smoke is displayed in a manner similar to clouds.</span></span> <span data-ttu-id="7df3b-118">Normalmente requiere varias cartelera, como nubes complejas.</span><span class="sxs-lookup"><span data-stu-id="7df3b-118">It typically requires multiple billboards, like complex clouds.</span></span> <span data-ttu-id="7df3b-119">El humo normalmente Billows y aumenta con el tiempo, por lo que las cartelera que conforman el humo deben moverse en consecuencia.</span><span class="sxs-lookup"><span data-stu-id="7df3b-119">Smoke usually billows and rises over time, so the billboards that make up the smoke plume need to move accordingly.</span></span> <span data-ttu-id="7df3b-120">Es posible que tenga que agregar más cartelera a medida que la ciruela aumenta y se dispersa.</span><span class="sxs-lookup"><span data-stu-id="7df3b-120">You may need to add more billboards as the plume rises and disperses.</span></span>

<span data-ttu-id="7df3b-121">Un rastro de vapor es una ciruela de humo que no aumenta.</span><span class="sxs-lookup"><span data-stu-id="7df3b-121">A vapor trail is a smoke plume that doesn't rise.</span></span> <span data-ttu-id="7df3b-122">Sin embargo, al igual que un humo, se dispersa con el tiempo.</span><span class="sxs-lookup"><span data-stu-id="7df3b-122">However, like a smoke plume, it disperses over time.</span></span> <span data-ttu-id="7df3b-123">En la ilustración siguiente se muestra la técnica de uso de las cartelera para simular una pista de vapor.</span><span class="sxs-lookup"><span data-stu-id="7df3b-123">The following illustration shows the technique of using billboards to simulate a vapor trail.</span></span>

![Ilustración de las cartelera que simulan un rastro de vapor](images/vapor.png)

## <a name="related-topics"></a><span data-ttu-id="7df3b-125">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="7df3b-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7df3b-126">Ejemplos de alfa</span><span class="sxs-lookup"><span data-stu-id="7df3b-126">Alpha Examples</span></span>](alpha-examples.md)
</dt> </dl>

 

 



