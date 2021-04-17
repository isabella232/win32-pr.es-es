---
description: Si se establece el bit de control CDROMVolume, el control muestra todos los volúmenes de la instalación actual más todos los volúmenes de CD-ROM.
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: Atributo de control CDROMVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a687cfd52f347d9bfd24e74fb10b15f865e13b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652595"
---
# <a name="cdromvolume-control-attribute"></a>Atributo de control CDROMVolume

Si se establece el bit de control CDROMVolume, el control muestra todos los volúmenes de la instalación actual más todos los volúmenes de CD-ROM.

Si no se establece este bit, el control muestra todos los volúmenes de la instalación actual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                              |
|---------|-------------|---------------------------------------|
| 524 288  | 0x00080000  | **msidbControlAttributesCDROMVolume** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit CDROMVolume en la columna Attributes del registro del control en la [tabla de control](control-table.md).

Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).

 

 



