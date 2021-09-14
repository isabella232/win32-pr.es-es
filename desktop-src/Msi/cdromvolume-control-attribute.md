---
description: Si se establece el bit CDROMVolume Control, el control muestra todos los volúmenes de la instalación actual más todos los volúmenes de CD-ROM.
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: CdROMVolume (atributo de control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25a687cfd52f347d9bfd24e74fb10b15f865e13b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127158936"
---
# <a name="cdromvolume-control-attribute"></a>CdROMVolume (atributo de control)

Si se establece el bit CDROMVolume Control, el control muestra todos los volúmenes de la instalación actual más todos los volúmenes de CD-ROM.

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

Para establecer este atributo en un control, incluya el bit CDROMVolume en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



