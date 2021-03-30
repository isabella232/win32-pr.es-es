---
description: Use las siguientes estructuras al trabajar con datos de rendimiento.
ms.assetid: 97118b64-3a2f-49c0-92e7-324df08bdb12
title: Estructuras de contadores de rendimiento
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 0629aa1763f08dfce9e2cc646bd1b5744d6591cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104001963"
---
# <a name="performance-counters-structures"></a>Estructuras de contadores de rendimiento

Use las siguientes estructuras al trabajar con datos de rendimiento.

Para obtener información acerca de las funciones que están disponibles para trabajar con contadores de rendimiento, consulte [funciones de contadores de rendimiento](performance-counters-functions.md).

## <a name="performance-data-helper-pdh-structures"></a>Estructuras del ayudante de datos de rendimiento (PDH)

Los consumidores que usan las funciones del [ayudante de datos de rendimiento (PDH)](using-the-pdh-functions-to-consume-counter-data.md) usan las siguientes estructuras:

- [**PDH \_ Browse \_ Dlg \_ config**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a)
- [**PDH \_ Browse \_ Dlg \_ config \_ H**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha)
- [**\_información del contador PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_info_a)
- [**\_elementos de \_ ruta de acceso de contador PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)
- [**\_elementos de \_ ruta de elementos de datos de PDH \_ \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_data_item_path_elements_a)
- [**VALOR de de PDH \_ FMT \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)
- [**\_elemento de \_ contravalor de PDH FMT \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue_item_a)
- [**\_contador sin formato de PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)
- [**\_elemento de \_ contador sin formato PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter_item_a)
- [**\_registro de \_ registro sin procesar de PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_log_record)
- [**estadísticas de PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)
- [**\_información de hora de PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

## <a name="perflib-v2-consumer-structures"></a>Estructuras de consumidor de PerfLib V2

Los consumidores que usan las funciones de [consumidor de Perflib V2](using-the-perflib-functions-to-consume-counter-data.md) usan las siguientes estructuras:

- [**\_datos de contadores de rendimiento \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_data)
- [**\_encabezado del contador de rendimiento \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_header)
- [**\_identificador del contador de rendimiento \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identifier)
- [**\_información de \_ registro del contador de rendimiento \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_reg_info)
- [**\_información de \_ registro de COUNTERSET de rendimiento \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_reg_info)
- [**\_encabezado de datos de rendimiento \_**](/windows/desktop/api/Perflib/ns-perflib-perf_data_header)
- [**\_encabezado de instancia de rendimiento \_**](/windows/desktop/api/Perflib/ns-perflib-perf_instance_header)
- [**\_contadores de rendimiento múltiple \_**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_counters)
- [**\_instancias múltiples de rendimiento \_**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_instances)
- [**\_encabezado de \_ búfer de cadena de rendimiento \_**](/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header)
- [**\_encabezado de \_ contador de cadena de rendimiento \_**](/windows/win32/api/perflib/ns-perflib-perf_string_counter_header)

## <a name="perflib-v2-provider-structures"></a>Estructuras de proveedor de PerfLib V2

Los [proveedores de datos de rendimiento V2](providing-counter-data-using-version-2-0.md) usan las siguientes estructuras:

- [**\_identidad del contador de rendimiento \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [**\_información del contador de rendimiento \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [**\_información de COUNTERSET de rendimiento \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [**\_instancia de COUNTERSET de rendimiento \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)
- [**\_contexto del proveedor de rendimiento \_**](/windows/win32/api/perflib/ns-perflib-perf_provider_context)

## <a name="performance-dll-structures"></a>Estructuras de DLL de rendimiento

Los [proveedores de archivos dll de extensión de rendimiento](providing-counter-data-using-a-performance-dll.md) y los [consumidores que usan las funciones del registro para consumir datos de contador](using-the-registry-functions-to-consume-counter-data.md) usan las siguientes estructuras:

- [**\_bloque de contadores de rendimiento \_**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block)
- [**\_definición del contador de rendimiento \_**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)
- [**\_bloque de datos de rendimiento \_**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)
- [**definición de la instancia de rendimiento \_ \_**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition)
- [**\_tipo de objeto de rendimiento \_**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)
