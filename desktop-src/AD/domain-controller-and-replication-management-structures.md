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
# <a name="domain-controller-and-replication-management-structures"></a><span data-ttu-id="f7143-103">Controlador de dominio y estructuras de administración de replicación</span><span class="sxs-lookup"><span data-stu-id="f7143-103">Domain Controller and Replication Management Structures</span></span>

<span data-ttu-id="f7143-104">El controlador de dominio y las funciones de administración de replicación usan las siguientes estructuras:</span><span class="sxs-lookup"><span data-stu-id="f7143-104">The domain controller and replication management functions use the following structures:</span></span>

-   [<span data-ttu-id="f7143-105">**Información del controlador de dominio de DS \_ \_ \_ \_ 1**</span><span class="sxs-lookup"><span data-stu-id="f7143-105">**DS\_DOMAIN\_CONTROLLER\_INFO\_1**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_1a)
-   [<span data-ttu-id="f7143-106">**\_ \_ \_ Información 2 del controlador de dominio de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-106">**DS\_DOMAIN\_CONTROLLER\_INFO\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_2a)
-   [<span data-ttu-id="f7143-107">**\_ \_ \_ Información 3 del controlador de dominio de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-107">**DS\_DOMAIN\_CONTROLLER\_INFO\_3**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_domain_controller_info_3a)
-   [<span data-ttu-id="f7143-108">**\_resultado de nombre de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-108">**DS\_NAME\_RESULT**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_resulta)
-   [<span data-ttu-id="f7143-109">**\_elemento de \_ resultado de nombre de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-109">**DS\_NAME\_RESULT\_ITEM**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_name_result_itema)
-   [<span data-ttu-id="f7143-110">**metadatos de \_ atributo REPL de DS \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-110">**DS\_REPL\_ATTR\_META\_DATA**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data)
-   [<span data-ttu-id="f7143-111">**Metadatos de atributo de REPL de DS \_ \_ \_ \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f7143-111">**DS\_REPL\_ATTR\_META\_DATA\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_2)
-   [<span data-ttu-id="f7143-112">**\_BLOB de \_ \_ \_ metadatos de ATTR REPL de \_ DS**</span><span class="sxs-lookup"><span data-stu-id="f7143-112">**DS\_REPL\_ATTR\_META\_DATA\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_meta_data_blob)
-   [<span data-ttu-id="f7143-113">**metadatos de \_ \_ valor de atributo REPL de \_ \_ DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-113">**DS\_REPL\_ATTR\_VALUE\_META\_DATA**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data)
-   [<span data-ttu-id="f7143-114">**\_Meta data de valor de atributo REPL de DS \_ \_ \_ \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f7143-114">**DS\_REPL\_ATTR\_VALUE\_META\_DATA\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_2)
-   [<span data-ttu-id="f7143-115">**\_ \_ \_ \_ \_ ext metadatos de valor de atributo REPL \_ de DS**</span><span class="sxs-lookup"><span data-stu-id="f7143-115">**DS\_REPL\_ATTR\_VALUE\_META\_DATA\_EXT**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_attr_value_meta_data_ext)
-   [<span data-ttu-id="f7143-116">**\_cursor de replicación de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-116">**DS\_REPL\_CURSOR**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor)
-   [<span data-ttu-id="f7143-117">**CURSOR de replicación de DS \_ \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f7143-117">**DS\_REPL\_CURSOR\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_2)
-   [<span data-ttu-id="f7143-118">**CURSOR de replicación de DS \_ \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="f7143-118">**DS\_REPL\_CURSOR\_3**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_3w)
-   [<span data-ttu-id="f7143-119">**\_BLOB de \_ cursor de replicación de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-119">**DS\_REPL\_CURSOR\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursor_blob)
-   [<span data-ttu-id="f7143-120">**\_cursores de replicación de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-120">**DS\_REPL\_CURSORS**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors)
-   [<span data-ttu-id="f7143-121">**\_Cursores de replicación de DS \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f7143-121">**DS\_REPL\_CURSORS\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_2)
-   [<span data-ttu-id="f7143-122">**\_Cursores de replicación de DS \_ \_ 3**</span><span class="sxs-lookup"><span data-stu-id="f7143-122">**DS\_REPL\_CURSORS\_3**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_cursors_3w)
-   [<span data-ttu-id="f7143-123">**\_error de \_ DSA de KCC de REPL de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-123">**DS\_REPL\_KCC\_DSA\_FAILURE**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew)
-   [<span data-ttu-id="f7143-124">**\_errores de \_ DSA de KCC de REPL de DS \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-124">**DS\_REPL\_KCC\_DSA\_FAILURES**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failuresw)
-   [<span data-ttu-id="f7143-125">**\_BLOB de \_ FAILUREW de KCC \_ \_ de la replicación \_ de DS**</span><span class="sxs-lookup"><span data-stu-id="f7143-125">**DS\_REPL\_KCC\_DSA\_FAILUREW\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_kcc_dsa_failurew_blob)
-   [<span data-ttu-id="f7143-126">**\_vecino de REPL de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-126">**DS\_REPL\_NEIGHBOR**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw)
-   [<span data-ttu-id="f7143-127">**\_vecinos de REPL de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-127">**DS\_REPL\_NEIGHBORS**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborsw)
-   [<span data-ttu-id="f7143-128">**\_BLOB de \_ NEIGHBORW de replicación de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-128">**DS\_REPL\_NEIGHBORW\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_neighborw_blob)
-   [<span data-ttu-id="f7143-129">**\_metadatos \_ obj de REPL \_ de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-129">**DS\_REPL\_OBJ\_META\_DATA**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data)
-   [<span data-ttu-id="f7143-130">**Metadatos del obj de REPL de DS \_ \_ \_ \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f7143-130">**DS\_REPL\_OBJ\_META\_DATA\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_obj_meta_data_2)
-   [<span data-ttu-id="f7143-131">**\_operación de replicación de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-131">**DS\_REPL\_OP**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw)
-   [<span data-ttu-id="f7143-132">**\_BLOB de \_ opw de replicación de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-132">**DS\_REPL\_OPW\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_opw_blob)
-   [<span data-ttu-id="f7143-133">**\_ \_ operaciones pendientes de replicación de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-133">**DS\_REPL\_PENDING\_OPS**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_pending_opsw)
-   [<span data-ttu-id="f7143-134">**\_cola de replicación de \_ \_ STATISTICSW de DS**</span><span class="sxs-lookup"><span data-stu-id="f7143-134">**DS\_REPL\_QUEUE\_STATISTICSW**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_queue_statisticsw)
-   <span data-ttu-id="f7143-135">[**\_ \_ BLOB STATISTICSW de cola de replicación de \_ DS \_**](/previous-versions/windows/desktop/legacy/ms676274(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f7143-135">[**DS\_REPL\_QUEUE\_STATISTICSW\_BLOB**](/previous-versions/windows/desktop/legacy/ms676274(v=vs.85))</span></span>
-   [<span data-ttu-id="f7143-136">**metadatos de valor de REPL de DS \_ \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-136">**DS\_REPL\_VALUE\_META\_DATA**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data)
-   [<span data-ttu-id="f7143-137">**Metadatos de valor de REPL de DS \_ \_ \_ \_ \_ 2**</span><span class="sxs-lookup"><span data-stu-id="f7143-137">**DS\_REPL\_VALUE\_META\_DATA\_2**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_2)
-   [<span data-ttu-id="f7143-138">**\_ \_ \_ \_ ext metadatos de valor de REPL de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-138">**DS\_REPL\_VALUE\_META\_DATA\_EXT**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_ext)
-   [<span data-ttu-id="f7143-139">**\_BLOB de \_ \_ \_ metadatos del valor REPL de \_ DS**</span><span class="sxs-lookup"><span data-stu-id="f7143-139">**DS\_REPL\_VALUE\_META\_DATA\_BLOB**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob)
-   [<span data-ttu-id="f7143-140">**valor de replicación de DS \_ \_ ext de \_ \_ BLOB de metadatos \_ \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-140">**DS\_REPL\_VALUE\_META\_DATA\_BLOB\_EXT**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repl_value_meta_data_blob_ext)
-   [<span data-ttu-id="f7143-141">**\_ERRINFO REPSYNCALL \_ DS**</span><span class="sxs-lookup"><span data-stu-id="f7143-141">**DS\_REPSYNCALL\_ERRINFO**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_errinfoa)
-   [<span data-ttu-id="f7143-142">**\_sincronización de REPSYNCALL de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-142">**DS\_REPSYNCALL\_SYNC**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_synca)
-   [<span data-ttu-id="f7143-143">**\_actualización de REPSYNCALL de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-143">**DS\_REPSYNCALL\_UPDATE**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_repsyncall_updatea)
-   [<span data-ttu-id="f7143-144">**\_asignación de \_ GUID de esquema de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-144">**DS\_SCHEMA\_GUID\_MAP**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_schema_guid_mapa)
-   [<span data-ttu-id="f7143-145">**\_información de \_ costo del sitio de DS \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-145">**DS\_SITE\_COST\_INFO**</span></span>](/windows/desktop/api/Ntdsapi/ns-ntdsapi-ds_site_cost_info)
-   [<span data-ttu-id="f7143-146">**PLANEA**</span><span class="sxs-lookup"><span data-stu-id="f7143-146">**SCHEDULE**</span></span>](/windows/desktop/api/Schedule/ns-schedule-schedule)
-   [<span data-ttu-id="f7143-147">**encabezado de programación \_**</span><span class="sxs-lookup"><span data-stu-id="f7143-147">**SCHEDULE\_HEADER**</span></span>](/windows/desktop/api/Schedule/ns-schedule-schedule_header)

## <a name="related-topics"></a><span data-ttu-id="f7143-148">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="f7143-148">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f7143-149">Estructuras en Active Directory Domain Services</span><span class="sxs-lookup"><span data-stu-id="f7143-149">Structures in Active Directory Domain Services</span></span>](structures-in-active-directory-domain-services.md)
</dt> </dl>

 

 