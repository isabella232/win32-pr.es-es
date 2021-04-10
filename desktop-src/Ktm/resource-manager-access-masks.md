---
description: KTM define las siguientes máscaras de acceso de inscripción que se usarán al abrir un administrador de recursos.
ms.assetid: 6b901b73-516d-4f27-b258-3b93a8f9675f
title: Administrador de recursos máscaras de acceso (Winnt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f0f579a96ed80de100a5cb41cb9c4e9b847a060
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104156364"
---
# <a name="resource-manager-access-masks"></a><span data-ttu-id="0e3b4-103">Máscaras de acceso Administrador de recursos</span><span class="sxs-lookup"><span data-stu-id="0e3b4-103">Resource Manager Access Masks</span></span>

<span data-ttu-id="0e3b4-104">KTM define las siguientes máscaras de acceso de inscripción que se usarán al abrir un administrador de recursos.</span><span class="sxs-lookup"><span data-stu-id="0e3b4-104">KTM defines the following enlistment access masks to be used when opening a resource manager.</span></span>

<dl> <dt>

<span data-ttu-id="0e3b4-105"><span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**\_información de consulta de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="0e3b4-105"><span id="RESOURCEMANAGER_QUERY_INFORMATION"></span><span id="resourcemanager_query_information"></span>**RESOURCEMANAGER\_QUERY\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0e3b4-106">El autor de la llamada puede consultar la información de Resource Manager (RM).</span><span class="sxs-lookup"><span data-stu-id="0e3b4-106">The caller can query for the resource manager (RM) information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e3b4-107"><span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**\_información del conjunto de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="0e3b4-107"><span id="RESOURCEMANAGER_SET_INFORMATION"></span><span id="resourcemanager_set_information"></span>**RESOURCEMANAGER\_SET\_INFORMATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0e3b4-108">El autor de la llamada puede establecer la información de RM.</span><span class="sxs-lookup"><span data-stu-id="0e3b4-108">The caller can set the RM information.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e3b4-109"><span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**recuperación de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="0e3b4-109"><span id="RESOURCEMANAGER_RECOVER"></span><span id="resourcemanager_recover"></span>**RESOURCEMANAGER\_RECOVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0e3b4-110">El autor de la llamada puede recuperar el RM especificado.</span><span class="sxs-lookup"><span data-stu-id="0e3b4-110">The caller can recover the specified RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e3b4-111"><span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**\_dar de alta RESOURCEMANAGER**</span><span class="sxs-lookup"><span data-stu-id="0e3b4-111"><span id="RESOURCEMANAGER_ENLIST"></span><span id="resourcemanager_enlist"></span>**RESOURCEMANAGER\_ENLIST**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0e3b4-112">El autor de la llamada puede dar de alta un RM en una transacción.</span><span class="sxs-lookup"><span data-stu-id="0e3b4-112">The caller can enlist an RM in a transaction.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e3b4-113"><span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**\_notificación get de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="0e3b4-113"><span id="RESOURCEMANAGER_GET_NOTIFICATION"></span><span id="resourcemanager_get_notification"></span>**RESOURCEMANAGER\_GET\_NOTIFICATION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0e3b4-114">El autor de la llamada puede recibir una notificación de un RM.</span><span class="sxs-lookup"><span data-stu-id="0e3b4-114">The caller can receive a notification for an RM.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e3b4-115"><span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**\_lectura genérica de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="0e3b4-115"><span id="RESOURCEMANAGER_GENERIC_READ"></span><span id="resourcemanager_generic_read"></span>**RESOURCEMANAGER\_GENERIC\_READ**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0e3b4-116">El autor de la llamada tiene los siguientes privilegios: \_ derechos estándar \_ leídos, información de consulta de ResourceManager \_ \_ y recuperación de ResourceManager \_ .</span><span class="sxs-lookup"><span data-stu-id="0e3b4-116">The caller has the following privileges: STANDARD\_RIGHTS\_READ, RESOURCEMANAGER\_QUERY\_INFORMATION, and RESOURCEMANAGER\_RECOVER.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e3b4-117"><span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**\_escritura genérica de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="0e3b4-117"><span id="RESOURCEMANAGER_GENERIC_WRITE"></span><span id="resourcemanager_generic_write"></span>**RESOURCEMANAGER\_GENERIC\_WRITE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0e3b4-118">El autor de la llamada tiene los siguientes privilegios: estándar de \_ \_ escritura de derechos, información de conjunto de ResourceManager, error de inscripción de ResourceManager \_ \_ \_ y notificación de obtención de ResourceManager \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="0e3b4-118">The caller has the following privileges: STANDARD\_RIGHTS\_WRITE, RESOURCEMANAGER\_SET\_INFORMATION, RESOURCEMANAGER\_ENLIST, and RESOURCEMANAGER\_GET\_NOTIFICATION.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e3b4-119"><span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**\_ejecución genérica de RESOURCEMANAGER \_**</span><span class="sxs-lookup"><span data-stu-id="0e3b4-119"><span id="RESOURCEMANAGER_GENERIC_EXECUTE"></span><span id="resourcemanager_generic_execute"></span>**RESOURCEMANAGER\_GENERIC\_EXECUTE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0e3b4-120">El autor de la llamada tiene los siguientes privilegios: estándar \_ \_ Execute, ResourceManager \_ dar de alta y ResourceManager \_ Get \_ Notification.</span><span class="sxs-lookup"><span data-stu-id="0e3b4-120">The caller has the following privileges: STANDARD\_RIGHTS\_EXECUTE, RESOURCEMANAGER\_ENLIST, and RESOURCEMANAGER\_GET\_NOTIFICATION.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="0e3b4-121"><span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**\_ \_ acceso a RESOURCEMANAGER**</span><span class="sxs-lookup"><span data-stu-id="0e3b4-121"><span id="RESOURCEMANAGER_ALL_ACCESS"></span><span id="resourcemanager_all_access"></span>**RESOURCEMANAGER\_ALL\_ACCESS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="0e3b4-122">El autor de la llamada tiene el siguiente privilegio: \_ derechos estándar \_ requeridos.</span><span class="sxs-lookup"><span data-stu-id="0e3b4-122">The caller has the following privilege: STANDARD\_RIGHTS\_REQUIRED.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0e3b4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e3b4-123">Requirements</span></span>



| <span data-ttu-id="0e3b4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e3b4-124">Requirement</span></span> | <span data-ttu-id="0e3b4-125">Value</span><span class="sxs-lookup"><span data-stu-id="0e3b4-125">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e3b4-126">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e3b4-126">Minimum supported client</span></span><br/> | <span data-ttu-id="0e3b4-127">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0e3b4-127">Windows Vista</span></span><br/>                                                           |
| <span data-ttu-id="0e3b4-128">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0e3b4-128">Minimum supported server</span></span><br/> | <span data-ttu-id="0e3b4-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0e3b4-129">Windows Server 2008</span></span><br/>                                                     |
| <span data-ttu-id="0e3b4-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0e3b4-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="0e3b4-131"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e3b4-131"><dt>WinNT.h</dt></span></span> </dl> |



 

 




