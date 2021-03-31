---
title: Controlador de dominio y estructuras de administración de replicación
description: El controlador de dominio y las funciones de administración de replicación usan las siguientes estructuras.
ms.assetid: 42b20d3b-1799-4f5f-b74e-fe9284dd8ac3
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4afe084e4285f4851457f9a519e747952e3bbd67
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/17/2020
ms.locfileid: "103904502"
---
# <a name="domain-controller-and-replication-management-structures"></a>Controlador de dominio y estructuras de administración de replicación

El controlador de dominio y las funciones de administración de replicación usan las siguientes estructuras:

-   [**Información del controlador de dominio de DS \_ \_ \_ \_ 1**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a)
-   [**\_ \_ \_ Información 2 del controlador de dominio de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a)
-   [**\_ \_ \_ Información 3 del controlador de dominio de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_3a)
-   [**\_resultado de nombre de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_resulta)
-   [**\_elemento de \_ resultado de nombre de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_result_itema)
-   [**metadatos de \_ atributo REPL de DS \_ \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data)
-   [**Metadatos de atributo de REPL de DS \_ \_ \_ \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_2)
-   [**\_BLOB de \_ \_ \_ metadatos de ATTR REPL de \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_blob)
-   [**metadatos de \_ \_ valor de atributo REPL de \_ \_ DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data)
-   [**\_Meta data de valor de atributo REPL de DS \_ \_ \_ \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_2)
-   [**\_ \_ \_ \_ \_ ext metadatos de valor de atributo REPL \_ de DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_ext)
-   [**\_cursor de replicación de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
-   [**CURSOR de replicación de DS \_ \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_2)
-   [**CURSOR de replicación de DS \_ \_ \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_3w)
-   [**\_BLOB de \_ cursor de replicación de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_blob)
-   [**\_cursores de replicación de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)
-   [**\_Cursores de replicación de DS \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_2)
-   [**\_Cursores de replicación de DS \_ \_ 3**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_3w)
-   [**\_error de \_ DSA de KCC de REPL de DS \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew)
-   [**\_errores de \_ DSA de KCC de REPL de DS \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failuresw)
-   [**\_BLOB de \_ FAILUREW de KCC \_ \_ de la replicación \_ de DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew_blob)
-   [**\_vecino de REPL de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw)
-   [**\_vecinos de REPL de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborsw)
-   [**\_BLOB de \_ NEIGHBORW de replicación de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw_blob)
-   [**\_metadatos \_ obj de REPL \_ de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data)
-   [**Metadatos del obj de REPL de DS \_ \_ \_ \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data_2)
-   [**\_operación de replicación de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw)
-   [**\_BLOB de \_ opw de replicación de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw_blob)
-   [**\_ \_ operaciones pendientes de replicación de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_pending_opsw)
-   [**\_cola de replicación de \_ \_ STATISTICSW de DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_queue_statisticsw)
-   [**\_ \_ BLOB STATISTICSW de cola de replicación de \_ DS \_**](/previous-versions/windows/desktop/legacy/ms676274(v=vs.85))
-   [**metadatos de valor de REPL de DS \_ \_ \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data)
-   [**Metadatos de valor de REPL de DS \_ \_ \_ \_ \_ 2**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_2)
-   [**\_ \_ \_ \_ ext metadatos de valor de REPL de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_ext)
-   [**\_BLOB de \_ \_ \_ metadatos del valor REPL de \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob)
-   [**valor de replicación de DS \_ \_ ext de \_ \_ BLOB de metadatos \_ \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob_ext)
-   [**\_ERRINFO REPSYNCALL \_ DS**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa)
-   [**\_sincronización de REPSYNCALL de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_synca)
-   [**\_actualización de REPSYNCALL de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_updatea)
-   [**\_asignación de \_ GUID de esquema de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_schema_guid_mapa)
-   [**\_información de \_ costo del sitio de DS \_**](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_site_cost_info)
-   [**PLANEA**](/windows/desktop/api/Schedule/ns-schedule-schedule)
-   [**encabezado de programación \_**](/windows/desktop/api/Schedule/ns-schedule-schedule_header)

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Estructuras en Active Directory Domain Services](structures-in-active-directory-domain-services.md)
</dt> </dl>

 

 