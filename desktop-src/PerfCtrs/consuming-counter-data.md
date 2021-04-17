---
description: 'Puede consumir datos de rendimiento mediante una de las interfaces siguientes: la interfaz de la aplicación auxiliar de datos de rendimiento (PDH), que proporciona acceso de alto nivel a los datos de los proveedores de contadores de rendimiento de la versión 1 y la versión 2. La interfaz del registro, que proporciona acceso de bajo nivel a los datos de los proveedores de contadores de rendimiento. La interfaz de la biblioteca de rendimiento, que proporciona acceso directo a los datos de los proveedores de contadores de rendimiento de la versión 2. La interfaz PDH es más fácil de usar que la interfaz del registro y se recomienda para la mayoría de las tareas de recopilación de datos de rendimiento. La interfaz PDH es esencialmente una abstracción de nivel superior de la funcionalidad que proporciona la interfaz del registro. Use la interfaz de la biblioteca de rendimiento solo si no puede usar las funciones de nivel de abstracción de PDH.'
ms.assetid: a42f6cdd-47e9-4f43-aeaf-37a5abb0fa36
title: Consumir datos de contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: c8c50b29d8f898f544b021f7fe3f3fd0d4a2094e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667342"
---
# <a name="consuming-counter-data"></a>Consumir datos de contador

Los programas que deseen leer y usar los datos del contador de rendimiento de Windows pueden utilizar una de varias interfaces según sea necesario para el escenario.

- Los scripts pueden usar las [clases de contador de rendimiento de WMI](/windows/desktop/WmiSdk/monitoring-performance-data) o la herramienta [TypePerf](/windows-server/administration/windows-commands/typeperf) .
- Los programas .NET pueden usar la [clase PerformanceCounter](/dotnet/api/system.diagnostics.performancecounter).
- La [biblioteca del ayudante de datos de rendimiento (PDH)](using-the-pdh-functions-to-consume-counter-data.md) proporciona acceso de alto nivel a los datos de los proveedores de contadores de rendimiento V1 y V2 a través de una API Win32 (C/C++).
- La [interfaz del registro](using-the-registry-functions-to-consume-counter-data.md) proporciona acceso a los datos de los proveedores de contadores de rendimiento V1 y V2 a través de la `HKEY_PERFORMANCE_DATA` clave del registro especial.
- Las [funciones de consumidor de Perflib V2](using-the-perflib-functions-to-consume-counter-data.md) proporcionan acceso de bajo nivel a los datos de los proveedores de contadores de rendimiento V2 a través de una API Win32 (C/C++).

La interfaz PDH se recomienda para la mayoría de las tareas de recopilación de datos de rendimiento de C/C++ porque es más fácil de usar que las interfaces Registry y PerfLib.
