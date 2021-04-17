---
description: Se trata de una combinación del orden de lectura de derecha a izquierda RTLRO, los atributos RightAligned y LeftScroll.
ms.assetid: 4eaec16f-ee1c-437b-8b76-7ebbdc4e2f71
title: Atributo de control BiDi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 556195c1b3170983083473598f69acb99cdcfaf7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105652603"
---
# <a name="bidi-control-attribute"></a>Atributo de control BiDi

Se trata de una combinación del orden de lectura de derecha a izquierda [RTLRO](rtlro-control-attribute.md), los atributos [RightAligned](rightaligned-control-attribute.md)y [LeftScroll](leftscroll-control-attribute.md) .

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



| Decimal | Hexadecimal | Constante                       |
|---------|-------------|--------------------------------|
| 224     | 0x000000E0  | **msidbControlAttributesBiDi** |



 

## <a name="remarks"></a>Observaciones

Para establecer este atributo en un control, incluya el bit BiDi en la columna Attributes del registro del control en la [tabla de control](control-table.md).

Vea [atributos de control](control-attributes.md) y el control que debe crear en [controles](controls.md).

 

 



