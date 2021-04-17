---
description: Si se establece este bit de estilo, el texto del control se muestra en un orden de lectura de derecha a izquierda.
ms.assetid: 68394498-98ca-4bcd-86c0-3f692a26a258
title: Atributo de control RTLRO
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c452a4b5b4533b24e8e59b6fe70dc2884baec0c1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105678245"
---
# <a name="rtlro-control-attribute"></a>Atributo de control RTLRO

Si se establece este bit de estilo, el texto del control se muestra en un orden de lectura de derecha a izquierda.

## <a name="valid-controls"></a>Controles válidos

[GroupBox](groupbox-control.md)

 

[ProgressBar](progressbar-control.md)

 

[Botones](pushbutton-control.md)

 

[ScrollableText](scrollabletext-control.md)

 

[Texto](text-control.md)

 

[VolumeCostList](volumecostlist-control.md)

 

[CheckBox](checkbox-control.md)

 

[ComboBox](combobox-control.md)

 

[DirectoryList](directorylist-control.md)

 

[DirectoryCombo](directorycombo-control.md)

 

[Editar](edit-control.md)

 

[PathEdit](pathedit-control.md)

 

[ListBox](listbox-control.md)

 

[ListView](listview-control.md)

 

[RadioButtonGroup](radiobuttongroup-control.md)

 

[SelectionTree](selectiontree-control.md)

 

[VolumeSelectCombo](volumeselectcombo-control.md)

## <a name="value"></a>Value



| Decimal | Hexadecimal | Constante                        |
|---------|-------------|---------------------------------|
| 32      | 0x00000020  | **msidbControlAttributesRTLRO** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit RTLRO en la columna Attributes del registro del control en la [tabla de control](control-table.md).

Vea [controles y](controls.md) [atributos de control](control-attributes.md) .

 

 



