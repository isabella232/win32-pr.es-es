---
description: Los términos siguientes se usan al describir la depuración.
ms.assetid: 580f2787-d944-4350-a2c2-c00816b3f515
title: Terminología de depuración
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: feb8de5035887f3d3c19cca1e8475ff17cb930b1142c712481e096e0e612ea81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119692084"
---
# <a name="debugging-terminology"></a>Terminología de depuración

Los términos siguientes se usan al describir la depuración.

<dl> <dt>

<span id="Blue_screen"></span><span id="blue_screen"></span><span id="BLUE_SCREEN"></span>Pantalla azul
</dt> <dd>

Cuando el sistema encuentra un problema de hardware, una incoherencia de datos o un error similar, puede mostrar una pantalla azul que contiene información que se puede usar para determinar la causa del error. Esta información incluye el código STOP y si se creó un archivo de volcado de memoria. También puede incluir una lista de controladores cargados y un seguimiento de la pila.

</dd> <dt>

<span id="Crash_dump_file"></span><span id="crash_dump_file"></span><span id="CRASH_DUMP_FILE"></span>Archivo de volcado de memoria
</dt> <dd>

Puede configurar el sistema para escribir información en un archivo de volcado de memoria en el disco duro cada vez que se genera un código STOP. El archivo contiene información que el depurador puede usar para analizar el error. Este archivo puede ser tan grande como la memoria física contenida en el equipo.

</dd> <dt>

<span id="Debugger"></span><span id="debugger"></span><span id="DEBUGGER"></span>Depurador
</dt> <dd>

Un programa diseñado para ayudar a detectar, localizar y corregir errores en otro programa. Permite al desarrollador seguir paso a paso la ejecución del proceso y sus subprocesos, supervisar la memoria, las variables y otros elementos del contexto de proceso y subproceso.

</dd> <dt>

<span id="Kernel_mode"></span><span id="kernel_mode"></span><span id="KERNEL_MODE"></span>Modo kernel
</dt> <dd>

Modo de procesador en el que se ejecutan los servicios del sistema y los controladores de dispositivo. Todas las interfaces e instrucciones de CPU están disponibles y se puede acceder a toda la memoria.

</dd> <dt>

<span id="Minidump_file"></span><span id="minidump_file"></span><span id="MINIDUMP_FILE"></span>Archivo minivolquete
</dt> <dd>

Las aplicaciones pueden generar archivos de minivolcación en modo de usuario, que contienen un subconjunto útil de la información contenida en un archivo de volcado de memoria. Para obtener más información, vea [Archivos de minivolfón](minidump-files.md).

</dd> <dt>

<span id="STOP_code"></span><span id="stop_code"></span><span id="STOP_CODE"></span>CÓDIGO STOP
</dt> <dd>

Código de error que identifica el error que impidió que el kernel del sistema continuara en ejecución.

</dd> <dt>

<span id="Symbol_files"></span><span id="symbol_files"></span><span id="SYMBOL_FILES"></span>Archivos de símbolos
</dt> <dd>

Todas las aplicaciones, controladores y archivos DLL del sistema se han creado de forma que su información de depuración resida en archivos independientes conocidos como archivos de símbolos. Por lo tanto, el sistema es más pequeño y rápido, pero todavía se puede depurar si se instalan los archivos de símbolos. Para obtener más información, vea [Archivos de símbolos](symbol-files.md).

</dd> <dt>

<span id="User_mode"></span><span id="user_mode"></span><span id="USER_MODE"></span>Modo de usuario
</dt> <dd>

Modo de procesador en el que se ejecutan las aplicaciones. En este modo hay disponible un conjunto limitado de interfaces y el acceso a los datos del sistema es limitado.

</dd> </dl>

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Configuración de la depuración automática](configuring-automatic-debugging.md)
</dt> </dl>

 

 



