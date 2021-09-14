---
description: Windows El instalador contiene funcionalidad que permite a los desarrolladores de paquetes de instalación crear una interfaz gráfica de usuario (GUI) que se muestra al usuario final durante la instalación.
ms.assetid: 58ef0043-fb30-4f64-9291-e703d7a28bb5
title: Acerca de la Interfaz de usuario
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8639a19c5ec045d77cb90648323388d5cb6e452
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127159251"
---
# <a name="about-the-user-interface"></a>Acerca de la Interfaz de usuario

Windows El instalador contiene funcionalidad que permite a los desarrolladores de paquetes de instalación crear una interfaz gráfica de usuario (GUI) que se muestra al usuario final durante la instalación. Esta interfaz de usuario puede mostrar el comportamiento del asistente de [interfaz](user-interface-wizard-behavior.md)de usuario, mostrar cuadros de diálogo y paneles, y presentar controles interactivos a los usuarios durante la instalación.

La interfaz de usuario interna del instalador se administra y controla a través de un conjunto de tablas de base de datos Windows instalador. El instalador proporciona solo un pequeño conjunto de cuadros de diálogo predeterminados que están diseñados para controlar mensajes de error e información. El autor del paquete debe crear todos los cuadros de diálogo personalizados.

No hay ninguna API específica Windows Installer para permitir que un autor del paquete cree una interfaz de usuario mediante programación. Es posible usar Microsoft Windows API para crear una interfaz de usuario mediante programación; sin embargo, se recomienda que los autores de paquetes usen la interfaz de usuario interna proporcionada.

Los autores de paquetes del instalador crean cuadros de diálogo personalizados especificando el nombre de su diálogo personalizado en la columna "Cuadro de diálogo" de la tabla de diálogos y especificando el tamaño, la posición y otros atributos mediante las columnas \_ restantes.

Windows El instalador también implementa una serie de controles estándar que un autor del paquete puede colocar en los cuadros de diálogo. No todos los controles estándar Windows microsoft están disponibles y no se pueden crear controles personalizados para su uso con la interfaz de usuario del instalador.

Los controles se crean en un cuadro de diálogo específico especificando el nombre del cuadro de diálogo, la clave principal de la entrada del cuadro de diálogo en la tabla de diálogo, en el segundo campo de la tabla de control y especificando el tamaño, la posición y otros atributos del control mediante las columnas restantes.

Los controles activos deben vincularse a un control ControlEvent en la [tabla ControlEvent](controlevent-table.md) para permitir la interacción del usuario con la instalación. Los controles pasivos que reciben y muestran información deben suscribirse a un control ControlEvent adecuado en la [tabla EventMapping](eventmapping-table.md).

Para obtener más información sobre ControlEvents, vea [Información general de ControlEvent.](controlevent-overview.md) Tenga en cuenta que un control publica un control ControlEvent si aparece en la tabla ControlEvent y se suscribe a un evento si aparece en la tabla EventMapping.

La presentación de la interfaz de usuario del instalador durante la instalación se administra a través de las tablas de secuencia de interfaz de usuario: [InstallUISequence Table](installuisequence-table.md)y [AdminUISequence Table](adminuisequence-table.md). Una de estas tablas de secuencia se ejecuta en función de la acción de nivel superior que inició la instalación: [INSTALL,](install-action.md) [ADMIN](admin-action.md)o [ADVERTISE](advertise-action.md).

Para obtener más información sobre cómo implementar una interfaz de usuario en Windows Installer, vea Usar el esquema [Interfaz de usuario](using-the-user-interface.md), [Interfaz de usuario ,](user-interface-schema.md)así como los temas individuales de los cuadros de diálogo y los controles.

 

 



