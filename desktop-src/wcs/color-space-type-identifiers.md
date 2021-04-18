---
title: Identificadores de tipo de espacio de color
description: Estas constantes especifican el tipo de una matriz de espacio de color PostScript 2. Los valores siguientes son tipos de matriz de espacio de colores válidos.
ms.assetid: dc312db2-3bc5-461f-819c-37ff14cff896
topic_type:
- apiref
api_name:
- CSA_A
- CSA_GRAY
- CSA_ABC
- CSA_DEF
- CSA_RGB
- CSA_Lab
- CSA_DEFG
- CSA_CMYK
api_type:
- NA
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 973db6c56dda5bde8614dffa13f461761934fcde
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 02/02/2021
ms.locfileid: "105721161"
---
# <a name="color-space-type-identifiers"></a><span data-ttu-id="a7e96-104">Identificadores de tipo de espacio de color</span><span class="sxs-lookup"><span data-stu-id="a7e96-104">Color Space Type Identifiers</span></span>

<span data-ttu-id="a7e96-105">Estas constantes especifican el tipo de una matriz de espacio de color PostScript 2.</span><span class="sxs-lookup"><span data-stu-id="a7e96-105">These constants specify the type of a Postscript 2 color space array.</span></span> <span data-ttu-id="a7e96-106">Los valores siguientes son tipos de matriz de espacio de colores válidos.</span><span class="sxs-lookup"><span data-stu-id="a7e96-106">The following values are valid color space array types.</span></span>

<dl> <dt>

<span data-ttu-id="a7e96-107"><span id="CSA_A"></span><span id="csa_a"></span>**CSA \_ A**</span><span class="sxs-lookup"><span data-stu-id="a7e96-107"><span id="CSA_A"></span><span id="csa_a"></span>**CSA\_A**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7e96-108">Obtiene una matriz de espacio de colores de CIEBasedA desde el perfil monocromo.</span><span class="sxs-lookup"><span data-stu-id="a7e96-108">Get a CIEBasedA color space array from the monochrome profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7e96-109"><span id="CSA_GRAY"></span><span id="csa_gray"></span>**gris de CSA \_**</span><span class="sxs-lookup"><span data-stu-id="a7e96-109"><span id="CSA_GRAY"></span><span id="csa_gray"></span>**CSA\_GRAY**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7e96-110">Obtiene una matriz de espacio de colores de CIEBasedA desde el perfil monocromo.</span><span class="sxs-lookup"><span data-stu-id="a7e96-110">Get a CIEBasedA color space array from the monochrome profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7e96-111"><span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA \_ ABC**</span><span class="sxs-lookup"><span data-stu-id="a7e96-111"><span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA\_ABC**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7e96-112">Obtiene una matriz de espacio de colores de CIEBasedABC desde el perfil RGB o L <sup>\*</sup> a <sup>\*</sup> b.</span><span class="sxs-lookup"><span data-stu-id="a7e96-112">Get a CIEBasedABC color space array from the RGB or L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7e96-113"><span id="CSA_DEF"></span><span id="csa_def"></span>**CSA \_ Def**</span><span class="sxs-lookup"><span data-stu-id="a7e96-113"><span id="CSA_DEF"></span><span id="csa_def"></span>**CSA\_DEF**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7e96-114">Obtiene una matriz de espacio de colores de CIEBasedDEF desde el perfil RGB o L <sup>\*</sup> a <sup>\*</sup> b.</span><span class="sxs-lookup"><span data-stu-id="a7e96-114">Get a CIEBasedDEF color space array from the RGB or L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7e96-115"><span id="CSA_RGB"></span><span id="csa_rgb"></span>**RVA de CSA \_**</span><span class="sxs-lookup"><span data-stu-id="a7e96-115"><span id="CSA_RGB"></span><span id="csa_rgb"></span>**CSA\_RGB**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7e96-116">Obtiene una matriz de espacio de colores de CIEBasedDEF seguida de una matriz de espacio de colores CIEBasedABC del perfil RGB.</span><span class="sxs-lookup"><span data-stu-id="a7e96-116">Get a CIEBasedDEF color space array followed by a CIEBasedABC color space array from the RGB profile.</span></span> <span data-ttu-id="a7e96-117">En la ejecución, si la impresora no admite los espacios de colores de CIEBasedDEF, la función utiliza la definición de CIEBasedABC.</span><span class="sxs-lookup"><span data-stu-id="a7e96-117">On execution, if the printer doesn't support CIEBasedDEF color spaces, the function uses the CIEBasedABC definition.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7e96-118"><span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**Laboratorio de CSA \_**</span><span class="sxs-lookup"><span data-stu-id="a7e96-118"><span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**CSA\_Lab**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7e96-119">Obtiene una matriz de espacio de colores CIEBasedABC del <sup>\*</sup> perfil L a <sup>\*</sup> b.</span><span class="sxs-lookup"><span data-stu-id="a7e96-119">Gets a CIEBasedABC color space array from the L<sup>\*</sup>a<sup>\*</sup>b profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7e96-120"><span id="CSA_DEFG"></span><span id="csa_defg"></span>**CSA \_ DEFG**</span><span class="sxs-lookup"><span data-stu-id="a7e96-120"><span id="CSA_DEFG"></span><span id="csa_defg"></span>**CSA\_DEFG**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7e96-121">Obtiene una matriz de espacio de colores de CIEBasedDEFG desde el perfil CMYK.</span><span class="sxs-lookup"><span data-stu-id="a7e96-121">Get a CIEBasedDEFG color space array from the CMYK profile.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="a7e96-122"><span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA \_ CMYK**</span><span class="sxs-lookup"><span data-stu-id="a7e96-122"><span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA\_CMYK**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="a7e96-123">Obtiene una matriz de espacio de colores de CIEBasedCMYK desde el perfil CMYK.</span><span class="sxs-lookup"><span data-stu-id="a7e96-123">Get a CIEBasedCMYK color space array from the CMYK profile.</span></span>


</dt> </dl> </dd> </dl>

## <a name="see-also"></a><span data-ttu-id="a7e96-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="a7e96-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7e96-125">Conceptos básicos de la administración del color</span><span class="sxs-lookup"><span data-stu-id="a7e96-125">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="a7e96-126">Constantes de ICM</span><span class="sxs-lookup"><span data-stu-id="a7e96-126">ICM Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 




