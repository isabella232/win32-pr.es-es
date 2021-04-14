---
title: Funciones del adaptador de almacenamiento
description: Un adaptador de almacenamiento administra las bases de datos de plantilla.
ms.assetid: bfb0c9e5-a95e-4054-bc83-98ff682994a0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 04b5b864ab37416bb215769a700bae410c9b882c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105665663"
---
# <a name="storage-adapter-functions"></a>Funciones del adaptador de almacenamiento

Un adaptador de almacenamiento administra las bases de datos de plantilla. El desarrollador del adaptador debe implementar las siguientes funciones. Los llama el servicio biométrico de Windows.

## <a name="in-this-section"></a>En esta sección



| Tema                                                                                         | Descripción                                                                                                                             |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| [**StorageAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn)<br/>                           | Proporciona al adaptador de almacenamiento la oportunidad de realizar cualquier trabajo necesario para devolver el componente de almacenamiento a un estado de inactividad.<br/>         |
| [**StorageAdapterAddRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn)<br/>                         | Agrega una plantilla a la base de datos.<br/>                                                                                             |
| [**StorageAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn)<br/>                               | Agrega un adaptador de almacenamiento a la canalización de procesamiento de la unidad biométrica.<br/>                                                     |
| [**StorageAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn)<br/>                   | Prepara la canalización de procesamiento de la unidad biométrica para una nueva operación.<br/>                                                  |
| [**StorageAdapterCloseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn)<br/>                 | Cierra la base de datos asociada a la canalización y libera todos los recursos relacionados.<br/>                                            |
| [**StorageAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn)<br/>                     | Realiza una operación de control definida por el proveedor que no requiere privilegios elevados.<br/>                                        |
| [**StorageAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn)<br/> | Realiza una operación de control definida por el proveedor que requiere privilegios elevados.<br/>                                                |
| [**StorageAdapterCreateDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn)<br/>               | Crea y configura una nueva base de datos.<br/>                                                                                       |
| [**StorageAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn)<br/>                       | Proporciona al adaptador de almacenamiento la oportunidad de realizar cualquier trabajo necesario para poner el componente de almacenamiento en un estado de inactividad.<br/>             |
| [**StorageAdapterDeleteRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn)<br/>                   | Elimina una o más plantillas de la base de datos.<br/>                                                                             |
| [**StorageAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn)<br/>                               | Libera los recursos específicos del adaptador conectados a la canalización.<br/>                                                                |
| [**StorageAdapterEraseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn)<br/>                 | Borra la base de datos y la marca para su eliminación.<br/>                                                                               |
| [**StorageAdapterFirstRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn)<br/>                     | Coloca el cursor del conjunto de resultados en el primer registro del conjunto.<br/>                                                              |
| [**StorageAdapterGetCurrentRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn)<br/>           | Recupera el contenido del registro actual del conjunto de resultados de la canalización.<br/>                                                     |
| [**StorageAdapterGetDatabaseSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn)<br/>             | Recupera el tamaño de la base de datos y el espacio disponible.<br/>                                                                             |
| [**StorageAdapterGetDataFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn)<br/>                 | Recupera la información de formato y de versión usada por la base de datos actual asociada a la canalización.<br/>                          |
| [**StorageAdapterGetRecordCount**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn)<br/>               | Recupera el número de registros de plantilla en el conjunto de resultados de la canalización.<br/>                                                         |
| [**StorageAdapterNextRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn)<br/>                       | Hace avanzar el cursor del conjunto de resultados en un registro.<br/>                                                                                |
| [*StorageAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn)<br/>           | Recibe una notificación sobre un cambio en el estado de energía del equipo y prepara el adaptador de almacenamiento según corresponda.<br/>               |
| [**StorageAdapterOpenDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn)<br/>                   | Abre una base de datos para que la use el adaptador de almacenamiento.<br/>                                                                             |
| [**StorageAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn)<br/>             | Proporciona al adaptador de almacenamiento la oportunidad de realizar cualquier limpieza en preparación para cerrar la base de datos de plantilla.<br/>                |
| [**StorageAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn)<br/>                   | Proporciona al adaptador de almacenamiento la oportunidad de realizar cualquier inicialización que permanezca incompleta.<br/>                                  |
| [**StorageAdapterQueryByContent**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn)<br/>               | Consulta la base de datos que está abierta actualmente para las plantillas asociadas a un vector de índice especificado.<br/>                          |
| [**StorageAdapterQueryBySubject**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn)<br/>               | Consulta la base de datos que está abierta actualmente para plantillas asociadas a una identidad y subfactor especificados.<br/>               |
| [**StorageAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn)<br/>         | Determina las capacidades y limitaciones del componente de almacenamiento biométrico.<br/>                                              |
| [**WbioQueryStorageInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioquerystorageinterface)<br/>                     | Recupera un puntero a la estructura de la [**\_ \_ interfaz de almacenamiento de WINBIO**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_storage_interface) para el adaptador de almacenamiento.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones de complemento](plug-in-functions.md)
</dt> </dl>

 

 





