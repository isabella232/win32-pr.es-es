---
title: Enumeración MPDETECTION_ORIGIN (MpClient. h)
description: Origen de la detección.
ms.assetid: 9FEE2FAD-3E44-4134-B968-53E971F6B092
keywords:
- MPDETECTION_ORIGIN enumeración características de entorno heredado de Windows
- PMPDETECTION_ORIGIN el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPDETECTION_ORIGIN
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed4224aafef2c72db2a8d3b27f338ca83feaf64f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105656519"
---
# <a name="mpdetection_origin-enumeration"></a><span data-ttu-id="0895c-105">\_Enumeración de origen MPDETECTION</span><span class="sxs-lookup"><span data-stu-id="0895c-105">MPDETECTION\_ORIGIN enumeration</span></span>

<span data-ttu-id="0895c-106">Origen de la detección.</span><span class="sxs-lookup"><span data-stu-id="0895c-106">Detection origin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0895c-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0895c-107">Syntax</span></span>


```C++
typedef enum tagMPDETECTION_ORIGIN { 
  MPDETECTION_ORIGIN_UNKNOWN        = 0,
  MPDETECTION_ORIGIN_LOCAL_MACHINE  = 1 << 0,
  MPDETECTION_ORIGIN_NETWORKSHARE   = 1 << 1,
  MPDETECTION_ORIGIN_INTERNET       = 1 << 2,
  MPDETECTION_ORIGIN_OUTBOUND       = 1 << 3,
  MPDETECTION_ORIGIN_INBOUND        = 1 << 4
} MPDETECTION_ORIGIN, *PMPDETECTION_ORIGIN;
```



## <a name="constants"></a><span data-ttu-id="0895c-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="0895c-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="0895c-109"><span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**origen de MPDETECTION \_ \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="0895c-109"><span id="MPDETECTION_ORIGIN_UNKNOWN"></span><span id="mpdetection_origin_unknown"></span>**MPDETECTION\_ORIGIN\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="0895c-110">Origen detectado de amenaza desconocida.</span><span class="sxs-lookup"><span data-stu-id="0895c-110">Threat detected origin unknown.</span></span>

</dd> <dt>

<span data-ttu-id="0895c-111"><span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**\_ \_ máquina local de origen de MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="0895c-111"><span id="MPDETECTION_ORIGIN_LOCAL_MACHINE"></span><span id="mpdetection_origin_local_machine"></span>**MPDETECTION\_ORIGIN\_LOCAL\_MACHINE**</span></span>
</dt> <dd>

<span data-ttu-id="0895c-112">Amenaza detectada en el equipo local.</span><span class="sxs-lookup"><span data-stu-id="0895c-112">Threat detected on local machine.</span></span>

</dd> <dt>

<span data-ttu-id="0895c-113"><span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION \_ Origin \_ NETWORKSHARE**</span><span class="sxs-lookup"><span data-stu-id="0895c-113"><span id="MPDETECTION_ORIGIN_NETWORKSHARE"></span><span id="mpdetection_origin_networkshare"></span>**MPDETECTION\_ORIGIN\_NETWORKSHARE**</span></span>
</dt> <dd>

<span data-ttu-id="0895c-114">Amenaza detectada en el recurso compartido de red.</span><span class="sxs-lookup"><span data-stu-id="0895c-114">Threat detected on network share.</span></span>

</dd> <dt>

<span data-ttu-id="0895c-115"><span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**MPDETECTION \_ Origin \_ Internet**</span><span class="sxs-lookup"><span data-stu-id="0895c-115"><span id="MPDETECTION_ORIGIN_INTERNET"></span><span id="mpdetection_origin_internet"></span>**MPDETECTION\_ORIGIN\_INTERNET**</span></span>
</dt> <dd>

<span data-ttu-id="0895c-116">Amenaza detectada en Internet.</span><span class="sxs-lookup"><span data-stu-id="0895c-116">Threat detected on internet.</span></span>

</dd> <dt>

<span data-ttu-id="0895c-117"><span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**\_salida de origen de MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="0895c-117"><span id="MPDETECTION_ORIGIN_OUTBOUND"></span><span id="mpdetection_origin_outbound"></span>**MPDETECTION\_ORIGIN\_OUTBOUND**</span></span>
</dt> <dd>

<span data-ttu-id="0895c-118">Amenaza detectada en una conexión de salida.</span><span class="sxs-lookup"><span data-stu-id="0895c-118">Threat detected on an outbound connection.</span></span>

</dd> <dt>

<span data-ttu-id="0895c-119"><span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**\_entrada de origen de MPDETECTION \_**</span><span class="sxs-lookup"><span data-stu-id="0895c-119"><span id="MPDETECTION_ORIGIN_INBOUND"></span><span id="mpdetection_origin_inbound"></span>**MPDETECTION\_ORIGIN\_INBOUND**</span></span>
</dt> <dd>

<span data-ttu-id="0895c-120">Amenaza detectada en una conexión entrante.</span><span class="sxs-lookup"><span data-stu-id="0895c-120">Threat detected on an inbound connection.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0895c-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0895c-121">Requirements</span></span>



| <span data-ttu-id="0895c-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0895c-122">Requirement</span></span> | <span data-ttu-id="0895c-123">Value</span><span class="sxs-lookup"><span data-stu-id="0895c-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0895c-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0895c-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0895c-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="0895c-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0895c-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0895c-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0895c-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="0895c-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="0895c-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0895c-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="0895c-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="0895c-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





