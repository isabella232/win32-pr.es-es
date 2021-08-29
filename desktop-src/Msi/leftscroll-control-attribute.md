---
description: Si se establece este bit, la barra de desplazamiento se encuentra en el lado izquierdo del control.
ms.assetid: bf59ec6b-ac24-4a0b-9326-aea181b7539b
title: Atributo de control LeftScroll
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e3bfbfd0ce92e337b7de3504847c39a3b2250562f05f18280a8f46916909fd0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120043255"
---
# <a name="leftscroll-control-attribute"></a>Atributo de control LeftScroll

Si se establece este bit, la barra de desplazamiento se encuentra en el lado izquierdo del control.

Si no se establece este bit, la barra de desplazamiento se encuentra en el lado derecho del control.

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



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control, incluya el bit LeftScroll en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Controles y atributos](control-attributes.md) de [control.](controls.md)

 

 



