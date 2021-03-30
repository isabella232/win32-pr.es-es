---
title: Origen de la imagen insertada
description: Origen de la imagen insertada
ms.assetid: 6cc290d8-2c15-4789-970d-9a3663a64d08
keywords:
- Máscaras móviles de Windows Media Player, origen de imagen de botón
- máscaras, origen de imagen de botón
- referencia de las máscaras, botones
- botones en máscaras, origen de imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 021c77a305e0f6981823c8a1e471862554c32e08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777089"
---
# <a name="pushed-image-source"></a><span data-ttu-id="88cb1-108">Origen de la imagen insertada</span><span class="sxs-lookup"><span data-stu-id="88cb1-108">Pushed Image Source</span></span>

<span data-ttu-id="88cb1-109">Debe definir el origen de la imagen que desea mostrar cuando el usuario presiona un botón.</span><span class="sxs-lookup"><span data-stu-id="88cb1-109">You must define the source of the image you want to display when the user pushes a button.</span></span> <span data-ttu-id="88cb1-110">La imagen procede del archivo que definió como insertada en la sección mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="88cb1-110">The image comes from the file you defined as Pushed in the Bitmaps section.</span></span> <span data-ttu-id="88cb1-111">Debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio.</span><span class="sxs-lookup"><span data-stu-id="88cb1-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="88cb1-112">A continuación, debe especificar dos enteros positivos que definan las coordenadas superior e izquierda (en píxeles) de la imagen que desea usar dentro del archivo de imagen insertado.</span><span class="sxs-lookup"><span data-stu-id="88cb1-112">You must then enter two positive integers that define the top and left coordinates (in pixels) of the image you want to use inside the Pushed image file.</span></span> <span data-ttu-id="88cb1-113">La ubicación en la que se mostrará la imagen procede de las coordenadas definidas para el botón en relación con la imagen de fondo. pero la ubicación desde la que procede se define mediante los dos números que siguen a "push @" y es relativo a la imagen insertada de la que está leyendo la imagen.</span><span class="sxs-lookup"><span data-stu-id="88cb1-113">The location at which the image will be displayed comes from the coordinates defined for the button relative to the Background image; but the location it comes from is defined by the two numbers following "Pushed @" and is relative to the Pushed image you are reading the image from.</span></span>

<span data-ttu-id="88cb1-114">Por ejemplo, para usar una imagen de la imagen insertada que se encuentra en el archivo insertado cuya ubicación superior izquierda es 50, 60 usaría el siguiente código:</span><span class="sxs-lookup"><span data-stu-id="88cb1-114">For example, to use an image from the Pushed image that is in the Pushed file whose top-left location is 50,60 you would use the following code:</span></span>


```C++
Pushed @ 50,60

```



<span data-ttu-id="88cb1-115">Si no desea mostrar una imagen diferente, puede definir el mapa de bits de fondo como mapa de bits insertado.</span><span class="sxs-lookup"><span data-stu-id="88cb1-115">If you do not want to display a different image, you can define the Background bitmap as your Pushed bitmap.</span></span> <span data-ttu-id="88cb1-116">Para ello, especifique el archivo de fondo como el archivo insertado y especifique el desplazamiento en la esquina superior izquierda del botón:</span><span class="sxs-lookup"><span data-stu-id="88cb1-116">To do this, specify the Background file as your pushed file and specify the offset to the top-left corner of the button:</span></span>


```C++
Pushed @ 50,60

```



<span data-ttu-id="88cb1-117">Si lo hace, ninguno de los botones puede mostrar una imagen insertada.</span><span class="sxs-lookup"><span data-stu-id="88cb1-117">If you do this, none of your buttons can display a Pushed image.</span></span> <span data-ttu-id="88cb1-118">Se recomienda mostrar una imagen insertada para todos los botones con el fin de proporcionar una indicación visual al usuario, ya que no siempre está claro si una derivación produce un resultado, especialmente cuando se está reproduciendo música o se desactiva el sonido punteo.</span><span class="sxs-lookup"><span data-stu-id="88cb1-118">We recommend that you display a Pushed image for all buttons to give your user a visual indication, because it is not always clear whether a tap produces a result, especially when music is playing or the tapping sound is turned off.</span></span>

## <a name="related-topics"></a><span data-ttu-id="88cb1-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="88cb1-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="88cb1-120">**Botones**</span><span class="sxs-lookup"><span data-stu-id="88cb1-120">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




