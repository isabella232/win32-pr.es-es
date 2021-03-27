---
description: El lápiz, el pincel, el mapa de bits, la paleta, la región y la ruta de acceso asociados a un controlador de dominio se denominan objetos gráficos. Los atributos siguientes están asociados a cada uno de estos objetos.
ms.assetid: 95c82efa-257e-4718-9853-7ef10cdfd76c
title: Objetos gráficos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b80aadcb0988e7bd64910d04ecfbf6ec608845d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997360"
---
# <a name="graphic-objects"></a><span data-ttu-id="3ef1c-104">Objetos gráficos</span><span class="sxs-lookup"><span data-stu-id="3ef1c-104">Graphic Objects</span></span>

<span data-ttu-id="3ef1c-105">El lápiz, el pincel, el mapa de bits, la paleta, la región y la ruta de acceso asociados a un controlador de dominio se denominan objetos gráficos.</span><span class="sxs-lookup"><span data-stu-id="3ef1c-105">The pen, brush, bitmap, palette, region, and path associated with a DC are referred to as its graphic objects.</span></span> <span data-ttu-id="3ef1c-106">Los atributos siguientes están asociados a cada uno de estos objetos.</span><span class="sxs-lookup"><span data-stu-id="3ef1c-106">The following attributes are associated with each of these objects.</span></span>



| <span data-ttu-id="3ef1c-107">Objeto gráfico</span><span class="sxs-lookup"><span data-stu-id="3ef1c-107">Graphic object</span></span> | <span data-ttu-id="3ef1c-108">Atributos asociados</span><span class="sxs-lookup"><span data-stu-id="3ef1c-108">Associated attributes</span></span>                                                               |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3ef1c-109">Bitmap</span><span class="sxs-lookup"><span data-stu-id="3ef1c-109">Bitmap</span></span>         | <span data-ttu-id="3ef1c-110">Tamaño, en bytes; dimensiones, en píxeles; formato de color; esquema de compresión; etc.</span><span class="sxs-lookup"><span data-stu-id="3ef1c-110">Size, in bytes; dimensions, in pixels; color-format; compression scheme; and so on.</span></span> |
| <span data-ttu-id="3ef1c-111">Pincel</span><span class="sxs-lookup"><span data-stu-id="3ef1c-111">Brush</span></span>          | <span data-ttu-id="3ef1c-112">Estilo, color, patrón y origen.</span><span class="sxs-lookup"><span data-stu-id="3ef1c-112">Style, color, pattern, and origin.</span></span>                                                  |
| <span data-ttu-id="3ef1c-113">Paleta</span><span class="sxs-lookup"><span data-stu-id="3ef1c-113">Palette</span></span>        | <span data-ttu-id="3ef1c-114">Colores y tamaño (o número de colores).</span><span class="sxs-lookup"><span data-stu-id="3ef1c-114">Colors and size (or number of colors).</span></span>                                              |
| <span data-ttu-id="3ef1c-115">Fuente</span><span class="sxs-lookup"><span data-stu-id="3ef1c-115">Font</span></span>           | <span data-ttu-id="3ef1c-116">Nombre del tipo de letra, ancho, alto, peso, juego de caracteres, etc.</span><span class="sxs-lookup"><span data-stu-id="3ef1c-116">Typeface name, width, height, weight, character set, and so on.</span></span>                     |
| <span data-ttu-id="3ef1c-117">Ruta</span><span class="sxs-lookup"><span data-stu-id="3ef1c-117">Path</span></span>           | <span data-ttu-id="3ef1c-118">Forma.</span><span class="sxs-lookup"><span data-stu-id="3ef1c-118">Shape.</span></span>                                                                              |
| <span data-ttu-id="3ef1c-119">Lápiz</span><span class="sxs-lookup"><span data-stu-id="3ef1c-119">Pen</span></span>            | <span data-ttu-id="3ef1c-120">Estilo, ancho y color.</span><span class="sxs-lookup"><span data-stu-id="3ef1c-120">Style, width, and color.</span></span>                                                            |
| <span data-ttu-id="3ef1c-121">Region</span><span class="sxs-lookup"><span data-stu-id="3ef1c-121">Region</span></span>         | <span data-ttu-id="3ef1c-122">Ubicación y dimensiones.</span><span class="sxs-lookup"><span data-stu-id="3ef1c-122">Location and dimensions.</span></span>                                                            |



 

<span data-ttu-id="3ef1c-123">Cuando una aplicación crea un controlador de dominio, el sistema almacena automáticamente un conjunto de objetos predeterminados en él (no hay ningún mapa de bits o ruta de acceso predeterminados).</span><span class="sxs-lookup"><span data-stu-id="3ef1c-123">When an application creates a DC, the system automatically stores a set of default objects in it (there is no default bitmap or path).</span></span> <span data-ttu-id="3ef1c-124">Una aplicación puede examinar los atributos de los objetos predeterminados llamando a las funciones [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) y [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) .</span><span class="sxs-lookup"><span data-stu-id="3ef1c-124">An application can examine the attributes of the default objects by calling the [**GetCurrentObject**](/windows/desktop/api/Wingdi/nf-wingdi-getcurrentobject) and [**GetObject**](/windows/desktop/api/Wingdi/nf-wingdi-getobject) functions.</span></span> <span data-ttu-id="3ef1c-125">La aplicación puede cambiar estos valores predeterminados si crea un nuevo objeto y lo selecciona en el controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="3ef1c-125">The application can change these defaults by creating a new object and selecting it into the DC.</span></span> <span data-ttu-id="3ef1c-126">Un objeto se selecciona en un controlador de dominio mediante una llamada a la función [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) .</span><span class="sxs-lookup"><span data-stu-id="3ef1c-126">An object is selected into a DC by calling the [**SelectObject**](/windows/desktop/api/Wingdi/nf-wingdi-selectobject) function.</span></span>

<span data-ttu-id="3ef1c-127">Una aplicación puede establecer el color del pincel actual en un valor de color especificado con [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor).</span><span class="sxs-lookup"><span data-stu-id="3ef1c-127">An application can set the current brush color to a specified color value with [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor).</span></span>

<span data-ttu-id="3ef1c-128">La función [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) devuelve el color del pincel de DC.</span><span class="sxs-lookup"><span data-stu-id="3ef1c-128">The [**GetDCBrushColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcbrushcolor) function returns the DC brush color.</span></span> <span data-ttu-id="3ef1c-129">La función [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) establece el color del lápiz en un valor de color especificado.</span><span class="sxs-lookup"><span data-stu-id="3ef1c-129">The [**SetDCPenColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcpencolor) function sets the pen color to a specified color value.</span></span> <span data-ttu-id="3ef1c-130">La función [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) devuelve el color del lápiz del controlador de dominio.</span><span class="sxs-lookup"><span data-stu-id="3ef1c-130">The [**GetDCPenColor**](/windows/desktop/api/WinGdi/nf-wingdi-getdcpencolor) function returns the DC pen color.</span></span>

 

 



