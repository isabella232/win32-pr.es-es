---
title: Detalles de implementación de WOW64
description: El emulador WOW64 se ejecuta en modo de usuario.
ms.assetid: 93daf9d0-dfdb-42c3-8c3d-397b21991e83
keywords:
- WOW64 64 bits de programación Windows , variables de entorno
- WOW64 64 bits de programación Windows , implementación
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4c7d095369b883171e39bffd4dc629b7f80a7f39
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127581296"
---
# <a name="wow64-implementation-details"></a>Detalles de implementación de WOW64

El emulador WOW64 se ejecuta en modo de usuario. Proporciona una interfaz entre la versión de 32 bits de Ntdll.dll y el kernel del procesador, e intercepta las llamadas de kernel. El emulador WOW64 consta de los siguientes archivos DLL:

-   Wow64.dll proporciona la infraestructura de emulación principal y los elementos thunk para las Ntoskrnl.exe de punto de entrada.
-   Wow64Win.dll proporciona thunks para las Win32k.sys de punto de entrada.
-   (solo x64) Wow64Cpu.dll compatibilidad para ejecutar programas x86 en x64.
-   (Solo Intel Itanium) IA32Exec.bin contiene el emulador de software x86.
-   (Solo Intel Itanium) Wowia32x.dll proporciona la interfaz entre IA32Exec.bin y WOW64.
-   (solo ARM64) xtajit.dll el emulador de software x86.
-   (solo ARM64) wowarmw.dll compatibilidad para ejecutar programas ARM32 en ARM64.

Estos archivos DLL, junto con la versión de 64 bits de Ntdll.dll, son los únicos archivos binarios de 64 bits que se pueden cargar en un proceso de 32 bits. En Windows 10 arm, los archivos binarios CHPE (ejecutable portable híbrido compilado) también se pueden cargar en un proceso x86 de 32 bits.

En el inicio, Wow64.dll carga la versión x86 de Ntdll.dll (o la versión CHPE, si está habilitada) y ejecuta su código de inicialización, que carga todos los archivos DLL de 32 bits necesarios. Casi todos los archivos DLL de 32 bits son copias sin modificar de archivos binarios de Windows de 32 bits, aunque algunos se cargan como CHPE por motivos de rendimiento. Algunos de estos archivos DLL se escriben para comportarse de forma diferente en WOW64 que en Windows de 32 bits, normalmente porque comparten memoria con componentes del sistema de 64 bits. El sistema reserva todo el espacio de direcciones en modo de usuario por encima del límite de 32 bits. Para obtener más información, vea [Rendimiento y consumo de memoria en WOW64.](performance-and-memory-consumption.md)

En lugar de usar la secuencia de llamadas del servicio del sistema x86, los archivos binarios de 32 bits que realicen llamadas del sistema se recompilan para usar una secuencia de llamada personalizada. Esta secuencia de llamada es económica para que WOW64 la intercepte porque permanece completamente en modo de usuario. Cuando se detecta la secuencia de llamada personalizada, la CPU WOW64 vuelve al modo nativo de 64 bits y llama a Wow64.dll. Thunking se realiza en modo de usuario para reducir el impacto en el kernel de 64 bits y para reducir el riesgo de un error en el código thunk que podría provocar un bloqueo en modo kernel, daños en los datos o un problema de seguridad. Los thunks extraen argumentos de la pila de 32 bits, los extienden a 64 bits y, a continuación, hacen la llamada nativa del sistema.

## <a name="environment-variables"></a>Variables de entorno

Cuando un proceso de 64 bits crea un proceso de 32 bits o cuando un proceso de 64 bits lo crea un proceso de 32 bits, WOW64 establece las variables de entorno para el proceso creado como se muestra en la tabla siguiente.



| Proceso                   | Variables de entorno                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Proceso de 64 bits<br/> | ARQUITECTURA \_ DEL PROCESADOR=AMD64 o \_ ARQUITECTURA DEL PROCESADOR=IA64 o \_ ARQUITECTURA DEL PROCESADOR=ARM64<br/> ProgramFiles=%ProgramFiles%<br/> ProgramW6432=%ProgramFiles%<br/> CommonProgramFiles=%CommonProgramFiles%<br/> CommonProgramW6432=%CommonProgramFiles%<br/> **Windows Server 2008, Windows Vista, Windows Server 2003 y Windows XP:** Las variables de entorno ProgramW6432 y CommonProgramW6432 se agregaron a partir de Windows 7 y Windows Server 2008 R2. <br/> |
| Proceso de 32 bits<br/> | ARQUITECTURA \_ DEL PROCESADOR=x86<br/> PROCESSOR \_ ARCHITEW6432=%PROCESSOR \_ ARCHITECTURE%<br/> ProgramFiles=%ProgramFiles(x86)%<br/> ProgramW6432=%ProgramFiles%<br/> CommonProgramFiles=%CommonProgramFiles(x86)%<br/> CommonProgramW6432=%CommonProgramFiles%<br/>                                                                                                                                                                                                                  |



 

## <a name="global-hooks"></a>Enlaces globales

La [**función SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa) se puede usar para insertar un archivo DLL en otro proceso si se cumplen las condiciones siguientes:

-   Un archivo DLL de 32 bits solo se puede insertar en un proceso de 32 bits y un archivo DLL de 64 bits solo se puede insertar en un proceso de 64 bits. No es posible insertar un archivo DLL de 32 bits en un proceso de 64 bits o viceversa.
-   Los archivos DLL de 32 y 64 bits deben tener nombres diferentes.
-   Las arquitecturas del archivo DLL y el proceso deben coincidir. Por ejemplo, no puede insertar un archivo DLL x86 de 32 bits en un proceso arm de 32 bits.

Para obtener más información, [**vea SetWindowsHookEx**](/windows/win32/api/winuser/nf-winuser-setwindowshookexa).

Tenga en cuenta que se puede llamar a los enlaces **WH \_ MOUSE**, **WH \_ KEYBOARD**, **WH JOURNAL \_ \* *_, _* WH \_ SHELL** y de bajo nivel en el subproceso que instaló el enlace en lugar de al subproceso que procesa el enlace. Para estos enlaces, es posible que se llame a los enlaces de 32 y 64 bits si un enlace de 32 bits está por delante de un enlace de 64 bits en la cadena de enlace. Para obtener más información, [vea Using Hooks](../winmsg/using-hooks.md).

 

