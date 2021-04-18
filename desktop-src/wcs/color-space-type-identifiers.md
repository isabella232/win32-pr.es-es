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
# <a name="color-space-type-identifiers"></a>Identificadores de tipo de espacio de color

Estas constantes especifican el tipo de una matriz de espacio de color PostScript 2. Los valores siguientes son tipos de matriz de espacio de colores válidos.

<dl> <dt>

<span id="CSA_A"></span><span id="csa_a"></span>**CSA \_ A**
</dt> <dd> <dl> <dt>



Obtiene una matriz de espacio de colores de CIEBasedA desde el perfil monocromo.


</dt> </dl> </dd> <dt>

<span id="CSA_GRAY"></span><span id="csa_gray"></span>**gris de CSA \_**
</dt> <dd> <dl> <dt>



Obtiene una matriz de espacio de colores de CIEBasedA desde el perfil monocromo.


</dt> </dl> </dd> <dt>

<span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA \_ ABC**
</dt> <dd> <dl> <dt>



Obtiene una matriz de espacio de colores de CIEBasedABC desde el perfil RGB o L <sup>\*</sup> a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_DEF"></span><span id="csa_def"></span>**CSA \_ Def**
</dt> <dd> <dl> <dt>



Obtiene una matriz de espacio de colores de CIEBasedDEF desde el perfil RGB o L <sup>\*</sup> a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_RGB"></span><span id="csa_rgb"></span>**RVA de CSA \_**
</dt> <dd> <dl> <dt>



Obtiene una matriz de espacio de colores de CIEBasedDEF seguida de una matriz de espacio de colores CIEBasedABC del perfil RGB. En la ejecución, si la impresora no admite los espacios de colores de CIEBasedDEF, la función utiliza la definición de CIEBasedABC.


</dt> </dl> </dd> <dt>

<span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**Laboratorio de CSA \_**
</dt> <dd> <dl> <dt>



Obtiene una matriz de espacio de colores CIEBasedABC del <sup>\*</sup> perfil L a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_DEFG"></span><span id="csa_defg"></span>**CSA \_ DEFG**
</dt> <dd> <dl> <dt>



Obtiene una matriz de espacio de colores de CIEBasedDEFG desde el perfil CMYK.


</dt> </dl> </dd> <dt>

<span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA \_ CMYK**
</dt> <dd> <dl> <dt>



Obtiene una matriz de espacio de colores de CIEBasedCMYK desde el perfil CMYK.


</dt> </dl> </dd> </dl>

## <a name="see-also"></a>Vea también

<dl> <dt>

[Conceptos básicos de la administración del color](basic-color-management-concepts.md)
</dt> <dt>

[Constantes de ICM](wcs-constants.md)
</dt> </dl>

 

 




