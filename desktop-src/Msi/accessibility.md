---
description: Los autores deben tener en cuenta las tablas y los campos de la lista siguiente al diseñar su interfaz de usuario para que cumpla con Active Accessibility directrices.
ms.assetid: 516e504e-7895-4388-a38e-fd2fc7dfd61d
title: Accesibilidad (Windows instalador)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8811d47bc7288e966ca5d536b435611c79fd81f3a38fa0b2dbdd422b5939a42
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120078235"
---
# <a name="accessibility-windows-installer"></a>Accesibilidad (Windows instalador)

Los autores deben tener en cuenta las tablas y los campos de la lista siguiente al diseñar su interfaz de usuario para que cumpla con Active Accessibility directrices. La interfaz de usuario de un paquete de instalador debe facilitar la accesibilidad de la aplicación o el producto a todos los usuarios.

-   El texto de la información sobre herramientas se encuentra en la columna Ayuda de la [tabla Control](control-table.md). Los lectores de pantalla muestran este texto para los controles que contienen una imagen.
-   El campo Text de la [tabla Control de](control-table.md) los controles [VolumeCostList](volumecostlist-control.md), [ListView,](listview-control.md) [DirectoryList](directorylist-control.md) y [SelectionTree](selectiontree-control.md) nunca se muestra. En su lugar, se puede leer mediante utilidades de revisión de pantalla como la descripción del control. Las personas que no pueden usar la información visual en la pantalla pueden interpretar la información con la ayuda de una utilidad de revisión de pantalla. Las utilidades de revisión de pantalla (también conocidas como programas de lector de pantalla o utilidades de acceso de voz) toman la información mostrada en la pantalla y la dirigen a través de medios alternativos, como voz sintetizada o una pantalla de Utilities actualizable.
-   Los controles de los cuadros de diálogo deben vincularse mediante el campo Control \_ Siguiente de la tabla [Control](control-table.md). Los controles deben crearse de forma que todos se puedan alcanzar mediante la tecla TAB.
-   Se deben proporcionar teclas de método abreviado para obtener acceso directo a los controles.
-   El color del texto que se muestra en la interfaz de usuario se establece en la [tabla TextStyle](textstyle-table.md). Si el color de texto elegido está demasiado cerca del del fondo, se omite la opción de color del texto.
-   El tamaño y la fuente del texto se establecen en la [tabla TextStyle](textstyle-table.md). Se deben usar tamaños de fuente más grandes para los paquetes destinados al mercado asiático. Por ejemplo, un tamaño de fuente de 10 puntos que sea legible para el texto en inglés puede no ser necesariamente true para el chino.
-   Para [los](edit-control.md)controles Edit , [PathEdit](pathedit-control.md), [ListView](listview-control.md), [ComboBox](combobox-control.md) o [VolumeSelectCombo](volumeselectcombo-control.md), los lectores de pantalla toman accName y accKeyboardShortcut de un control de texto que debe preceder al [control](text-control.md) en la secuencia Control Siguiente del cuadro de \_ diálogo. El lector de pantalla toma accName del campo Texto del control Texto y accKeyboardShortcut del método abreviado de teclado del campo Texto, si existe un acceso directo.
-   Dado que el texto estático no puede tomar el foco, un control Text que describe un [control](text-control.md) [Edit](edit-control.md), [PathEdit](pathedit-control.md), [ListView](listview-control.md), [ComboBox](combobox-control.md) o [VolumeSelectCombo](volumeselectcombo-control.md) debe ser el primer control del cuadro de diálogo para garantizar la compatibilidad con los lectores de pantalla.
-   Para un [control PushButton](pushbutton-control.md) que muestra un icono o una imagen de mapa de bits, accName y accKeyboardShortcut se especifican en el campo Ayuda del registro de tabla [Control,](control-table.md) a la izquierda del \| separador.
-   Evite el uso de controles de texto sobre mapas de bits en blanco porque, en contraste alto negro, el texto puede volverse invisible.
-   No coloque un control de texto negro en un fondo que sea una imagen de mapa de bits en blanco. Este texto no es visible para un usuario que cambia el Windows muestra a contraste alto Negro.
-   No coloque un control de texto blanco en un fondo que sea una imagen de mapa de bits todo negro. Este texto no es visible para un usuario que cambia la Windows a contraste alto Blanco.
-   No coloque controles de [texto transparentes sobre](text-control.md) mapas de bits de color. Es posible que el texto no esté visible si el usuario cambia la combinación de colores para mostrar. Por ejemplo, el texto puede hacerse invisible si el usuario establece el parámetro de contraste alto para la accesibilidad.
-   Tenga en cuenta que el foco en un cuadro de diálogo no se tabula en un [control RadioButtonGroup](radiobuttongroup-control.md) hasta que se ha seleccionado uno de los botones del grupo. Para convertir la pestaña de foco en este grupo de botones, especifique uno de los botones como configuración predeterminada para el control.
-   Para proporcionar a los programas de lector de pantalla texto descriptivo adicional sobre un [control RadioButtonGroup](radiobuttongroup-control.md). Siga el ejemplo proporcionado en [Agregar texto adicional a botones de radio.](adding-extra-text-to-radio-buttons.md)
-   El tamaño relativo de los cuadros de diálogo, los controles y las fuentes puede cambiar en función del tamaño de fuente elegido. Para obtener más información, vea [Unidades del instalador.](installer-units.md) Para asegurarse de que se muestra correctamente el texto y los controles en la interfaz de usuario, los desarrolladores de configuración siempre deben probar su aplicación con todos los tamaños de fuente que se puedan usar.

 

 



