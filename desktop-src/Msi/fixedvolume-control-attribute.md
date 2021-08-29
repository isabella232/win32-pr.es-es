---
description: Si se establece el bit De control FixedVolume, el control muestra todos los volúmenes implicados en la instalación actual más todas las unidades de disco duro internas fijas.
ms.assetid: e0917a8c-f43a-412d-9b91-9d5f80779f41
title: Atributo de control FixedVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d872c4bf891aaa3d93a755058b0047598cb80b0e07629cca7f8f8fc981af8ee
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828855"
---
# <a name="fixedvolume-control-attribute"></a>Atributo de control FixedVolume

Si se establece el bit De control FixedVolume, el control muestra todos los volúmenes implicados en la instalación actual más todas las unidades de disco duro internas fijas.

Si no se establece este bit, el control enumera los volúmenes de la instalación actual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)



| Decimal | Hexadecimal | Constante                              |
|---------|-------------|---------------------------------------|
| 131 072  | 0x00020000  | **msidbControlAttributesFixedVolume** |



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control, incluya el bit FixedVolume en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



