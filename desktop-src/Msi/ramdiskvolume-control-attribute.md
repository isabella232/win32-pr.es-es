---
description: Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual más todos los volúmenes de disco RAM. Si no se establece este bit, el control muestra los volúmenes en la instalación actual.
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: Atributo de control RAMDiskVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4324af143bab619c6f881925586186be45b44a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677767"
---
# <a name="ramdiskvolume-control-attribute"></a>Atributo de control RAMDiskVolume

Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual más todos los volúmenes de disco RAM. Si no se establece este bit, el control muestra los volúmenes en la instalación actual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                                |
|---------|-------------|-----------------------------------------|
| 1048567 | 0x00100000  | **msidbControlAttributesRAMDiskVolume** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit RAMDiskVolume en la columna Attributes del registro del control en la [tabla de control](control-table.md).

Vea [controles y](controls.md) [atributos de control](control-attributes.md) .

 

 



