---
title: Cuadro de diálogo cambiar el tamaño del adquisición de licencias
description: Cuadro de diálogo cambiar el tamaño del adquisición de licencias
ms.assetid: e091d981-1574-4ffc-bdc4-b92f74396cb7
keywords:
- Windows Media Player, cambiar el tamaño de la adquisición de licencias (cuadro de diálogo)
- Windows Media Player, cuadro de diálogo adquisición de licencias
- Media Player de Windows, atributo de DRM_LicenseAcqURL
- cuadro de diálogo para cambiar el tamaño de la adquisición de licencias
- Cuadro de diálogo adquisición de licencias
- DRM_LicenseAcqURL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 440683ce65417653251bbed58d59c4d9a34dbc57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418902"
---
# <a name="resizing-the-license-acquisition-dialog-box"></a><span data-ttu-id="e51c6-109">Cuadro de diálogo cambiar el tamaño del adquisición de licencias</span><span class="sxs-lookup"><span data-stu-id="e51c6-109">Resizing the License Acquisition Dialog Box</span></span>

<span data-ttu-id="e51c6-110">Puede anexar parámetros de cadena de consulta a la dirección URL que proporcione para que el atributo **\_ LicenseAcqURL de DRM** especifique un tamaño para el cuadro de diálogo adquisición de licencias de Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e51c6-110">You can append query string parameters to the URL you provide for the **DRM\_LicenseAcqURL** attribute to specify a size for the Windows Media Player 10 or later license acquisition dialog box.</span></span> <span data-ttu-id="e51c6-111">En la tabla siguiente se enumeran los parámetros.</span><span class="sxs-lookup"><span data-stu-id="e51c6-111">The following table lists the parameters.</span></span>



| <span data-ttu-id="e51c6-112">Parámetro</span><span class="sxs-lookup"><span data-stu-id="e51c6-112">Parameter</span></span> | <span data-ttu-id="e51c6-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="e51c6-113">Description</span></span>                                        |
|-----------|----------------------------------------------------|
| <span data-ttu-id="e51c6-114">*DlgX*</span><span class="sxs-lookup"><span data-stu-id="e51c6-114">*DlgX*</span></span>    | <span data-ttu-id="e51c6-115">Especifica el ancho del cuadro de diálogo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="e51c6-115">Specifies the width of the dialog box, in pixels.</span></span>  |
| <span data-ttu-id="e51c6-116">*DlgY*</span><span class="sxs-lookup"><span data-stu-id="e51c6-116">*DlgY*</span></span>    | <span data-ttu-id="e51c6-117">Especifica el alto del cuadro de diálogo, en píxeles.</span><span class="sxs-lookup"><span data-stu-id="e51c6-117">Specifies the height of the dialog box, in pixels.</span></span> |



 

<span data-ttu-id="e51c6-118">Por ejemplo, la siguiente dirección URL de adquisición de licencias haría que el cuadro de diálogo adquisición de licencias se abrira con un tamaño de 800 x 600 píxeles:</span><span class="sxs-lookup"><span data-stu-id="e51c6-118">For example, the following license acquisition URL would cause the license acquisition dialog box to open with a size of 800 by 600 pixels:</span></span>


```C++
https://www.proseware.com/license/lic_acq.htm?DlgX=800&DlgY=600

```



<span data-ttu-id="e51c6-119">El tamaño máximo del cuadro de diálogo nunca superará las dimensiones de pantalla actuales menos 20 píxeles.</span><span class="sxs-lookup"><span data-stu-id="e51c6-119">The maximum size for the dialog box will never exceed the current screen dimensions minus 20 pixels.</span></span> <span data-ttu-id="e51c6-120">El tamaño mínimo es 333 x 210 píxeles (el tamaño predeterminado).</span><span class="sxs-lookup"><span data-stu-id="e51c6-120">The minimum size is 333 x 210 pixels (the default size).</span></span>

<span data-ttu-id="e51c6-121">Esta característica requiere Windows Media Player 10 o posterior.</span><span class="sxs-lookup"><span data-stu-id="e51c6-121">This feature requires Windows Media Player 10 or later.</span></span>

## <a name="related-topics"></a><span data-ttu-id="e51c6-122">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="e51c6-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e51c6-123">**Reproductor de Windows Media**</span><span class="sxs-lookup"><span data-stu-id="e51c6-123">**Windows Media Player**</span></span>](windows-media-player.md)
</dt> </dl>

 

 




