---
description: Los desarrolladores de paquetes de instalación pueden crear una interfaz de usuario que contenga los controles descritos en este tema.
ms.assetid: ed9fa158-9dad-4d2d-8153-78122b19a34e
title: Controles (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ec286adf25c0642ae044bfd0b89e66182ef6839
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104361648"
---
# <a name="controls-windows-installer"></a>Controles (Windows Installer)

Los desarrolladores de paquetes de instalación pueden crear una interfaz de usuario que contenga los controles descritos en este tema. Para obtener información sobre cómo agregar un control determinado a un cuadro de diálogo, vea el tema correspondiente a ese control y lea la sección [Agregar controles y texto](adding-controls-and-text.md).

Algunos controles, como CheckBox y ComboBox, están asociados a una propiedad especificada en la columna de propiedades de la [tabla de control](control-table.md). Un usuario cambia el valor de esta propiedad interactuando con el control. Los controles pasivos, como la cartelera y el mapa de bits, no están asociados a este tipo de propiedad.

Por seguridad, los usuarios que interactúan con la interfaz de usuario no pueden cambiar las propiedades privadas. Para que la interfaz de usuario establezca una propiedad, debe ser una propiedad pública y en mayúsculas. Vea también [About Properties (propiedades](about-properties.md)).

En algunos casos, un control puede volver a dibujarse incorrectamente al cancelar un diálogo. Esto tiene que hacer con el orden en que los controles reciben mensajes de WM \_ Paint después de quitar el cuadro de diálogo cancelar. Para corregirlo, intente cambiar el orden de los controles en la tabla de control.



| Nombre del control                                       | Propiedad asociada | Breve descripción del control                                                                                                                                                          |
|----------------------------------------------------|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Valla](billboard-control.md)                 | No                  | Muestra las cartelera basadas en mensajes de progreso.                                                                                                                                       |
| [Bitmap](bitmap-control.md)                       | No                  | Muestra una imagen estática de un mapa de bits.                                                                                                                                                |
| [CheckBox](checkbox-control.md)                   | Sí                 | Casilla de dos Estados.                                                                                                                                                                |
| [ComboBox](combobox-control.md)                   | Sí                 | Lista desplegable con un campo de edición.                                                                                                                                                  |
| [DirectoryCombo](directorycombo-control.md)       | Sí                 | Seleccione todo excepto el último segmento de la ruta de acceso.                                                                                                                                       |
| [DirectoryList](directorylist-control.md)         | Sí                 | Muestra las carpetas situadas debajo de la parte principal de la ruta de acceso.                                                                                                                                         |
| [Editar](edit-control.md)                           | Sí                 | Un campo de edición normal para cualquier cadena o entero.                                                                                                                                       |
| [GroupBox](groupbox-control.md)                   | No                  | Muestra un rectángulo que agrupa otros controles.                                                                                                                             |
| [Hipervínculo](hyperlink-control.md)                 | No                  | Muestra un vínculo HTML a una dirección, que se abre en el explorador predeterminado. **[Windows Installer 4,5 y versiones anteriores](not-supported-in-windows-installer-4-5.md):** No compatible.<br/> |
| [Icono](icon-control.md)                           | No                  | Muestra una imagen estática de un icono.                                                                                                                                                 |
| [Line](line-control.md)                           | No                  | Muestra una línea horizontal.                                                                                                                                                           |
| [ListBox](listbox-control.md)                     | Sí                 | Lista desplegable sin un campo de edición.                                                                                                                                               |
| [ListView](listview-control.md)                   | Sí                 | Muestra una columna de valores con iconos para la selección.                                                                                                                                 |
| [MaskedEdit](maskededit-control.md)               | Sí                 | Un campo de edición con una máscara en el campo de texto.                                                                                                                                          |
| [PathEdit](pathedit-control.md)                   | Sí                 | Muestra el nombre de la carpeta o la ruta de acceso completa en un campo de edición.                                                                                                                                 |
| [ProgressBar (control)](progressbar-control.md)     | No                  | Gráfico de barras que cambia la longitud a medida que recibe mensajes de progreso.                                                                                                                       |
| [Botones](pushbutton-control.md)               | No                  | Muestra un botón de reenvío básico.                                                                                                                                                         |
| [RadioButtonGroup](radiobuttongroup-control.md)   | Sí                 | Un grupo de botones de radio.                                                                                                                                                             |
| [ScrollableText](scrollabletext-control.md)       | No                  | Muestra una cadena de texto larga.                                                                                                                                                       |
| [SelectionTree](selectiontree-control.md)         | Sí                 | Muestra información de la tabla de características y permite al usuario cambiar su estado de selección.                                                                                     |
| [Texto](text-control.md)                           | No                  | Muestra texto estático.                                                                                                                                                                 |
| [VolumeCostList](volumecostlist-control.md)       | No                  | Muestra información de costos en volúmenes diferentes.                                                                                                                                    |
| [VolumeSelectCombo](volumeselectcombo-control.md) | Sí                 | Selecciona volumen en una lista alfabética.                                                                                                                                             |



 

 

 




