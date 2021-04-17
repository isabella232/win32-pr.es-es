---
description: El volteo de páginas es importante en el software multimedia, de animación y de juegos. es análogo a la forma en que se puede realizar la animación con un panel de papel.
ms.assetid: b6824962-c7cb-4e7f-8731-2971b0d9a2b0
title: Intercambio de páginas y almacenamiento en búfer de retroceso (Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bffad581c5d4250c7f36980ba1f278a9f770912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/06/2021
ms.locfileid: "105714689"
---
# <a name="page-flipping-and-back-buffering-direct3d-9"></a><span data-ttu-id="2ced0-103">Intercambio de páginas y almacenamiento en búfer de retroceso (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2ced0-103">Page Flipping and Back Buffering (Direct3D 9)</span></span>

<span data-ttu-id="2ced0-104">El volteo de páginas es importante en el software multimedia, de animación y de juegos. es análogo a la forma en que se puede realizar la animación con un panel de papel.</span><span class="sxs-lookup"><span data-stu-id="2ced0-104">Page flipping is key in multimedia, animation, and game software; it is analogous to the way you can do animation with a pad of paper.</span></span> <span data-ttu-id="2ced0-105">En cada página, el artista cambia ligeramente la figura, de modo que cuando se gira rápidamente entre las hojas, el dibujo aparece animado.</span><span class="sxs-lookup"><span data-stu-id="2ced0-105">On each page, the artist changes the figure slightly, so that when you flip rapidly between sheets, the drawing appears animated.</span></span>

<span data-ttu-id="2ced0-106">El volteo de páginas del software es similar a este proceso.</span><span class="sxs-lookup"><span data-stu-id="2ced0-106">Page flipping in software is similar to this process.</span></span> <span data-ttu-id="2ced0-107">Direct3D implementa la funcionalidad de volteo de páginas a través de una cadena de intercambio, que es una propiedad del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="2ced0-107">Direct3D implements page flipping functionality through a swap chain, which is a property of the device.</span></span> <span data-ttu-id="2ced0-108">Inicialmente, se configura una serie de búferes de Direct3D que se voltean a la pantalla en la forma en que el papel del artista se mueve a la página siguiente.</span><span class="sxs-lookup"><span data-stu-id="2ced0-108">Initially, you set up a series of Direct3D buffers that flip to the screen in the way that the artist's paper flips to the next page.</span></span> <span data-ttu-id="2ced0-109">El primer búfer se conoce como el búfer frontal de color.</span><span class="sxs-lookup"><span data-stu-id="2ced0-109">The first buffer is referred to as the color front buffer.</span></span> <span data-ttu-id="2ced0-110">Los búferes subyacentes se denominan búferes de reserva.</span><span class="sxs-lookup"><span data-stu-id="2ced0-110">The buffers behind it are called back buffers.</span></span> <span data-ttu-id="2ced0-111">La aplicación escribe en un búfer de reserva y, a continuación, voltea el búfer frontal de color para que el búfer de reserva aparezca en la pantalla.</span><span class="sxs-lookup"><span data-stu-id="2ced0-111">Your application writes to a back buffer and then flips the color front buffer so that the back buffer appears on screen.</span></span> <span data-ttu-id="2ced0-112">Mientras el sistema muestra la imagen, el software vuelve a escribir en un búfer de reserva.</span><span class="sxs-lookup"><span data-stu-id="2ced0-112">While the system displays the image, your software is again writing to a back buffer.</span></span> <span data-ttu-id="2ced0-113">El proceso continúa mientras se anima, lo que permite animar imágenes de forma eficaz.</span><span class="sxs-lookup"><span data-stu-id="2ced0-113">The process continues as long as you are animating, enabling you to animate images efficiently.</span></span>

<span data-ttu-id="2ced0-114">Direct3D facilita la configuración de esquemas de volteo de páginas: desde un simple esquema de doble búfer (un búfer frontal de color con un búfer de reserva) a esquemas más sofisticados con búferes de reserva adicionales.</span><span class="sxs-lookup"><span data-stu-id="2ced0-114">Direct3D makes it easy to set up page flipping schemes - from a simple double-buffered scheme (a color front buffer with one back buffer) to more sophisticated schemes with additional back buffers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2ced0-115">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="2ced0-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2ced0-116">Superficies de Direct3D</span><span class="sxs-lookup"><span data-stu-id="2ced0-116">Direct3D Surfaces</span></span>](direct3d-surfaces.md)
</dt> <dt>

[<span data-ttu-id="2ced0-117">¿Qué es una cadena de intercambio? (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="2ced0-117">What Is a Swap Chain? (Direct3D 9)</span></span>](what-is-a-swap-chain-.md)
</dt> </dl>

 

 



