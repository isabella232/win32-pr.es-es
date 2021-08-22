---
description: Si se establece el bit control FloppyVolume, el control muestra todos los volúmenes implicados en la instalación actual más todos los volúmenes de disquete.
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: Atributo de control FloppyVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4639960fee79336048082c91088e19c1b360f857216f2cf0ad9ed07c64b52b8b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118947016"
---
# <a name="floppyvolume-control-attribute"></a>Atributo de control FloppyVolume

Si se establece el bit control FloppyVolume, el control muestra todos los volúmenes implicados en la instalación actual más todos los volúmenes de disquete.

Si no se establece este bit, el control enumera los volúmenes de la instalación actual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

[VolumeCostList](volumecostlist-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                               |
|---------|-------------|----------------------------------------|
| 2 097 152 | 0x00200000  | **msidbControlAttributesFstonepyVolume** |



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control, incluya el bit FloppyVolume en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



