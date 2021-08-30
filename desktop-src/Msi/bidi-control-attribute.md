---
description: Se trata de una combinación de los atributos RTLRO, RightAligned y LeftScroll del orden de lectura de derecha a izquierda.
ms.assetid: 4eaec16f-ee1c-437b-8b76-7ebbdc4e2f71
title: Atributo de control BiDi
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5fd152bbff384961a51350d31759b35ea2b0b4444cac20c78df3dbc7af13bfd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045265"
---
# <a name="bidi-control-attribute"></a>Atributo de control BiDi

Se trata de una combinación del orden de lectura de derecha a izquierda [RTLRO,](rtlro-control-attribute.md)los atributos [RightAligned](rightaligned-control-attribute.md)y [LeftScroll.](leftscroll-control-attribute.md)

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



 

## <a name="remarks"></a>Comentarios

Para establecer este atributo en un control, incluya el bit BiDi en la columna Atributos del registro del control en la [tabla Control](control-table.md).

Vea [Atributos de](control-attributes.md) control y el control que debe crear en [Controles](controls.md).

 

 



