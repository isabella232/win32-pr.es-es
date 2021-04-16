---
title: Atributos de escucha
description: Atributos de escucha
ms.assetid: 51b10507-5c2e-49ca-b560-6db6a1a7ee87
keywords:
- Aspectos de Windows Media Player, atributos de escucha
- máscaras, atributos de escucha
- referencia de máscaras, atributos de escucha
- atributos de escucha
- atributos, escuchar
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 349a549966f7fba5ea152f8f0bb002a92f6dfb8e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532061"
---
# <a name="listening-attributes"></a><span data-ttu-id="4a631-108">Atributos de escucha</span><span class="sxs-lookup"><span data-stu-id="4a631-108">Listening Attributes</span></span>

<span data-ttu-id="4a631-109">Un atributo de escucha se usa para conectar un atributo a otro, de modo que su valor cambia cada vez que cambia el valor del otro atributo.</span><span class="sxs-lookup"><span data-stu-id="4a631-109">A listening attribute is used to connect one attribute to another so that its value changes every time the value of the other attribute changes.</span></span>

<span data-ttu-id="4a631-110">El atributo de escucha **wmpprop:** es el más útil.</span><span class="sxs-lookup"><span data-stu-id="4a631-110">The listening attribute **wmpprop:** is the most useful.</span></span> <span data-ttu-id="4a631-111">Si se especifica el valor de un atributo para que sea **wmpprop:** de un segundo atributo, el primer valor se actualizará automáticamente para reflejar el segundo valor cada vez que cambie el segundo valor.</span><span class="sxs-lookup"><span data-stu-id="4a631-111">If the value of one attribute is specified to be the **wmpprop:** of a second attribute, the first value will be automatically updated to reflect the second value each time the second value changes.</span></span>

<span data-ttu-id="4a631-112">**Ejemplo**:</span><span class="sxs-lookup"><span data-stu-id="4a631-112">**Example:**</span></span>


```C++
<TEXT
  value="wmpprop:mySlider.value"
/>

```



<span data-ttu-id="4a631-113">De esta manera, el valor de un control deslizante, que se muestra en la posición del control deslizante, también puede mostrarse como un número dentro de un cuadro de texto.</span><span class="sxs-lookup"><span data-stu-id="4a631-113">In this way, the value of mySlider, shown by the position of the slider control, can also be shown as a number within a text box.</span></span>

<span data-ttu-id="4a631-114">Los otros dos atributos de escucha, **wmpenabled:** y **wmpdisabled:**, se pueden usar para cambiar el atributo **habilitado** de un control en función de si su funcionalidad está actualmente disponible en el reproductor.</span><span class="sxs-lookup"><span data-stu-id="4a631-114">The two other listening attributes, **wmpenabled:** and **wmpdisabled:**, can be used to change the **enabled** attribute of a control depending on whether its functionality is currently available in the player.</span></span> <span data-ttu-id="4a631-115">Estos atributos solo pueden escuchar a los métodos del objeto de **control** .</span><span class="sxs-lookup"><span data-stu-id="4a631-115">These attributes can listen only to methods of the **Controls** object.</span></span>

<span data-ttu-id="4a631-116">**Ejemplo**:</span><span class="sxs-lookup"><span data-stu-id="4a631-116">**Example:**</span></span>


```C++
<BUTTON 
  id="play" 
  enabled="wmpenabled:player.controls.play"
/>

```



## <a name="related-topics"></a><span data-ttu-id="4a631-117">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="4a631-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a631-118">**Varios**</span><span class="sxs-lookup"><span data-stu-id="4a631-118">**Miscellaneous**</span></span>](miscellaneous.md)
</dt> </dl>

 

 




