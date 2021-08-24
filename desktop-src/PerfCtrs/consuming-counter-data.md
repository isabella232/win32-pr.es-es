---
description: 'Puede consumir datos de rendimiento mediante una de las interfaces siguientes: La interfaz del asistente de datos de rendimiento (PDH), que proporciona acceso de alto nivel a los datos de los proveedores de contadores de rendimiento de la versión 1 y la versión 2. La interfaz del Registro, que proporciona acceso de bajo nivel a los datos de los proveedores de contadores de rendimiento. La interfaz de la biblioteca de rendimiento, que proporciona acceso directo a los datos de los proveedores de contadores de rendimiento de la versión 2. La interfaz PDH es más fácil de usar que la interfaz del Registro y se recomienda para la mayoría de las tareas de recopilación de datos de rendimiento. La interfaz PDH es básicamente una abstracción de nivel superior de la funcionalidad que proporciona la interfaz del Registro. Use la interfaz de la biblioteca de rendimiento solo si no puede usar las funciones de capa de abstracción de PDH.'
ms.assetid: a42f6cdd-47e9-4f43-aeaf-37a5abb0fa36
title: Consumo de datos de contador
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: f3abcc6dd5a385ebffdc887516613efb76b53359e5f8995bc28ba7f6239187b0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119775685"
---
# <a name="consuming-counter-data"></a>Consumo de datos de contador

Los programas que desean leer y hacer uso de los Windows contadores de rendimiento pueden usar una de varias interfaces según corresponda para el escenario.

- Los scripts pueden usar las [clases de contador de rendimiento wmi](/windows/desktop/WmiSdk/monitoring-performance-data) o la herramienta [TypePerf.](/windows-server/administration/windows-commands/typeperf)
- Los programas .NET pueden usar [la clase PerformanceCounter](/dotnet/api/system.diagnostics.performancecounter).
- La biblioteca Del asistente de datos de rendimiento [(PDH)](using-the-pdh-functions-to-consume-counter-data.md) proporciona acceso de alto nivel a los datos de los proveedores de contadores de rendimiento V1 y V2 a través de una API Win32 (C/C++).
- La [interfaz del Registro](using-the-registry-functions-to-consume-counter-data.md) proporciona acceso a los datos de los proveedores de contadores de rendimiento V1 y V2 a través de la clave del Registro `HKEY_PERFORMANCE_DATA` especial.
- Las funciones consumidoras de [PerfLib V2](using-the-perflib-functions-to-consume-counter-data.md) proporcionan acceso de bajo nivel a los datos de los proveedores de contadores de rendimiento V2 a través de una API win32 (C/C++).

La interfaz PDH se recomienda para la mayoría de las tareas de recopilación de datos de rendimiento de C/C++, ya que es más fácil de usar que las interfaces de Registro y PerfLib.
