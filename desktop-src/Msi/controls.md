---
description: Los desarrolladores de paquetes de instalación pueden crear una interfaz de usuario que contenga los controles que se debaten en este tema.
ms.assetid: ed9fa158-9dad-4d2d-8153-78122b19a34e
title: Controles (Windows Instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47755cafc3d4d3d04ed443410571a9c4fc2cf215a3efb3584265dcbeb2f9d520
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143369"
---
# <a name="controls-windows-installer"></a>Controles (Windows Instalador)

Los desarrolladores de paquetes de instalación pueden crear una interfaz de usuario que contenga los controles que se debaten en este tema. Para obtener información sobre cómo agregar un control determinado a un cuadro de diálogo, vea el tema de ese control y lea la sección [Agregar controles y texto](adding-controls-and-text.md).

Algunos controles, como CheckBox y ComboBox, están asociados a una propiedad especificada en la columna Property de la [tabla Control](control-table.md). Un usuario cambia el valor de esta propiedad mediante la interacción con el control . Los controles pasivos, como Asín y Mapa de bits, no están asociados a dicha propiedad.

Por motivos de seguridad, un usuario que interactúa con la interfaz de usuario no puede cambiar las propiedades privadas. Para que la interfaz de usuario establezca una propiedad, debe ser una propiedad pública y en mayúsculas. Vea también [Acerca de las propiedades](about-properties.md).

En algunos casos, un control puede volver a dibujarse incorrectamente al cancelar un cuadro de diálogo. Esto tiene que ver con el orden en que los controles reciben mensajes \_ WM PAINT después de quitar el cuadro de diálogo Cancelar. Para corregirlo, intente cambiar el orden de los controles de la tabla Control.



| Nombre del control                                       | Propiedad asociada | Breve descripción del control                                                                                                                                                          |
|----------------------------------------------------|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Cartelera](billboard-control.md)                 | No                  | Muestra los paneles de pantalla basados en los mensajes de progreso.                                                                                                                                       |
| [Bitmap](bitmap-control.md)                       | No                  | Muestra una imagen estática de un mapa de bits.                                                                                                                                                |
| [CheckBox](checkbox-control.md)                   | Sí                 | Casilla de verificación de dos estados.                                                                                                                                                                |
| [ComboBox](combobox-control.md)                   | Sí                 | Lista desplegable con un campo de edición.                                                                                                                                                  |
| [DirectoryCombo](directorycombo-control.md)       | Sí                 | Seleccione todos excepto el último segmento de la ruta de acceso.                                                                                                                                       |
| [DirectoryList](directorylist-control.md)         | Sí                 | Muestra las carpetas debajo de la parte principal de la ruta de acceso.                                                                                                                                         |
| [Editar](edit-control.md)                           | Sí                 | Campo de edición normal para cualquier cadena o entero.                                                                                                                                       |
| [GroupBox](groupbox-control.md)                   | No                  | Muestra un rectángulo que agrupa otros controles.                                                                                                                             |
| [Hipervínculo](hyperlink-control.md)                 | No                  | Muestra un vínculo HTML a una dirección, que se abre en el explorador predeterminado. **[Windows instalador 4.5 y versiones anteriores:](not-supported-in-windows-installer-4-5.md)** No se admite.<br/> |
| [Icono](icon-control.md)                           | No                  | Muestra una imagen estática de un icono.                                                                                                                                                 |
| [Línea](line-control.md)                           | No                  | Muestra una línea horizontal.                                                                                                                                                           |
| [ListBox](listbox-control.md)                     | Sí                 | Lista desplegable sin un campo de edición.                                                                                                                                               |
| [ListView](listview-control.md)                   | Sí                 | Muestra una columna de valores con iconos para la selección.                                                                                                                                 |
| [MaskedEdit](maskededit-control.md)               | Sí                 | Campo de edición con una máscara en el campo de texto.                                                                                                                                          |
| [PathEdit](pathedit-control.md)                   | Sí                 | Muestra el nombre de la carpeta o la ruta de acceso completa en un campo de edición.                                                                                                                                 |
| [Control ProgressBar](progressbar-control.md)     | No                  | Gráfico de barras que cambia la longitud a medida que recibe mensajes de progreso.                                                                                                                       |
| [Pulsador](pushbutton-control.md)               | No                  | Muestra un botón de inserción básico.                                                                                                                                                         |
| [RadioButtonGroup](radiobuttongroup-control.md)   | Sí                 | Un grupo de botones de radio.                                                                                                                                                             |
| [ScrollableText](scrollabletext-control.md)       | No                  | Muestra una cadena larga de texto.                                                                                                                                                       |
| [SelectionTree](selectiontree-control.md)         | Sí                 | Muestra información de la tabla Característica y permite al usuario cambiar su estado de selección.                                                                                     |
| [Texto](text-control.md)                           | No                  | Muestra texto estático.                                                                                                                                                                 |
| [VolumeCostList](volumecostlist-control.md)       | No                  | Muestra información de costos en distintos volúmenes.                                                                                                                                    |
| [VolumeSelectCombo](volumeselectcombo-control.md) | Sí                 | Selecciona el volumen de una lista alfabética.                                                                                                                                             |



 

 

 




