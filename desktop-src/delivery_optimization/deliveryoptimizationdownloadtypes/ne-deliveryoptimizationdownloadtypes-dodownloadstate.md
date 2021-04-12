---
title: Enumeración DODownloadState
description: Especifica el identificador del estado de descarga actual, que forma parte de la estructura de **DO_DOWNLOAD_STATUS** .
keywords:
- Enumeración DODownloadState, DODownloadState
topic_type:
- apiref
api_name:
- DODownloadState
api_location:
- deliveryoptimizationdownloadtypes.h
api_type:
- HeaderDef
ms.localizationpriority: low
ms.topic: reference
ms.date: 07/02/2019
ms.openlocfilehash: 4fb882a26d20de3094aa46763d6e1538ccf0c643
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104534930"
---
# <a name="dodownloadstate-enumeration"></a><span data-ttu-id="3beb1-104">Enumeración DODownloadState</span><span class="sxs-lookup"><span data-stu-id="3beb1-104">DODownloadState enumeration</span></span>

<span data-ttu-id="3beb1-105">La enumeración **DODownloadState** especifica el identificador del estado de descarga actual, que forma parte de la estructura de **DO_DOWNLOAD_STATUS** .</span><span class="sxs-lookup"><span data-stu-id="3beb1-105">The **DODownloadState** enumeration specifies the ID of the current download state, which is part of the **DO_DOWNLOAD_STATUS** structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="3beb1-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3beb1-106">Syntax</span></span>

```cpp
typedef enum _DODownloadState
{
  DODownloadState_Created = 0, 
  DODownloadState_Transferring,
  DODownloadState_Transferred, 
  DODownloadState_Finalized,   
  DODownloadState_Aborted,     
  DODownloadState_Paused
} DODownloadState;
```

## <a name="constants"></a><span data-ttu-id="3beb1-107">Constantes</span><span class="sxs-lookup"><span data-stu-id="3beb1-107">Constants</span></span>

| <span data-ttu-id="3beb1-108">Requisito</span><span class="sxs-lookup"><span data-stu-id="3beb1-108">Requirement</span></span> | <span data-ttu-id="3beb1-109">Value</span><span class="sxs-lookup"><span data-stu-id="3beb1-109">Value</span></span> |
|-|-|
| <span data-ttu-id="3beb1-110">DODownloadState_Created</span><span class="sxs-lookup"><span data-stu-id="3beb1-110">DODownloadState_Created</span></span> | <span data-ttu-id="3beb1-111">Se ha creado el objeto de descarga, pero aún no se ha iniciado.</span><span class="sxs-lookup"><span data-stu-id="3beb1-111">Download object is created but hasn't been started yet.</span></span> |
| <span data-ttu-id="3beb1-112">DODownloadState_Transferring</span><span class="sxs-lookup"><span data-stu-id="3beb1-112">DODownloadState_Transferring</span></span> | <span data-ttu-id="3beb1-113">La descarga está en curso.</span><span class="sxs-lookup"><span data-stu-id="3beb1-113">Download is in progress.</span></span> |
| <span data-ttu-id="3beb1-114">DODownloadState_Transferred</span><span class="sxs-lookup"><span data-stu-id="3beb1-114">DODownloadState_Transferred</span></span> | <span data-ttu-id="3beb1-115">La descarga se transfiere y puede volver a empezar descargando otra parte del archivo.</span><span class="sxs-lookup"><span data-stu-id="3beb1-115">Download is transferred and can start again by downloading another portion of the file.</span></span> |
| <span data-ttu-id="3beb1-116">DODownloadState_Finalized</span><span class="sxs-lookup"><span data-stu-id="3beb1-116">DODownloadState_Finalized</span></span> | <span data-ttu-id="3beb1-117">La descarga se ha finalizado y no se puede volver a iniciar.</span><span class="sxs-lookup"><span data-stu-id="3beb1-117">Download is finalized and cannot be started again.</span></span> |
| <span data-ttu-id="3beb1-118">DODownloadState_Aborted</span><span class="sxs-lookup"><span data-stu-id="3beb1-118">DODownloadState_Aborted</span></span> | <span data-ttu-id="3beb1-119">Se anuló la descarga.</span><span class="sxs-lookup"><span data-stu-id="3beb1-119">Download was aborted.</span></span> |
| <span data-ttu-id="3beb1-120">DODownloadState_Paused</span><span class="sxs-lookup"><span data-stu-id="3beb1-120">DODownloadState_Paused</span></span> | <span data-ttu-id="3beb1-121">La descarga se ha pausado a petición o debido a un error transitorio.</span><span class="sxs-lookup"><span data-stu-id="3beb1-121">Download has been paused on demand or due to transient error.</span></span> |

## <a name="requirements"></a><span data-ttu-id="3beb1-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3beb1-122">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="3beb1-123">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="3beb1-123">**Minimum supported client**</span></span> | <span data-ttu-id="3beb1-124">Solo aplicaciones Win32 de Windows 10, versión 1809 \[\]</span><span class="sxs-lookup"><span data-stu-id="3beb1-124">Windows 10, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="3beb1-125">**Servidor mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="3beb1-125">**Minimum supported server**</span></span> | <span data-ttu-id="3beb1-126">Windows Server, versión 1809 \[ Win32 Applications Only\]</span><span class="sxs-lookup"><span data-stu-id="3beb1-126">Windows Server, version 1809 \[Win32 applications only\]</span></span> |
| <span data-ttu-id="3beb1-127">**Header**</span><span class="sxs-lookup"><span data-stu-id="3beb1-127">**Header**</span></span> | <span data-ttu-id="3beb1-128">DeliveryOptimizationDownloadTypes. h</span><span class="sxs-lookup"><span data-stu-id="3beb1-128">DeliveryOptimizationDownloadTypes.h</span></span> |
