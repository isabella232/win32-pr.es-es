---
title: Combinaciones de texto
description: Combinaciones de texto
ms.assetid: 0220b77e-5f1e-4569-a8fe-5085e0c16338
keywords:
- Aspectos móviles de Windows Media Player, marquesinas
- máscaras, marquesinas
- referencia de las máscaras, marquesinas
- marquesinas en máscaras, combinaciones de texto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5668a9e18555b871c82bae7ed1826766ec9429e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104532224"
---
# <a name="text-combinations"></a><span data-ttu-id="10d46-107">Combinaciones de texto</span><span class="sxs-lookup"><span data-stu-id="10d46-107">Text Combinations</span></span>

<span data-ttu-id="10d46-108">Este valor es una lista de combinaciones de cuadro de presentación de texto, separadas por comas.</span><span class="sxs-lookup"><span data-stu-id="10d46-108">This value is a list of text display box combinations, separated by commas.</span></span> <span data-ttu-id="10d46-109">Los cuadros de visualización de texto pueden combinarse mediante un carácter más para crear un nuevo valor de presentación de marquesina y cualquier tipo de texto definido en la sección tipo de texto se puede usar en el marco.</span><span class="sxs-lookup"><span data-stu-id="10d46-109">Text display boxes can be joined together by a plus character to create a new marquee display value and any text type defined in the Text Type section can be used in your marquee.</span></span>

<span data-ttu-id="10d46-110">Al determinar lo que se va a mostrar, Windows Media Player Mobile evalúa cada elemento de la lista para ver si todos los elementos están disponibles.</span><span class="sxs-lookup"><span data-stu-id="10d46-110">When determining what to display, Windows Media Player Mobile evaluates each item in the list to see if all parts are available.</span></span> <span data-ttu-id="10d46-111">Si no es así, se evalúa el elemento siguiente, y así sucesivamente, hasta que se hayan encontrado todos los elementos disponibles.</span><span class="sxs-lookup"><span data-stu-id="10d46-111">If not, the next item is evaluated, and so on, until all the available parts have been found.</span></span> <span data-ttu-id="10d46-112">Por ejemplo, si desea mostrar el autor y el título, pero no está seguro de si ambos están disponibles, utilice el siguiente valor:</span><span class="sxs-lookup"><span data-stu-id="10d46-112">For example, if you want to display Author and Title, but you're not sure whether both are available, use the following value:</span></span>


```C++
Title+Author, Title, Author

```



<span data-ttu-id="10d46-113">En el ejemplo anterior, se mostrará el título y el autor si se han definido el título y el autor para el elemento multimedia.</span><span class="sxs-lookup"><span data-stu-id="10d46-113">In the preceding example, the Title+Author will be displayed if the title and author have been defined for the media item.</span></span> <span data-ttu-id="10d46-114">Si no se definen ambos, el título se evalúa y se muestra si se define.</span><span class="sxs-lookup"><span data-stu-id="10d46-114">If both are not defined, the Title is evaluated and displayed if defined.</span></span> <span data-ttu-id="10d46-115">Si no se define el título, se muestra el autor si está definido.</span><span class="sxs-lookup"><span data-stu-id="10d46-115">If the Title is not defined, the Author is displayed if defined.</span></span> <span data-ttu-id="10d46-116">Si no se define ninguno, no se muestra nada.</span><span class="sxs-lookup"><span data-stu-id="10d46-116">If neither is defined, then nothing is displayed.</span></span>

<span data-ttu-id="10d46-117">Al usar el signo más para la concatenación, asegúrese de que no haya espacios a ambos lados del signo más.</span><span class="sxs-lookup"><span data-stu-id="10d46-117">When using the plus sign for concatenation, be sure you have no spaces on either side of the plus sign.</span></span>

## <a name="related-topics"></a><span data-ttu-id="10d46-118">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="10d46-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="10d46-119">**Marquesina**</span><span class="sxs-lookup"><span data-stu-id="10d46-119">**Marquee**</span></span>](marquee.md)
</dt> <dt>

[<span data-ttu-id="10d46-120">**Tipo de texto**</span><span class="sxs-lookup"><span data-stu-id="10d46-120">**Text Type**</span></span>](text-type.md)
</dt> </dl>

 

 




