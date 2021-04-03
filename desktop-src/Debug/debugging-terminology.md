---
description: Los siguientes términos se usan al describir la depuración.
ms.assetid: 580f2787-d944-4350-a2c2-c00816b3f515
title: Terminología de depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ffa12e24a6c763f9cda983ad961ba85a41c63cec
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103998061"
---
# <a name="debugging-terminology"></a>Terminología de depuración

Los siguientes términos se usan al describir la depuración.

<dl> <dt>

<span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Pantalla azul
</dt> <dd>

Cuando el sistema detecta un problema de hardware, una incoherencia en los datos o un error similar, puede mostrar una pantalla azul que contenga información que se pueda utilizar para determinar la causa del error. Esta información incluye el código de detención y si se ha creado un archivo de volcado. También puede incluir una lista de los controladores cargados y un seguimiento de la pila.

</dd> <dt>

<span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Archivo de volcado de memoria
</dt> <dd>

Puede configurar el sistema para escribir información en un archivo de volcado de memoria en el disco duro siempre que se genere un código de detención. El archivo contiene información que el depurador puede utilizar para analizar el error. Este archivo puede ser tan grande como la memoria física incluida en el equipo.

</dd> <dt>

<span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Depurador
</dt> <dd>

Programa diseñado para ayudar a detectar, localizar y corregir errores en otro programa. Permite al desarrollador recorrer paso a paso la ejecución del proceso y sus subprocesos, la supervisión de la memoria, las variables y otros elementos del contexto del proceso y del subproceso.

</dd> <dt>

<span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Modo kernel
</dt> <dd>

El modo de procesador en el que se ejecutan los servicios del sistema y los controladores de dispositivos. Todas las interfaces y las instrucciones de CPU están disponibles y se puede tener acceso a toda la memoria.

</dd> <dt>

<span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Archivo de minivolcado
</dt> <dd>

Las aplicaciones pueden generar archivos de minivolcado en modo usuario, que contienen un subconjunto útil de la información contenida en un archivo de volcado. Para obtener más información, consulte [archivos de minivolcado](minidump-files.md).

</dd> <dt>

<span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>DETENER código
</dt> <dd>

Código de error que identifica el error que detuvo la ejecución del kernel del sistema.

</dd> <dt>

<span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Archivos de símbolos
</dt> <dd>

Todas las aplicaciones del sistema, los controladores y los archivos DLL se compilan de forma que la información de depuración reside en archivos independientes conocidos como archivos de símbolos. Por lo tanto, el sistema es más pequeño y más rápido, pero todavía se puede depurar si se instalan los archivos de símbolos. Para obtener más información, vea [archivos de símbolos](symbol-files.md).

</dd> <dt>

<span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>Modo de usuario
</dt> <dd>

Modo de procesador en el que se ejecutan las aplicaciones. Hay un conjunto limitado de interfaces disponibles en este modo y el acceso a los datos del sistema es limitado.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la depuración automática](configuring-automatic-debugging.md)
</dt> </dl>

 

 



