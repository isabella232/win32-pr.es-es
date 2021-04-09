---
title: Código completo para la máscara simple
description: Código completo para la máscara simple
ms.assetid: ece437d2-1a11-4096-8b3b-db2b4def8248
keywords:
- crear máscaras, ejemplos de código
- Aspectos de Windows Media Player, ejemplos de código
- máscaras, ejemplos de código
- archivos de definición de máscara, ejemplos de código
- crear máscaras, ejemplos
- Aspectos de Windows Media Player, ejemplos
- máscaras, ejemplos
- archivos de definición de máscara, ejemplos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3682e6143c751d1c72cd8799f849fef7c9c27adb
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103903623"
---
# <a name="complete-code-for-simple-skin"></a><span data-ttu-id="0b617-111">Código completo para la máscara simple</span><span class="sxs-lookup"><span data-stu-id="0b617-111">Complete Code for Simple Skin</span></span>

<span data-ttu-id="0b617-112">Este es el código completo de la primera máscara de ejemplo:</span><span class="sxs-lookup"><span data-stu-id="0b617-112">Here is the complete code for the first sample skin:</span></span>


```C++
<THEME>
    <VIEW
        clippingColor = "#CCCC00"
        backgroundImage = "background.bmp"
        titleBar = "false">
         
        <BUTTONGROUP
            mappingImage = "map.bmp"
            hoverImage = "hover.bmp"> 
                
        <BUTTONELEMENT
            mappingColor = "#00FF00"
            upToolTip = "Play"
            onClick="JScript: player.URL='https://proseware.com/laure.wma';" />
                          
        <BUTTONELEMENT
            mappingColor = "#FF0000"
            upToolTip = "Close"
            onClick = "JScript: view.close(); " />
                
        </BUTTONGROUP>
    </VIEW>
</THEME>

```



<span data-ttu-id="0b617-113">Ahora tiene todas las piezas colocadas.</span><span class="sxs-lookup"><span data-stu-id="0b617-113">Now you have all the pieces put together.</span></span>

<span data-ttu-id="0b617-114">Cree un archivo comprimido con la extensión de nombre de archivo. zip.</span><span class="sxs-lookup"><span data-stu-id="0b617-114">Create a compressed file with a .zip file name extension.</span></span> <span data-ttu-id="0b617-115">Este archivo comprimido contiene el archivo de definición de máscara, los mapas de bits y los archivos multimedia digitales que desee incluir.</span><span class="sxs-lookup"><span data-stu-id="0b617-115">This compressed file contains your skin definition file, bitmaps, and any digital media files you want to include.</span></span> <span data-ttu-id="0b617-116">Cambie el nombre del archivo para que tenga una extensión de nombre de archivo. WMZ.</span><span class="sxs-lookup"><span data-stu-id="0b617-116">Rename the file so that it has a .wmz file name extension.</span></span> <span data-ttu-id="0b617-117">Después, al hacer doble clic en la máscara comprimida se iniciará la reproducción.</span><span class="sxs-lookup"><span data-stu-id="0b617-117">Then double-clicking your compressed skin will start it playing.</span></span>

<span data-ttu-id="0b617-118">Puede ver una máscara sencilla funcional similar en la sección de ejemplos del SDK.</span><span class="sxs-lookup"><span data-stu-id="0b617-118">You can see a similar working simple skin in the samples section of the SDK.</span></span>

## <a name="related-topics"></a><span data-ttu-id="0b617-119">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="0b617-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0b617-120">**Crear el archivo de definición de máscara**</span><span class="sxs-lookup"><span data-stu-id="0b617-120">**Creating the Skin Definition File**</span></span>](creating-the-skin-definition-file.md)
</dt> </dl>

 

 




