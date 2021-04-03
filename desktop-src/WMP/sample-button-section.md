---
title: Sección de botón de ejemplo
description: Sección de botón de ejemplo
ms.assetid: 52358f83-8c74-4957-87c4-ca1ed7f667fc
keywords:
- Aspectos de Windows Media Player Mobile, sección de botones
- aspectos, sección de botones
- referencia de las máscaras, sección de botones
- botones en máscaras, sección de botones
- archivos de definición de máscara, sección de botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c35a4efd0e52dd7f5fd0cf87fc269eb4a9f4c27
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075965"
---
# <a name="sample-button-section"></a><span data-ttu-id="11f6f-108">Sección de botón de ejemplo</span><span class="sxs-lookup"><span data-stu-id="11f6f-108">Sample Button Section</span></span>

<span data-ttu-id="11f6f-109">Las siguientes líneas muestran una sección típica de los botones de un archivo de definición de máscara:</span><span class="sxs-lookup"><span data-stu-id="11f6f-109">The following lines show a typical Buttons section of a skin definition file:</span></span>


```C++
[ Buttons ]

//  <Function> <Type>     <Location>     <Push Image Src>  <Dis Image Src>    <Hit R,G,B>  <Norm 2 Image Src>  <Push 2 Image Src>
//  ---------- ------     ----------     ----------------  ---------------    -----------  ------------------  ------------------
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98
    Info       PushHit    97,49,43,43    Pushed @ 57,0     Disabled @ 57,0      0,  0,  0
    Stop       PushHit    97,173,43,43   Pushed @ 57,124   Disabled @ 57,124  255,255,  0
    Prev       PushHit    40,83,43,43    Pushed @ 0,34     Disabled @ 0,34      0,  0,255
    Next       PushHit    153,83,43,43   Pushed @ 113,34   Disabled @ 113,34  255,  0,  0
    Shuffle    ToggleHit  40,136,43,43   Pushed @ 0,87     Disabled @ 0,87      0,255,  0
    Repeat     ToggleHit  153,136,43,43  Pushed @ 113,87   Disabled @ 113,87  255,  0,255
    Mute       Toggle     5,220,24,23    Super @ 247,29    Super @ 4,28         0,  0,  0

```



<span data-ttu-id="11f6f-110">Este código define ocho botones que se usan para proporcionar todas las funciones siguientes en una máscara:</span><span class="sxs-lookup"><span data-stu-id="11f6f-110">This code defines eight buttons that are used to provide all of the following functions in a skin:</span></span>

-   <span data-ttu-id="11f6f-111">Reproducir, pausar y detener elementos multimedia.</span><span class="sxs-lookup"><span data-stu-id="11f6f-111">Play, pause, and stop media items.</span></span>
-   <span data-ttu-id="11f6f-112">Orden aleatorio, repetir y desplazarse por la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="11f6f-112">Shuffle, repeat, and move through the playlist.</span></span>
-   <span data-ttu-id="11f6f-113">Silenciar el volumen.</span><span class="sxs-lookup"><span data-stu-id="11f6f-113">Mute the volume.</span></span>

<span data-ttu-id="11f6f-114">Todos los botones, excepto el botón silenciar, son botones de región.</span><span class="sxs-lookup"><span data-stu-id="11f6f-114">All the buttons except the mute button are region buttons.</span></span> <span data-ttu-id="11f6f-115">El botón silenciar obtiene las imágenes insertadas y deshabilitadas del súper mapa de bits para mayor comodidad.</span><span class="sxs-lookup"><span data-stu-id="11f6f-115">The mute button gets its Pushed and Disabled images from the Super bitmap for convenience.</span></span>

> [!Note]  
> <span data-ttu-id="11f6f-116">Los tipos de botones están en desuso en las máscaras de Windows Media Player 10 Mobile o posterior.</span><span class="sxs-lookup"><span data-stu-id="11f6f-116">Buttons types are deprecated in skins for Windows Media Player 10 Mobile or later.</span></span> <span data-ttu-id="11f6f-117">En lugar de un tipo de botón declarado en el archivo de máscara, escriba "NA" para cada tipo.</span><span class="sxs-lookup"><span data-stu-id="11f6f-117">Instead of a button type declared in your skin file, enter "NA" for each type.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="11f6f-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="11f6f-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="11f6f-119">**Botones**</span><span class="sxs-lookup"><span data-stu-id="11f6f-119">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




