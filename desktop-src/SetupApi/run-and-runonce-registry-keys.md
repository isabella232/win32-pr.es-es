---
description: Ejecutar y RunOnce las claves del registro hacen que los programas se ejecuten cada vez que un usuario inicia sesión.
ms.assetid: 5a6c17f1-d4c0-4005-9b26-036d8b27703a
title: Ejecutar y RunOnce claves del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89cf51ad3c7e2096aeffbbd6ed98c02a202f2ce8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105669791"
---
# <a name="run-and-runonce-registry-keys"></a>Ejecutar y RunOnce claves del registro

Ejecutar y RunOnce las claves del registro hacen que los programas se ejecuten cada vez que un usuario inicia sesión. El valor de datos de una clave es una línea de comandos de no más de 260 caracteres. Registre los programas que se van a ejecutar agregando entradas de la cadena de *Descripción* de formulario -  = *commandLine*. Puede escribir varias entradas en una clave. Si se registra más de un programa en una clave determinada, el orden en el que se ejecutan dichos programas es indeterminado.

El registro de Windows incluye las cuatro claves de ejecución y RunOnce siguientes:

-   **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**
-   **HKEY \_ Current \_ User \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ Run**
-   **HKEY \_ local \_ Machine \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**
-   **HKEY \_ Current \_ User \\ software \\ Microsoft \\ Windows \\ CurrentVersion \\ RunOnce**

De forma predeterminada, el valor de una clave RunOnce se elimina antes de que se ejecute la línea de comandos. Puede anteponer un nombre de valor RunOnce con un signo de exclamación (!) para aplazar la eliminación del valor hasta después de que se ejecute el comando. Sin el prefijo del signo de exclamación, si se produce un error en la operación RunOnce, no se le pedirá que se ejecute la próxima vez que inicie el equipo.

De forma predeterminada, estas claves se omiten cuando el equipo se inicia en modo seguro. El nombre de valor de las claves RunOnce puede ir precedido por un asterisco ( \* ) para forzar que el programa se ejecute incluso en modo seguro.

Un programa ejecutado desde cualquiera de estas claves no debe escribir en la clave durante su ejecución, ya que esto interferirá con la ejecución de otros programas registrados en la clave. Las aplicaciones deben usar la clave RunOnce solo para condiciones transitorias, como para completar la configuración de la aplicación. Una aplicación no debe volver a crear continuamente entradas en RunOnce, ya que esto interferirá con programa de instalación de Windows.
