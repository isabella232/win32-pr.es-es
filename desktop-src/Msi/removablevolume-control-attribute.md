---
description: Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual más todos los volúmenes extraíbles. Si no se establece este bit, el control enumera los volúmenes de la instalación actual.
ms.assetid: fc16ca46-54a1-4b24-ba51-8b4d358268f4
title: Atributo de control RemovableVolume
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9da559935a6f325c9f47fdbd902fe7b586870327b8107b14b6ae421f472a659
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119912785"
---
# <a name="removablevolume-control-attribute"></a>Atributo de control RemovableVolume

Si se establece este bit, el control muestra todos los volúmenes implicados en la instalación actual más todos los volúmenes extraíbles. Si no se establece este bit, el control enumera los volúmenes de la instalación actual.

## <a name="valid-controls"></a>Controles válidos

[DirectoryCombo](directorycombo-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                                  |
|---------|-------------|-------------------------------------------|
| 65536   | 0x00010000  | **msidbControlAttributesRemovableVolume** |



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control , incluya el bit RemovableVolume en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Controles y atributos](control-attributes.md) de [control.](controls.md)

 

 



