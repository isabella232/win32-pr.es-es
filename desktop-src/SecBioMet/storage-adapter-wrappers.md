---
title: Contenedores del adaptador de almacenamiento
description: Funciones que se pueden usar para llamar a funciones en el adaptador de almacenamiento. Estas funciones se definen en Winbio \_ Adapter. h.
ms.assetid: 3e7ff098-b8f3-4745-aa75-712a392c6c78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c5dfdf562546e1520ee85c5a9a0164acdff53904
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418760"
---
# <a name="storage-adapter-wrappers"></a>Contenedores del adaptador de almacenamiento

Las siguientes funciones de contenedor se definen en Winbio \_ Adapter. h. Puede usarlos para llamar a funciones en el adaptador de almacenamiento.



| Función                                    | Descripción                                                                                                                                                                     |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioStorageActivate<br/>              | Llama a la función [**StorageAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn) .<br/> Esta función contenedora se admite a partir de Windows 10.<br/>                   |
| WbioStorageAddRecord<br/>             | Llama a la función [**StorageAdapterAddRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn) .<br/>                                                                                       |
| WbioStorageAttach<br/>                | Llama a la función [**StorageAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn) .<br/>                                                                                             |
| WbioStorageClearContext<br/>          | Llama a la función [**StorageAdapterClearContext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn) .<br/>                                                                                 |
| WbioStorageCloseDatabase<br/>         | Llama a la función [**StorageAdapterCloseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn) .<br/>                                                                               |
| WbioStorageControlUnit<br/>           | Llama a la función [**StorageAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn) .<br/>                                                                                   |
| WbioStorageControlUnitPrivileged<br/> | Llama a la función [**StorageAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn) .<br/>                                                               |
| WbioStorageCreateDatabase<br/>        | Llama a la función [**StorageAdapterCreateDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn) .<br/>                                                                             |
| WbioStorageDeactivate<br/>            | Llama a la función [**StorageAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn) .<br/> Esta función contenedora se admite a partir de Windows 10.<br/>               |
| WbioStorageDeleteRecord<br/>          | Llama a la función [**StorageAdapterDeleteRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn) .<br/>                                                                                 |
| WbioStorageDetach<br/>                | Llama a la función [**StorageAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn) .<br/>                                                                                             |
| WbioStorageEraseDatabase<br/>         | Llama a la función [**StorageAdapterEraseDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn) .<br/>                                                                               |
| WbioStorageFirstRecord<br/>           | Llama a la función [**StorageAdapterFirstRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn) .<br/>                                                                                   |
| WbioStorageGetCurrentRecord<br/>      | Llama a la función [**StorageAdapterGetCurrentRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn) .<br/>                                                                         |
| WbioStorageGetDatabaseSize<br/>       | Llama a la función [**StorageAdapterGetDatabaseSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn) .<br/>                                                                           |
| WbioStorageGetDataFormat<br/>         | Llama a la función [**StorageAdapterGetDataFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn) .<br/>                                                                               |
| WbioStorageGetRecordCount<br/>        | Llama a la función [**StorageAdapterGetRecordCount**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn) .<br/>                                                                             |
| WbioStorageNextRecord<br/>            | Llama a la función [**StorageAdapterNextRecord**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn) .<br/>                                                                                     |
| WbioStorageNotifyPowerChange<br/>     | Llama a la función [*StorageAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn) .<br/> Esta función contenedora se admite a partir de Windows 8.<br/>    |
| WbioStorageOpenDatabase<br/>          | Llama a la función [**StorageAdapterOpenDatabase**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn) .<br/>                                                                                 |
| WbioStoragePipelineCleanup<br/>       | Llama a la función [**StorageAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn) .<br/> Esta función contenedora se admite a partir de Windows 10.<br/>     |
| WbioStoragePipelineInit<br/>          | Llama a la función [**StorageAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn) .<br/> Esta función contenedora se admite a partir de Windows 10.<br/>           |
| WbioStorageQueryByContent<br/>        | Llama a la función [**StorageAdapterQueryByContent**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn) .<br/>                                                                             |
| WbioStorageQueryBySubject<br/>        | Llama a la función [**StorageAdapterQueryBySubject**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn) .<br/>                                                                             |
| WbioStorageQueryExtendedInfo<br/>     | Llama a la función [**StorageAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn) .<br/> Esta función contenedora se admite a partir de Windows 10.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones del adaptador de almacenamiento](storage-adapter-functions.md)
</dt> <dt>

[Funciones de complemento](plug-in-functions.md)
</dt> </dl>

 

 





