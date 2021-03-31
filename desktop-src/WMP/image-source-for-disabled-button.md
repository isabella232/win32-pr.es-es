---
title: Origen de imagen para botón deshabilitado
description: Origen de imagen para botón deshabilitado
ms.assetid: 6c50e0bd-c174-4335-8d34-ae25feec9ec6
keywords:
- Máscaras móviles de Windows Media Player, origen de imagen de botón
- máscaras, origen de imagen de botón
- referencia de las máscaras, botones
- botones en máscaras, origen de imagen
- origen de imagen para máscaras, botones
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d05ccd0362f3dd11acec71eaf0b92574f2c27c77
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418727"
---
# <a name="image-source-for-disabled-button"></a><span data-ttu-id="0c1c2-108">Origen de imagen para botón deshabilitado</span><span class="sxs-lookup"><span data-stu-id="0c1c2-108">Image Source for Disabled Button</span></span>

<span data-ttu-id="0c1c2-109">Debe definir el origen de la imagen que desea mostrar cuando un botón está deshabilitado o tiene un estado que corresponde a desactivado.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-109">You must define the source of the image you want to display when a button is disabled or has a state that corresponds to off.</span></span> <span data-ttu-id="0c1c2-110">La imagen procede del archivo definido como deshabilitado en la sección mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-110">The image comes from the file you defined as Disabled in the Bitmaps section.</span></span> <span data-ttu-id="0c1c2-111">Debe escribir el tipo de imagen seguido de un espacio y el símbolo @ y otro espacio.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-111">You must enter the image type followed by a space and the @ symbol and another space.</span></span> <span data-ttu-id="0c1c2-112">A continuación, debe especificar dos enteros positivos que definan las coordenadas superior izquierda (en píxeles) de la imagen que desea usar dentro del archivo de mapa de bits.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-112">You must then enter two positive integers that define the top-left coordinates (in pixels) of the image you want to use inside the bitmap file.</span></span> <span data-ttu-id="0c1c2-113">La ubicación en la que se mostrará la imagen procede de las coordenadas definidas para el botón en relación con la imagen de fondo, pero la ubicación desde la que procede se define mediante los dos números que siguen a "Disabled @" y es relativo al mapa de bits deshabilitado del que se lee la imagen.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-113">The location at which the image will be displayed comes from the coordinates defined for the button relative to the Background image, but the location it comes from is defined by the two numbers following "Disabled @" and is relative to the Disabled bitmap you are reading the image from.</span></span>

<span data-ttu-id="0c1c2-114">Por ejemplo, para usar una imagen del mapa de bits deshabilitado que se encuentra en el archivo deshabilitado en una ubicación superior e izquierda de 50, 60 píxeles, use el código siguiente:</span><span class="sxs-lookup"><span data-stu-id="0c1c2-114">For example, to use an image from the Disabled bitmap that is in the Disabled file at a top and left location of 50,60 pixels, use the following code:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="0c1c2-115">Debe definir un mapa de bits deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-115">You must define a Disabled bitmap.</span></span> <span data-ttu-id="0c1c2-116">Si no desea mostrar una imagen diferente, puede definir el mapa de bits de fondo como el mapa de bits deshabilitado con un desplazamiento de 0, 0:</span><span class="sxs-lookup"><span data-stu-id="0c1c2-116">If you do not want to display a different image, you can define the Background bitmap as your Disabled bitmap with an offset of 0,0:</span></span>


```C++
Disabled @ 50,60

```



<span data-ttu-id="0c1c2-117">En el ejemplo anterior, 50, 60 es la ubicación del botón con el que está trabajando en el archivo deshabilitado (en este caso, la misma ubicación que el botón en el mapa de bits de fondo).</span><span class="sxs-lookup"><span data-stu-id="0c1c2-117">In the preceding example, 50,60 is the location of the button you are working with in the Disabled file (in this case, the same location as the button on the Background bitmap).</span></span> <span data-ttu-id="0c1c2-118">Sin embargo, se recomienda encarecidamente mostrar una imagen deshabilitada para todos los botones a fin de que los usuarios tengan una indicación visual, ya que no se podrán usar muchos botones en determinadas condiciones, como una lista de reproducción vacía.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-118">However, it is highly recommended that you display a Disabled image for all buttons to give your users a visual indication, because many buttons will not be useable under certain conditions, such as an empty playlist.</span></span> <span data-ttu-id="0c1c2-119">Si los usuarios saben que un botón está deshabilitado, no seguirán intentando hacer clic en él o piensa que la piel no funciona según lo previsto.</span><span class="sxs-lookup"><span data-stu-id="0c1c2-119">If users know a button is disabled, they will not keep trying to click on it or think your skin is not functioning as designed.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0c1c2-120">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0c1c2-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0c1c2-121">**Botones**</span><span class="sxs-lookup"><span data-stu-id="0c1c2-121">**Buttons**</span></span>](buttons.md)
</dt> </dl>

 

 




