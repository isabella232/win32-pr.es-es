---
description: Windows Installer contiene funcionalidad que permite a los desarrolladores de paquetes de instalación crear una interfaz gráfica de usuario (GUI) que se muestra al usuario final durante la instalación.
ms.assetid: 58ef0043-fb30-4f64-9291-e703d7a28bb5
title: Acerca de la interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8639a19c5ec045d77cb90648323388d5cb6e452
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909149"
---
# <a name="about-the-user-interface"></a>Acerca de la interfaz de usuario

Windows Installer contiene funcionalidad que permite a los desarrolladores de paquetes de instalación crear una interfaz gráfica de usuario (GUI) que se muestra al usuario final durante la instalación. Esta interfaz de usuario puede presentar el [comportamiento del Asistente para interfaz de usuario](user-interface-wizard-behavior.md), Mostrar cuadros de diálogo y cartelera y presentar controles interactivos a los usuarios durante la instalación.

La interfaz de usuario interna del instalador se administra y controla a través de un conjunto de tablas de base de datos en Windows Installer misma. El instalador solo proporciona un pequeño conjunto de cuadros de diálogo predeterminados que se han diseñado para controlar los mensajes de información y errores. El autor del paquete debe crear todos los cuadros de diálogo personalizados.

No hay ninguna API de Windows Installer específica para permitir que el autor de un paquete cree una interfaz de usuario mediante programación. Es posible usar la API de Microsoft Windows para crear una interfaz de usuario mediante programación. sin embargo, se recomienda que los autores de paquetes usen la interfaz de usuario interna proporcionada.

Los autores del paquete del instalador crean cuadros de diálogo personalizados escribiendo el nombre de su cuadro de diálogo personalizado en la \_ columna "cuadro de diálogo" de la tabla del cuadro de diálogo y especificando el tamaño, la posición y otros atributos con las columnas restantes.

Windows Installer también implementa un número de controles estándar que el autor de un paquete puede colocar en los cuadros de diálogo. No están disponibles todos los controles estándar de Microsoft Windows y no se pueden crear controles personalizados para usarlos con la interfaz de usuario del instalador.

Los controles se crean en un cuadro de diálogo específico escribiendo el nombre del cuadro de diálogo, la clave principal de la entrada del cuadro de diálogo en la tabla del cuadro de diálogo, en el segundo campo de la tabla de control y especificando el tamaño, la posición y otros atributos del control con las columnas restantes.

Los controles activos deben estar vinculados a un ControlEvent, de la [tabla ControlEvent,](controlevent-table.md) para permitir la interacción del usuario con la instalación. Los controles pasivos que reciben y muestran información se deben suscribir a un ControlEvent, adecuado en la [tabla EventMapping](eventmapping-table.md).

Para obtener más información sobre ControlEvents, vea [información general sobre ControlEvent,](controlevent-overview.md). Tenga en cuenta que un control publica un ControlEvent, si aparece en la tabla ControlEvent, y se suscribe a un evento si se muestra en la tabla EventMapping.

La interfaz de usuario del instalador que se muestra durante la instalación se administra a través de las tablas de secuencia de IU: [InstallUISequence Table](installuisequence-table.md)y [AdminUISequence Table](adminuisequence-table.md). Una de estas tablas de secuencia se ejecuta según la acción de nivel superior que inició la instalación: [instalar](install-action.md), [administrar](admin-action.md)o [anunciar](advertise-action.md).

Para obtener más información sobre la implementación de una interfaz de usuario en Windows Installer, consulte [uso de la interfaz de usuario](using-the-user-interface.md), el esquema de la [interfaz de usuario](user-interface-schema.md), así como los temas individuales de cuadros de diálogo y controles.

 

 



