---
description: En la tabla siguiente se enumeran los
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: Herramientas de contadores de rendimiento
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dc40dd5dfe640e09ac6f7258856389f04d60215f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001962"
---
# <a name="performance-counters-tools"></a>Herramientas de contadores de rendimiento

## <a name="data-collection-tools"></a>Herramientas de recopilación de datos

Las herramientas siguientes son útiles cuando se consumen o manipulan datos del contador de rendimiento de Windows.

|Herramienta|Descripción
|----|-----------
| [PerfMon](/windows-server/administration/windows-commands/perfmon) | Herramienta de GUI para recopilar y ver los datos del contador de rendimiento. `perfmon.exe` inicia MMC con el complemento monitor de rendimiento, que proporciona acceso al monitor de rendimiento, los conjuntos de recopiladores de datos y las herramientas de informes.
| [TypePerf](/windows-server/administration/windows-commands/typeperf) |Herramienta de línea de comandos para recopilar e imprimir datos de contadores de rendimiento. Se puede usar para enumerar los contraconjuntos disponibles, enumerar los contadores disponibles, imprimir los datos de contador en la consola o recopilar datos de contadores en un archivo de registro (CSV, TDF, BLG).
| [Registro](/windows-server/administration/windows-commands/relog) |Herramienta de línea de comandos para transformar y combinar archivos de registro (CSV, TDF, BLG) capturados mediante `typeperf.exe` o a través de las `PDH.dll` API.
| [LogMan](/windows-server/administration/windows-commands/logman) |Herramienta de línea de comandos para controlar conjuntos de recopiladores de datos.

## <a name="data-provider-tools"></a>Herramientas del proveedor de datos

Las herramientas siguientes son útiles cuando se publican datos del contador de rendimiento de Windows.

|Herramienta|Descripción
|----|-----------
| [CtrPP](ctrpp.md) | Herramienta de compilación de línea de comandos de la Windows SDK que valida y compila el manifiesto de proveedor de los contadores de rendimiento V2. Esta herramienta genera los `.h` encabezados y los `.rc` scripts de recursos necesarios para compilar un proveedor V2.
| [LodCtr](/windows-server/administration/windows-commands/lodctr) | Herramienta de línea de comandos que se usa para instalar el proveedor en un sistema.
| [UnlodCtr](/windows-server/administration/windows-commands/unlodctr_1) | Herramienta de línea de comandos que se usa para desinstalar el proveedor de un sistema.
