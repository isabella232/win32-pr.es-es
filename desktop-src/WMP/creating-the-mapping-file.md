---
title: Crear el archivo de asignación
description: Crear el archivo de asignación
ms.assetid: d882cd5b-1404-4dfd-8b51-a61e1505fae1
keywords:
- crear máscaras, archivos de asignación
- Aspectos de Windows Media Player, archivos de imagen
- máscaras, archivos de imagen
- archivos para máscaras, arte
- archivos de imagen para máscaras, imágenes de asignación
- Máscaras de Windows Media Player, imágenes de asignación
- máscaras, imágenes de asignación
- asignar imágenes en máscaras
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49b71682f48ecdba098f76a9e27f656b27d5fe8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418380"
---
# <a name="creating-the-mapping-file"></a><span data-ttu-id="3306b-111">Crear el archivo de asignación</span><span class="sxs-lookup"><span data-stu-id="3306b-111">Creating the Mapping File</span></span>

<span data-ttu-id="3306b-112">Una vez que haya creado las piezas del archivo de imagen principal, es relativamente fácil crear un archivo de asignación.</span><span class="sxs-lookup"><span data-stu-id="3306b-112">Once you have created the pieces of your primary art file, it is relatively easy to create a mapping file.</span></span> <span data-ttu-id="3306b-113">Creará el nuevo archivo de asignación combinando el arte de las dos capas de botones que ya ha creado.</span><span class="sxs-lookup"><span data-stu-id="3306b-113">You will create the new mapping file by combining the art from the two button layers you already created.</span></span>

1.  <span data-ttu-id="3306b-114">Tendrá que tomar los dos botones que creó para el archivo de imagen principal y copiarlos en una nueva capa.</span><span class="sxs-lookup"><span data-stu-id="3306b-114">You will need to take the two buttons you created for the primary art file and copy them to a new layer.</span></span> <span data-ttu-id="3306b-115">Siga estos pasos: copiar la capa del botón Cerrar, quitar cualquier efecto de capa y cambiarle el nombre a "cerrar mapa".</span><span class="sxs-lookup"><span data-stu-id="3306b-115">Use the following steps: Copy the Close button layer, remove any Layer effects, and rename it "Close map".</span></span> <span data-ttu-id="3306b-116">El arte debe ser plano, sin biseles.</span><span class="sxs-lookup"><span data-stu-id="3306b-116">The art should look flat, with no bevels.</span></span>
2.  <span data-ttu-id="3306b-117">Use el selector de colores para crear un color de primer plano de rojo puro.</span><span class="sxs-lookup"><span data-stu-id="3306b-117">Use the Color Picker to create a foreground color of pure red.</span></span> <span data-ttu-id="3306b-118">Asegúrese de que el valor del número de color es " \# FF0000".</span><span class="sxs-lookup"><span data-stu-id="3306b-118">Be sure the color number value is "\#FF0000".</span></span> <span data-ttu-id="3306b-119">A continuación, use la herramienta Cubo de pintura para rellenar el interior del círculo de la capa de mapa de cierre.</span><span class="sxs-lookup"><span data-stu-id="3306b-119">Then use the Paint Bucket tool to fill the inside of the circle of the Close map layer.</span></span>
3.  <span data-ttu-id="3306b-120">Copie la capa del botón de reproducción, quite los efectos de capa y cambie su nombre por "Play Map".</span><span class="sxs-lookup"><span data-stu-id="3306b-120">Copy the Play button layer, remove any Layer effects, and rename it "Play map".</span></span> <span data-ttu-id="3306b-121">Una vez más, la imagen debe ser plana.</span><span class="sxs-lookup"><span data-stu-id="3306b-121">Again, the art should look flat.</span></span> <span data-ttu-id="3306b-122">No desea ningún efecto en la capa de asignación porque simplemente está definiendo regiones del mapa de bits que Windows Media Player usará para determinar dónde realiza una acción el mouse y qué desea hacer con él.</span><span class="sxs-lookup"><span data-stu-id="3306b-122">You do not want any effects in the mapping layer because you are just defining regions of the bitmap that Windows Media Player will use to determine where the mouse performs an action and what you want to do with it.</span></span>
4.  <span data-ttu-id="3306b-123">Use el selector de colores para crear un color de primer plano de verde puro.</span><span class="sxs-lookup"><span data-stu-id="3306b-123">Use the Color Picker to create a foreground color of pure green.</span></span> <span data-ttu-id="3306b-124">Asegúrese de que el valor del número de color es " \# 00FF00".</span><span class="sxs-lookup"><span data-stu-id="3306b-124">Be sure the color number value is "\#00FF00".</span></span> <span data-ttu-id="3306b-125">A continuación, use la herramienta Cubo de pintura para rellenar el interior del círculo de la capa Play map.</span><span class="sxs-lookup"><span data-stu-id="3306b-125">Then use the Paint Bucket tool to fill the inside of the circle of the Play map layer.</span></span>

<span data-ttu-id="3306b-126">Ahora está listo para crear el archivo de imagen de asignación.</span><span class="sxs-lookup"><span data-stu-id="3306b-126">You are now ready to create the mapping art file.</span></span> <span data-ttu-id="3306b-127">Oculte todas las capas y, a continuación, muestre solo las siguientes capas, en este orden (de arriba abajo):</span><span class="sxs-lookup"><span data-stu-id="3306b-127">Hide all layers, and then show only the following layers, in this order (top to bottom):</span></span>

<span data-ttu-id="3306b-128">Reproducir asignación</span><span class="sxs-lookup"><span data-stu-id="3306b-128">Play map</span></span>

<span data-ttu-id="3306b-129">Cerrar mapa</span><span class="sxs-lookup"><span data-stu-id="3306b-129">Close map</span></span>

<span data-ttu-id="3306b-130">Guarde en un archivo nuevo con el comando Guardar una copia del menú archivo.</span><span class="sxs-lookup"><span data-stu-id="3306b-130">Save to a new file using the Save a Copy command from the File menu.</span></span> <span data-ttu-id="3306b-131">Seleccione la opción BMP en la parte guardar como del cuadro de diálogo guardar una copia y escriba un nombre de archivo al que se hará referencia más adelante en el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="3306b-131">Select the BMP option in the Save As portion of the Save a Copy dialog box and type a file name that you will refer to later in your skin definition file.</span></span> <span data-ttu-id="3306b-132">Idealmente, debería estar en el mismo directorio que el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="3306b-132">Ideally it should be in the same directory as your skin definition file.</span></span> <span data-ttu-id="3306b-133">Por ejemplo, podría llamar a este archivo map.bmp.</span><span class="sxs-lookup"><span data-stu-id="3306b-133">For example, you could call this file map.bmp.</span></span> <span data-ttu-id="3306b-134">Elija la configuración predeterminada y guarde el archivo.</span><span class="sxs-lookup"><span data-stu-id="3306b-134">Choose the default settings and save the file.</span></span>

<span data-ttu-id="3306b-135">El archivo de asignación debería tener un aspecto similar al de la siguiente ilustración.</span><span class="sxs-lookup"><span data-stu-id="3306b-135">Your mapping file should look like the following illustration.</span></span>

![mapping file](images/g01map.png)

<span data-ttu-id="3306b-137">Como puede imaginar, el área verde se usará para determinar cuándo se debe iniciar Windows Media Player y el área roja para indicarle que se detenga.</span><span class="sxs-lookup"><span data-stu-id="3306b-137">As you might guess, the green area will be used to determine when to make Windows Media Player start and the red area is for telling it to stop.</span></span> <span data-ttu-id="3306b-138">Se pueden usar dos colores cualesquiera, siempre que use los números de color al configurar el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="3306b-138">Any two colors can be used, as long as you use the color numbers when you set up the skin definition file.</span></span> <span data-ttu-id="3306b-139">Asegúrese de que los colores del mapa son colores puros para la región que desea usar y que tienen bordes distintos.</span><span class="sxs-lookup"><span data-stu-id="3306b-139">Be sure the colors in the map are pure colors for the region you want to use and have distinct edges.</span></span> <span data-ttu-id="3306b-140">Un color puro sería aquél en el que cada píxel individual del área tiene el mismo valor de color.</span><span class="sxs-lookup"><span data-stu-id="3306b-140">A pure color would be one where every single pixel in the area has the same color value.</span></span> <span data-ttu-id="3306b-141">El uso de un efecto puede desenfocar o distorsionar el borde, con lo que se modifican ligeramente los colores de algunos de los píxeles.</span><span class="sxs-lookup"><span data-stu-id="3306b-141">Using an effect may blur or distort the edge, thereby slightly modifying the colors of some of the pixels.</span></span> <span data-ttu-id="3306b-142">El archivo de asignación solo lo verá el mouse, no un usuario, por lo que no molestarse en decorarlo y quitar cualquier efecto de capa que haya podido haber realizado desde otras capas.</span><span class="sxs-lookup"><span data-stu-id="3306b-142">The mapping file is only seen by the mouse, not a human, so do not bother decorating it, and remove any layer effects you may have carried over from other layers.</span></span>

<span data-ttu-id="3306b-143">Al guardar el archivo, el nombre de archivo que elija se usará más adelante como el valor del atributo **mappingImage** del elemento **BUTTONGROUP** en el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="3306b-143">When you save your file, the file name you choose will later be used as the value for the **mappingImage** attribute of the **BUTTONGROUP** element in your skin definition file.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3306b-144">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="3306b-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3306b-145">**Creación de la primera máscara**</span><span class="sxs-lookup"><span data-stu-id="3306b-145">**Building Your First Skin**</span></span>](building-your-first-skin.md)
</dt> </dl>

 

 




