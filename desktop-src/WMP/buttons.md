---
title: Botones (SDK de Windows Media Player)
description: Botones
ms.assetid: 1212e2d9-e8f8-45d8-8c7f-20865c9c9c94
keywords:
- Máscaras de Windows Media Player Mobile, información general sobre el botón
- aspectos, información general sobre los botones
- referencia de las máscaras, botones
- botones en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0f06eb2fe21ee18a24f92e92d4fa760e9c76887
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104149832"
---
# <a name="buttons-windows-media-player-sdk"></a><span data-ttu-id="eef85-107">Botones (SDK de Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="eef85-107">Buttons (Windows Media Player SDK)</span></span>

<span data-ttu-id="eef85-108">Querrá usar uno o varios botones en la máscara y cada botón debe definirse en el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="eef85-108">You will want to use one or more buttons in your skin, and each button must be defined in the skin definition file.</span></span> <span data-ttu-id="eef85-109">Si no define un botón en esta sección, la máscara no podrá utilizarlo.</span><span class="sxs-lookup"><span data-stu-id="eef85-109">If you do not define a button in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="eef85-110">La sección de botones del archivo de definición de máscara comienza con esta línea:</span><span class="sxs-lookup"><span data-stu-id="eef85-110">The buttons section of the skin definition file begins with this line:</span></span>


```C++
[ Buttons ]

```



<span data-ttu-id="eef85-111">A continuación, debe agregar una o más líneas que contengan información sobre cada uno de los botones de la máscara.</span><span class="sxs-lookup"><span data-stu-id="eef85-111">You then must add one or more lines that contain information about each of the buttons in your skin.</span></span> <span data-ttu-id="eef85-112">Una línea típica podría ser:</span><span class="sxs-lookup"><span data-stu-id="eef85-112">A typical line might be:</span></span>


```C++
    PlayPause  2PushHit   84,99,67,67   Pushed @ 44,50    Disabled @ 44,50     0,255,255  Pushed @ 160,5      Pushed @ 160,98

```



<span data-ttu-id="eef85-113">Tenga en cuenta que este código debe escribirse como una línea que empieza por "PlayPause" y termina por "push @ 160, 98".</span><span class="sxs-lookup"><span data-stu-id="eef85-113">Note that this code should be typed as one line starting with "PlayPause" and ending with "Pushed @ 160,98".</span></span>

<span data-ttu-id="eef85-114">Puede usar la siguiente plantilla para la sección de botón del archivo de definición de máscara:</span><span class="sxs-lookup"><span data-stu-id="eef85-114">You can use the following template for the Button section of your skin definition file:</span></span>


```C++
//  <Function> <Type>     <Location>     <Push Image Src> <Dis Image Src>    <Hit R,G,B> <Norm 2 Image Src> <Push 2 Image Src>
//  ---------- ------     ----------     ---------------- ---------------    ----------- ------------------ ------------------

```



<span data-ttu-id="eef85-115">De nuevo, tenga en cuenta que deben escribirse como líneas únicas, la primera empezando por "// <Function> " y terminando por " &lt; Inserte 2 Image src &gt; ".</span><span class="sxs-lookup"><span data-stu-id="eef85-115">Again, note that these should be typed as single lines, the first starting with "// <Function>" and ending with "&lt;Push 2 Image Src&gt;".</span></span> <span data-ttu-id="eef85-116">La segunda línea comienza con "//----------" y termina con "------------------."</span><span class="sxs-lookup"><span data-stu-id="eef85-116">The second line starts with "// ----------" and ends with "------------------."</span></span>

<span data-ttu-id="eef85-117">La información del botón para cada línea de la sección Button debe aparecer en el orden siguiente.</span><span class="sxs-lookup"><span data-stu-id="eef85-117">Button information for each line in the Button section must appear in the following order.</span></span> <span data-ttu-id="eef85-118">Solo se requieren las seis primeras partes de la línea.</span><span class="sxs-lookup"><span data-stu-id="eef85-118">Only the first six parts of the line are required.</span></span> <span data-ttu-id="eef85-119">Las imágenes secundarias no se incluyen a menos que sean necesarias.</span><span class="sxs-lookup"><span data-stu-id="eef85-119">Secondary images are not included unless they are needed.</span></span>

1.  [<span data-ttu-id="eef85-120">Función Button</span><span class="sxs-lookup"><span data-stu-id="eef85-120">Button Function</span></span>](button-function.md)
2.  [<span data-ttu-id="eef85-121">Tipo de botón</span><span class="sxs-lookup"><span data-stu-id="eef85-121">Button Type</span></span>](button-type.md)
3.  [<span data-ttu-id="eef85-122">Ubicación del botón</span><span class="sxs-lookup"><span data-stu-id="eef85-122">Button Location</span></span>](button-location.md)
4.  [<span data-ttu-id="eef85-123">Origen de la imagen insertada</span><span class="sxs-lookup"><span data-stu-id="eef85-123">Pushed Image Source</span></span>](pushed-image-source.md)
5.  [<span data-ttu-id="eef85-124">Origen de imagen para botón deshabilitado</span><span class="sxs-lookup"><span data-stu-id="eef85-124">Image Source for Disabled Button</span></span>](image-source-for-disabled-button.md)
6.  [<span data-ttu-id="eef85-125">Golpear color RGB</span><span class="sxs-lookup"><span data-stu-id="eef85-125">Hit RGB Color</span></span>](hit-rgb-color.md)
7.  [<span data-ttu-id="eef85-126">Origen de imagen secundaria normal</span><span class="sxs-lookup"><span data-stu-id="eef85-126">Normal Secondary Image Source</span></span>](normal-secondary-image-source.md)
8.  [<span data-ttu-id="eef85-127">Origen de imagen terciario normal</span><span class="sxs-lookup"><span data-stu-id="eef85-127">Normal Tertiary Image Source</span></span>](normal-tertiary-image-source.md)
9.  [<span data-ttu-id="eef85-128">Origen de la imagen secundaria insertada</span><span class="sxs-lookup"><span data-stu-id="eef85-128">Pushed Secondary Image Source</span></span>](pushed-secondary-image-source.md)
10. [<span data-ttu-id="eef85-129">Origen de la imagen terciaria insertada</span><span class="sxs-lookup"><span data-stu-id="eef85-129">Pushed Tertiary Image Source</span></span>](pushed-tertiary-image-source.md)

<span data-ttu-id="eef85-130">Para obtener un ejemplo de código de botón, consulte la [sección del botón de ejemplo](sample-button-section.md).</span><span class="sxs-lookup"><span data-stu-id="eef85-130">For an example of button code, see [Sample Button Section](sample-button-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="eef85-131">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="eef85-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="eef85-132">**Referencia de máscara**</span><span class="sxs-lookup"><span data-stu-id="eef85-132">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




