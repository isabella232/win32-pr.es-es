---
title: Escritorios
description: Un escritorio tiene una superficie de visualización lógica y contiene objetos de la interfaz de usuario, como ventanas, menús y enlaces. se puede usar para crear y administrar Windows.
ms.assetid: c56cd63b-c260-40d0-9a62-1dee1eb18679
keywords:
- objetos de escritorio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44ca0b390ec4d34cc943c9d18d958cdea6466634
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105714409"
---
# <a name="desktops"></a>Escritorios

Un *escritorio* tiene una superficie de visualización lógica y contiene objetos de la interfaz de usuario, como ventanas, menús y enlaces. se puede usar para crear y administrar Windows. Cada objeto de escritorio es un objeto protegible. Cuando se crea un escritorio, se asocia a la estación de [ventana](window-stations.md) actual del proceso de llamada y se asigna al subproceso que realiza la llamada.

Los mensajes de ventana solo se pueden enviar entre procesos que se encuentran en el mismo escritorio. Además, el procedimiento de enlace de un proceso que se ejecuta en un escritorio determinado solo puede recibir mensajes destinados a Windows creados en el mismo escritorio.

Los escritorios asociados con la estación de ventana interactiva, Winsta0, se pueden crear para mostrar una interfaz de usuario y recibir datos proporcionados por el usuario, pero solo uno de estos escritorios a la vez está activo. Este Active Desktop, también conocido como *escritorio de entrada*, es el que está visible actualmente para el usuario y que recibe la entrada del usuario. Las aplicaciones pueden usar la función [**OpenInputDesktop**](/windows/win32/api/winuser/nf-winuser-openinputdesktop) para obtener un identificador del escritorio de entrada. Las aplicaciones que tienen el acceso necesario pueden usar la función [**SwitchDesktop**](/windows/win32/api/winuser/nf-winuser-switchdesktop) para especificar un escritorio de entrada diferente.

De forma predeterminada, hay tres equipos de escritorio en la estación de ventana interactiva: predeterminado, protector de pantalla y Winlogon.

El escritorio predeterminado se crea cuando Winlogon inicia el proceso inicial como el usuario que ha iniciado sesión. En ese momento, el escritorio predeterminado se activa y se usa para interactuar con el usuario.

Cada vez que se activa un protector de pantalla seguro, el sistema cambia automáticamente al escritorio del protector de pantalla, que protege los procesos del escritorio predeterminado de usuarios no autorizados. Los protectores de pantalla no seguros se ejecutan en el \\ valor predeterminado de Winsta0.

El escritorio Winlogon está activo mientras un usuario inicia sesión. El sistema cambia al escritorio predeterminado cuando el shell indica que está listo para mostrar algo o después de treinta segundos, lo que suceda primero. Durante la sesión del usuario, el sistema cambia al escritorio Winlogon cuando el usuario presiona la secuencia de teclas CTRL + ALT + SUPR, o cuando el cuadro de diálogo control de cuentas de usuario (UAC) está abierto.

**Windows Server 2003 y Windows XP/2000:** No se admite el cuadro de diálogo UAC.

El descriptor de seguridad del escritorio de Winlogon permite el acceso a un conjunto de cuentas muy restringido, incluida la [cuenta LocalSystem](/windows/desktop/Services/localsystem-account). Por lo general, las aplicaciones no incluyen los SID de estas cuentas en sus tokens y, por lo tanto, no pueden tener acceso al escritorio Winlogon ni cambiar a otro escritorio mientras el escritorio Winlogon está activo.

Para obtener más información, vea los temas siguientes:

-   [Creación de estación de ventana y escritorio](window-station-and-desktop-creation.md)
-   [Conexión de subprocesos a un escritorio](thread-connection-to-a-desktop.md)
-   [Seguridad de escritorio y derechos de acceso](desktop-security-and-access-rights.md)

 

 