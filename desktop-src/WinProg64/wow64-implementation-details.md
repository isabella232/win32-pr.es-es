---
title: Detalles de la implementación de WOW64
description: El emulador WOW64 se ejecuta en modo usuario.
ms.assetid: 93daf9d0-dfdb-42c3-8c3d-397b21991e83
keywords:
- WOW64 64 bits programación de Windows, variables de entorno
- Programación de Windows de 64 de bits WOW64, implementación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7d095369b883171e39bffd4dc629b7f80a7f39
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149367"
---
# <a name="wow64-implementation-details"></a>Detalles de la implementación de WOW64

El emulador WOW64 se ejecuta en modo usuario. Proporciona una interfaz entre la versión de 32 bits de Ntdll.dll y el kernel del procesador e intercepta las llamadas de kernel. El emulador WOW64 consta de los siguientes archivos dll:

-   Wow64.dll proporciona la infraestructura de emulación principal y los códigos thunk para las funciones de punto de entrada Ntoskrnl.exe.
-   Wow64Win.dll proporciona códigos thunk para las funciones de punto de entrada Win32k.sys.
-   (solo x64) Wow64Cpu.dll proporciona compatibilidad para ejecutar programas x86 en x64.
-   (Sólo Intel Itanium) IA32Exec. bin contiene el emulador de software x86.
-   (Intel Itanium Only) Wowia32x.dll proporciona la interfaz entre IA32Exec. bin y WOW64.
-   (Solo ARM64) xtajit.dll contiene el emulador de software x86.
-   (Solo ARM64) wowarmw.dll proporciona compatibilidad para ejecutar programas de ARM32 en ARM64.

Estos archivos dll, junto con la versión de 64 bits de Ntdll.dll, son los únicos archivos binarios de 64 bits que se pueden cargar en un proceso de 32 bits. En Windows 10 en ARM, los binarios de CHPE (archivos ejecutables híbridos compilados) también se pueden cargar en un proceso de 32 bits x86.

Al iniciarse, Wow64.dll carga la versión x86 de Ntdll.dll (o la versión CHPE, si está habilitada) y ejecuta el código de inicialización, que carga todos los archivos dll de 32 bits necesarios. Casi todos los archivos dll de 32 bits son copias sin modificar de archivos binarios de Windows de 32 bits, aunque algunos se cargan como CHPE por motivos de rendimiento. Algunos de estos archivos DLL se escriben para comportarse de forma diferente en WOW64 que en Windows de 32 bits, normalmente porque comparten memoria con componentes del sistema de 64 bits. El sistema reserva todo el espacio de direcciones del modo de usuario por encima del límite de 32 bits. Para obtener más información, consulte [rendimiento y consumo de memoria en WOW64](performance-and-memory-consumption.md).

En lugar de utilizar la secuencia de llamada de servicio del sistema x86, se vuelven a generar los archivos binarios de 32 bits que realizan llamadas del sistema para usar una secuencia de llamada personalizada. Esta secuencia de llamada es económica para que WOW64 la intercepte porque permanece completamente en modo de usuario. Cuando se detecta la secuencia de llamada personalizada, la CPU de WOW64 vuelve al modo de 64 bits nativo y llama a Wow64.dll. El código thunk se realiza en modo de usuario para reducir el impacto en el kernel de 64 bits y para reducir el riesgo de que se produzca un error en el código thunk que podría provocar un bloqueo en modo kernel, daños en los datos o un agujero de seguridad. Los códigos thunk extraen los argumentos de la pila de 32 bits, los amplían a 64 bits y, a continuación, realizan la llamada del sistema nativa.

## <a name="environment-variables"></a>Variables de entorno

Cuando un proceso de 64 bits crea un proceso de 32 bits, o cuando se crea un proceso de 64 bits mediante un proceso de 32 bits, WOW64 establece las variables de entorno para el proceso creado tal como se muestra en la tabla siguiente.



| Proceso                   | Variables de entorno                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| proceso de 64 bits<br/> | \_Arquitectura de procesador = AMD64 o \_ arquitectura de procesador = ia64 o arquitectura de procesador \_ = ARM64<br/> ProgramFiles =% ProgramFiles%<br/> ProgramW6432 =% ProgramFiles%<br/> CommonProgramFiles =% CommonProgramFiles%<br/> CommonProgramW6432 =% CommonProgramFiles%<br/> **Windows server 2008, Windows Vista, Windows server 2003 y Windows XP:** Las variables de entorno ProgramW6432 y CommonProgramW6432 se agregaron a partir de Windows 7 y Windows Server 2008 R2. <br/> |
| proceso de 32 bits<br/> | Arquitectura de procesador \_ = x86<br/> ARCHITEW6432 de procesador \_ =% de arquitectura de procesador \_ %<br/> ProgramFiles =% ProgramFiles (x86)%<br/> ProgramW6432 =% ProgramFiles%<br/> CommonProgramFiles =% CommonProgramFiles (x86)%<br/> CommonProgramW6432 =% CommonProgramFiles%<br/>                                                                                                                                                                                                                  |



 

## <a name="global-hooks"></a>Enlaces globales

La función [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) se puede usar para insertar un archivo dll en otro proceso si se cumplen las condiciones siguientes:

-   Un archivo DLL de 32 bits solo se puede insertar en un proceso de 32 bits y un archivo DLL de 64 bits solo se puede insertar en un proceso de 64 bits. No es posible insertar un archivo DLL de 32 bits en un proceso de 64 bits o viceversa.
-   Los archivos dll de 32 bits y 64 bits deben tener nombres diferentes.
-   Las arquitecturas de la DLL y el proceso deben coincidir. Por ejemplo, no se puede insertar un archivo DLL x86 de 32 bits en un proceso ARM de 32 bits.

Para obtener más información, vea [**SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa).

Tenga en cuenta que se puede llamar a la **\_ acción del mouse**, **qu \_**, el **\_ diario \*** de qu, qu y el **\_ Shell** de bajo nivel en el subproceso que instaló el enlace, en lugar del subproceso que procesa el enlace. Para estos enlaces, es posible que se llame a los enlaces de 32 bits y 64 bits si un enlace de 32 bits está por encima de un enlace de 64 bits en la cadena de enlace. Para obtener más información, vea [usar enlaces](../winmsg/using-hooks.md).

 

