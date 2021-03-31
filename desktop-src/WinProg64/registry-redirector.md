---
title: Redirector del registro
description: El redirector del registro aísla las aplicaciones de 32 y 64 bits proporcionando vistas lógicas independientes de ciertas partes del registro en WOW64.
ms.assetid: b3989f79-0439-485a-96c1-4f2227d48653
keywords:
- Guía de programación de Windows de 64 bits guía de programación de Windows de 64 bits, redirector del registro
- redirector del registro 64 programación de Windows de bits
- redirección 64 programación de Windows de bits
- La programación de Windows de 64 bits de WOW64, redirector del registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04c11e68f307aa014adb7cae8415f1baba155678
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418798"
---
# <a name="registry-redirector"></a>Redirector del registro

El redirector del registro aísla las aplicaciones de 32 y 64 bits proporcionando vistas lógicas independientes de ciertas partes del registro en WOW64. El redirector del registro intercepta las llamadas del registro de 32 bits y 64 bits a sus respectivas vistas del registro lógicas y las asigna a la ubicación física del registro correspondiente. El proceso de redireccionamiento es transparente para la aplicación. Por lo tanto, una aplicación de 32 bits puede tener acceso a los datos del registro como si se ejecutara en Windows de 32 bits aunque los datos se almacenen en una ubicación diferente en Windows de 64 bits.

**Windows 10 en ARM:** Además de la vista lógica de 32 bits para las aplicaciones x86, Windows 10 en ARM incluye una vista lógica independiente para las aplicaciones ARM de 32 bits.

Se comparte un subconjunto de claves en las rutas de acceso redirigidas del registro. no se redirigen las llamadas del registro de 32 bits a claves compartidas. En su lugar, se asigna una copia física de la clave a cada vista lógica del registro. Para obtener una lista de claves redirigidas y claves compartidas, consulte [claves del registro afectadas por WOW64](shared-registry-keys.md).

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Para habilitar la interoperabilidad de la aplicación a través de COM y otros mecanismos, también se *refleja* un subconjunto de claves del registro redirigidas. El proceso de reflexión del registro copia las claves y los valores del registro entre dos vistas del registro para mantenerlas sincronizadas. La reflexión del registro se quitó a partir de Windows 7 y Windows Server 2008 R2. Para obtener más información, vea [reflexión del registro](registry-reflection.md).

En el escenario siguiente se muestra el uso de estas vistas lógicas:

-   Una aplicación x86 de 32 bits comprueba la existencia de la siguiente clave del registro: **HKEY \_ local \_ Machine \\ software \\ Hello**. Si la clave no existe, la aplicación la crea con un valor predeterminado de "Hello 32-bit x86 World"; de lo contrario, Lee y muestra el valor.
-   La misma aplicación se modifica para escribir "Hello 64-bit World" en lugar de "Hello 32-bit x86 World" y se vuelve a compilar como una aplicación de 64 bits x64 o ARM64.
-   **Windows 10 en ARM:** Se modifica la misma aplicación para escribir "Hello 32-bit ARM World" y se vuelve a compilar como una aplicación de ARM de 32 bits.
-   Cuando se ejecuta la aplicación x86 de 32 bits en Windows de 64 bits, se muestra "Hello 32-bit x86 World". Cuando se ejecuta la aplicación de 64 bits, se muestra "Hello 64-bit World". **Windows 10 en ARM:** Cuando la aplicación de ARM de 32 bits se ejecuta en Windows de 64 bits ARM64, muestra "Hello 32-bit ARM World". Todas las aplicaciones llaman a las mismas funciones del registro con el mismo identificador predefinido y el mismo nombre de clave. la diferencia es que cada aplicación opera en su vista lógica del registro y cada vista se asigna a una ubicación física independiente del registro, lo que mantiene todas las versiones de la cadena intactas.

Las claves redirigidas se asignan a ubicaciones físicas en **Wow6432Node**. Por ejemplo, **HKEY \_ local \_ Machine \\ software** se redirige a **HKEY \_ local \_ Machine \\ software \\ Wow6432Node**. Sin embargo, el sistema debe tener en cuenta la ubicación física de las claves redirigidas. Las aplicaciones no deben tener acceso directamente a la ubicación física de una clave, ya que esta ubicación puede cambiar. Para obtener más información, vea [obtener acceso a una vista del registro alternativa](accessing-an-alternate-registry-view.md).

**Windows 10 en ARM:** Las claves de ARM de 32 bits redirigidas se asignan a ubicaciones físicas en WowAA32Node.

Para ayudar a las aplicaciones de 32 bits que escriben los datos de **reg \_ SZ** o **reg \_ Expand \_** SZ que contienen% ProgramFiles% o% COMMONPROGRAMFILES% en el registro, WOW64 intercepta estas operaciones de escritura y las reemplaza por "% ProgramFiles (x86)%" y "% COMMONPROGRAMFILES (x86)%". Por ejemplo, si el directorio archivos de programa se encuentra en la unidad C, "% ProgramFiles (x86)%" se expande a "C: \\ archivos de programa (x86)". El reemplazo solo se produce si se cumplen las condiciones siguientes:

-   La cadena debe comenzar con% ProgramFiles% o% COMMONPROGRAMFILES%. Si la cadena comienza con un espacio o un carácter distinto de%, no se reemplaza.
-   El caso de% ProgramFiles% o% COMMONPROGRAMFILES% debe ser exactamente como se muestra porque la comparación de cadenas distingue entre mayúsculas y minúsculas. Por ejemplo, si la cadena comienza con% CommonProgramFiles% en lugar de% CommonProgramFiles%, no se reemplaza.
-   La cadena no puede superar la ruta de acceso máxima de \_ \* 2 + 15 caracteres. Si supera esta longitud, no se reemplaza.
-   No se puede abrir la clave con la clave \_ WOW64 \_ 64KEY. Esta marca especifica que las operaciones en la clave deben realizarse en la vista del registro de 64 bits, por lo que no se reemplaza. Para obtener más información, vea [obtener acceso a una vista del registro alternativa](accessing-an-alternate-registry-view.md).

**Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** La \_ marca Key WOW \_ 64 \_ 64KEY no afecta a si se reemplaza una clave. Esta marca afecta a la sustitución a partir de Windows 7 y Windows Server 2008 R2.

Además, \_ las claves reg SZ o REG \_ Expand \_ que contienen system32 se reemplazan por SysWow64. La cadena debe comenzar por la ruta de acceso que señala a o en% WINDIR% \\ system32. La comparación de cadenas no distingue entre mayúsculas y minúsculas. Las variables de entorno se expanden antes de que coincidan con la ruta de acceso, por lo que se reemplazan todas las siguientes rutas de acceso:% WINDIR% \\ system32,% SystemRoot% \\ system32 y C: \\ Windows \\ system32. Esta revisión solo se aplica a las claves que se han reflejado antes de Windows 7.

Para obtener más información, vea los temas siguientes:

-   [Reflexión del registro](registry-reflection.md)
-   [Claves del Registro afectadas por WOW64](shared-registry-keys.md)
-   [Obtener acceso a una vista del registro alternativa](accessing-an-alternate-registry-view.md)
-   [Ejemplo de redirección del registro en WOW64](example-of-registry-reflection-and-redirection-on-wow64.md)
-   [Acceso remoto al registro en Windows de 64 bits](remote-registry-access-in-64-bit-windows.md)

 

 




