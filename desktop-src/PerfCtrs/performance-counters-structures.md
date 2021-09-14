---
description: Las estructuras siguientes se usan al trabajar con datos de rendimiento.
ms.assetid: 97118b64-3a2f-49c0-92e7-324df08bdb12
title: Estructuras de contadores de rendimiento
ms.topic: article
ms.date: 08/17/2020
ms.openlocfilehash: 0629aa1763f08dfce9e2cc646bd1b5744d6591cb
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250557"
---
# <a name="performance-counters-structures"></a>Estructuras de contadores de rendimiento

Las estructuras siguientes se usan al trabajar con datos de rendimiento.

Para obtener información sobre las funciones disponibles para trabajar con contadores de rendimiento, vea [Funciones de contadores de rendimiento](performance-counters-functions.md).

## <a name="performance-data-helper-pdh-structures"></a>Estructuras del asistente de datos de rendimiento (PDH)

Los consumidores que usan las funciones del Asistente de datos [de rendimiento (PDH)](using-the-pdh-functions-to-consume-counter-data.md) usan las estructuras siguientes:

- [**PDH \_ BROWSE \_ DLG \_ CONFIG**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_a)
- [**PDH \_ BROWSE \_ DLG \_ CONFIG \_ H**](/windows/win32/api/pdh/ns-pdh-pdh_browse_dlg_config_ha)
- [**INFORMACIÓN DEL \_ CONTADOR DE \_ PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_info_a)
- [**ELEMENTOS DE RUTA \_ DE ACCESO DE CONTADOR \_ PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_counter_path_elements_a)
- [**ELEMENTOS DE RUTA \_ DE ACCESO DE ELEMENTOS DE \_ \_ DATOS \_ PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_data_item_path_elements_a)
- [**PDH \_ FMT \_ COUNTERVALUE**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue)
- [**ELEMENTO \_ COUNTERVALUE de FMT \_ PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_fmt_countervalue_item_a)
- [**CONTADOR SIN \_ FORMATO DE \_ PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter)
- [**ELEMENTO DE CONTADOR \_ SIN \_ FORMATO \_ PDH**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_counter_item_a)
- [**REGISTRO SIN FORMATO DE PDH \_ \_ \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_raw_log_record)
- [**ESTADÍSTICAS DE PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_statistics)
- [**INFORMACIÓN DE HORA \_ PDH \_**](/windows/desktop/api/Pdh/ns-pdh-pdh_time_info)

## <a name="perflib-v2-consumer-structures"></a>Estructuras de consumidor de PerfLib V2

Los consumidores que usan las [funciones De consumidor de PerfLib V2](using-the-perflib-functions-to-consume-counter-data.md) usan las siguientes estructuras:

- [**DATOS DEL \_ CONTADOR DE RENDIMIENTO \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_data)
- [**ENCABEZADO DE \_ CONTADOR \_ PERF**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_header)
- [**IDENTIFICADOR DEL \_ CONTADOR DE RENDIMIENTO \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identifier)
- [**INFORMACIÓN DE REG \_ DEL CONTADOR \_ DE RENDIMIENTO \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_reg_info)
- [**PERF \_ COUNTERSET \_ REG \_ INFO**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_reg_info)
- [**ENCABEZADO DE DATOS \_ DE \_ PERF**](/windows/desktop/api/Perflib/ns-perflib-perf_data_header)
- [**ENCABEZADO DE INSTANCIA \_ DE \_ PERF**](/windows/desktop/api/Perflib/ns-perflib-perf_instance_header)
- [**CONTADORES \_ MÚLTIPLES DE PERF \_**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_counters)
- [**INSTANCIAS MÚLTIPLES DE PERF \_ \_**](/windows/desktop/api/Perflib/ns-perflib-perf_multi_instances)
- [**ENCABEZADO DE BÚFER \_ DE \_ CADENA DE \_ PERF**](/windows/win32/api/perflib/ns-perflib-perf_string_buffer_header)
- [**ENCABEZADO DE CONTADOR \_ DE \_ CADENA DE \_ PERF**](/windows/win32/api/perflib/ns-perflib-perf_string_counter_header)

## <a name="perflib-v2-provider-structures"></a>Estructuras de proveedor de PerfLib V2

[Los proveedores de datos de rendimiento V2](providing-counter-data-using-version-2-0.md) usan las siguientes estructuras:

- [**IDENTIDAD DEL \_ CONTADOR DE RENDIMIENTO \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_identity)
- [**INFORMACIÓN DEL CONTADOR DE RENDIMIENTO \_ \_**](/windows/desktop/api/Perflib/ns-perflib-perf_counter_info)
- [**INFORMACIÓN DEL \_ CONJUNTO DE CONTADORES DE \_ RENDIMIENTO**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_info)
- [**INSTANCIA DE \_ CONJUNTO DE CONTADORES DE \_ PERF**](/windows/desktop/api/Perflib/ns-perflib-perf_counterset_instance)
- [**CONTEXTO DEL \_ PROVEEDOR DE \_ PERF**](/windows/win32/api/perflib/ns-perflib-perf_provider_context)

## <a name="performance-dll-structures"></a>Estructuras DLL de rendimiento

[Los proveedores de dll de extensión](providing-counter-data-using-a-performance-dll.md) de rendimiento y los consumidores que usan las funciones del Registro para consumir datos de [contador](using-the-registry-functions-to-consume-counter-data.md) usan las estructuras siguientes:

- [**BLOQUE DE \_ CONTADORES DE \_ PERF**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_block)
- [**DEFINICIÓN DEL \_ CONTADOR DE RENDIMIENTO \_**](/windows/desktop/api/Winperf/ns-winperf-perf_counter_definition)
- [**BLOQUE DE DATOS \_ DE \_ PERF**](/windows/desktop/api/Winperf/ns-winperf-perf_data_block)
- [**DEFINICIÓN DE INSTANCIA \_ DE \_ PERF**](/windows/desktop/api/Winperf/ns-winperf-perf_instance_definition)
- [**TIPO DE \_ OBJETO \_ PERF**](/windows/desktop/api/Winperf/ns-winperf-perf_object_type)
