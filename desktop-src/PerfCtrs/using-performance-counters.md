---
description: Para consumir datos de contadores, vea consumir datos de contador.
ms.assetid: fff8bc4a-3d7a-4d70-ba03-347f9f063c84
title: Uso de contadores de rendimiento
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: abc055a34f0937e056d1d983354fc0a3edf182a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105667238"
---
# <a name="using-performance-counters"></a>Uso de contadores de rendimiento

Los **consumidores** del contador de rendimiento son componentes de software que recopilan y utilizan los datos del contador de rendimiento. Los consumidores de ejemplo proporcionados por Microsoft incluyen monitor de rendimiento (perfmon.exe), Monitor de recursos (resmon.exe), administrador de registros (logman.exe) y typeperf.exe. Los componentes de software de terceros también pueden recopilar datos de rendimiento a través de las API de recopilación de rendimiento o a través de clases de contador de rendimiento de WMI.

Los **proveedores** de contadores de rendimiento son componentes de software que publican datos de contadores de rendimiento. Los componentes del sistema operativo, los controladores de dispositivo y los servicios pueden proporcionar los contadores de rendimiento. Muchos contadores de rendimiento se proporcionan como parte del sistema operativo Windows. Los componentes de software de terceros pueden proporcionar contadores adicionales a través de las API del proveedor de contador de rendimiento.

- Use [las herramientas del contador de rendimiento](performance-counters-tools.md) si desea recopilar o ver los datos del contador de un sistema.
- Use las [API del consumidor del contador de rendimiento](consuming-counter-data.md) cuando desee escribir un programa que recopile datos del contador del sistema local.
- Use [clases de contador de rendimiento de WMI](/windows/desktop/WmiSdk/monitoring-performance-data) si desea recopilar datos de contadores de un sistema local o remoto mediante WMI.
- Use las [API de proveedor de contador de rendimiento](providing-counter-data.md) cuando desee publicar datos de contadores de rendimiento del componente de software.

## <a name="see-also"></a>Vea también

[Acerca de los contadores de rendimiento](about-performance-counters.md)

[Referencia de contadores de rendimiento](performance-counters-reference.md)
