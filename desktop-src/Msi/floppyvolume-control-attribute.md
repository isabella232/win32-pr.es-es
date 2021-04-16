---
description: Si se establece el bit de control FloppyVolume, el control muestra todos los volúmenes implicados en la instalación actual, además de todos los volúmenes de disquete.
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: Atributo de control FloppyVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70045ee5d6e16fbe1f679eafd83e6d657c9bf6e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104544270"
---
# <a name="floppyvolume-control-attribute"></a>Atributo de control FloppyVolume

Si se establece el bit de control FloppyVolume, el control muestra todos los volúmenes implicados en la instalación actual, además de todos los volúmenes de disquete.

Si no se establece este bit, el control muestra los volúmenes en la instalación actual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

[VolumeCostList](volumecostlist-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                               |
|---------|-------------|----------------------------------------|
| 2 097 152 | 0x00200000  | **msidbControlAttributesFloppyVolume** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit FloppyVolume en la columna Attributes del registro del control en la [tabla de control](control-table.md).

Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).

 

 



