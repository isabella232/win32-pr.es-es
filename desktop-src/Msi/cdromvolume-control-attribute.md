---
description: Si se establece el bit CDROMVolume Control, el control muestra todos los volúmenes de la instalación actual más todos los volúmenes de CD-ROM.
ms.assetid: 233df659-413d-416e-a3d7-d05a67e9bd73
title: CdROMVolume (atributo de control)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 78abd961ddfd710defea9b464ea861f731fcf84a0989062f0607fda8ced5b381
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078045"
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



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control , incluya el bit CDROMVolume en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



