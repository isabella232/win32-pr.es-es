---
title: Archivo deshabilitado
description: Archivo deshabilitado
ms.assetid: 8b3339f6-a5d5-4501-826c-6ce33bfbf0cb
keywords:
- Aspectos móviles de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, archivos deshabilitados
- Aspectos móviles de Windows Media Player, archivos deshabilitados
- máscaras, archivos deshabilitados
- Archivos deshabilitados en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9608c67ded6625d46126955ad42a24548a9d002c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075972"
---
# <a name="disabled-file"></a><span data-ttu-id="69158-110">Archivo deshabilitado</span><span class="sxs-lookup"><span data-stu-id="69158-110">Disabled File</span></span>

<span data-ttu-id="69158-111">El archivo deshabilitado contiene las imágenes que se mostrarán cuando no se pueda usar una función de botón determinada o cuando un estado de botón esté desactivado.</span><span class="sxs-lookup"><span data-stu-id="69158-111">The Disabled file contains the images that will be displayed when a particular button function cannot be used or a button state is off.</span></span> <span data-ttu-id="69158-112">Por ejemplo, si se define una lista de reproducción vacía, se mostrarán los botones **siguiente** y **anterior** , y deben mostrarse con una imagen deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="69158-112">For example, if an empty playlist is defined, the **Next** and **Prev** buttons will be displayed, and they should be displayed using a disabled image.</span></span> <span data-ttu-id="69158-113">Además, en el caso de los botones de alternancia, se usa la imagen deshabilitada para indicar que el estado es OFF.</span><span class="sxs-lookup"><span data-stu-id="69158-113">Also, for toggle buttons, the Disabled image is used to indicate that the state is off.</span></span>

<span data-ttu-id="69158-114">La siguiente imagen es un archivo deshabilitado típico.</span><span class="sxs-lookup"><span data-stu-id="69158-114">The following image is a typical Disabled file.</span></span>

![archivo deshabilitado](images/cesdkdis.png)

<span data-ttu-id="69158-116">Esto almacena las imágenes de los botones de tipo de acceso que están deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="69158-116">This stores the images for hit-type buttons that are disabled.</span></span> <span data-ttu-id="69158-117">Las imágenes son similares al archivo en segundo plano, pero los colores son más claros.</span><span class="sxs-lookup"><span data-stu-id="69158-117">The images are similar to the Background file, but the colors are lighter.</span></span> <span data-ttu-id="69158-118">Con el desplazamiento definido en la sección de mapas de bits del archivo de definición de máscara, las imágenes de botón se alinean con la imagen de archivo de fondo.</span><span class="sxs-lookup"><span data-stu-id="69158-118">Using the offset defined in the Bitmaps section of the skin definition file, the button images line up with the Background file image.</span></span>

<span data-ttu-id="69158-119">Observe que el fondo de la imagen del botón coincide exactamente con el área correspondiente en el archivo en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="69158-119">Notice that the background of the button image exactly matches the corresponding area in the Background file.</span></span> <span data-ttu-id="69158-120">Esto es importante, porque cuando un botón de tipo de aciertos no está disponible, el rectángulo completo definido para la imagen deshabilitada reemplazará el área de coincidencia en el archivo en segundo plano.</span><span class="sxs-lookup"><span data-stu-id="69158-120">This is important, because when a hit-type button is unavailable, the entire rectangle defined for the disabled image will replace the matching area in the Background file.</span></span> <span data-ttu-id="69158-121">Mantenga el gráfico coherente con la imagen de fondo para asegurarse de que solo cambian las partes del botón que desea que aparezcan de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="69158-121">Keep the graphic consistent with the background image to ensure that only the parts of the button that you want to appear different will actually change.</span></span>

## <a name="related-topics"></a><span data-ttu-id="69158-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="69158-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="69158-123">**Archivos de imagen**</span><span class="sxs-lookup"><span data-stu-id="69158-123">**Art Files**</span></span>](art-files-mobile.md)
</dt> </dl>

 

 




