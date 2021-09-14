---
description: Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual más todos los volúmenes de disco RAM. Si este bit no está establecido, el control enumera los volúmenes de la instalación actual.
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: Atributo de control RAMDiskVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dc4324af143bab619c6f881925586186be45b44a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127362319"
---
# <a name="ramdiskvolume-control-attribute"></a>Atributo de control RAMDiskVolume

Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual más todos los volúmenes de disco RAM. Si este bit no está establecido, el control enumera los volúmenes de la instalación actual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                                |
|---------|-------------|-----------------------------------------|
| 1048567 | 0x00100000  | **msidbControlAttributesRAMDiskVolume** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control , incluya el bit RAMDiskVolume en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Controles y atributos](control-attributes.md) de [control.](controls.md)

 

 



