---
title: Funciones del adaptador de sensor
description: Un adaptador de sensor encapsula un dispositivo biométrico y proporciona una interfaz estándar que permite al servicio biométrico de Windows configurar el sensor, capturar ejemplos y controlar el flujo de datos biométricos al motor de procesamiento.
ms.assetid: 32cf28d3-cb78-442d-81db-7827f55b0ba8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cefc5e9221a56a7766e6af6a47449db4405b369
ms.sourcegitcommit: 8a30948ba97ab969fcaa7f7ff05b853f59d8bd5c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 07/14/2020
ms.locfileid: "103789393"
---
# <a name="sensor-adapter-functions"></a>Funciones del adaptador de sensor

Un adaptador de sensor encapsula un dispositivo biométrico y proporciona una interfaz estándar que permite al servicio biométrico de Windows configurar el sensor, capturar ejemplos y controlar el flujo de datos biométricos al motor de procesamiento. El desarrollador del adaptador debe implementar las siguientes funciones. Los llama el servicio biométrico de Windows.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                           | Descripción                                                                                                                                                                  |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SensorAdapterAcceptCalibrationData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_accept_calibration_data_fn)<br/>     | Pasa los datos de calibración del adaptador de motor al adaptador de sensor.<br/>                                                                                            |
| [**SensorAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_activate_fn)<br/>                               | Proporciona al adaptador de sensor la oportunidad de realizar cualquier trabajo necesario para sacar el componente de sensor de un estado de inactividad.<br/>                                                |
| [**SensorAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_attach_fn)<br/>                                   | Agrega un adaptador de sensor a la canalización de procesamiento de la unidad biométrica.<br/>                                                                                           |
| [**SensorAdapterCancel**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_cancel_fn)<br/>                                   | Cancela todas las operaciones de sensor pendientes.<br/>                                                                                                                            |
| [**SensorAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn)<br/>                       | Prepara la canalización de procesamiento de la unidad biométrica para una nueva operación.<br/>                                                                                       |
| [**SensorAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_fn)<br/>                         | Realiza una operación de control definida por el proveedor que no requiere privilegios elevados.<br/>                                                                             |
| [**SensorAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_control_unit_privileged_fn)<br/>     | Realiza una operación de control definida por el proveedor que requiere privilegios elevados.<br/>                                                                                     |
| [**SensorAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_deactivate_fn)<br/>                           | Proporciona al adaptador de sensor la oportunidad de realizar cualquier trabajo necesario para poner el componente de sensor en un estado de inactividad.<br/>                                                    |
| [**SensorAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_detach_fn)<br/>                                   | Libera los recursos específicos del adaptador conectados a la canalización.<br/>                                                                                                     |
| [**SensorAdapterExportSensorData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_export_sensor_data_fn)<br/>               | Recupera el ejemplo biométrico capturado más recientemente con formato de estructura [**\_ Bir de WINBIO**](winbio-bir.md) estándar.<br/>                                        |
| [**SensorAdapterFinishCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn)<br/>                     | Lo llama el Plataforma de biometría de Windows para esperar a que se complete una operación de captura iniciada por la función SensorAdapterStartCapture.<br/>                                                                                       |
| [**SensorAdapterGetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_get_indicator_status_fn)<br/>           | Recupera un valor que indica si el indicador del sensor está activado o desactivado.<br/>                                                                                       |
| [*SensorAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_notify_power_change_fn)<br/>               | Recibe una notificación sobre un cambio en el estado de energía del equipo y prepara el adaptador de sensor en consecuencia.<br/>                                                     |
| [**SensorAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_cleanup_fn)<br/>                 | Proporciona al adaptador de sensor la oportunidad de realizar cualquier limpieza en que requiera ayuda de los componentes del adaptador de almacenamiento o del motor.<br/>                                   |
| [**SensorAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_pipeline_init_fn)<br/>                       | Proporciona al adaptador de sensor la posibilidad de realizar cualquier inicialización que permanezca incompleta y que requiere ayuda de los componentes del adaptador de almacenamiento o del motor.<br/> |
| [**SensorAdapterPushDataToEngine**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn)<br/>               | Hace que el contenido actual del búfer de ejemplo esté disponible para el adaptador de motor.<br/>                                                                                  |
| [**SensorAdapterQueryCalibrationFormats**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_calibration_formats_fn)<br/> | Determina el conjunto de formatos de calibración que admite el adaptador del sensor.<br/>                                                                                        |
| [**SensorAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_extended_info_fn)<br/>             | Determina las capacidades y limitaciones del componente de sensor biométrico.<br/>                                                                                    |
| [**SensorAdapterQueryStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_query_status_fn)<br/>                         | Recupera información sobre el estado actual del dispositivo de sensor.<br/>                                                                                              |
| [**SensorAdapterReset**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_reset_fn)<br/>                                     | Reinicializa el sensor.<br/>                                                                                                                                         |
| [**SensorAdapterSetCalibrationFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_calibration_format_fn)<br/>       | Notifica al adaptador de sensor que el adaptador de motor ha seleccionado un formato de datos de calibración determinado.<br/>                                                    |
| [**SensorAdapterSetIndicatorStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_indicator_status_fn)<br/>           | Activa o desactiva el indicador de sensor.<br/>                                                                                                                           |
| [**SensorAdapterSetMode**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_set_mode_fn)<br/>                                 | Establece el modo de adaptador de sensor.<br/>                                                                                                                                     |
| [**SensorAdapterStartCapture**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn)<br/>                       | Comienza una captura de biométrica asincrónica.<br/>                                                                                                                         |
| [**WbioQuerySensorInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerysensorinterface)<br/>                         | Recupera un puntero a la estructura [**de \_ \_ interfaz del sensor de WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_sensor_interface) para el adaptador del sensor.<br/>                                         |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de complemento](plug-in-functions.md)
</dt> </dl>

 

 





