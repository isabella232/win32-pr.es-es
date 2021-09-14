---
title: Contenedores del adaptador de motor
description: Funciones que puede usar para llamar a funciones en el adaptador del motor. Estas funciones se definen en Winbio \_ adapter.h.
ms.assetid: b3d6d617-e423-4ed5-9d29-be72c5dd8b49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5ec0fcc3b6ea358e8238061bc74e2933d8bf87
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127250407"
---
# <a name="engine-adapter-wrappers"></a>Contenedores del adaptador de motor

Las siguientes funciones contenedoras se definen en Winbio \_ adapter.h. Puede usarlas para llamar a funciones en el adaptador del motor.



| Función                                           | Descripción                                                                                                                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioEngineAcceptSampleData<br/>              | Llama a [**la función EngineAdapterAcceptSampleData.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn)<br/>                                                                                                 |
| WbioEngineActivate<br/>                      | Llama a [**la función EngineAdapterActivate.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_activate_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>                                           |
| WbioEngineAttach<br/>                        | Llama a [**la función EngineAdapterAttach.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_attach_fn)<br/>                                                                                                                     |
| WbioEngineCheckForDuplicate<br/>             | Llama a [**la función EngineAdapterCheckForDuplicate.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn)<br/>                                                                                               |
| WbioEngineClearContext<br/>                  | Llama a [**la función EngineAdapterClearContext.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn)<br/>                                                                                                         |
| WbioEngineCommitEnrollment<br/>              | Llama a [**la función EngineAdapterCommitEnrollment.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn)<br/>                                                                                                 |
| WbioEngineControlUnit<br/>                   | Llama a [**la función EngineAdapterControlUnit.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_fn)<br/>                                                                                                           |
| WbioEngineControlUnitPrivileged<br/>         | Llama a [**la función EngineAdapterControlUnitPrivileged.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_privileged_fn)<br/>                                                                                       |
| WbioEngineCreateEnrollment<br/>              | Llama a [**la función EngineAdapterCreateEnrollment.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn)<br/>                                                                                                 |
| WbioEngineDeactivate<br/>                    | Llama a [**la función EngineAdapterDeactivate.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_deactivate_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>                                       |
| WbioEngineDetach<br/>                        | Llama a [**la función EngineAdapterDetach.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_detach_fn)<br/>                                                                                                                     |
| WbioEngineDiscardEnrollment<br/>             | Llama a [**la función EngineAdapterDiscardEnrollment.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn)<br/>                                                                                               |
| WbioEngineExportEngineData<br/>              | Llama a [**la función EngineAdapterExportEngineData.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_export_engine_data_fn)<br/>                                                                                                 |
| WbioEngineGetEnrollmentHash<br/>             | Llama a [**la función EngineAdapterGetEnrollmentHash.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn)<br/>                                                                                               |
| WbioEngineGetEnrollmentStatus<br/>           | Llama a [**la función EngineAdapterGetEnrollmentStatus.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_status_fn)<br/>                                                                                           |
| WbioEngineIdentifyAll<br/>                   | Llama a [**la función EngineAdapterIdentifyAll.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>                                     |
| WbioEngineIdentifyFeatureSet<br/>            | Llama a [**la función EngineAdapterIdentifyFeatureSet.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_fn)<br/>                                                                                             |
| WbioEngineNotifyPowerChange<br/>             | Llama a [*la función EngineAdapterNotifyPowerChange.*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_notify_power_change_fn)<br/> Esta función contenedora se admite a partir de Windows 8.<br/>                            |
| WbioEnginePipelineCleanup<br/>               | Llama a [**la función EngineAdapterPipelineCleanup.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_cleanup_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>                             |
| WbioEnginePipelineInit<br/>                  | Llama a [**la función EngineAdapterPipelineInit.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_init_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>                                   |
| WbioEngineQuery YabrationData<br/>          | Llama a [**la función EngineAdapterQuery QuebrationData.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_calibration_data_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>                   |
| WbioEngineQueryExtendedEnrollmentStatus<br/> | Llama a [**la función EngineAdapterQueryExtendedEnrollmentStatus.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/> |
| WbioEngineQueryExtendedInfo<br/>             | Llama a [**la función EngineAdapterQueryExtendedInfo.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>                         |
| WbioEngineQueryHashAlgorithms<br/>           | Llama a [**la función EngineAdapterQueryHashAlgorithms.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_hash_algorithms_fn)<br/>                                                                                           |
| WbioEngineQueryIndexVectorSize<br/>          | Llama a [**la función EngineAdapterQueryIndexVectorSize.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_index_vector_size_fn)<br/>                                                                                         |
| WbioEngineQueryPreferredFormat<br/>          | Llama a [**la función EngineAdapterQueryPreferredFormat.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_preferred_format_fn)<br/>                                                                                         |
| WbioEngineQuerySampleHint<br/>               | Llama a [**la función EngineAdapterQuerySampleHint.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_sample_hint_fn)<br/>                                                                                                   |
| WbioEngineRefreshCache<br/>                  | Llama a [**la función EngineAdapterRefreshCache.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_refresh_cache_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>                                   |
| WbioEngineSelectElecbrationFormat<br/>       | Llama a [**la función EngineAdapterSelectSelectSelectbrationFormat.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_select_calibration_format_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>             |
| WbioEngineSetAccountPolicy<br/>              | Llama a [**la función EngineAdapterSetAccountPolicy.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>                           |
| WbioEngineSetEnrollmentParameters<br/>       | Llama a [**la función EngineAdapterSetEnrollmentParameters.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>             |
| WbioEngineSetEnrollmentSelector<br/>         | Llama a [**la función EngineAdapterSetEnrollmentSelector.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_selector_fn)<br/> Esta función contenedora se admite a partir de Windows 10.<br/>                 |
| WbioEngineSetHashAlgorithm<br/>              | Llama a [**la función EngineAdapterSetHashAlgorithm.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn)<br/>                                                                                                 |
| WbioEngineUpdateEnrollment<br/>              | Llama a [**la función EngineAdapterUpdateEnrollment.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn)<br/>                                                                                                 |
| WbioEngineVerifyFeatureSet<br/>              | Llama a [**la función EngineAdapterVerifyFeatureSet.**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_verify_feature_set_fn)<br/>                                                                                                 |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Funciones del adaptador de motor](engine-adapter-functions.md)
</dt> <dt>

[Funciones de complemento](plug-in-functions.md)
</dt> </dl>

 

 





