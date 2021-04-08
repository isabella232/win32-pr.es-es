---
title: Estado (SDK de Windows Media Player)
description: Status
ms.assetid: b8d6d026-819c-4889-a894-c82fe81ec922
keywords:
- Aspectos de Windows Media Player Mobile, presentación de estado
- máscaras, presentación de estado
- referencia de máscaras, presentación de estado
- presentación de estado en máscaras, acerca de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f6f1cd9e0df209d6a37ed880765fd607e939765
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/10/2020
ms.locfileid: "104078693"
---
# <a name="status-windows-media-player-sdk"></a><span data-ttu-id="6b3bc-107">Estado (SDK de Windows Media Player)</span><span class="sxs-lookup"><span data-stu-id="6b3bc-107">Status (Windows Media Player SDK)</span></span>

<span data-ttu-id="6b3bc-108">Puede que desee usar una pantalla de estado en la máscara.</span><span class="sxs-lookup"><span data-stu-id="6b3bc-108">You may want to use a status display in your skin.</span></span> <span data-ttu-id="6b3bc-109">En ese caso, el elemento de estado se debe definir en el archivo de definición de máscara.</span><span class="sxs-lookup"><span data-stu-id="6b3bc-109">If so, the status element must be defined in the skin definition file.</span></span> <span data-ttu-id="6b3bc-110">Como alternativa, también puede mostrar esta información mediante el atributo status en el elemento de texto.</span><span class="sxs-lookup"><span data-stu-id="6b3bc-110">As an alternative, you may also display this information by using the Status attribute in the Text element.</span></span>

<span data-ttu-id="6b3bc-111">La sección de estado del archivo de definición de máscara comienza con esta línea:</span><span class="sxs-lookup"><span data-stu-id="6b3bc-111">The Status section of the skin definition file begins with this line:</span></span>


```C++
[ Status ]

```



<span data-ttu-id="6b3bc-112">A continuación, debe agregar una o más líneas que contengan información sobre la presentación de estado en la máscara.</span><span class="sxs-lookup"><span data-stu-id="6b3bc-112">You then must add one or more lines that contain information about the status display in your skin.</span></span>


```C++
    On           45,193,120,13    Left    Tahoma,8,B        0,255,  0

```



<span data-ttu-id="6b3bc-113">Puede usar la siguiente plantilla para la sección de estado del archivo de definición de máscara:</span><span class="sxs-lookup"><span data-stu-id="6b3bc-113">You can use the following template for the Status section of your skin definition file:</span></span>


```C++
//  <Item>       <Location>     <Align>  <Font>          <Color>
//  ------       ----------     -------  ------          -------

```



<span data-ttu-id="6b3bc-114">Debe usar el orden mostrado en la plantilla anterior para ver la información de visualización de estado de cada línea en la sección estado.</span><span class="sxs-lookup"><span data-stu-id="6b3bc-114">You must use the order shown in the preceding template for status display information for each line in the Status section.</span></span> <span data-ttu-id="6b3bc-115">Cada parte de la línea es obligatoria.</span><span class="sxs-lookup"><span data-stu-id="6b3bc-115">Each part of the line is required.</span></span> <span data-ttu-id="6b3bc-116">En las secciones siguientes se describe cada elemento:</span><span class="sxs-lookup"><span data-stu-id="6b3bc-116">The following sections describe each item:</span></span>

-   [<span data-ttu-id="6b3bc-117">Elemento de estado</span><span class="sxs-lookup"><span data-stu-id="6b3bc-117">Status Item</span></span>](status-item.md)
-   [<span data-ttu-id="6b3bc-118">Ubicación de estado</span><span class="sxs-lookup"><span data-stu-id="6b3bc-118">Status Location</span></span>](status-location.md)
-   [<span data-ttu-id="6b3bc-119">Alineación del estado</span><span class="sxs-lookup"><span data-stu-id="6b3bc-119">Status Alignment</span></span>](status-alignment.md)
-   [<span data-ttu-id="6b3bc-120">Fuente de estado</span><span class="sxs-lookup"><span data-stu-id="6b3bc-120">Status Font</span></span>](status-font.md)
-   [<span data-ttu-id="6b3bc-121">Color de estado</span><span class="sxs-lookup"><span data-stu-id="6b3bc-121">Status Color</span></span>](status-color.md)

<span data-ttu-id="6b3bc-122">Para obtener un ejemplo de código de estado, consulte la [sección estado de ejemplo](sample-status-section.md).</span><span class="sxs-lookup"><span data-stu-id="6b3bc-122">For an example of Status code, see [Sample Status Section](sample-status-section.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="6b3bc-123">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="6b3bc-123">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6b3bc-124">**Referencia de máscara**</span><span class="sxs-lookup"><span data-stu-id="6b3bc-124">**Skin Reference**</span></span>](skin-reference.md)
</dt> </dl>

 

 




