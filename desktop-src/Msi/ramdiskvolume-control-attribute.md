---
description: Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual más todos los volúmenes de disco RAM. Si este bit no está establecido, el control enumera los volúmenes de la instalación actual.
ms.assetid: 52526f39-26fb-4a67-a95f-77f7eb761372
title: Atributo de control RAMDiskVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9167c045a8437fff12c312999d71bd8fc2c7927f1ac8d3acf2260127b73cbb83
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120129025"
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



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control , incluya el bit RAMDiskVolume en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Controles y atributos](control-attributes.md) de [control.](controls.md)

 

 



