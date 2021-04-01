---
title: Texto (SDK de Windows Media Player)
description: Texto
ms.assetid: 8c10cefb-d0d0-4214-8712-d171a76de95d
keywords:
- Aspectos de Windows Media Player Mobile, texto
- máscaras, texto
- referencia de máscaras, texto
- texto en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c801d93698bc7a17eea34df71514dd88b485f0d9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "103904964"
---
# <a name="text-windows-media-player-sdk"></a><span data-ttu-id="02f3f-107">Texto (SDK de Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="02f3f-107">Text (Windows Media Player SDK)</span></span>

<span data-ttu-id="02f3f-108">Puede que desee usar uno o varios cuadros de presentación de texto en la máscara.</span><span class="sxs-lookup"><span data-stu-id="02f3f-108">You may want to use one or more text display boxes in your skin.</span></span> <span data-ttu-id="02f3f-109">Cada cuadro de texto que use debe definirse en el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="02f3f-109">Each text display box you use must be defined in the skin definition file.</span></span> <span data-ttu-id="02f3f-110">Si no define un cuadro de presentación de texto en esta sección, la máscara no podrá utilizarlo.</span><span class="sxs-lookup"><span data-stu-id="02f3f-110">If you do not define a text display box in this section, your skin will not be able to use it.</span></span>

<span data-ttu-id="02f3f-111">La sección de texto del archivo de definición de máscara comienza con esta línea:</span><span class="sxs-lookup"><span data-stu-id="02f3f-111">The Text section of the skin definition file begins with this line:</span></span>


```C++
[ Text ]

```



<span data-ttu-id="02f3f-112">A continuación, debe agregar una o más líneas que contengan información sobre cada uno de los cuadros de presentación de texto de la máscara.</span><span class="sxs-lookup"><span data-stu-id="02f3f-112">You then must add one or more lines that contain information about each of the text display boxes in your skin</span></span>


```C++
    Time         180,46,50,30   Right    Tahoma,16,N     255,255,255

```



<span data-ttu-id="02f3f-113">Puede usar la siguiente plantilla para la sección de texto del archivo de definición de máscara:</span><span class="sxs-lookup"><span data-stu-id="02f3f-113">You can use the following template for the Text section of your skin definition file:</span></span>


```C++
//  <Type>       <Location>     <Align> <Font>          <Color>
//  ------       ----------     ------- ------          -------

```



<span data-ttu-id="02f3f-114">Debe usar el orden mostrado en la plantilla anterior para obtener información del cuadro de presentación de texto para cada línea de la sección de texto.</span><span class="sxs-lookup"><span data-stu-id="02f3f-114">You must use the order shown in the preceding template for text display box information for each line in the Text section.</span></span> <span data-ttu-id="02f3f-115">Cada parte de la línea es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="02f3f-115">Each part of the line is required.</span></span> <span data-ttu-id="02f3f-116">En las secciones siguientes se describe cada elemento en detalle.</span><span class="sxs-lookup"><span data-stu-id="02f3f-116">The following sections describe each item in detail.</span></span>

1.  [<span data-ttu-id="02f3f-117">Tipo de texto</span><span class="sxs-lookup"><span data-stu-id="02f3f-117">Text Type</span></span>](text-type.md)
2.  [<span data-ttu-id="02f3f-118">Ubicación del texto</span><span class="sxs-lookup"><span data-stu-id="02f3f-118">Text Location</span></span>](text-location.md)
3.  [<span data-ttu-id="02f3f-119">Alineación del texto</span><span class="sxs-lookup"><span data-stu-id="02f3f-119">Text Alignment</span></span>](text-alignment.md)
4.  [<span data-ttu-id="02f3f-120">Fuente de texto</span><span class="sxs-lookup"><span data-stu-id="02f3f-120">Text Font</span></span>](text-font.md)
5.  [<span data-ttu-id="02f3f-121">Color del texto</span><span class="sxs-lookup"><span data-stu-id="02f3f-121">Text Color</span></span>](text-color.md)

<span data-ttu-id="02f3f-122">Para obtener un ejemplo de código de texto, consulte la [sección texto de ejemplo](sample-text-section.md).</span><span class="sxs-lookup"><span data-stu-id="02f3f-122">For an example of Text code, see [Sample Text Section](sample-text-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="02f3f-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="02f3f-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02f3f-124">**Referencia de máscara**</span><span class="sxs-lookup"><span data-stu-id="02f3f-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




