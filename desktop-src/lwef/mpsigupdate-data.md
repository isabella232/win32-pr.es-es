---
title: MPSIGUPDATE_DATA estructura (MpClient. h)
description: Datos de notificación pasados a la función de devolución de llamada de actualización de firma.
ms.assetid: E999ABC2-CC72-43CC-86D9-4F29E9128E1A
keywords:
- MPSIGUPDATE_DATA estructura de las características heredadas del entorno de Windows
- Puntero de estructura de PMPSIGUPDATE_DATA características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPSIGUPDATE_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 442b19da394043b6fc6b8693f51c5f150233f970
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150572"
---
# <a name="mpsigupdate_data-structure"></a><span data-ttu-id="186fd-105">\_Estructura de datos MPSIGUPDATE</span><span class="sxs-lookup"><span data-stu-id="186fd-105">MPSIGUPDATE\_DATA structure</span></span>

<span data-ttu-id="186fd-106">Datos de notificación pasados a la función de devolución de llamada de actualización de firma.</span><span class="sxs-lookup"><span data-stu-id="186fd-106">Notification data passed to the signature update callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="186fd-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="186fd-107">Syntax</span></span>


```C++
typedef struct tagMPSIGUPDATE_DATA {
  DWORD                 dwPercentComplete;
  DWORD                 dwTotalUpdates;
  DWORD                 dwCurrentUpdateIndex;
  MPSIGUPDATE_TYPE      eType;
  MP_UPDATE_STAGE       Stage;
  MP_MIDL_STRING LPWSTR Path;
} MPSIGUPDATE_DATA, *PMPSIGUPDATE_DATA;
```



## <a name="members"></a><span data-ttu-id="186fd-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="186fd-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="186fd-109">**dwPercentComplete**</span><span class="sxs-lookup"><span data-stu-id="186fd-109">**dwPercentComplete**</span></span>
</dt> <dd>

<span data-ttu-id="186fd-110">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="186fd-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="186fd-111">Una estimación del porcentaje en todas las actualizaciones que se han descargado o instalado.</span><span class="sxs-lookup"><span data-stu-id="186fd-111">An estimate of the percentage across all the updates that have been downloaded and/or installed.</span></span>

</dd> <dt>

<span data-ttu-id="186fd-112">**dwTotalUpdates**</span><span class="sxs-lookup"><span data-stu-id="186fd-112">**dwTotalUpdates**</span></span>
</dt> <dd>

<span data-ttu-id="186fd-113">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="186fd-113">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="186fd-114">Número total de actualizaciones para descargar o instalar.</span><span class="sxs-lookup"><span data-stu-id="186fd-114">Total number of updates to download and/or install.</span></span>

</dd> <dt>

<span data-ttu-id="186fd-115">**dwCurrentUpdateIndex**</span><span class="sxs-lookup"><span data-stu-id="186fd-115">**dwCurrentUpdateIndex**</span></span>
</dt> <dd>

<span data-ttu-id="186fd-116">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="186fd-116">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="186fd-117">Valor de índice de base cero que especifica qué actualización entre las necesarias se está descargando o instalando actualmente.</span><span class="sxs-lookup"><span data-stu-id="186fd-117">Zero-based index value that specifies which update among those required is currently being downloaded and/or installed.</span></span>

</dd> <dt>

<span data-ttu-id="186fd-118">**eType**</span><span class="sxs-lookup"><span data-stu-id="186fd-118">**eType**</span></span>
</dt> <dd>

<span data-ttu-id="186fd-119">Tipo: **MPSIGUPDATE \_ Type**</span><span class="sxs-lookup"><span data-stu-id="186fd-119">Type: **MPSIGUPDATE\_TYPE**</span></span>

</dd> <dd>

<span data-ttu-id="186fd-120">Tipo de actualización.</span><span class="sxs-lookup"><span data-stu-id="186fd-120">Update type.</span></span> <span data-ttu-id="186fd-121">Uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="186fd-121">One of the following possible values:</span></span>



| <span data-ttu-id="186fd-122">Value</span><span class="sxs-lookup"><span data-stu-id="186fd-122">Value</span></span>                                                                                                                                                                                                                             | <span data-ttu-id="186fd-123">Significado</span><span class="sxs-lookup"><span data-stu-id="186fd-123">Meaning</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------|
| <span id="MPSIGUPDATE_TYPE_NONE"></span><span id="mpsigupdate_type_none"></span><dl> <span data-ttu-id="186fd-124"><dt>**MPSIGUPDATE \_ tipo \_ ninguno**</dt></span><span class="sxs-lookup"><span data-stu-id="186fd-124"><dt>**MPSIGUPDATE\_TYPE\_NONE**</dt></span></span> </dl>                                            |                                                                             |
| <span id="MPSIGUPDATE_TYPE_MANAGED"></span><span id="mpsigupdate_type_managed"></span><dl> <span data-ttu-id="186fd-125"><dt>**\_tipo MPSIGUPDATE \_ administrado**</dt></span><span class="sxs-lookup"><span data-stu-id="186fd-125"><dt>**MPSIGUPDATE\_TYPE\_MANAGED**</dt></span></span> </dl>                                   | <span data-ttu-id="186fd-126">Actualización de WSUS.</span><span class="sxs-lookup"><span data-stu-id="186fd-126">WSUS update.</span></span> <span data-ttu-id="186fd-127">La cancelación requiere derechos de administrador.</span><span class="sxs-lookup"><span data-stu-id="186fd-127">Cancel requires administrator rights.</span></span><br/>               |
| <span id="MPSIGUPDATE_TYPE_HTTP"></span><span id="mpsigupdate_type_http"></span><dl> <span data-ttu-id="186fd-128"><dt>**MPSIGUPDATE \_ tipo \_ http**</dt></span><span class="sxs-lookup"><span data-stu-id="186fd-128"><dt>**MPSIGUPDATE\_TYPE\_HTTP**</dt></span></span> </dl>                                            | <span data-ttu-id="186fd-129">Actualización HTTP.</span><span class="sxs-lookup"><span data-stu-id="186fd-129">HTTP update.</span></span> <span data-ttu-id="186fd-130">Derechos de administrador no necesarios para cancelar.</span><span class="sxs-lookup"><span data-stu-id="186fd-130">Administrator rights not needed to cancel.</span></span><br/>          |
| <span id="MPSIGUPDATE_TYPE_HTTP_SRV"></span><span id="mpsigupdate_type_http_srv"></span><dl> <span data-ttu-id="186fd-131"><dt>**MPSIGUPDATE \_ tipo \_ http \_ SRV**</dt></span><span class="sxs-lookup"><span data-stu-id="186fd-131"><dt>**MPSIGUPDATE\_TYPE\_HTTP\_SRV**</dt></span></span> </dl>                               | <span data-ttu-id="186fd-132">HTTP desde el servicio.</span><span class="sxs-lookup"><span data-stu-id="186fd-132">HTTP from service.</span></span> <span data-ttu-id="186fd-133">La cancelación requiere derechos de administrador.</span><span class="sxs-lookup"><span data-stu-id="186fd-133">Cancel requires administrator rights.</span></span><br/>         |
| <span id="MPSIGUPDATE_TYPE_UNC"></span><span id="mpsigupdate_type_unc"></span><dl> <span data-ttu-id="186fd-134"><dt>**MPSIGUPDATE \_ tipo \_ UNC**</dt></span><span class="sxs-lookup"><span data-stu-id="186fd-134"><dt>**MPSIGUPDATE\_TYPE\_UNC**</dt></span></span> </dl>                                               | <span data-ttu-id="186fd-135">Recurso compartido UNC.</span><span class="sxs-lookup"><span data-stu-id="186fd-135">UNC share.</span></span> <span data-ttu-id="186fd-136">Derechos de administrador no necesarios para cancelar.</span><span class="sxs-lookup"><span data-stu-id="186fd-136">Administrator rights not needed to cancel.</span></span><br/>            |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED"></span><span id="mpsigupdate_type_unmanaged"></span><dl> <span data-ttu-id="186fd-137"><dt>**tipo de MPSIGUPDATE \_ \_ no administrado**</dt></span><span class="sxs-lookup"><span data-stu-id="186fd-137"><dt>**MPSIGUPDATE\_TYPE\_UNMANAGED**</dt></span></span> </dl>                             | <span data-ttu-id="186fd-138">Actualización de MU/WU.</span><span class="sxs-lookup"><span data-stu-id="186fd-138">MU/WU update.</span></span> <span data-ttu-id="186fd-139">La cancelación requiere derechos de administrador.</span><span class="sxs-lookup"><span data-stu-id="186fd-139">Cancel requires administrator rights.</span></span><br/>              |
| <span id="MPSIGUPDATE_TYPE_MANAGED_PLATFORM"></span><span id="mpsigupdate_type_managed_platform"></span><dl> <span data-ttu-id="186fd-140"><dt>**\_ \_ plataforma administrada de tipo MPSIGUPDATE \_**</dt></span><span class="sxs-lookup"><span data-stu-id="186fd-140"><dt>**MPSIGUPDATE\_TYPE\_MANAGED\_PLATFORM**</dt></span></span> </dl>       | <span data-ttu-id="186fd-141">Actualización de WSUS para la plataforma.</span><span class="sxs-lookup"><span data-stu-id="186fd-141">WSUS update for PLATFORM.</span></span> <span data-ttu-id="186fd-142">La cancelación requiere derechos de administrador.</span><span class="sxs-lookup"><span data-stu-id="186fd-142">Cancel requires administrator rights.</span></span><br/>  |
| <span id="MPSIGUPDATE_TYPE_UNMANAGED_PLATFORM"></span><span id="mpsigupdate_type_unmanaged_platform"></span><dl> <span data-ttu-id="186fd-143"><dt>**MPSIGUPDATE \_ tipo de \_ plataforma no administrada \_**</dt></span><span class="sxs-lookup"><span data-stu-id="186fd-143"><dt>**MPSIGUPDATE\_TYPE\_UNMANAGED\_PLATFORM**</dt></span></span> </dl> | <span data-ttu-id="186fd-144">Actualización de MU/WU para la plataforma.</span><span class="sxs-lookup"><span data-stu-id="186fd-144">MU/WU update for PLATFORM.</span></span> <span data-ttu-id="186fd-145">La cancelación requiere derechos de administrador.</span><span class="sxs-lookup"><span data-stu-id="186fd-145">Cancel requires administrator rights.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="186fd-146">**Fase**</span><span class="sxs-lookup"><span data-stu-id="186fd-146">**Stage**</span></span>
</dt> <dd>

<span data-ttu-id="186fd-147">Tipo: **\_ \_ fase de actualización del módulo de administración**</span><span class="sxs-lookup"><span data-stu-id="186fd-147">Type: **MP\_UPDATE\_STAGE**</span></span>

</dd> <dd>

<span data-ttu-id="186fd-148">Actualizar fase.</span><span class="sxs-lookup"><span data-stu-id="186fd-148">Update stage.</span></span> <span data-ttu-id="186fd-149">Uno de los siguientes valores posibles:</span><span class="sxs-lookup"><span data-stu-id="186fd-149">One of the following possible values:</span></span>



| <span data-ttu-id="186fd-150">Value</span><span class="sxs-lookup"><span data-stu-id="186fd-150">Value</span></span>                                                                                                                                                                         | <span data-ttu-id="186fd-151">Significado</span><span class="sxs-lookup"><span data-stu-id="186fd-151">Meaning</span></span>                           |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------|
| <span id="MP_STAGE_UNKNOWN"></span><span id="mp_stage_unknown"></span><dl> <span data-ttu-id="186fd-152"><dt>**fase de MP \_ \_ desconocida**</dt></span><span class="sxs-lookup"><span data-stu-id="186fd-152"><dt>**MP\_STAGE\_UNKNOWN**</dt></span></span> </dl>       | <span data-ttu-id="186fd-153">Fase de actualización desconocida.</span><span class="sxs-lookup"><span data-stu-id="186fd-153">Update stage unknown.</span></span><br/>  |
| <span id="MP_SEARCH_UPDATE"></span><span id="mp_search_update"></span><dl> <span data-ttu-id="186fd-154"><dt>**actualización de la búsqueda de MP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="186fd-154"><dt>**MP\_SEARCH\_UPDATE**</dt></span></span> </dl>       | <span data-ttu-id="186fd-155">Actualizar la fase de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="186fd-155">Update search stage.</span></span><br/>   |
| <span id="MP_DOWNLOAD_UPDATE"></span><span id="mp_download_update"></span><dl> <span data-ttu-id="186fd-156"><dt>**actualización de módulo de administración \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="186fd-156"><dt>**MP\_DOWNLOAD\_UPDATE**</dt></span></span> </dl> | <span data-ttu-id="186fd-157">Actualizar la fase de descarga.</span><span class="sxs-lookup"><span data-stu-id="186fd-157">Update download stage.</span></span><br/> |
| <span id="MP_INSTALL_UPDATE"></span><span id="mp_install_update"></span><dl> <span data-ttu-id="186fd-158"><dt>**actualización de la instalación de MP \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="186fd-158"><dt>**MP\_INSTALL\_UPDATE**</dt></span></span> </dl>    | <span data-ttu-id="186fd-159">Actualizar la fase de instalación.</span><span class="sxs-lookup"><span data-stu-id="186fd-159">Update install stage.</span></span><br/>  |



 

</dd> <dt>

<span data-ttu-id="186fd-160">**Ruta de acceso**</span><span class="sxs-lookup"><span data-stu-id="186fd-160">**Path**</span></span>
</dt> <dd>

<span data-ttu-id="186fd-161">Type: **MP \_ MIDL \_ String LPWStr**</span><span class="sxs-lookup"><span data-stu-id="186fd-161">Type: **MP\_MIDL\_STRING LPWSTR**</span></span>

</dd> <dd>

<span data-ttu-id="186fd-162">Ruta de actualización.</span><span class="sxs-lookup"><span data-stu-id="186fd-162">Update path.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="186fd-163">Requisitos</span><span class="sxs-lookup"><span data-stu-id="186fd-163">Requirements</span></span>



| <span data-ttu-id="186fd-164">Requisito</span><span class="sxs-lookup"><span data-stu-id="186fd-164">Requirement</span></span> | <span data-ttu-id="186fd-165">Value</span><span class="sxs-lookup"><span data-stu-id="186fd-165">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="186fd-166">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="186fd-166">Minimum supported client</span></span><br/> | <span data-ttu-id="186fd-167">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="186fd-167">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="186fd-168">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="186fd-168">Minimum supported server</span></span><br/> | <span data-ttu-id="186fd-169">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="186fd-169">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="186fd-170">Encabezado</span><span class="sxs-lookup"><span data-stu-id="186fd-170">Header</span></span><br/>                   | <dl> <span data-ttu-id="186fd-171"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="186fd-171"><dt>MpClient.h</dt></span></span> </dl> |



 

 





