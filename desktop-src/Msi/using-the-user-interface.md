---
description: Esta sección se centra principalmente en cómo los desarrolladores de paquetes de instalación de crear una interfaz de usuario de instalación (UI) mediante la base de datos del instalador y la interfaz de usuario interna.
ms.assetid: c04e32ba-08a9-49fe-9a4a-db258767f0b3
title: Uso de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714d41ab6b91bb0f3ce519887f7004f919c5c6b2
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127473916"
---
# <a name="using-the-user-interface"></a>Uso de la interfaz de usuario

Esta sección se centra principalmente en cómo los desarrolladores de paquetes de instalación de crear una interfaz de usuario de instalación (UI) mediante la base de datos del instalador y la interfaz de usuario interna. Para obtener más información sobre la diferencia entre una interfaz de usuario interna y externa, vea [Acerca de la Interfaz de usuario](about-the-user-interface.md).

Para mostrar una secuencia o un cuadro de diálogo durante la instalación, el nombre del cuadro de diálogo debe especificarse en la columna Acción de la tabla de secuencia de acciones adecuada. El nombre del cuadro de diálogo debe aparecer en la tabla [InstallUISequence](installuisequence-table.md) o [AdminUISequence](adminuisequence-table.md) en función de si la interfaz de usuario está programada para ejecutarse en la acción [INSTALL](install-action.md), [ADVERTISE](advertise-action.md)o [ADMIN](admin-action.md).

Aunque el instalador admite la creación de cuadros de diálogo y paneles personalizados, también hay una serie de nombres reservados para determinadas secuencias de cuadros de diálogo. Dado que el instalador usa estos nombres al ejecutar determinadas acciones, estos nombres solo deben usarse con los tipos de cuadros de diálogo para los que están reservados. En Cuadros de diálogo se ofrece una lista de estos nombres reservados y una descripción de cada una de las secuencias de cuadros de diálogo [especiales.](dialog-boxes.md)

Las propiedades de cada cuadro de diálogo o cuadro de diálogo de la interfaz de usuario deben especificarse en las tablas [Dialog](dialog-table.md) y [BillBoard,](billboard-table.md) respectivamente. El estilo de cada cuadro de diálogo también debe especificarse en la tabla Dialog estableciendo la marca de bits [de estilo del](dialog-style-bits.md) diálogo.

Los controles y el texto deben agregarse al cuadro de diálogo, y estos deben estar vinculados a [ControlEvents](controlevent-overview.md), para permitir que el usuario interactúe con el proceso de instalación. Vea [Agregar controles y texto](adding-controls-and-text.md) para obtener más información sobre cómo agregar controles a un cuadro de diálogo.

Windows El controlador de interfaz de usuario interno del instalador puede mostrar u ocultar cuadros de diálogo de forma selectiva para controlar el nivel de interactividad del usuario final durante la instalación. Estos niveles de interactividad del usuario final se conocen como completos, reducidos, básicos y ninguno. Vea [Interfaz de usuario levels](user-interface-levels.md). para obtener una descripción completa de estos niveles de IA.

Hay dos métodos para establecer el nivel de interfaz de usuario. El nivel de interfaz de usuario se puede establecer mediante programación con una llamada a [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)y el primer parámetro de **MsiSetInternalUI** especifica el nivel de interfaz de usuario. Los desarrolladores de paquetes también pueden establecer el nivel de interfaz de usuario mediante la [opción de línea de comandos](command-line-options.md) "/q".

El comportamiento de cada uno de los niveles de interfaz de usuario viene determinado por la creación del archivo .msi el desarrollador del paquete. El autor de una interfaz de usuario interna tiene flexibilidad en el comportamiento de estos niveles para un paquete. La disponibilidad de estos niveles depende de la creación del paquete de instalación. El autor debe especificar todos los cuadros de diálogo y controles de la interfaz de usuario en las tablas Dialog y Control.

-   Normalmente, una interfaz de usuario completa muestra el comportamiento del asistente de [interfaz](user-interface-wizard-behavior.md)de usuario, como cada cuadro de diálogo de una secuencia que contiene un **botón>>** siguiente. Esta forma de interfaz de usuario es familiar para muchos usuarios y es el tipo de interfaz de usuario más común para que lo cree un autor. El instalador presenta una secuencia lógica de cuadros de diálogo y solicita al usuario que interactúe con los controles ubicados en cada cuadro de diálogo.
-   Una interfaz de usuario reducida normalmente suprime la presentación del comportamiento del asistente.
-   Normalmente, una interfaz de usuario básica solo muestra los mensajes de progreso al usuario.
-   Un nivel de interfaz de usuario ninguno significa una instalación silenciosa.

Windows El instalador proporciona un indicador de barra de progreso único en el [control ProgressBar](progressbar-control.md) que muestra al usuario una estimación del tiempo total restante hasta que se completa la instalación. Para obtener más información sobre la barra de progreso, vea [Creación de un control ProgressBar](authoring-a-progressbar-control.md).

Los autores de la interfaz de usuario deben facilitar la accesibilidad de su aplicación o producto para todos los usuarios. Para obtener más información sobre Active Accessibility y Windows instalador, vea [Accesibilidad](accessibility.md).

Para obtener más información sobre la creación de una interfaz de usuario, vea Adding [Controls and Text](adding-controls-and-text.md), [Authoring a ProgressBar Control](authoring-a-progressbar-control.md), [Authoring Disk Prompt Messages](authoring-disk-prompt-messages.md), [Authoring a Conditional "Please Wait . . ." Cuadro de mensaje](authoring-a-conditional-please-wait-------message-box.md)y vista [previa del Interfaz de usuario](previewing-the-user-interface.md). Para obtener más información sobre los paneles de autor, [vea Mostrar las pantallas en un cuadro de diálogo modeless.](displaying-billboards-on-a-modeless-dialog.md)

A partir Windows Installer 4.5, se puede incrustar una interfaz de usuario personalizada en el paquete Windows Installer. Para obtener un ejemplo de una interfaz de usuario personalizada incrustada, [consulte Uso de una interfaz de usuario incrustada.](using-an-embedded-ui.md)

 

 



