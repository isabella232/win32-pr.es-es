---
title: Marquesina
description: Marquesina
ms.assetid: 2715732a-25cc-4ba9-9aa6-181ebb9e1d1c
keywords:
- Aspectos móviles de Windows Media Player, marquesinas
- máscaras, marquesinas
- referencia de las máscaras, marquesinas
- marquesinas en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7efa2db2c6079d47d207240b18a57ebbf7e41ae1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418934"
---
# <a name="marquee"></a><span data-ttu-id="62e28-107">Marquesina</span><span class="sxs-lookup"><span data-stu-id="62e28-107">Marquee</span></span>

<span data-ttu-id="62e28-108">Una marquesina es un cuadro de texto de desplazamiento que muestra información de uno o varios cuadros de presentación de texto.</span><span class="sxs-lookup"><span data-stu-id="62e28-108">A marquee is a scrolling text display box that displays information from one or more text display boxes.</span></span> <span data-ttu-id="62e28-109">No es necesario agregar una marquesina, pero puede ser muy útil cuando se tiene información detallada que se desea mostrar al usuario en un espacio limitado.</span><span class="sxs-lookup"><span data-stu-id="62e28-109">You do not need to add a marquee, but it can be very useful when you have detailed information you want to display to the user in a limited space.</span></span>

<span data-ttu-id="62e28-110">El texto de la marquesina solo se desplazará si se cumplen las dos condiciones siguientes:</span><span class="sxs-lookup"><span data-stu-id="62e28-110">The text in the marquee will scroll only if both of the following conditions are met:</span></span>

-   <span data-ttu-id="62e28-111">Tiene más texto que mostrar en la marquesina que el ancho del cuadro de visualización de marquesina.</span><span class="sxs-lookup"><span data-stu-id="62e28-111">You have more text to display in the marquee than the width of the marquee display box.</span></span>
-   <span data-ttu-id="62e28-112">El elemento multimedia está detenido o en pausa.</span><span class="sxs-lookup"><span data-stu-id="62e28-112">The media item is either stopped or paused.</span></span>

<span data-ttu-id="62e28-113">La sección de marquesina del archivo de definición de máscara debe comenzar con esta línea:</span><span class="sxs-lookup"><span data-stu-id="62e28-113">The Marquee section of the skin definition file must begin with this line:</span></span>


```C++
[ Marquee ]

```



> [!Note]  
> <span data-ttu-id="62e28-114">Para mantener la compatibilidad con versiones de Windows Media Player Mobile anteriores a Windows Media Player 10 Mobile, el uso de "Marquis" en un archivo de definición de máscara todavía se considera válido.</span><span class="sxs-lookup"><span data-stu-id="62e28-114">To maintain compatibility with versions of Windows Media Player Mobile older than Windows Media Player 10 Mobile, using "Marquis" in a skin definition file is still considered valid.</span></span>

 

<span data-ttu-id="62e28-115">A continuación, debe agregar una o más líneas que contengan información sobre cada uno de los cuadros de visualización de marquesina de la máscara.</span><span class="sxs-lookup"><span data-stu-id="62e28-115">You then must add one or more lines that contain information about each of the marquee display boxes in your skin.</span></span>


```C++
    3,2,234,20   Tahoma,12,N  255,0,0    Playlist, Time, Filename

```



<span data-ttu-id="62e28-116">Puede usar la siguiente plantilla para la sección marquesina del archivo de definición de máscara:</span><span class="sxs-lookup"><span data-stu-id="62e28-116">You can use the following template for the Marquee section of your skin definition file:</span></span>


```C++
//  <Location>   <Font>       <Color>      <Text item combinations>
//  ----------   ------       -------      ------------------------

```



<span data-ttu-id="62e28-117">Debe usar el orden siguiente para obtener información en cada línea de la sección marquesina (se requiere cada parte de la línea):</span><span class="sxs-lookup"><span data-stu-id="62e28-117">You must use the following order for information in each line of the Marquee section (each part of the line is required):</span></span>

1.  [<span data-ttu-id="62e28-118">Ubicación de marquesina</span><span class="sxs-lookup"><span data-stu-id="62e28-118">Marquee Location</span></span>](marquee-location.md)
2.  [<span data-ttu-id="62e28-119">Fuente de marquesina</span><span class="sxs-lookup"><span data-stu-id="62e28-119">Marquee Font</span></span>](marquee-font.md)
3.  [<span data-ttu-id="62e28-120">Color de marquesina</span><span class="sxs-lookup"><span data-stu-id="62e28-120">Marquee Color</span></span>](marquee-color.md)
4.  [<span data-ttu-id="62e28-121">Combinaciones de texto</span><span class="sxs-lookup"><span data-stu-id="62e28-121">Text Combinations</span></span>](text-combinations.md)

<span data-ttu-id="62e28-122">Para obtener un ejemplo de código de marquesina, vea [sección marquesina de ejemplo](sample-marquee-section.md).</span><span class="sxs-lookup"><span data-stu-id="62e28-122">For an example of Marquee code, see [Sample Marquee Section](sample-marquee-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="62e28-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="62e28-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="62e28-124">**Referencia de máscara**</span><span class="sxs-lookup"><span data-stu-id="62e28-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




