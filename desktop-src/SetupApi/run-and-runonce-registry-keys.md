---
description: Las claves del Registro Run y RunOnce hacen que los programas se ejecuten cada vez que un usuario inicia sesión.
ms.assetid: 5a6c17f1-d4c0-4005-9b26-036d8b27703a
title: Ejecutar y ejecutar claves del Registro RunOnce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3e69559a1034e3dcdb6eae215400d475fb9ca8be4025a38d064e914837af8544
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665245"
---
# <a name="run-and-runonce-registry-keys"></a>Ejecutar y ejecutar claves del Registro RunOnce

Las claves del Registro Run y RunOnce hacen que los programas se ejecuten cada vez que un usuario inicia sesión. El valor de datos de una clave es una línea de comandos que no tiene más de 260 caracteres. Registre los programas que se ejecutarán agregando entradas de la línea de comandos de la cadena *de* - *descripción* = *del formulario*. Puede escribir varias entradas bajo una clave. Si se registra más de un programa con una clave determinada, el orden en que se ejecutan esos programas es indeterminado.

El Windows incluye las cuatro claves Run y RunOnce siguientes:

-   **HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Run**
-   **HKEY \_ CURRENT USER Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Run**
-   **HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ RunOnce**
-   **HKEY \_ CURRENT USER Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ RunOnce**

De forma predeterminada, el valor de una clave RunOnce se elimina antes de ejecutar la línea de comandos. Puede anteponer un nombre de valor RunOnce con un signo de exclamación (!) para aplazar la eliminación del valor hasta después de que se ejecute el comando. Sin el prefijo de signo de exclamación, si se produce un error en la operación RunOnce, no se le pedirá al programa asociado que se ejecute la próxima vez que inicie el equipo.

De forma predeterminada, estas claves se omiten cuando el equipo se inicia en Caja fuerte modo. El nombre de valor de las claves RunOnce puede ir precedido de un asterisco ( ) para forzar que el programa se ejecute incluso \* Caja fuerte modo.

Un programa ejecutado desde cualquiera de estas claves no debe escribir en la clave durante su ejecución porque esto interferirá con la ejecución de otros programas registrados bajo la clave. Las aplicaciones deben usar la clave RunOnce solo para condiciones transitorias, como completar la configuración de la aplicación. Una aplicación no debe volver a crear continuamente las entradas en RunOnce porque esto interferirá con Windows instalación.
