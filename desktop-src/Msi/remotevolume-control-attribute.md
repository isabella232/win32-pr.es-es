---
description: Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual, además de todos los volúmenes remotos. Si no se establece este bit, el control muestra los volúmenes en la instalación actual.
ms.assetid: be70cd86-6aaf-4307-a553-715d6185accd
title: Atributo de control RemoteVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeabf4ea1f0174700301c23e780d0933f62743f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677355"
---
# <a name="remotevolume-control-attribute"></a>Atributo de control RemoteVolume

Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual, además de todos los volúmenes remotos. Si no se establece este bit, el control muestra los volúmenes en la instalación actual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

[VolumeCostList](volumecostlist-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                               |
|---------|-------------|----------------------------------------|
| 262 144  | 0x00040000  | **msidbControlAttributesRemoteVolume** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit RemoteVolume en la columna Attributes del registro del control en la [tabla de control](control-table.md).

Vea [controles y](controls.md) [atributos de control](control-attributes.md) .

 

 



