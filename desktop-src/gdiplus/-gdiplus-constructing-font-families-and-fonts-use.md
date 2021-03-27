---
description: Windows GDI+ agrupa fuentes con el mismo tipo de letra pero con distintos estilos en familias de fuentes.
ms.assetid: 57428fae-6af4-47a5-a499-717dc378767a
title: Construir fuentes y familias de fuentes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2761923847a15be6b1ad51eec0d683129b70b349
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104997516"
---
# <a name="constructing-font-families-and-fonts"></a><span data-ttu-id="d692b-103">Construir fuentes y familias de fuentes</span><span class="sxs-lookup"><span data-stu-id="d692b-103">Constructing Font Families and Fonts</span></span>

<span data-ttu-id="d692b-104">Windows GDI+ agrupa fuentes con el mismo tipo de letra pero con distintos estilos en familias de fuentes.</span><span class="sxs-lookup"><span data-stu-id="d692b-104">Windows GDI+ groups fonts with the same typeface but different styles into font families.</span></span> <span data-ttu-id="d692b-105">Por ejemplo, la familia de fuentes Arial contiene las siguientes fuentes:</span><span class="sxs-lookup"><span data-stu-id="d692b-105">For example, the Arial font family contains the following fonts:</span></span>

-   <span data-ttu-id="d692b-106">Arial normal</span><span class="sxs-lookup"><span data-stu-id="d692b-106">Arial Regular</span></span>
-   <span data-ttu-id="d692b-107">Arial negrita</span><span class="sxs-lookup"><span data-stu-id="d692b-107">Arial Bold</span></span>
-   <span data-ttu-id="d692b-108">Arial cursiva</span><span class="sxs-lookup"><span data-stu-id="d692b-108">Arial Italic</span></span>
-   <span data-ttu-id="d692b-109">Arial negrita cursiva</span><span class="sxs-lookup"><span data-stu-id="d692b-109">Arial Bold Italic</span></span>

<span data-ttu-id="d692b-110">GDI+ utiliza cuatro estilos para formar familias: normal, negrita, cursiva y negrita cursiva.</span><span class="sxs-lookup"><span data-stu-id="d692b-110">GDI+ uses four styles to form families: regular, bold, italic, and bold italic.</span></span> <span data-ttu-id="d692b-111">Los adjetivos como *estrechos* y *redondeados* no se consideran estilos; en su lugar, forman parte del nombre de familia.</span><span class="sxs-lookup"><span data-stu-id="d692b-111">Adjectives such as *narrow* and *rounded* are not considered styles; rather they are part of the family name.</span></span> <span data-ttu-id="d692b-112">Por ejemplo, Arial Narrow es una familia de fuentes cuyos miembros son los siguientes:</span><span class="sxs-lookup"><span data-stu-id="d692b-112">For example, Arial Narrow is a font family whose members are the following:</span></span>

-   <span data-ttu-id="d692b-113">Arial Narrow regular</span><span class="sxs-lookup"><span data-stu-id="d692b-113">Arial Narrow Regular</span></span>
-   <span data-ttu-id="d692b-114">Arial Narrow negrita</span><span class="sxs-lookup"><span data-stu-id="d692b-114">Arial Narrow Bold</span></span>
-   <span data-ttu-id="d692b-115">Arial Narrow cursiva</span><span class="sxs-lookup"><span data-stu-id="d692b-115">Arial Narrow Italic</span></span>
-   <span data-ttu-id="d692b-116">Arial Narrow negrita cursiva</span><span class="sxs-lookup"><span data-stu-id="d692b-116">Arial Narrow Bold Italic</span></span>

<span data-ttu-id="d692b-117">Antes de poder dibujar texto con GDI+, debe construir un objeto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) y un objeto [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) .</span><span class="sxs-lookup"><span data-stu-id="d692b-117">Before you can draw text with GDI+, you need to construct a [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object and a [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) object.</span></span> <span data-ttu-id="d692b-118">Los objetos **FontFamily** especifican el tipo de letra (por ejemplo, Arial) y el objeto **Font** especifica el tamaño, el estilo y las unidades.</span><span class="sxs-lookup"><span data-stu-id="d692b-118">The **FontFamily** objects specifies the typeface (for example, Arial), and the **Font** object specifies the size, style, and units.</span></span>

<span data-ttu-id="d692b-119">En el ejemplo siguiente se crea una fuente Arial de estilo normal con un tamaño de 16 píxeles:</span><span class="sxs-lookup"><span data-stu-id="d692b-119">The following example constructs a regular style Arial font with a size of 16 pixels:</span></span>


```
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 16, FontStyleRegular, UnitPixel);
            
```



<span data-ttu-id="d692b-120">En el código anterior, el primer argumento pasado al constructor de [**fuente**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) es la dirección del objeto [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) .</span><span class="sxs-lookup"><span data-stu-id="d692b-120">In the preceding code, the first argument passed to the [**Font**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-font) constructor is the address of the [**FontFamily**](/windows/desktop/api/gdiplusheaders/nl-gdiplusheaders-fontfamily) object.</span></span> <span data-ttu-id="d692b-121">El segundo argumento especifica el tamaño de la fuente que se mide en unidades identificadas por el cuarto argumento.</span><span class="sxs-lookup"><span data-stu-id="d692b-121">The second argument specifies the size of the font measured in units identified by the fourth argument.</span></span> <span data-ttu-id="d692b-122">El tercer argumento identifica el estilo.</span><span class="sxs-lookup"><span data-stu-id="d692b-122">The third argument identifies the style.</span></span>

<span data-ttu-id="d692b-123">[\* \* \* \* UnitPixel \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) \* \* es un miembro de la enumeración **Unit** y [\* \* \* \* FontStyleRegular \* \*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) \* \* es un miembro de la enumeración **fontStyle** .</span><span class="sxs-lookup"><span data-stu-id="d692b-123">[\*\*\*\*UnitPixel\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-unit) is a member of the **Unit** enumeration, and [\*\*\*\*FontStyleRegular\*\*\*\*](/windows/desktop/api/Gdiplusenums/ne-gdiplusenums-fontstyle) is a member of the **FontStyle** enumeration.</span></span> <span data-ttu-id="d692b-124">Ambas enumeraciones se declaran en Gdiplusenums. h.</span><span class="sxs-lookup"><span data-stu-id="d692b-124">Both enumerations are declared in Gdiplusenums.h.</span></span>

 

 



