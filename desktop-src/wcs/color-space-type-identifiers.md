---
title: Identificadores de tipo de espacio de color
description: Estas constantes especifican el tipo de una matriz de espacios de color Postscript 2. Los siguientes valores son tipos de matriz de espacio de colores válidos.
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
ms.openlocfilehash: 199348fc23282a104c66f153b5c1ea43027464e5aa2522db61c6658d3425bdc1
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007695"
---
# <a name="color-space-type-identifiers"></a>Identificadores de tipo de espacio de color

Estas constantes especifican el tipo de una matriz de espacios de color Postscript 2. Los siguientes valores son tipos de matriz de espacio de colores válidos.

<dl> <dt>

<span id="CSA_A"></span><span id="csa_a"></span>**CSA \_ A**
</dt> <dd> <dl> <dt>



Obtenga una matriz de espacio de colores CIEBasedA del perfil monocromo.


</dt> </dl> </dd> <dt>

<span id="CSA_GRAY"></span><span id="csa_gray"></span>**GRIS \_ CSA**
</dt> <dd> <dl> <dt>



Obtenga una matriz de espacio de colores CIEBasedA del perfil monocromo.


</dt> </dl> </dd> <dt>

<span id="CSA_ABC"></span><span id="csa_abc"></span>**CSA \_ ABC**
</dt> <dd> <dl> <dt>



Obtenga una matriz de espacios de colores CIEBasedABC del perfil RGB o L <sup>\*</sup> a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_DEF"></span><span id="csa_def"></span>**CSA \_ DEF**
</dt> <dd> <dl> <dt>



Obtenga una matriz de espacios de color CIEBasedDEF del perfil RGB o L <sup>\*</sup> a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_RGB"></span><span id="csa_rgb"></span>**CSA \_ RGB**
</dt> <dd> <dl> <dt>



Obtenga una matriz de espacios de colores CIEBasedDEF seguida de una matriz de espacios de colores CIEBasedABC del perfil RGB. En la ejecución, si la impresora no admite espacios de colores CIEBasedDEF, la función usa la definición CIEBasedABC.


</dt> </dl> </dd> <dt>

<span id="CSA_Lab"></span><span id="csa_lab"></span><span id="CSA_LAB"></span>**Laboratorio de \_ CSA**
</dt> <dd> <dl> <dt>



Obtiene una matriz de espacios de colores CIEBasedABC del perfil L <sup>\*</sup> a <sup>\*</sup> b.


</dt> </dl> </dd> <dt>

<span id="CSA_DEFG"></span><span id="csa_defg"></span>**CSA \_ DEFG**
</dt> <dd> <dl> <dt>



Obtenga una matriz de espacios de color CIEBasedDEFG del perfil MULTIDIMENSIONAL.


</dt> </dl> </dd> <dt>

<span id="CSA_CMYK"></span><span id="csa_cmyk"></span>**CSA \_ GNI**
</dt> <dd> <dl> <dt>



Obtenga una matriz de espacio de colores CIEBasedMULTIDIMENSIONAL del perfil MULTIDIMENSIONAL.


</dt> </dl> </dd> </dl>

## <a name="see-also"></a>Vea también

<dl> <dt>

[Conceptos básicos de administración de colores](basic-color-management-concepts.md)
</dt> <dt>

[ICM constantes](wcs-constants.md)
</dt> </dl>

 

 




