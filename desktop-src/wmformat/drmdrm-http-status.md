---
title: Enumeración DRM_HTTP_STATUS (wmdrmsdk. h)
description: El \_ \_ tipo de enumeración de estado http de DRM define un intervalo de Estados http para una solicitud DRM.
ms.assetid: 09183ef9-4832-4469-a960-dbeb67381949
keywords:
- DRM_HTTP_STATUS enumeración formato de Windows Media
- enumeración Windows Media Format
topic_type:
- apiref
api_name:
- DRM_HTTP_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c5a40af45fd573f7f5033b9be3b037079cb30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105709142"
---
# <a name="drm_http_status-enumeration-wmdrmsdkh"></a><span data-ttu-id="63e27-105">Enumeración DRM_HTTP_STATUS (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="63e27-105">DRM_HTTP_STATUS enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="63e27-106">El tipo de enumeración de **\_ \_ Estado http de DRM** define un intervalo de Estados http para una solicitud DRM.</span><span class="sxs-lookup"><span data-stu-id="63e27-106">The **DRM\_HTTP\_STATUS** enumeration type defines a range of HTTP states for a DRM request.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e27-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="63e27-107">Syntax</span></span>


```C++
typedef enum DRM_HTTP_STATUS { 
  HTTP_NOTINITIATED  = 0,
  HTTP_CONNECTING    = 1,
  HTTP_REQUESTING    = 2,
  HTTP_RECEIVING     = 3,
  HTTP_COMPLETED     = 4
} ;
```



## <a name="constants"></a><span data-ttu-id="63e27-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="63e27-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="63e27-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**\_NOTINITIATED http**</span><span class="sxs-lookup"><span data-stu-id="63e27-109"><span id="HTTP_NOTINITIATED"></span><span id="http_notinitiated"></span>**HTTP\_NOTINITIATED**</span></span>
</dt> <dd>

<span data-ttu-id="63e27-110">No se han iniciado las operaciones HTTP.</span><span class="sxs-lookup"><span data-stu-id="63e27-110">The HTTP operations have not been initiated.</span></span>

</dd> <dt>

<span data-ttu-id="63e27-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**\_Conexión http**</span><span class="sxs-lookup"><span data-stu-id="63e27-111"><span id="HTTP_CONNECTING"></span><span id="http_connecting"></span>**HTTP\_CONNECTING**</span></span>
</dt> <dd>

<span data-ttu-id="63e27-112">Se está estableciendo la conexión.</span><span class="sxs-lookup"><span data-stu-id="63e27-112">The connection is being established.</span></span>

</dd> <dt>

<span data-ttu-id="63e27-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**\_solicitud http**</span><span class="sxs-lookup"><span data-stu-id="63e27-113"><span id="HTTP_REQUESTING"></span><span id="http_requesting"></span>**HTTP\_REQUESTING**</span></span>
</dt> <dd>

<span data-ttu-id="63e27-114">Se están solicitando los datos.</span><span class="sxs-lookup"><span data-stu-id="63e27-114">Data is being requested.</span></span>

</dd> <dt>

<span data-ttu-id="63e27-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**\_recepción http**</span><span class="sxs-lookup"><span data-stu-id="63e27-115"><span id="HTTP_RECEIVING"></span><span id="http_receiving"></span>**HTTP\_RECEIVING**</span></span>
</dt> <dd>

<span data-ttu-id="63e27-116">Se están recibiendo los datos.</span><span class="sxs-lookup"><span data-stu-id="63e27-116">Data is being received.</span></span>

</dd> <dt>

<span data-ttu-id="63e27-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP \_ completado**</span><span class="sxs-lookup"><span data-stu-id="63e27-117"><span id="HTTP_COMPLETED"></span><span id="http_completed"></span>**HTTP\_COMPLETED**</span></span>
</dt> <dd>

<span data-ttu-id="63e27-118">Las operaciones HTTP se han completado.</span><span class="sxs-lookup"><span data-stu-id="63e27-118">The HTTP operations are complete.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="63e27-119">Observaciones</span><span class="sxs-lookup"><span data-stu-id="63e27-119">Remarks</span></span>

<span data-ttu-id="63e27-120">Esta enumeración se usa en la estructura de [**\_ \_ Estado**](drmwm-individualize-status.md) de la función de WM.</span><span class="sxs-lookup"><span data-stu-id="63e27-120">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="63e27-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63e27-121">Requirements</span></span>



| <span data-ttu-id="63e27-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="63e27-122">Requirement</span></span> | <span data-ttu-id="63e27-123">Value</span><span class="sxs-lookup"><span data-stu-id="63e27-123">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="63e27-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="63e27-124">Header</span></span><br/> | <dl> <span data-ttu-id="63e27-125"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="63e27-125"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63e27-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="63e27-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e27-127">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="63e27-127">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





