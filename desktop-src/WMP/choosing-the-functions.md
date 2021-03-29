---
title: Elección de las funciones
description: Elección de las funciones
ms.assetid: ded3c578-5087-4e4f-bf21-2149cf72719d
keywords:
- Máscaras móviles de Windows Media Player, funciones para audio
- máscaras, funciones para audio
- crear máscaras, funciones para audio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a139dc21a7d10847a7920955988ec2b02fced0f3
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104419055"
---
# <a name="choosing-the-functions"></a><span data-ttu-id="af941-106">Elección de las funciones</span><span class="sxs-lookup"><span data-stu-id="af941-106">Choosing the Functions</span></span>

<span data-ttu-id="af941-107">La finalidad de esta máscara es proporcionar la funcionalidad básica para reproducir audio.</span><span class="sxs-lookup"><span data-stu-id="af941-107">The purpose of this skin is to provide basic functionality for playing audio.</span></span> <span data-ttu-id="af941-108">Se usarán las siguientes funciones:</span><span class="sxs-lookup"><span data-stu-id="af941-108">The following functions will be used:</span></span>



| <span data-ttu-id="af941-109">Función</span><span class="sxs-lookup"><span data-stu-id="af941-109">Function</span></span>                     | <span data-ttu-id="af941-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="af941-110">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                          |
|------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="af941-111">PlayPause o PlayPauseStop\*</span><span class="sxs-lookup"><span data-stu-id="af941-111">PlayPause or PlayPauseStop\*</span></span> | <span data-ttu-id="af941-112">El inicio del elemento multimedia es de importancia primordial.</span><span class="sxs-lookup"><span data-stu-id="af941-112">Starting the media item is of prime importance.</span></span> <span data-ttu-id="af941-113">Si va a crear una máscara para Windows Media Player 10 Mobile o posterior, debe utilizar PlayPauseStop.</span><span class="sxs-lookup"><span data-stu-id="af941-113">If you are creating a skin for Windows Media Player 10 Mobile or later, then you should use PlayPauseStop.</span></span> <span data-ttu-id="af941-114">Si está trabajando con una versión anterior de Windows Media Player Mobile, debe usar PlayPause.</span><span class="sxs-lookup"><span data-stu-id="af941-114">If you are working with an earlier version of Windows Media Player Mobile, then you must use PlayPause.</span></span> <span data-ttu-id="af941-115">Ambas funciones ofrecen la funcionalidad agregada de pausar, pero solo PlayPauseStop permite detener una difusión en directo cuando no está disponible la funcionalidad de pausa.</span><span class="sxs-lookup"><span data-stu-id="af941-115">Both functions give you the added functionality of pausing, but only PlayPauseStop allows you to stop a live broadcast when pause functionality is not available.</span></span> |
| <span data-ttu-id="af941-116">Stop</span><span class="sxs-lookup"><span data-stu-id="af941-116">Stop</span></span>                         | <span data-ttu-id="af941-117">Querrá agregar STOP para detener la reproducción del elemento.</span><span class="sxs-lookup"><span data-stu-id="af941-117">You will want to add Stop to stop playing the item.</span></span> <span data-ttu-id="af941-118">Si va a crear una máscara para Windows Media Player 10 Mobile o posterior, la función PlayPauseStop ya proporciona esta funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="af941-118">If you are creating a skin for Windows Media Player 10 Mobile or later, the PlayPauseStop function already provides this functionality.</span></span>                                                                                                                                                                                                                                          |
| <span data-ttu-id="af941-119">Siguientes</span><span class="sxs-lookup"><span data-stu-id="af941-119">Next</span></span>                         | <span data-ttu-id="af941-120">Si tiene una lista de reproducción, querrá poder elegir el elemento siguiente.</span><span class="sxs-lookup"><span data-stu-id="af941-120">If you have a playlist, you will want to be able to choose the next item.</span></span> <span data-ttu-id="af941-121">Lo necesita para la navegación básica de los medios digitales.</span><span class="sxs-lookup"><span data-stu-id="af941-121">You need this for basic navigation of digital media.</span></span>                                                                                                                                                                                                                                                                                                       |
| <span data-ttu-id="af941-122">Anterior</span><span class="sxs-lookup"><span data-stu-id="af941-122">Prev</span></span>                         | <span data-ttu-id="af941-123">Aunque podría usar Next para desplazarse por la lista de reproducción hasta que llegó al principio, al agregar Prev, se facilitará que el usuario se desplace hacia atrás y hacia delante al navegar por la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="af941-123">While you could use Next to cycle through the playlist until you came to the beginning, adding Prev will make it easy for the user to go backward as well as forward when navigating the playlist.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="af941-124">VolumeUp o VolumeDown\*</span><span class="sxs-lookup"><span data-stu-id="af941-124">VolumeUp or VolumeDown\*</span></span>     | <span data-ttu-id="af941-125">Querrá proporcionar al usuario la capacidad de activar o desactivar el volumen.</span><span class="sxs-lookup"><span data-stu-id="af941-125">You will want to provide the user with the ability to turn the volume up or down.</span></span>                                                                                                                                                                                                                                                                                                                                                    |



 

<span data-ttu-id="af941-126">\*Disponible para Windows Media Player 10 Mobile o posterior.</span><span class="sxs-lookup"><span data-stu-id="af941-126">\*Available for Windows Media Player 10 Mobile or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="af941-127">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="af941-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="af941-128">**Guía de máscara**</span><span class="sxs-lookup"><span data-stu-id="af941-128">**Skin Guide**</span></span>](skin-guide.md)
</dt> </dl>

 

 




