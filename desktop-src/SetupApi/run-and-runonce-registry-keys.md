---
description: Las claves del Registro Run y RunOnce hacen que los programas se ejecuten cada vez que un usuario inicia sesión.
ms.assetid: 5a6c17f1-d4c0-4005-9b26-036d8b27703a
title: Ejecutar y ejecutar claves del Registro RunOnce
ms.topic: article
ms.date: 09/10/2021
ms.openlocfilehash: 024d04ad535fc85022a6076b3fbc260e52f7488d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127175203"
---
# <a name="run-and-runonce-registry-keys"></a>Ejecutar y ejecutar claves del Registro RunOnce

`Run` y `RunOnce` las claves del Registro hacen que los programas se ejecuten cada vez que un usuario inicia sesión. El valor de datos de una clave es una línea de comandos que no tiene más de 260 caracteres. Registre los programas que se ejecutarán agregando entradas de la línea de comandos de la cadena *de* - *descripción* = *del formulario*. Puede escribir varias entradas bajo una clave. Si hay más de un programa registrado en una clave determinada, el orden en que se ejecutan esos programas es indeterminado.

El registro Windows incluye las cuatro claves `Run` y `RunOnce` siguientes:

-   **HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Run**
-   **HKEY \_ LOCAL MACHINE Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ RunOnce**
-   **HKEY \_ CURRENT USER Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ Run**
-   **HKEY \_ CURRENT USER Software Microsoft Windows \_ \\ \\ \\ \\ CurrentVersion \\ RunOnce**

De forma predeterminada, el valor de una `RunOnce` clave se elimina antes de ejecutar la línea de comandos. Puede anteponer un nombre de valor con un signo de exclamación (!) para aplazar la eliminación del valor hasta que se `RunOnce` ejecute el comando. Sin el prefijo de signo de exclamación, si se produce un error en la operación, no se le pedirá al programa asociado que se ejecute la próxima vez que `RunOnce` inicie el equipo.

De forma predeterminada, estas claves se omiten cuando el equipo se inicia en Caja fuerte modo. El nombre de valor de las claves puede ir precedido de un asterisco ( ) para forzar que el programa se ejecute `RunOnce` \* incluso en Caja fuerte automático.

Un programa que se ejecuta desde cualquiera de estas claves no debe escribir en la clave durante su ejecución porque esto interferirá con la ejecución de otros programas registrados bajo la clave. Las aplicaciones deben usar la `RunOnce` clave solo para condiciones transitorias, como completar la configuración de la aplicación. Una aplicación no debe volver a crear continuamente las entradas en `RunOnce` porque esto interferirá con Windows instalación.
