---
description: Si se establece el bit De control FixedVolume, el control muestra todos los volúmenes implicados en la instalación actual más todas las unidades de disco duro internas fijas.
ms.assetid: e0917a8c-f43a-412d-9b91-9d5f80779f41
title: Atributo de control FixedVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c524bd228d19dbef823df00eff83e34df503a438
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074772"
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



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit FixedVolume en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



