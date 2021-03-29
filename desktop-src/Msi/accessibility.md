---
description: Los autores deben tener en cuenta las tablas y los campos de la siguiente lista al diseñar la interfaz de usuario para que cumplan las directrices de Active Accessibility.
ms.assetid: 516e504e-7895-4388-a38e-fd2fc7dfd61d
title: Accesibilidad (Windows Installer)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46325c11337ef1e1db6f2da5728f06f9d4ee0649
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909146"
---
# <a name="accessibility-windows-installer"></a>Accesibilidad (Windows Installer)

Los autores deben tener en cuenta las tablas y los campos de la siguiente lista al diseñar la interfaz de usuario para que cumplan las directrices de Active Accessibility. La interfaz de usuario de un paquete del instalador debe facilitar la accesibilidad de la aplicación o el producto a todos los usuarios.

-   El texto de información sobre herramientas se encuentra en la columna de ayuda de la [tabla de control](control-table.md). Los lectores de pantalla muestran este texto para los controles que contienen una imagen.
-   Nunca se muestra el campo de texto de la [tabla de control](control-table.md) de los controles [VolumeCostList](volumecostlist-control.md), [ListView](listview-control.md), [DirectoryList](directorylist-control.md) y [SelectionTree](selectiontree-control.md) . En su lugar, las utilidades de revisión de pantalla pueden leerla como Descripción del control. Las personas que no pueden usar la información visual de la pantalla pueden interpretar la información con la ayuda de una utilidad de revisión de pantalla. Las utilidades de revisión de pantalla (también denominadas programas de lector de pantalla o utilidades de acceso de voz) toman la información mostrada en pantalla y la dirigen a través de medios alternativos, como voz sintetizada o pantalla de Braille actualizable.
-   Los controles de los cuadros de diálogo se deben vincular mediante el \_ campo de control siguiente de la [tabla de control](control-table.md). Los controles deben crearse de modo que se puedan alcanzar todos mediante la tecla TAB.
-   Se deben proporcionar teclas de método abreviado para obtener acceso a los controles directamente.
-   El color del texto que se muestra en la interfaz de usuario se establece en la [tabla TextStyle](textstyle-table.md). Si el color del texto elegido está demasiado cerca del del fondo, se omite la opción de color del texto.
-   El tamaño y la fuente del texto se establecen en la [tabla TextStyle](textstyle-table.md). Los tamaños de fuente mayores deben usarse para los paquetes destinados al mercado asiático. Por ejemplo, es posible que un tamaño de fuente de 10 puntos que sea legible para el texto en inglés no sea necesariamente verdadero para el chino.
-   En el caso de [los controles](volumeselectcombo-control.md) [Edit](edit-control.md), [PathEdit](pathedit-control.md), [ListView](listview-control.md), [ComboBox](combobox-control.md) o VolumeSelectCombo, los lectores de pantalla toman accName y accKeyboardShortcut de un [control de texto](text-control.md) que debe preceder al control en la \_ siguiente secuencia de control del cuadro de diálogo. El lector de pantalla toma accName del campo de texto del control de texto y accKeyboardShortcut del método abreviado de teclado en el campo de texto, si existe un acceso directo.
-   Dado que el texto estático no puede tomar el foco, un [control de texto](text-control.md) que describe un control [Edit](edit-control.md), [PathEdit](pathedit-control.md), [ListView](listview-control.md), [ComboBox](combobox-control.md) o [VolumeSelectCombo](volumeselectcombo-control.md) se debe convertir en el primer control del cuadro de diálogo para garantizar la compatibilidad con los lectores de pantalla.
-   Para un [control Pushbutton](pushbutton-control.md) que muestra un icono o una imagen de mapa de bits, AccName y accKeyboardShortcut se especifican en el campo ayuda del registro de la [tabla de control](control-table.md) , a la izquierda del \| separador.
-   Evite el uso de controles de texto en la parte superior de los mapas de bits en blanco porque, en contraste alto negro, el texto puede quedar invisible.
-   No coloque un control de texto negro en un fondo que sea una imagen de mapa de bits en blanco. Este texto no es visible para un usuario que cambie la pantalla de Windows a contraste alto negro.
-   No coloque un control de texto blanco sobre un fondo que sea una imagen de mapa de bits de color negro. Este texto no es visible para un usuario que cambie la pantalla de Windows a contraste alto blanco.
-   No coloque controles de [texto](text-control.md) transparente sobre los mapas de bits de color. Es posible que el texto no esté visible si el usuario cambia la combinación de colores de la pantalla. Por ejemplo, el texto puede volverse invisible si el usuario establece el parámetro de contraste alto para accesibilidad.
-   Tenga en cuenta que el foco en un cuadro de diálogo no lleva a un [control RadioButtonGroup](radiobuttongroup-control.md) hasta que se ha seleccionado uno de los botones del grupo. Para convertir la pestaña enfoque en este grupo de botones, especifique uno de los botones como valor predeterminado para el control.
-   Para proporcionar a los programas de lector de pantalla texto descriptivo adicional sobre un [control RadioButtonGroup](radiobuttongroup-control.md). Siga el ejemplo [que se proporciona en agregar texto adicional a los botones de radio](adding-extra-text-to-radio-buttons.md).
-   El tamaño relativo de los cuadros de diálogo, controles y fuentes puede cambiar en función del tamaño de fuente elegido. Para obtener más información, consulte [unidades de instalador](installer-units.md). Para garantizar la presentación correcta del texto y los controles en la interfaz de usuario, los desarrolladores del programa de instalación siempre deben probar la aplicación con todos los tamaños de fuente que se puedan utilizar.

 

 



