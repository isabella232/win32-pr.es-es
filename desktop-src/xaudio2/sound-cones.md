---
description: Modelo que describe la sonoridad del sonido orientado.
ms.assetid: 15252358-d932-22f4-f13a-8e4b8487dd86
title: Conos de sonido
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 215659ab08c33066abfade2faf206f6360a51051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105707126"
---
# <a name="sound-cones"></a><span data-ttu-id="3b126-103">Conos de sonido</span><span class="sxs-lookup"><span data-stu-id="3b126-103">Sound Cones</span></span>

<span data-ttu-id="3b126-104">Modelo que describe la sonoridad del sonido orientado.</span><span class="sxs-lookup"><span data-stu-id="3b126-104">A model that describes the loudness of oriented sound.</span></span>

<span data-ttu-id="3b126-105">Un sonido sin orientación tiene la misma amplitud a una distancia determinada en todas las direcciones.</span><span class="sxs-lookup"><span data-stu-id="3b126-105">A sound with no orientation has the same amplitude at a given distance in all directions.</span></span> <span data-ttu-id="3b126-106">Un sonido con una orientación es lo más alto en la dirección de la orientación.</span><span class="sxs-lookup"><span data-stu-id="3b126-106">A sound with an orientation is loudest in the direction of orientation.</span></span> <span data-ttu-id="3b126-107">El modelo que describe la sonoridad del sonido orientado se denomina cono de sonido.</span><span class="sxs-lookup"><span data-stu-id="3b126-107">The model that describes the loudness of the oriented sound is called a sound cone.</span></span> <span data-ttu-id="3b126-108">Los conos de sonido se componen de un cono interior (o interno) y un cono exterior (o externo).</span><span class="sxs-lookup"><span data-stu-id="3b126-108">Sound cones are made up of an inside (or inner) cone and an outside (or outer) cone.</span></span> <span data-ttu-id="3b126-109">El ángulo del cono exterior siempre debe ser igual o mayor que el ángulo del cono interior.</span><span class="sxs-lookup"><span data-stu-id="3b126-109">The outside cone angle must always be equal to or greater than the inside cone angle.</span></span>

<span data-ttu-id="3b126-110">En cualquier ángulo del cono interior, el volumen del sonido se establece en el volumen del cono interno.</span><span class="sxs-lookup"><span data-stu-id="3b126-110">At any angle within the inner cone, the volume of the sound is set to the inner cone volume.</span></span> <span data-ttu-id="3b126-111">Esto tiene en cuenta el volumen básico del búfer, la distancia del agente de escucha, la orientación del agente de escucha si el agente de escucha tiene su propio cono y así sucesivamente.</span><span class="sxs-lookup"><span data-stu-id="3b126-111">This takes into account the basic volume of the buffer, the distance from the listener, the listener's orientation if the listener has its own cone, and so on.</span></span>

<span data-ttu-id="3b126-112">En cualquier ángulo fuera del cono exterior, el volumen normal se atenúa por un factor establecido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b126-112">At any angle outside the outer cone, the normal volume is attenuated by a factor set by the application.</span></span> <span data-ttu-id="3b126-113">El nivel de volumen del cono exterior se expresa como una amplitud lineal Scaler: 1,0 f no representa ninguna atenuación aplicada a la señal original, 0,5 f denota una atenuación de 6 dB y 0,0 f da como resultado el silencio.</span><span class="sxs-lookup"><span data-stu-id="3b126-113">The outside cone volume level is expressed as a linear amplitude scaler: 1.0 f represents no attenuation applied to the original signal, 0.5 f denotes an attenuation of 6 dB, and 0.0 f results in silence.</span></span> <span data-ttu-id="3b126-114">También se permite la amplificación (volumen > 1,0 f) y no está fija.</span><span class="sxs-lookup"><span data-stu-id="3b126-114">Amplification (volume > 1.0 f) is also allowed, and is not clamped.</span></span> <span data-ttu-id="3b126-115">El intervalo de volumen válido es, en realidad, de 0,0 a 2,0 f.</span><span class="sxs-lookup"><span data-stu-id="3b126-115">The valid volume range is actually 0.0 f to 2.0 f.</span></span>

<span data-ttu-id="3b126-116">Entre los conos interno y externo hay una zona de transición desde el volumen interior al volumen exterior.</span><span class="sxs-lookup"><span data-stu-id="3b126-116">Between the inner and outer cones is a zone of transition from the inside volume to the outside volume.</span></span> <span data-ttu-id="3b126-117">El volumen se aproxima al volumen exterior del cono a medida que aumenta el ángulo.</span><span class="sxs-lookup"><span data-stu-id="3b126-117">The volume approaches the cone's outer volume as the angle increases.</span></span>

<span data-ttu-id="3b126-118">Los conos pueden afectar a los parámetros distintos del volumen.</span><span class="sxs-lookup"><span data-stu-id="3b126-118">Cones can affect parameters other than volume.</span></span> <span data-ttu-id="3b126-119">El filtro de paso bajo y el nivel de envío de reverberación también se pueden ver afectados, por lo que la técnica es aún más espectacular.</span><span class="sxs-lookup"><span data-stu-id="3b126-119">Low pass filter and reverb send level may also be affected, making the technique even more dramatic.</span></span> <span data-ttu-id="3b126-120">Por ejemplo, con un cono en el agente de escucha, puede especificar que todos los sonidos detrás del agente de escucha se queden sin silenciar y que tengan un contenido de posición de reverberación a directo ligeramente superior.</span><span class="sxs-lookup"><span data-stu-id="3b126-120">For example, with a cone on the listener, one can specify all sounds behind the listener get a bit muffled, and have slightly higher reverb-to-direct ratio content.</span></span> <span data-ttu-id="3b126-121">Proporcionan más indicios de que el sonido está detrás del usuario.</span><span class="sxs-lookup"><span data-stu-id="3b126-121">These provide more cues that the sound is behind the user.</span></span> <span data-ttu-id="3b126-122">Esto mejora el realismo.</span><span class="sxs-lookup"><span data-stu-id="3b126-122">This enhances realism.</span></span>

<span data-ttu-id="3b126-123">En la ilustración siguiente se muestra el concepto de conos de sonido.</span><span class="sxs-lookup"><span data-stu-id="3b126-123">The following illustration shows the concept of sound cones.</span></span>

![conos de sonido](images/common-audio-concepts-sound-cones.png)

<span data-ttu-id="3b126-125">El diseño correcto de los conos de sonido puede agregar efectos drásticos a la aplicación.</span><span class="sxs-lookup"><span data-stu-id="3b126-125">Designing sound cones properly can add dramatic effects to your application.</span></span> <span data-ttu-id="3b126-126">Por ejemplo, podría colocar un origen de sonido en el centro de una habitación y establecer su orientación hacia una puerta abierta en un vestíbulo.</span><span class="sxs-lookup"><span data-stu-id="3b126-126">For example, you could position a sound source in the center of a room, setting its orientation toward an open door in a hallway.</span></span> <span data-ttu-id="3b126-127">A continuación, establezca el ángulo del cono interior de modo que se extienda hasta el ancho de la puerta, haga que el cono exterior sea un poco más amplio y, por último, establezca el volumen del cono exterior en inaudible.</span><span class="sxs-lookup"><span data-stu-id="3b126-127">Then set the angle of the inside cone so that it extends to the width of the doorway, make the outside cone a bit wider, and finally set the outside cone volume to inaudible.</span></span> <span data-ttu-id="3b126-128">Un agente de escucha que se mueve a lo largo del vestíbulo comenzará a oír el sonido solo cuando esté cerca de la puerta.</span><span class="sxs-lookup"><span data-stu-id="3b126-128">A listener moving along the hallway will begin to hear the sound only when near the doorway.</span></span> <span data-ttu-id="3b126-129">El sonido será más alto a medida que el agente de escucha pase delante de la puerta abierta.</span><span class="sxs-lookup"><span data-stu-id="3b126-129">The sound will be loudest as the listener passes in front of the open door.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3b126-130">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3b126-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3b126-131">Conceptos de audio comunes</span><span class="sxs-lookup"><span data-stu-id="3b126-131">Common Audio Concepts</span></span>](common-audio-concepts.md)
</dt> <dt>

[<span data-ttu-id="3b126-132">X3DAudio</span><span class="sxs-lookup"><span data-stu-id="3b126-132">X3DAudio</span></span>](x3daudio-overview.md)
</dt> <dt>

[<span data-ttu-id="3b126-133">**\_Cono X3DAUDIO**</span><span class="sxs-lookup"><span data-stu-id="3b126-133">**X3DAUDIO\_CONE**</span></span>](/windows/desktop/api/x3daudio/ns-x3daudio-x3daudio_cone)
</dt> </dl>

 

 



