---
description: Para consumir datos de contador, vea Consumo de datos de contador.
ms.assetid: fff8bc4a-3d7a-4d70-ba03-347f9f063c84
title: Uso de contadores de rendimiento
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: abc055a34f0937e056d1d983354fc0a3edf182a0
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127062873"
---
# <a name="using-performance-counters"></a>Uso de contadores de rendimiento

Los **consumidores de contadores de** rendimiento son componentes de software que recopilan y hacen uso de los datos del contador de rendimiento. Entre los consumidores de ejemplo proporcionados por Microsoft se incluyen Monitor de rendimiento (perfmon.exe), Monitor de recursos (resmon.exe), Log Manager (logman.exe) y typeperf.exe. Los componentes de software de terceros también pueden recopilar datos de rendimiento a través de las API de recopilación de rendimiento o a través de clases de contadores de rendimiento WMI.

Los proveedores de **contadores de** rendimiento son componentes de software que publican datos de contadores de rendimiento. Los componentes del sistema operativo, los controladores de dispositivos y los servicios pueden proporcionar contadores de rendimiento. Muchos contadores de rendimiento se proporcionan como parte del Windows operativo. Los componentes de software de terceros pueden proporcionar contadores adicionales a través de las API del proveedor de contadores de rendimiento.

- Use [las herramientas de contador de](performance-counters-tools.md) rendimiento cuando desee recopilar o ver los datos del contador de un sistema.
- Use [las API de consumidor de contadores](consuming-counter-data.md) de rendimiento cuando desee escribir un programa que recopile datos de contadores del sistema local.
- Use [clases de contadores de](/windows/desktop/WmiSdk/monitoring-performance-data) rendimiento wmi cuando desee recopilar datos de contadores de un sistema local o remoto mediante WMI.
- Use [las API del proveedor de contadores de](providing-counter-data.md) rendimiento cuando desee publicar datos de contadores de rendimiento desde el componente de software.

## <a name="see-also"></a>Consulte también

[Acerca de los contadores de rendimiento](about-performance-counters.md)

[Referencia de contadores de rendimiento](performance-counters-reference.md)
