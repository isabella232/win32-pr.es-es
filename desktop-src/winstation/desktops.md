---
title: Escritorios
description: Un escritorio tiene una superficie de presentación lógica y contiene objetos de interfaz de usuario, como ventanas, menús y enlaces. se puede usar para crear y administrar ventanas.
ms.assetid: c56cd63b-c260-40d0-9a62-1dee1eb18679
keywords:
- objetos de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b763c05c3d45c701da0bdd606fa906dec3f8af07ce72d256b402e7df5d9319b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119587355"
---
# <a name="desktops"></a>Escritorios

Un *escritorio* tiene una superficie de presentación lógica y contiene objetos de interfaz de usuario, como ventanas, menús y enlaces. se puede usar para crear y administrar ventanas. Cada objeto de escritorio es un objeto protegible. Cuando se crea un escritorio, se asocia a la estación de [ventana](window-stations.md) actual del proceso de llamada y se asigna al subproceso que realiza la llamada.

Los mensajes de ventana solo se pueden enviar entre procesos que se encuentran en el mismo escritorio. Además, el procedimiento de enlace de un proceso que se ejecuta en un escritorio determinado solo puede recibir mensajes destinados a ventanas creadas en el mismo escritorio.

Los escritorios asociados a la estación de ventanas interactivas, Winsta0, se pueden crear para mostrar una interfaz de usuario y recibir la entrada del usuario, pero solo uno de estos escritorios a la vez está activo. Este escritorio activo, también conocido como escritorio de *entrada,* es el que está visible actualmente para el usuario y que recibe la entrada del usuario. Las aplicaciones pueden usar [**la función OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) para obtener un identificador para el escritorio de entrada. Las aplicaciones que tienen el acceso necesario pueden usar [**la función SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) para especificar un escritorio de entrada diferente.

De forma predeterminada, hay tres escritorios en la estación de ventana interactiva: Default, ScreenSaver y Winlogon.

El escritorio predeterminado se crea cuando Winlogon inicia el proceso inicial como usuario que ha iniciado sesión. En ese momento, el escritorio predeterminado se activa y se usa para interactuar con el usuario.

Cada vez que se activa un protector de pantalla seguro, el sistema cambia automáticamente al escritorio ScreenSaver, que protege los procesos en el escritorio predeterminado de usuarios no autorizados. Los protectores de pantalla no seguros se ejecutan en winsta0 \\ predeterminado.

El escritorio winlogon está activo mientras un usuario inicia sesión. El sistema cambia al escritorio predeterminado cuando el shell indica que está listo para mostrar algo, o después de treinta segundos, lo que llegue primero. Durante la sesión del usuario, el sistema cambia al escritorio winlogon cuando el usuario presiona la secuencia de teclas CTRL+ALT+SUPR, o cuando el cuadro de diálogo Control de cuentas de usuario (UAC) está abierto.

**Windows Server 2003 y Windows XP/2000:** No se admite el cuadro de diálogo UAC.

El descriptor de seguridad del escritorio winlogon permite el acceso a un conjunto muy restringido de cuentas, incluida [la cuenta LocalSystem](/windows/desktop/Services/localsystem-account). Por lo general, las aplicaciones no incluyen ningún SID de estas cuentas en sus tokens y, por tanto, no pueden acceder al escritorio winlogon ni cambiar a otro escritorio mientras el escritorio de Winlogon está activo.

Para obtener más información, vea los temas siguientes:

-   [Estación de ventana y creación de escritorio](window-station-and-desktop-creation.md)
-   [Conexión de subprocesos a un escritorio](thread-connection-to-a-desktop.md)
-   [Derechos de acceso y seguridad de escritorio](desktop-security-and-access-rights.md)

 

 