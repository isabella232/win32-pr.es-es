---
title: Trackbars
description: Trackbars
ms.assetid: b9676697-c3ab-465c-8b50-eb784f53bb11
keywords:
- Aspectos de Windows Media Player Mobile, trackbars
- máscaras, trackbars
- referencia de las máscaras, trackbars
- trackbars en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb7b64f7bada6f927b25aeecb71d584aa1ec2a68
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105704743"
---
# <a name="trackbars"></a><span data-ttu-id="1752b-107">Trackbars</span><span class="sxs-lookup"><span data-stu-id="1752b-107">Trackbars</span></span>

<span data-ttu-id="1752b-108">Una barra de aumento muestra una imagen que cambia en incrementos pequeños.</span><span class="sxs-lookup"><span data-stu-id="1752b-108">A trackbar displays an image that changes in small increments.</span></span> <span data-ttu-id="1752b-109">Trackbars se usan para los controles de volumen y los controles de posición de reproducción.</span><span class="sxs-lookup"><span data-stu-id="1752b-109">Trackbars are used for volume controls and playback position controls.</span></span> <span data-ttu-id="1752b-110">Puede usar trackbars para mostrar información sobre el elemento multimedia actual o para permitir que el usuario cambie la configuración o la posición de reproducción.</span><span class="sxs-lookup"><span data-stu-id="1752b-110">You can use trackbars to display information about the current media item or to allow the user to change settings or playback position.</span></span> <span data-ttu-id="1752b-111">Por ejemplo, puede utilizar una barra de presentación para permitir que el usuario ajuste el volumen y otro que pueda mostrar al usuario la posición de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="1752b-111">For example, you can use a trackbar to enable the user to adjust the volume, and another trackbar that can show the user the current playback position.</span></span> <span data-ttu-id="1752b-112">Trackbars tienen una imagen Thumb que define la configuración actual del valor de TrackBar.</span><span class="sxs-lookup"><span data-stu-id="1752b-112">Trackbars have a thumb image that defines the current setting of the trackbar value.</span></span>

<span data-ttu-id="1752b-113">La sección Trackbars del archivo de definición de máscara debe comenzar con esta línea:</span><span class="sxs-lookup"><span data-stu-id="1752b-113">The Trackbars section of the skin definition file must begin with this line:</span></span>


```C++
[ Trackbars ]

```



<span data-ttu-id="1752b-114">A continuación, debe agregar una o más líneas que contengan información sobre cada uno de los trackbars de la máscara.</span><span class="sxs-lookup"><span data-stu-id="1752b-114">You then must add one or more lines that contain information about each of the trackbars in your skin.</span></span>


```C++
    Seek        5,25,226,17    Disabled @ 4,1      SeekThumb.bmp      18,17
    Volume      32,220,172,23  Disabled @ 32,27    VolumeThumb.bmp    23,22

```



<span data-ttu-id="1752b-115">Puede usar la siguiente plantilla para la sección Trackbars del archivo de definición de máscara:</span><span class="sxs-lookup"><span data-stu-id="1752b-115">You can use the following template for the Trackbars section of your skin definition file:</span></span>


```C++
//  <Type> <Location>     <Dis Image Src> <Thumb Image Src> <Thumb Size>
//  ------ ----------     --------------- ----------------- ------------

```



<span data-ttu-id="1752b-116">Debe usar el orden siguiente para obtener información de TrackBar para cada línea de la sección Trackbars (se requiere cada parte de la línea):</span><span class="sxs-lookup"><span data-stu-id="1752b-116">You must use the following order for trackbar information for each line in the Trackbars section (each part of the line is required):</span></span>

1.  [<span data-ttu-id="1752b-117">Tipo de barra de texto</span><span class="sxs-lookup"><span data-stu-id="1752b-117">Trackbar Type</span></span>](trackbar-type.md)
2.  [<span data-ttu-id="1752b-118">Ubicación de TrackBar</span><span class="sxs-lookup"><span data-stu-id="1752b-118">Trackbar Location</span></span>](trackbar-location.md)
3.  [<span data-ttu-id="1752b-119">Origen de imagen para TrackBar deshabilitado</span><span class="sxs-lookup"><span data-stu-id="1752b-119">Image Source for Disabled Trackbar</span></span>](image-source-for-disabled-trackbar.md)
4.  [<span data-ttu-id="1752b-120">Origen de la imagen de Thumb</span><span class="sxs-lookup"><span data-stu-id="1752b-120">Thumb Image Source</span></span>](thumb-image-source.md)
5.  [<span data-ttu-id="1752b-121">Tamaño de Thumb</span><span class="sxs-lookup"><span data-stu-id="1752b-121">Thumb Size</span></span>](thumb-size.md)

<span data-ttu-id="1752b-122">Para obtener un ejemplo de código Trackbars, consulte la [sección Trackbars de ejemplo](sample-trackbars-section.md).</span><span class="sxs-lookup"><span data-stu-id="1752b-122">For an example of Trackbars code, see [Sample Trackbars Section](sample-trackbars-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="1752b-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="1752b-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1752b-124">**Referencia de máscara**</span><span class="sxs-lookup"><span data-stu-id="1752b-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




