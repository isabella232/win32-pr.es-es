---
title: Agregar un control deslizante
description: Agregar un control deslizante
ms.assetid: 7062d580-a9d1-4fd7-bc28-db2615464838
keywords:
- crear máscaras, controles deslizantes
- Aspectos de Windows Media Player, controles deslizantes
- máscaras, controles deslizantes
- controles deslizantes en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3efcae55b3826b69a7c88fed5a23a262526c9dd
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075976"
---
# <a name="adding-a-slider"></a><span data-ttu-id="4c52b-107">Agregar un control deslizante</span><span class="sxs-lookup"><span data-stu-id="4c52b-107">Adding a Slider</span></span>

<span data-ttu-id="4c52b-108">Puede Agregar un control deslizante para mostrar la posición actual del medio y permitir que el usuario cambie la posición en el archivo multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="4c52b-108">You can add a slider to show the current position of the media, and also enable the user to change the position in the current media file.</span></span>

<span data-ttu-id="4c52b-109">En primer lugar, debe agregar el elemento **Slider** :</span><span class="sxs-lookup"><span data-stu-id="4c52b-109">First you must add the **SLIDER** element:</span></span>


```C++
<SLIDER
  id = "myslider"
  min = "0"
  max = "wmpprop:player.currentMedia.duration"
  onmouseup = "player.controls.currentPosition = myslider.value; "
  tooltip = "current position"
  height = "10"
  width = "180"
  top = "150"
  left = "88"
  backgroundColor = "red"
  foregroundColor = "blue"
  thumbImage = "thumb.bmp"/>

```



<span data-ttu-id="4c52b-110">Esto establece un valor máximo en función de la duración del archivo multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="4c52b-110">This sets a maximum value based on the duration of the current media file.</span></span> <span data-ttu-id="4c52b-111">Utiliza un mapa de bits de imagen Thumb pequeño que es simplemente un cuadrado verde de 10 píxeles por 10 píxeles.</span><span class="sxs-lookup"><span data-stu-id="4c52b-111">This uses a tiny thumb image bitmap that is just a 10 pixel by 10 pixel green square.</span></span> <span data-ttu-id="4c52b-112">El fondo del control deslizante será rojo y el primer plano será azul.</span><span class="sxs-lookup"><span data-stu-id="4c52b-112">The background of the slider will be red and the foreground will be blue.</span></span> <span data-ttu-id="4c52b-113">Cuando el usuario arrastra la imagen Thumb a una nueva posición y permite ir al botón del mouse, el medio cambiará a esa posición.</span><span class="sxs-lookup"><span data-stu-id="4c52b-113">When the user drags the thumb image to a new position and lets go of the mouse button, the media will change to that position.</span></span>

<span data-ttu-id="4c52b-114">Pero el control deslizante no se moverá por sí solo a menos que mida la posición actual con el atributo **currentPosition \_ onchange** del elemento **Controls** , que se incrusta en el elemento **Player** .</span><span class="sxs-lookup"><span data-stu-id="4c52b-114">But the slider will not move by itself unless you measure the current position with the **currentPosition\_onchange** attribute of the **CONTROLS** element, which is embedded in the **PLAYER** element.</span></span>


```C++
<PLAYER
    URL = "https://proseware.com/laure.wma">

    <CONTROLS
        currentPosition_onchange = "myslider.value = player.controls.currentPosition; "/>

</PLAYER>

```



<span data-ttu-id="4c52b-115">Cuando cambia la posición del elemento multimedia, se desencadena un evento que, a continuación, ejecuta la línea de código que cambia el valor del control deslizante a la posición actual del medio.</span><span class="sxs-lookup"><span data-stu-id="4c52b-115">When the position of the media changes, this fires an event which then runs the line of code that changes the value of the slider to the current position of the media.</span></span>

<span data-ttu-id="4c52b-116">Puede ver una máscara de control deslizante de trabajo similar en la sección de ejemplo del SDK.</span><span class="sxs-lookup"><span data-stu-id="4c52b-116">You can see a similar working slider skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4c52b-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4c52b-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4c52b-118">**Guía de creación de máscaras**</span><span class="sxs-lookup"><span data-stu-id="4c52b-118">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




