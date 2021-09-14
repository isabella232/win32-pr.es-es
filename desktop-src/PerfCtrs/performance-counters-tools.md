---
description: En la tabla siguiente se enumeran los
ms.assetid: 3f47a52c-2d36-4a74-9d7f-df37645b8e72
title: Herramientas de contadores de rendimiento
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: dc40dd5dfe640e09ac6f7258856389f04d60215f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250556"
---
# <a name="performance-counters-tools"></a>Herramientas de contadores de rendimiento

## <a name="data-collection-tools"></a>Herramientas de recopilación de datos

Las siguientes herramientas son útiles al consumir o manipular datos Windows contador de rendimiento.

|Herramienta|Descripción
|----|-----------
| [PerfMon](/windows-server/administration/windows-commands/perfmon) | Herramienta GUI para recopilar y ver datos del contador de rendimiento. `perfmon.exe` inicia MMC con el complemento Monitor de rendimiento, que proporciona acceso a las herramientas Monitor de rendimiento, conjuntos de recopiladores de datos e informes.
| [TypePerf](/windows-server/administration/windows-commands/typeperf) |Herramienta de línea de comandos para recopilar e imprimir datos del contador de rendimiento. Se puede usar para enumerar los conjuntos de contadores disponibles, enumerar los contadores disponibles, imprimir datos de contadores en la consola o recopilar datos de contador en un archivo de registro (CSV, TDF, BLG).
| [Registro](/windows-server/administration/windows-commands/relog) |Herramienta de línea de comandos para transformar y combinar archivos de registro (CSV, TDF, BLG) capturados mediante o a través `typeperf.exe` de `PDH.dll` las API.
| [LogMan](/windows-server/administration/windows-commands/logman) |Herramienta de línea de comandos para controlar conjuntos de recopiladores de datos.

## <a name="data-provider-tools"></a>Herramientas del proveedor de datos

Las siguientes herramientas son útiles al publicar datos Windows contador de rendimiento.

|Herramienta|Descripción
|----|-----------
| [CtrPP](ctrpp.md) | Herramienta de compilación de línea de comandos del SDK Windows que valida y compila el manifiesto del proveedor de contadores de rendimiento V2. Esta herramienta genera los encabezados `.h` y los scripts de recursos necesarios para compilar un proveedor `.rc` V2.
| [LodCtr](/windows-server/administration/windows-commands/lodctr) | Herramienta de línea de comandos que se usa para instalar el proveedor en un sistema.
| [UnlodCtr](/windows-server/administration/windows-commands/unlodctr_1) | Herramienta de línea de comandos que se usa para desinstalar el proveedor de un sistema.
