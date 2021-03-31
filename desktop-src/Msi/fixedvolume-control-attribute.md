---
description: Si se establece el bit de control FixedVolume, el control muestra todos los volúmenes implicados en la instalación actual, además de todas las unidades de disco duro internas fijas.
ms.assetid: e0917a8c-f43a-412d-9b91-9d5f80779f41
title: Atributo de control FixedVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c524bd228d19dbef823df00eff83e34df503a438
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908441"
---
# <a name="fixedvolume-control-attribute"></a>Atributo de control FixedVolume

Si se establece el bit de control FixedVolume, el control muestra todos los volúmenes implicados en la instalación actual, además de todas las unidades de disco duro internas fijas.

Si no se establece este bit, el control muestra los volúmenes en la instalación actual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)



| Decimal | Hexadecimal | Constante                              |
|---------|-------------|---------------------------------------|
| 131 072  | 0x00020000  | **msidbControlAttributesFixedVolume** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit FixedVolume en la columna Attributes del registro del control en la [tabla de control](control-table.md).

Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).

 

 



