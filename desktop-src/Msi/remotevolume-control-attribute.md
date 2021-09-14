---
description: Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual más todos los volúmenes remotos. Si no se establece este bit, el control enumera los volúmenes de la instalación actual.
ms.assetid: be70cd86-6aaf-4307-a553-715d6185accd
title: Atributo de control RemoteVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eeabf4ea1f0174700301c23e780d0933f62743f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127069659"
---
# <a name="remotevolume-control-attribute"></a>Atributo de control RemoteVolume

Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual más todos los volúmenes remotos. Si no se establece este bit, el control enumera los volúmenes de la instalación actual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

[VolumeCostList](volumecostlist-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                               |
|---------|-------------|----------------------------------------|
| 262 144  | 0x00040000  | **msidbControlAttributesRemoteVolume** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control , incluya el bit RemoteVolume en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Controles y atributos](control-attributes.md) de [control.](controls.md)

 

 



