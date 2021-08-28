---
title: Contenedores del adaptador de sensor
description: Funciones que puede usar para llamar a funciones en el adaptador del sensor. Estas funciones se definen en Winbio \_ adapter.h.
ms.assetid: 302a831c-38f7-4d32-8d9f-5ff58931224b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55a9e4ade931e10a93320d132662bb7622e62028299816eb6ad0e41fd7bff527
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119683205"
---
# <a name="sensor-adapter-wrappers"></a>Contenedores del adaptador de sensor

Las siguientes funciones contenedoras se definen en Winbio \_ adapter.h. Puede usarlas para llamar a funciones en el adaptador del sensor.



| Función                                     | Descripción                                                                                                                                                                               |
|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioSensorAcceptEngbrationData<br/>   | Llama a [**la función SensorAdapterAcceptEngbrationData.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>     |
| WbioSensorActivate<br/>                | Llama a [**la función SensorAdapterActivate.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_activate_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>                               |
| WbioSensorAttach<br/>                  | Llama a [**la función SensorAdapterAttach.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn)<br/>                                                                                                         |
| WbioSensorCancel<br/>                  | Llama a [**la función SensorAdapterCancel.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn)<br/>                                                                                                         |
| WbioSensorClearContext<br/>            | Llama a [**la función SensorAdapterClearContext.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn)<br/>                                                                                             |
| WbioSensorControlUnit<br/>             | Llama a [**la función SensorAdapterControlUnit.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_fn)<br/>                                                                                               |
| WbioSensorControlUnitPrivileged<br/>   | Llama a [**la función SensorAdapterControlUnitPrivileged.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_privileged_fn)<br/>                                                                           |
| WbioSensorDeactivate<br/>              | Llama a [**la función SensorAdapterDeactivate.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_deactivate_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>                           |
| WbioSensorDetach<br/>                  | Llama a [**la función SensorAdapterDetach.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn)<br/>                                                                                                         |
| WbioSensorExportSensorData<br/>        | Llama a [**la función SensorAdapterExportSensorData.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn)<br/>                                                                                     |
| WbioSensorFinishCapture<br/>           | Llama a [**la función SensorAdapterFinishCapture.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn)<br/>                                                                                           |
| WbioSensorNotifyPowerChange<br/>       | Llama a [**la función SensorAdapterNotifyPowerChange.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_notify_power_change_fn)<br/> Esta función contenedora se admite a partir de Windows 8.<br/>              |
| WbioSensorPipelineCleanup<br/>         | Llama a [**la función SensorAdapterPipelineCleanup.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_cleanup_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>                 |
| WbioSensorPipelineInit<br/>            | Llama a [**la función SensorAdapterPipelineInit.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_init_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>                       |
| WbioSensorPushDataToEngine<br/>        | Llama a [**la función SensorAdapterPushDataToEngine.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn)<br/>                                                                                     |
| WbioSensorQuery YabrationFormats<br/> | Llama a [**la función SensorAdapterQuery QuebrationFormats.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/> |
| WbioSensorQueryExtendedInfo<br/>       | Llama a [**la función SensorAdapterQueryExtendedInfo.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_extended_info_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>             |
| WbioSensorQueryStatus<br/>             | Llama a [**la función SensorAdapterQueryStatus.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)<br/>                                                                                               |
| WbioSensorReset<br/>                   | Llama a [**la función SensorAdapterReset.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_reset_fn)<br/>                                                                                                           |
| WbioSensorSetSensorBrationFormat<br/>    | Llama a [**la función SensorAdapterSetFormat.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_calibration_format_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>       |
| WbioSensorSetMode<br/>                 | Llama a [**la función SensorAdapterSetMode.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn)<br/>                                                                                                       |
| WbioSensorStartCapture<br/>            | Llama a [**la función SensorAdapterStartCapture.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn)<br/>                                                                                             |



 

No hay ninguna función contenedora para las [**funciones SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn) y [**SensorAdapterSetIndicatorStatus.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones del adaptador de sensor](sensor-adapter-functions.md)
</dt> <dt>

[Funciones de complemento](plug-in-functions.md)
</dt> </dl>

 

 





