---
description: Si se establece el bit control FloppyVolume, el control muestra todos los volúmenes implicados en la instalación actual más todos los volúmenes de disquete.
ms.assetid: 65e17920-bb2c-4b98-a2dd-ebaee752ed0a
title: Atributo de control FloppyVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c70045ee5d6e16fbe1f679eafd83e6d657c9bf6e
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127074770"
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
| 2 097 152 | 0x00200000  | **msidbControlAttributesFloppyVolume** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control , incluya el bit FloppyVolume en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



