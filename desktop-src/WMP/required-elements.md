---
title: Elementos necesarios
description: Elementos necesarios
ms.assetid: 6aabbdcc-f834-4908-b25a-1dfce038132a
keywords:
- Aspectos móviles de Windows Media Player, elementos
- aspectos, elementos
- archivos de definición de máscara, elementos
- elementos, archivos de definición de máscara
- elementos, Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e1f05ba51b83fad6585d24c3ad19830598b8975
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "103776411"
---
# <a name="required-elements"></a><span data-ttu-id="a3023-108">Elementos necesarios</span><span class="sxs-lookup"><span data-stu-id="a3023-108">Required Elements</span></span>

<span data-ttu-id="a3023-109">Debe proporcionar los elementos siguientes en el archivo de definición de máscara:</span><span class="sxs-lookup"><span data-stu-id="a3023-109">You must provide the following elements in your skin definition file:</span></span>

-   <span data-ttu-id="a3023-110">**Encabezado.**</span><span class="sxs-lookup"><span data-stu-id="a3023-110">**Header.**</span></span> <span data-ttu-id="a3023-111">El encabezado principal del archivo de definición de máscara es obligatorio.</span><span class="sxs-lookup"><span data-stu-id="a3023-111">The main skin definition file header is required.</span></span> <span data-ttu-id="a3023-112">Para obtener información sobre la versión de encabezado, vea la tabla en la sección [creación de un archivo de definición de máscara](creating-a-skin-definition-file.md) .</span><span class="sxs-lookup"><span data-stu-id="a3023-112">For header version information, see the table in the [Creating a Skin Definition File](creating-a-skin-definition-file.md) section.</span></span>
-   <span data-ttu-id="a3023-113">**Sección de descripción.**</span><span class="sxs-lookup"><span data-stu-id="a3023-113">**Description section.**</span></span> <span data-ttu-id="a3023-114">La sección Descripción es necesaria cuando se crean máscaras para Windows Media Player 9 series para Windows Mobile.</span><span class="sxs-lookup"><span data-stu-id="a3023-114">The Description section is required when creating skins for Windows Media Player 9 Series for Windows Mobile.</span></span> <span data-ttu-id="a3023-115">Debe ser la primera sección del archivo de definición de máscara y debe especificar valores válidos para las dimensiones.</span><span class="sxs-lookup"><span data-stu-id="a3023-115">It must be the first section in the skin definition file, and it must specify valid values for Dimensions.</span></span> <span data-ttu-id="a3023-116">Especificar un valor para la orientación es opcional.</span><span class="sxs-lookup"><span data-stu-id="a3023-116">Specifying a value for Orientation is optional.</span></span>
-   <span data-ttu-id="a3023-117">**Sección de mapas de bits.**</span><span class="sxs-lookup"><span data-stu-id="a3023-117">**Bitmaps section.**</span></span> <span data-ttu-id="a3023-118">La sección de mapas de bits es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="a3023-118">The Bitmaps section is required.</span></span> <span data-ttu-id="a3023-119">Además, la sección de mapas de bits debe especificar nombres válidos para los archivos de fondo, deshabilitado, insertado, región y súper imagen.</span><span class="sxs-lookup"><span data-stu-id="a3023-119">Additionally, the Bitmaps section must specify valid names for Background, Disabled, Pushed, Region, and Super image files.</span></span>
-   <span data-ttu-id="a3023-120">**archivos de imagen.**</span><span class="sxs-lookup"><span data-stu-id="a3023-120">**Image files.**</span></span> <span data-ttu-id="a3023-121">Debe proporcionar los archivos Background, Disabled, Push, region y Super Image como parte de la máscara.</span><span class="sxs-lookup"><span data-stu-id="a3023-121">You must provide Background, Disabled, Pushed, Region, and Super image files as part of your skin.</span></span> <span data-ttu-id="a3023-122">Si va a crear máscaras para Windows Media Player 10 Mobile o posterior, no es necesario incluir archivos de región o de superimagen.</span><span class="sxs-lookup"><span data-stu-id="a3023-122">If you are creating skins for Windows Media Player 10 Mobile or later, you do not need to include Region or Super image files.</span></span>

<span data-ttu-id="a3023-123">Si crea una máscara solo con imágenes definidas, la máscara será visible, pero no proporcionará ninguna funcionalidad significativa al usuario.</span><span class="sxs-lookup"><span data-stu-id="a3023-123">If you create a skin with only images defined, the skin will be visible, but will not offer any meaningful functionality to the user.</span></span> <span data-ttu-id="a3023-124">Si decide crear una máscara sin botones, quizás para evitar que el usuario omita un determinado contenido, tenga en cuenta que todavía es posible asignar funcionalidad a los botones de hardware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a3023-124">If you decide to create a skin without buttons, perhaps to prevent the user from skipping over certain content, be aware that it may still be possible to map functionality to the hardware buttons on the device.</span></span>

<span data-ttu-id="a3023-125">Los archivos Thumb son obligatorios y el trackbars no se puede usar sin Thumbs.</span><span class="sxs-lookup"><span data-stu-id="a3023-125">Thumb files are required and your trackbars cannot be used without thumbs.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a3023-126">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a3023-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3023-127">**Archivo de definición de máscara**</span><span class="sxs-lookup"><span data-stu-id="a3023-127">**Skin Definition File**</span></span>](skin-definition-file-mobile.md)
</dt> </dl>

 

 




