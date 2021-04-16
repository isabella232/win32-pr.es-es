---
title: Enumeración DRM_HTTP_STATUS (Drmexternals. h)
description: El \_ \_ tipo de enumeración de estado http de DRM define un intervalo de Estados para una solicitud DRM.
ms.assetid: 9e0fb060-3fbf-45d0-872b-4d666ea9a88d
keywords:
- DRM_HTTP_STATUS enumeración formato de Windows Media
- enumeración Windows Media Format
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Drmexternals.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 93d61803cab6cb80932402e429e77228a1611fd9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676865"
---
# <a name="drm_http_status-enumeration-drmexternalsh"></a><span data-ttu-id="6a483-105">Enumeración DRM_HTTP_STATUS (Drmexternals. h)</span><span class="sxs-lookup"><span data-stu-id="6a483-105">DRM_HTTP_STATUS enumeration (Drmexternals.h)</span></span>

<span data-ttu-id="6a483-106">El tipo de enumeración de **\_ \_ Estado http de DRM** define un intervalo de Estados para una solicitud [*DRM*](wmformat-glossary.md) .</span><span class="sxs-lookup"><span data-stu-id="6a483-106">The **DRM\_HTTP\_STATUS** enumeration type defines a range of states for a [*DRM*](wmformat-glossary.md) request.</span></span>

## <a name="syntax"></a><span data-ttu-id="6a483-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6a483-107">Syntax</span></span>


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="6a483-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="6a483-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6a483-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**\_NOTINITIATED http**</span><span class="sxs-lookup"><span data-stu-id="6a483-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP\_NOTINITIATED**</span></span>
</dt> <dd>

<span data-ttu-id="6a483-110">No se han iniciado las operaciones HTTP.</span><span class="sxs-lookup"><span data-stu-id="6a483-110">The HTTP operations have not been initiated.</span></span>

</dd> <dt>

<span data-ttu-id="6a483-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**\_Conexión http**</span><span class="sxs-lookup"><span data-stu-id="6a483-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="6a483-112">Se está estableciendo la conexión.</span><span class="sxs-lookup"><span data-stu-id="6a483-112">The connection is being established.</span></span>

</dd> <dt>

<span data-ttu-id="6a483-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**\_solicitud http**</span><span class="sxs-lookup"><span data-stu-id="6a483-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP\_REQUESTING**</span></span>
</dt> <dd>

<span data-ttu-id="6a483-114">Se están solicitando los datos.</span><span class="sxs-lookup"><span data-stu-id="6a483-114">Data is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="6a483-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**\_recepción http**</span><span class="sxs-lookup"><span data-stu-id="6a483-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP\_RECEIVING**</span></span>
</dt> <dd>

<span data-ttu-id="6a483-116">Se están recibiendo los datos.</span><span class="sxs-lookup"><span data-stu-id="6a483-116">Data is being received.</span></span>

</dd> <dt>

<span data-ttu-id="6a483-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ completado**</span><span class="sxs-lookup"><span data-stu-id="6a483-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="6a483-118">Las operaciones HTTP se han completado.</span><span class="sxs-lookup"><span data-stu-id="6a483-118">The HTTP operations are complete.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6a483-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6a483-119">Remarks</span></span>

<span data-ttu-id="6a483-120">Esta enumeración se usa en la estructura de [**\_ \_ Estado**](wm-individualize-status.md) de la función de WM.</span><span class="sxs-lookup"><span data-stu-id="6a483-120">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](wm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a483-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a483-121">Requirements</span></span>



| <span data-ttu-id="6a483-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a483-122">Requirement</span></span> | <span data-ttu-id="6a483-123">Value</span><span class="sxs-lookup"><span data-stu-id="6a483-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a483-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a483-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6a483-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="6a483-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6a483-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6a483-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6a483-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="6a483-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6a483-128">Versión</span><span class="sxs-lookup"><span data-stu-id="6a483-128">Version</span></span><br/>                  | <span data-ttu-id="6a483-129">SDK de Windows Media Format 7 o versiones posteriores del SDK</span><span class="sxs-lookup"><span data-stu-id="6a483-129">Windows Media Format 7 SDK, or later versions of the SDK</span></span><br/>                       |
| <span data-ttu-id="6a483-130">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6a483-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a483-131"><dt>Drmexternals. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a483-131"><dt>Drmexternals.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6a483-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="6a483-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a483-133">**\_Estado de individualización de DRM \_**</span><span class="sxs-lookup"><span data-stu-id="6a483-133">**DRM\_INDIVIDUALIZATION\_STATUS**</span></span>](drm-individualization-status.md)
</dt> <dt>

[<span data-ttu-id="6a483-134">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="6a483-134">**Enumeration Types**</span></span>](enumeration-types.md)
</dt> </dl>

 

 





