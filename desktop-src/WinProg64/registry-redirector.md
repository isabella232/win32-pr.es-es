---
title: Redirector del Registro
description: El redirector del registro aísla aplicaciones de 32 y 64 bits al proporcionar vistas lógicas independientes de determinadas partes del registro en WOW64.
ms.assetid: b3989f79-0439-485a-96c1-4f2227d48653
keywords:
- Guía de programación de Windows de 64 bits de 64 Windows programación, redirector del Registro
- Programación de Windows del Windows del registro
- redireccionamiento de 64 bits Windows programación
- WOW64 64 bits de programación Windows , redirector del Registro
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac810a6ce2dba049f7b7e5b9d28386cda89712f2833eb7bf4f7892df59b34ad
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118561511"
---
# <a name="registry-redirector"></a>Redirector del Registro

El redirector del registro aísla aplicaciones de 32 y 64 bits al proporcionar vistas lógicas independientes de determinadas partes del registro en WOW64. El redirector del Registro intercepta las llamadas del Registro de 32 y 64 bits a sus respectivas vistas del registro lógico y las asigna a la ubicación del registro físico correspondiente. El proceso de redireccionamiento es transparente para la aplicación. Por lo tanto, una aplicación de 32 bits puede tener acceso a los datos del Registro como si se estuviera ejecutando en un Windows de 32 bits, incluso si los datos se almacenan en una ubicación diferente en un Windows de 64 bits.

**Windows 10 en ARM:** Además de la vista lógica de 32 bits para aplicaciones x86, Windows 10 en ARM incluye una vista lógica independiente para aplicaciones arm de 32 bits.

Se comparte un subconjunto de claves en rutas de acceso del Registro redirigidas. No se redirigen las llamadas del Registro de 32 bits a claves compartidas. En su lugar, una copia física de la clave se asigna a cada vista lógica del registro. Para obtener una lista de claves redirigidas y claves compartidas, vea [Claves del Registro afectadas por WOW64.](shared-registry-keys.md)

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Para habilitar la interoperabilidad de aplicaciones a través de COM y otros mecanismos, también se refleja un subconjunto de claves del Registro *redirigidas.* El proceso de reflexión del Registro copia las claves y los valores del Registro entre dos vistas del Registro para mantenerlas sincronizadas. La reflexión del Registro se quitó a partir Windows 7 y Windows Server 2008 R2. Para obtener más información, vea [Reflexión del Registro.](registry-reflection.md)

En el escenario siguiente se muestra el uso de estas vistas lógicas:

-   Una aplicación x86 de 32 bits comprueba la existencia de la siguiente clave del Registro: **HKEY \_ LOCAL MACHINE Software \_ \\ \\ Hello**. Si la clave no existe, la aplicación la crea con un valor predeterminado de "Hello 32-bit x86 world"; de lo contrario, lee y muestra el valor.
-   La misma aplicación se modifica para escribir "Hello 64-bit world" en lugar de "Hello 32-bit x86 world" y se vuelve a compilar como una aplicación x64 o ARM64 de 64 bits.
-   **Windows 10 en ARM:** La misma aplicación se modifica para escribir "Hello 32-bit ARM world" y se vuelve a compilar como una aplicación arm de 32 bits.
-   Cuando la aplicación x86 de 32 bits se ejecuta en un Windows de 64 bits, muestra "Hello 32-bit x86 world". Cuando se ejecuta la aplicación de 64 bits, se muestra "Hola mundo de 64 bits". **Windows 10 en ARM:** Cuando la aplicación arm de 32 bits se ejecuta en arm64 de 64 bits Windows, muestra "Hello 32-bit ARM world". Todas las aplicaciones llaman a las mismas funciones del Registro con el mismo identificador predefinido y el mismo nombre de clave; La diferencia es que cada aplicación funciona en su vista lógica del registro y cada vista se asigna a una ubicación física independiente del registro, lo que mantiene intactas todas las versiones de la cadena.

Las claves redirigidas se asignan a ubicaciones físicas **en Wow6432Node.** Por ejemplo, **HKEY \_ LOCAL MACHINE Software \_ \\ se** redirige a **HKEY LOCAL MACHINE Software \_ \_ \\ \\ Wow6432Node**. Sin embargo, el sistema debe considerar reservada la ubicación física de las claves redirigidas. Las aplicaciones no deben acceder directamente a la ubicación física de una clave, ya que esta ubicación puede cambiar. Para obtener más información, vea [Acceso a una vista alternativa del Registro](accessing-an-alternate-registry-view.md).

**Windows 10 en ARM:** Las claves de ARM de 32 bits redirigidas se asignan a ubicaciones físicas en WowAA32Node.

Para ayudar a las aplicaciones de 32 bits que escriben datos **REG \_ SZ** o **REG EXPAND \_ \_ SZ** que contienen %ProgramFiles% o %commonprogramfiles% en el Registro, WOW64 intercepta estas operaciones de escritura y las reemplaza por "%ProgramFiles(x86)%" y "%commonprogramfiles(x86)%". Por ejemplo, si el directorio Archivos de programa está en la unidad C, "%ProgramFiles(x86)%" se expande a "C: Archivos de \\ programa (x86)". El reemplazo solo se produce si se cumplen las condiciones siguientes:

-   La cadena debe comenzar con %ProgramFiles% o %commonprogramfiles%. Si la cadena comienza con un espacio o cualquier carácter distinto de %, no se reemplaza.
-   El caso de %ProgramFiles% o %commonprogramfiles% debe ser exactamente como se muestra porque la comparación de cadenas distingue mayúsculas de minúsculas. Por ejemplo, si la cadena comienza con %CommonProgramFiles% en lugar de %commonprogramfiles%, no se reemplaza.
-   La cadena no puede superar MAX \_ PATH \* 2+15 caracteres. Si supera esta longitud, no se reemplaza.
-   La clave no se puede abrir con KEY \_ WOW64 \_ 64KEY. Esta marca especifica que las operaciones en la clave se deben realizar en la vista del Registro de 64 bits, por lo que no se reemplaza. Para obtener más información, vea [Acceso a una vista alternativa del Registro](accessing-an-alternate-registry-view.md).

**Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** La marca \_ KEY WOW \_ 64 \_ 64KEY no afecta a si se reemplaza una clave. Esta marca afecta al reemplazo a partir de Windows 7 y Windows Server 2008 R2.

Además, las claves REG SZ o REG EXPAND SZ que contienen \_ \_ \_ system32 se reemplazan por syswow64. La cadena debe comenzar con la ruta de acceso que apunta a o en %windir% \\ system32. La comparación de cadenas no distingue mayúsculas de minúsculas. Las variables de entorno se expanden antes de coincidir con la ruta de acceso, por lo que se reemplazan todas las rutas de acceso siguientes: %windir% \\ system32, %SystemRoot% \\ system32 y C: \\ windows \\ system32. Esta revisión solo se aplica a las claves que se reflejaron antes de Windows 7.

Para obtener más información, vea los temas siguientes:

-   [Reflexión del Registro](registry-reflection.md)
-   [Claves del Registro afectadas por WOW64](shared-registry-keys.md)
-   [Acceso a una vista alternativa del Registro](accessing-an-alternate-registry-view.md)
-   [Ejemplo de redirección del Registro en WOW64](example-of-registry-reflection-and-redirection-on-wow64.md)
-   [Acceso remoto al Registro en aplicaciones de 64 Windows](remote-registry-access-in-64-bit-windows.md)

 

 




