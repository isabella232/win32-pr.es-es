---
title: Crear controles deslizantes personalizados
description: Crear controles deslizantes personalizados
ms.assetid: eb26ba44-a891-4cb6-be74-5acf881e896f
keywords:
- crear máscaras, controles deslizantes
- Aspectos de Windows Media Player, controles deslizantes
- máscaras, controles deslizantes
- controles deslizantes en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f205d46af003589fcc2c3b741a253ea08fae12
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532296"
---
# <a name="creating-custom-sliders"></a><span data-ttu-id="a22ae-107">Crear controles deslizantes personalizados</span><span class="sxs-lookup"><span data-stu-id="a22ae-107">Creating Custom Sliders</span></span>

<span data-ttu-id="a22ae-108">Puede crear controles deslizantes personalizados en cualquier forma que desee.</span><span class="sxs-lookup"><span data-stu-id="a22ae-108">You can create custom sliders in any shape you want.</span></span> <span data-ttu-id="a22ae-109">En este ejemplo, se elige una franja simple, pero la forma real puede ser cualquier cosa.</span><span class="sxs-lookup"><span data-stu-id="a22ae-109">For this example, a simple strip is chosen, but the actual shape can be anything.</span></span> <span data-ttu-id="a22ae-110">Este es el código del elemento **CUSTOMSLIDER** :</span><span class="sxs-lookup"><span data-stu-id="a22ae-110">Here is the code for the **CUSTOMSLIDER** element:</span></span>


```C++
<CustomSlider 
  top="160"
  left="130"
  min="0"
  max="100"
  toolTip="volume control"
  image="slider.bmp"
  positionImage="graymap.bmp"
  enabled="true"
  value="wmpprop:player.settings.volume"
  value_onchange="player.settings.volume = value" />

```



<span data-ttu-id="a22ae-111">Esto configura un valor inicial para el control deslizante.</span><span class="sxs-lookup"><span data-stu-id="a22ae-111">This sets up an initial value for the slider.</span></span> <span data-ttu-id="a22ae-112">Se introdujeron dos nuevos mapas de bits.</span><span class="sxs-lookup"><span data-stu-id="a22ae-112">Two new bitmaps are introduced.</span></span> <span data-ttu-id="a22ae-113">Uno es el mapa de bits de escala de grises (slider.bmp) que define los valores que se usarán cuando se haga clic en y el otro (slider.bmp) que determine la imagen que se mostrará cuando se haga clic en una parte determinada de la escala de grises.</span><span class="sxs-lookup"><span data-stu-id="a22ae-113">One is the grayscale bitmap (slider.bmp) that defines which values will be used when clicked on, and the other (slider.bmp) that determines which image will be shown when a particular portion of the grayscale is clicked on.</span></span>

<span data-ttu-id="a22ae-114">El valor inicial se determina mediante la escucha del volumen con wmpprop y, a continuación, se puede cambiar el volumen cuando el usuario hace clic en una parte del control deslizante que desencadena un cambio de valor.</span><span class="sxs-lookup"><span data-stu-id="a22ae-114">The initial value is determined by listening to the volume with wmpprop and then the volume can be changed when the user clicks on a portion of the slider that triggers a change in value.</span></span>

<span data-ttu-id="a22ae-115">Puede ver una máscara de control deslizante de trabajo similar en la sección de ejemplo del SDK.</span><span class="sxs-lookup"><span data-stu-id="a22ae-115">You can see a similar working slider skin in the sample section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a22ae-116">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a22ae-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a22ae-117">**Guía de creación de máscaras**</span><span class="sxs-lookup"><span data-stu-id="a22ae-117">**Skin Creation Guide**</span></span>](skin-creation-guide.md)
</dt> </dl>

 

 




