---
title: Crear un archivo de definición de máscara
description: Crear un archivo de definición de máscara
ms.assetid: ea7f8e7c-a505-478d-80c3-cb3a3f67859d
keywords:
- Máscaras móviles de Windows Media Player, archivos de definición de máscara
- máscaras, archivos de definición de máscara
- archivos para máscaras, definición de máscara
- archivos de definición de máscara, crear
- crear máscaras, acerca de
- crear máscaras, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8b8a2920a08a3f57f740ff5ed3ca6e291ffd1bde
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103777257"
---
# <a name="creating-a-skin-definition-file"></a><span data-ttu-id="f3130-109">Crear un archivo de definición de máscara</span><span class="sxs-lookup"><span data-stu-id="f3130-109">Creating a Skin Definition File</span></span>

<span data-ttu-id="f3130-110">Un archivo de definición de máscara es un archivo de texto que define una máscara y todas sus partes compuestas.</span><span class="sxs-lookup"><span data-stu-id="f3130-110">A skin definition file is a text file that defines a skin and all its composite parts.</span></span> <span data-ttu-id="f3130-111">La extensión de nombre de archivo debe ser. SKN.</span><span class="sxs-lookup"><span data-stu-id="f3130-111">The file name extension must be .skn.</span></span>

<span data-ttu-id="f3130-112">Cada archivo de definición de máscara debe comenzar con la línea siguiente, que especifica el número de versión del archivo de máscara.</span><span class="sxs-lookup"><span data-stu-id="f3130-112">Every skin definition file must start with the following line, which specifies the skin file version number.</span></span> <span data-ttu-id="f3130-113">En la tabla siguiente se muestran las versiones de Windows Media Player y la línea de código que se debe usar para identificar cada una de ellas en un archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="f3130-113">The following table shows Windows Media Player versions and the code line that should be used to identify each in a skin definition file.</span></span> <span data-ttu-id="f3130-114">Aunque algunos de los números de las líneas de código no son los que cabría esperar, son correctos como se muestra en la tabla siguiente.</span><span class="sxs-lookup"><span data-stu-id="f3130-114">Although some of the numbers in the code lines are not what you would expect, they are correct as shown in the following table.</span></span>



| <span data-ttu-id="f3130-115">Versión de Windows Media Player</span><span class="sxs-lookup"><span data-stu-id="f3130-115">Windows Media Player version</span></span> | <span data-ttu-id="f3130-116">Primera línea del archivo de definición de máscara</span><span class="sxs-lookup"><span data-stu-id="f3130-116">First line of skin definition file</span></span> |
|------------------------------|------------------------------------|
| <span data-ttu-id="f3130-117">1.01.1</span><span class="sxs-lookup"><span data-stu-id="f3130-117">1.01.1</span></span><br/>            | <span data-ttu-id="f3130-118">\[Archivo de máscara de Pocket WMP v 1.0\]</span><span class="sxs-lookup"><span data-stu-id="f3130-118">\[Pocket WMP Skin File v1.0\]</span></span>      |
| <span data-ttu-id="f3130-119">1.2</span><span class="sxs-lookup"><span data-stu-id="f3130-119">1.2</span></span>                          | <span data-ttu-id="f3130-120">\[Archivo de máscara de Pocket WMP v 1.2\]</span><span class="sxs-lookup"><span data-stu-id="f3130-120">\[Pocket WMP Skin File v1.2\]</span></span>      |
| <span data-ttu-id="f3130-121">7.0</span><span class="sxs-lookup"><span data-stu-id="f3130-121">7.0</span></span>                          | <span data-ttu-id="f3130-122">\[Archivo de máscara de Pocket WMP v 2.0\]</span><span class="sxs-lookup"><span data-stu-id="f3130-122">\[Pocket WMP Skin File v2.0\]</span></span>      |
| <span data-ttu-id="f3130-123">7.1</span><span class="sxs-lookup"><span data-stu-id="f3130-123">7.1</span></span>                          | <span data-ttu-id="f3130-124">\[Archivo de máscara de Pocket WMP v 8.0\]</span><span class="sxs-lookup"><span data-stu-id="f3130-124">\[Pocket WMP Skin File v8.0\]</span></span>      |
| <span data-ttu-id="f3130-125">Series 9</span><span class="sxs-lookup"><span data-stu-id="f3130-125">9 Series</span></span>                     | <span data-ttu-id="f3130-126">\[Archivo de máscara de Pocket WMP v 9.0.1\]</span><span class="sxs-lookup"><span data-stu-id="f3130-126">\[Pocket WMP Skin File v9.0.1\]</span></span>    |
| <span data-ttu-id="f3130-127">10 Mobile</span><span class="sxs-lookup"><span data-stu-id="f3130-127">10 Mobile</span></span>                    | <span data-ttu-id="f3130-128">\[Archivo de máscara de Pocket WMP v 9.0.1\]</span><span class="sxs-lookup"><span data-stu-id="f3130-128">\[Pocket WMP Skin File v9.0.1\]</span></span>    |
| <span data-ttu-id="f3130-129">móvil 10,1</span><span class="sxs-lookup"><span data-stu-id="f3130-129">10.1 Mobile</span></span>                  | <span data-ttu-id="f3130-130">\[Archivo de máscara de Pocket WMP v 9.0.1\]</span><span class="sxs-lookup"><span data-stu-id="f3130-130">\[Pocket WMP Skin File v9.0.1\]</span></span>    |



 

<span data-ttu-id="f3130-131">El número de versión 9.0.1 es para las máscaras creadas específicamente para Windows Media Player 9 series o posterior.</span><span class="sxs-lookup"><span data-stu-id="f3130-131">The version number 9.0.1 is for skins created specifically for Windows Media Player 9 Series or later.</span></span> <span data-ttu-id="f3130-132">Las máscaras que tienen un número de versión anterior se abren con Windows Media Player 9 series o posterior como modo vertical, con máscaras de 96 puntos por pulgada (PPP).</span><span class="sxs-lookup"><span data-stu-id="f3130-132">Skins having an earlier version number are opened by Windows Media Player 9 Series or later as portrait mode, 96 dots per inch (DPI) skins.</span></span>

<span data-ttu-id="f3130-133">El archivo de definición de máscara consta de varias secciones.</span><span class="sxs-lookup"><span data-stu-id="f3130-133">The skin definition file consists of several sections.</span></span> <span data-ttu-id="f3130-134">Cada sección define un área determinada de la máscara.</span><span class="sxs-lookup"><span data-stu-id="f3130-134">Each section defines a particular area of the skin.</span></span> <span data-ttu-id="f3130-135">Las secciones se deben colocar en el orden siguiente:</span><span class="sxs-lookup"><span data-stu-id="f3130-135">The sections must be placed in the following order:</span></span>

1.  <span data-ttu-id="f3130-136">Descripción</span><span class="sxs-lookup"><span data-stu-id="f3130-136">Description</span></span>
2.  <span data-ttu-id="f3130-137">Mapas de bits</span><span class="sxs-lookup"><span data-stu-id="f3130-137">Bitmaps</span></span>
3.  <span data-ttu-id="f3130-138">Vídeo</span><span class="sxs-lookup"><span data-stu-id="f3130-138">Video</span></span>
4.  <span data-ttu-id="f3130-139">Botones</span><span class="sxs-lookup"><span data-stu-id="f3130-139">Buttons</span></span>
5.  <span data-ttu-id="f3130-140">Status</span><span class="sxs-lookup"><span data-stu-id="f3130-140">Status</span></span>
6.  <span data-ttu-id="f3130-141">Texto</span><span class="sxs-lookup"><span data-stu-id="f3130-141">Text</span></span>
7.  <span data-ttu-id="f3130-142">Marquesina</span><span class="sxs-lookup"><span data-stu-id="f3130-142">Marquee</span></span>
8.  <span data-ttu-id="f3130-143">Trackbars</span><span class="sxs-lookup"><span data-stu-id="f3130-143">Trackbars</span></span>

<span data-ttu-id="f3130-144">Cada sección comienza con el nombre de la sección entre corchetes, por ejemplo:</span><span class="sxs-lookup"><span data-stu-id="f3130-144">Each section starts with the name of the section in square brackets, for example:</span></span>


```C++
[ Bitmaps ]

```



> [!Note]  
> <span data-ttu-id="f3130-145">El archivo de definición de máscara no se analizará correctamente a menos que incluya espacios entre los corchetes y el nombre de la sección.</span><span class="sxs-lookup"><span data-stu-id="f3130-145">Your skin definition file will not be parsed correctly unless you include spaces between the brackets and the name of the section.</span></span>

 

<span data-ttu-id="f3130-146">A continuación, una o más líneas definen imágenes individuales, botones, etc.</span><span class="sxs-lookup"><span data-stu-id="f3130-146">Then, one or more lines define individual images, buttons, and so on.</span></span> <span data-ttu-id="f3130-147">Por ejemplo, una sección de mapas de bits podría incluir lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="f3130-147">For example, a Bitmaps section might include the following:</span></span>


```C++
    Background  Background.bmp  0,0
    Disabled    Disabled.bmp    0,0
    Pushed      Pushed.bmp      0,0
    Region      Region.bmp      0,0
    Super       Super.bmp       0,0

```



<span data-ttu-id="f3130-148">No es necesario alinear los valores de las columnas, pero ayudará a que el código sea más legible.</span><span class="sxs-lookup"><span data-stu-id="f3130-148">It is not necessary to line up the values in columns, but it will help your code to be more readable.</span></span> <span data-ttu-id="f3130-149">Para obtener más información sobre cada sección del archivo de definición de máscara, vea la referencia de la [máscara](skin-reference.md).</span><span class="sxs-lookup"><span data-stu-id="f3130-149">For more details about each section of the skin definition file, see the [Skin Reference](skin-reference.md).</span></span>

> [!Note]  
> <span data-ttu-id="f3130-150">No use pestañas en ningún lugar del archivo; en su lugar, use espacios adicionales.</span><span class="sxs-lookup"><span data-stu-id="f3130-150">Do not use tabs anywhere in the file; use extra spaces instead.</span></span> <span data-ttu-id="f3130-151">Esto es muy importante, ya que si se presiona la tecla TAB mientras se escribe o edita el archivo de definición de máscara, se producirá un error en toda la máscara.</span><span class="sxs-lookup"><span data-stu-id="f3130-151">This is very important, because pressing the TAB key while writing or editing your skin definition file will cause the entire skin to fail.</span></span> <span data-ttu-id="f3130-152">Cada línea debe estar completa y no puede continuar en una segunda línea.</span><span class="sxs-lookup"><span data-stu-id="f3130-152">Each line must be complete and cannot continue onto a second line.</span></span> <span data-ttu-id="f3130-153">Además, la región y los súper valores están desusados para las máscaras usadas con Windows Media Player 10 Mobile o posterior.</span><span class="sxs-lookup"><span data-stu-id="f3130-153">Also, the Region and Super values are deprecated for skins used with Windows Media Player 10 Mobile or later.</span></span>

 

## <a name="related-topics"></a><span data-ttu-id="f3130-154">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f3130-154">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f3130-155">**Archivo de definición de máscara**</span><span class="sxs-lookup"><span data-stu-id="f3130-155">**Skin Definition File**</span></span>](skin-definition-file-mobile.md)
</dt> </dl>

 

 





