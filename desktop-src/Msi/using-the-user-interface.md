---
description: Esta sección se centra principalmente en la forma en que los desarrolladores de paquetes de instalación crean una interfaz de usuario (UI) de instalación mediante la base de datos del instalador y la interfaz de usuario interna.
ms.assetid: c04e32ba-08a9-49fe-9a4a-db258767f0b3
title: Uso de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 714d41ab6b91bb0f3ce519887f7004f919c5c6b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104276836"
---
# <a name="using-the-user-interface"></a>Uso de la interfaz de usuario

Esta sección se centra principalmente en la forma en que los desarrolladores de paquetes de instalación crean una interfaz de usuario (UI) de instalación mediante la base de datos del instalador y la interfaz de usuario interna. Para obtener más información sobre la diferencia entre una interfaz de usuario interna y externa, vea [acerca de la interfaz de usuario](about-the-user-interface.md).

Para mostrar una secuencia o una cartelera de cuadros de diálogo durante la instalación, debe escribir el nombre del cuadro de diálogo en la columna Acción de la tabla de secuencia de acciones adecuada. El nombre del cuadro de diálogo debe aparecer en la [tabla](adminuisequence-table.md) [InstallUISequence](installuisequence-table.md) o AdminUISequence, en función de si la interfaz de usuario está programada para ejecutarse en la [acción](admin-action.md)de [instalación](install-action.md), [anuncio](advertise-action.md)o administrador.

Aunque el instalador admite la creación de cuadros de diálogo y de cartelera personalizados, también hay varios nombres reservados para ciertas secuencias de cuadro de diálogo. Dado que el instalador usa estos nombres al ejecutar determinadas acciones, estos nombres solo se deben usar con los tipos de cuadros de diálogo para los que están reservados. En los [cuadros de diálogo](dialog-boxes.md)se proporciona una lista de estos nombres reservados y una descripción de cada una de las secuencias de cuadros de diálogo especiales.

Las propiedades de cada cuadro de diálogo o de la cartelera en la interfaz de usuario deben especificarse en las tablas [Dialog](dialog-table.md) y [cartelera](billboard-table.md) , respectivamente. El estilo de cada cuadro de diálogo también se debe especificar en la tabla de diálogo estableciendo la marca de [bits de estilo del](dialog-style-bits.md) cuadro de diálogo.

Los controles y el texto se deben agregar al cuadro de diálogo y deben estar vinculados a [ControlEvents](controlevent-overview.md)para permitir que el usuario interactúe con el proceso de instalación. Vea [Agregar controles y texto](adding-controls-and-text.md) para obtener más información sobre cómo agregar controles a un cuadro de diálogo.

Windows Installer controlador de la interfaz de usuario interna puede mostrar u ocultar selectivamente los cuadros de diálogo para controlar el nivel de interactividad del usuario final durante la instalación. Estos niveles de interactividad del usuario final se conocen como Full, Reduced, Basic y none. Vea [niveles](user-interface-levels.md)de la interfaz de usuario. para obtener una descripción completa de estos UIlevels.

Hay dos métodos para establecer el nivel de la interfaz de usuario. El nivel de interfaz de usuario se puede establecer mediante programación con una llamada a [**MsiSetInternalUI**](/windows/desktop/api/Msi/nf-msi-msisetinternalui)y el primer parámetro de **MsiSetInternalUI** especifica el nivel de la interfaz de usuario. Los desarrolladores de paquetes también pueden establecer el nivel de la interfaz de usuario mediante la [opción de línea de comandos](command-line-options.md) "/q".

El desarrollador del paquete determina el comportamiento de cada uno de los niveles de la interfaz de usuario. El autor de una interfaz de usuario interna tiene flexibilidad en cuanto a cómo se comportan estos niveles para un paquete. La disponibilidad de estos niveles depende de la creación del paquete de instalación. El autor debe especificar cada cuadro de diálogo y control en la interfaz de usuario en las tablas de controles y cuadros de diálogo.

-   Una interfaz de usuario completa normalmente exhibe el [comportamiento del Asistente para la interfaz de usuario](user-interface-wizard-behavior.md), como cada cuadro de diálogo en una secuencia que contiene un botón **>>siguiente** . Esta forma de interfaz de usuario está familiarizada con muchos usuarios y es el tipo de interfaz de usuario más común para que la cree un autor. El instalador presenta una secuencia lógica de cuadros de diálogo y solicita al usuario que interactúe con los controles ubicados en cada cuadro de diálogo.
-   Una interfaz de usuario reducida suprime normalmente la visualización del comportamiento del asistente.
-   Una interfaz de usuario básica normalmente solo muestra mensajes de progreso al usuario.
-   Un nivel de interfaz de usuario de ninguno significa una instalación silenciosa.

Windows Installer proporciona un indicador de barra de progreso único en el [control ProgressBar](progressbar-control.md) que muestra al usuario una estimación del tiempo total restante hasta que se complete la instalación. Para obtener más información sobre la barra de progreso, vea [crear un control ProgressBar](authoring-a-progressbar-control.md).

Los autores de la interfaz de usuario deben facilitar la accesibilidad de su aplicación o producto para todos los usuarios. Para obtener más información sobre Active Accessibility y Windows Installer, vea [accesibilidad](accessibility.md).

Para obtener más información sobre cómo crear una interfaz de usuario, vea [Agregar controles y texto](adding-controls-and-text.md), [crear un control ProgressBar](authoring-a-progressbar-control.md), [crear mensajes de petición de disco](authoring-disk-prompt-messages.md)y [crear una instrucción condicional "espere..." Cuadro de mensaje](authoring-a-conditional-please-wait-------message-box.md)y [vista previa de la interfaz de usuario](previewing-the-user-interface.md). Para obtener más información sobre el autor de las cartelera, consulte [visualización de las cartelera en un cuadro de diálogo no modal](displaying-billboards-on-a-modeless-dialog.md) .

A partir de Windows Installer 4,5, se puede incrustar una interfaz de usuario personalizada en el paquete de Windows Installer. Para obtener un ejemplo de una interfaz de usuario personalizada incrustada, vea [usar una interfaz de usuario incrustada](using-an-embedded-ui.md).

 

 



