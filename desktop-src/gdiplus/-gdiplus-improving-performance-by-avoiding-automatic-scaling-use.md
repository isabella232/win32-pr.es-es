---
description: Si solo pasa la esquina superior izquierda de una imagen al método DrawImage, Windows GDI+ podría escalar la imagen, lo que reduciría el rendimiento.
ms.assetid: da571970-a4fc-4d4a-9264-0085d9807d66
title: Mejorar el rendimiento evitando el escalado automático
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 54b505043bf8a303a58c6fc5936a31d794052c78
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104985163"
---
# <a name="improving-performance-by-avoiding-automatic-scaling"></a><span data-ttu-id="f5d94-103">Mejorar el rendimiento evitando el escalado automático</span><span class="sxs-lookup"><span data-stu-id="f5d94-103">Improving Performance by Avoiding Automatic Scaling</span></span>

<span data-ttu-id="f5d94-104">Si solo pasa la esquina superior izquierda de una imagen al método **DrawImage** , Windows GDI+ podría escalar la imagen, lo que reduciría el rendimiento.</span><span class="sxs-lookup"><span data-stu-id="f5d94-104">If you pass only the upper-left corner of an image to the **DrawImage** method, Windows GDI+ might scale the image, which would decrease performance.</span></span>

<span data-ttu-id="f5d94-105">La siguiente llamada al método **DrawImage** especifica una esquina superior izquierda de (50, 30) pero no especifica un rectángulo de destino:</span><span class="sxs-lookup"><span data-stu-id="f5d94-105">The following call to the **DrawImage** method specifies an upper-left corner of (50, 30) but does not specify a destination rectangle:</span></span>


```
graphics.DrawImage(&image, 50, 30);  // upper-left corner at (50, 30)
```



<span data-ttu-id="f5d94-106">Aunque esta es la versión más sencilla del método **DrawImage** en cuanto al número de argumentos necesarios, no es necesariamente el más eficaz.</span><span class="sxs-lookup"><span data-stu-id="f5d94-106">Although this is the easiest version of the **DrawImage** method in terms of the number of required arguments, it is not necessarily the most efficient.</span></span> <span data-ttu-id="f5d94-107">Si el número de puntos por pulgada en el dispositivo de pantalla actual es diferente del número de puntos por pulgada en el dispositivo en el que se creó la imagen, GDI+ escala la imagen para que su tamaño físico en el dispositivo de pantalla actual sea lo más cercano posible a su tamaño físico en el dispositivo en el que se creó.</span><span class="sxs-lookup"><span data-stu-id="f5d94-107">If the number of dots per inch on the current display device is different than the number of dots per inch on the device where the image was created, GDI+ scales the image so that its physical size on the current display device is as close as possible to its physical size on the device where it was created.</span></span>

<span data-ttu-id="f5d94-108">Si desea evitar el escalado, pase el ancho y el alto de un rectángulo de destino al método **DrawImage** .</span><span class="sxs-lookup"><span data-stu-id="f5d94-108">If you want to prevent such scaling, pass the width and height of a destination rectangle to the **DrawImage** method.</span></span> <span data-ttu-id="f5d94-109">En el ejemplo siguiente se dibuja la misma imagen dos veces.</span><span class="sxs-lookup"><span data-stu-id="f5d94-109">The following example draws the same image twice.</span></span> <span data-ttu-id="f5d94-110">En el primer caso, no se especifican el ancho y el alto del rectángulo de destino, y la imagen se escala automáticamente.</span><span class="sxs-lookup"><span data-stu-id="f5d94-110">In the first case, the width and height of the destination rectangle are not specified, and the image is automatically scaled.</span></span> <span data-ttu-id="f5d94-111">En el segundo caso, el ancho y el alto (medidos en píxeles) del rectángulo de destino se especifican de la misma forma que el ancho y el alto de la imagen original.</span><span class="sxs-lookup"><span data-stu-id="f5d94-111">In the second case, the width and height (measured in pixels) of the destination rectangle are specified to be the same as the width and height of the original image.</span></span>


```
Image image(L"Texture.jpg");
graphics.DrawImage(&image, 10, 10);
graphics.DrawImage(&image, 120, 10, image.GetWidth(), image.GetHeight());
```



<span data-ttu-id="f5d94-112">En la ilustración siguiente se muestra la imagen representada dos veces.</span><span class="sxs-lookup"><span data-stu-id="f5d94-112">The following illustration shows the image rendered twice.</span></span>

![captura de pantalla de una ventana que contiene dos versiones de una imagen en diferentes escalas](images/scaledtexture1.png)

 

 



