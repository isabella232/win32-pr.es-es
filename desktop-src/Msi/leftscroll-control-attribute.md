---
description: Si se establece este bit, la barra de desplazamiento se encuentra en el lado izquierdo del control.
ms.assetid: bf59ec6b-ac24-4a0b-9326-aea181b7539b
title: Atributo de control LeftScroll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99505e66f6f49b0a148b80a96d68bbef70d0f2b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686800"
---
# <a name="leftscroll-control-attribute"></a>Atributo de control LeftScroll

Si se establece este bit, la barra de desplazamiento se encuentra en el lado izquierdo del control.

Si no se establece este bit, la barra de desplazamiento está en el lado derecho del control.

## <a name="valid-controls"></a>Controles válidos

[ScrollableText](scrollabletext-control.md)

[VolumeCostList](volumecostlist-control.md)

[ComboBox](combobox-control.md)

[DirectoryList](directorylist-control.md)

[DirectoryCombo](directorycombo-control.md)

[Editar](edit-control.md)

[ListBox](listbox-control.md)

[ListView](listview-control.md)

[SelectionTree](selectiontree-control.md)

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                             |
|---------|-------------|--------------------------------------|
| 128     | 0x00000080  | **msidbControlAttributesLeftScroll** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit LeftScroll en la columna Attributes del registro del control en la [tabla de control](control-table.md).

Vea [controles y](controls.md) [atributos de control](control-attributes.md) .

 

 



