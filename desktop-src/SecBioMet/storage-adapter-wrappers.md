---
title: Storage Contenedores de adaptadores
description: Funciones que puede usar para llamar a funciones en el adaptador de almacenamiento. Estas funciones se definen en Winbio \_ adapter.h.
ms.assetid: 3e7ff098-b8f3-4745-aa75-712a392c6c78
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6308dda71cd279ae07e0849c0760526f116de6295bb0555f530f31a0033a5851
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118911608"
---
# <a name="storage-adapter-wrappers"></a>Storage Contenedores de adaptadores

Las siguientes funciones contenedoras se definen en Winbio \_ adapter.h. Puede usarlas para llamar a funciones en el adaptador de almacenamiento.



| Función                                    | Descripción                                                                                                                                                                     |
|---------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioStorageActivate<br/>              | Llama a [**la función StorageAdapterActivate.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_activate_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>                   |
| WbioStorageAddRecord<br/>             | Llama a [**la función StorageAdapterAddRecord.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_add_record_fn)<br/>                                                                                       |
| WbioStorageAttach<br/>                | Llama a [**la función StorageAdapterAttach.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_attach_fn)<br/>                                                                                             |
| WbioStorageClearContext<br/>          | Llama a [**la función StorageAdapterClearContext.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn)<br/>                                                                                 |
| WbioStorageCloseDatabase<br/>         | Llama a [**la función StorageAdapterCloseDatabase.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_close_database_fn)<br/>                                                                               |
| WbioStorageControlUnit<br/>           | Llama a [**la función StorageAdapterControlUnit.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_fn)<br/>                                                                                   |
| WbioStorageControlUnitPrivileged<br/> | Llama a [**la función StorageAdapterControlUnitPrivileged.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_control_unit_privileged_fn)<br/>                                                               |
| WbioStorageCreateDatabase<br/>        | Llama a [**la función StorageAdapterCreateDatabase.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_create_database_fn)<br/>                                                                             |
| WbioStorageDeactivate<br/>            | Llama a [**la función StorageAdapterDeactivate.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_deactivate_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>               |
| WbioStorageDeleteRecord<br/>          | Llama a [**la función StorageAdapterDeleteRecord.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_delete_record_fn)<br/>                                                                                 |
| WbioStorageDetach<br/>                | Llama a [**la función StorageAdapterDetach.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_detach_fn)<br/>                                                                                             |
| WbioStorageEraseDatabase<br/>         | Llama a [**la función StorageAdapterEraseDatabase.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_erase_database_fn)<br/>                                                                               |
| WbioStorageFirstRecord<br/>           | Llama a [**la función StorageAdapterFirstRecord.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_first_record_fn)<br/>                                                                                   |
| WbioStorageGetCurrentRecord<br/>      | Llama a [**la función StorageAdapterGetCurrentRecord.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_current_record_fn)<br/>                                                                         |
| WbioStorageGetDatabaseSize<br/>       | Llama a [**la función StorageAdapterGetDatabaseSize.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_database_size_fn)<br/>                                                                           |
| WbioStorageGetDataFormat<br/>         | Llama a [**la función StorageAdapterGetDataFormat.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_data_format_fn)<br/>                                                                               |
| WbioStorageGetRecordCount<br/>        | Llama a [**la función StorageAdapterGetRecordCount.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_get_record_count_fn)<br/>                                                                             |
| WbioStorageNextRecord<br/>            | Llama a [**la función StorageAdapterNextRecord.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_next_record_fn)<br/>                                                                                     |
| WbioStorageNotifyPowerChange<br/>     | Llama a [*la función StorageAdapterNotifyPowerChange.*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_notify_power_change_fn)<br/> Esta función contenedora se admite a partir de Windows 8.<br/>    |
| WbioStorageOpenDatabase<br/>          | Llama a [**la función StorageAdapterOpenDatabase.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_open_database_fn)<br/>                                                                                 |
| WbioStoragePipelineCleanup<br/>       | Llama a [**la función StorageAdapterPipelineCleanup.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_cleanup_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>     |
| WbioStoragePipelineInit<br/>          | Llama a [**la función StorageAdapterPipelineInit.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_pipeline_init_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>           |
| WbioStorageQueryByContent<br/>        | Llama a [**la función StorageAdapterQueryByContent.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_content_fn)<br/>                                                                             |
| WbioStorageQueryBySubject<br/>        | Llama a [**la función StorageAdapterQueryBySubject.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn)<br/>                                                                             |
| WbioStorageQueryExtendedInfo<br/>     | Llama a [**la función StorageAdapterQueryExtendedInfo.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_extended_info_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/> |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Storage Funciones del adaptador](storage-adapter-functions.md)
</dt> <dt>

[Funciones de complemento](plug-in-functions.md)
</dt> </dl>

 

 





