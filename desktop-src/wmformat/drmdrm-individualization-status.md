---
title: Enumeración DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)
description: El \_ \_ tipo de enumeración estado de individualización de DRM define los Estados válidos para la individualización DRM. | Enumeración DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)
ms.assetid: 4e6712e2-3297-4636-9b0c-07269bd63d52
keywords:
- DRM_INDIVIDUALIZATION_STATUS enumeración formato de Windows Media
- enumeración Windows Media Format
topic_type:
- apiref
api_name:
- DRM_INDIVIDUALIZATION_STATUS
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b395d3ad4271ccef9964f0d39c74a1e0ba158257
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671493"
---
# <a name="drm_individualization_status-enumeration-wmdrmsdkh"></a><span data-ttu-id="6ac13-106">Enumeración DRM_INDIVIDUALIZATION_STATUS (wmdrmsdk. h)</span><span class="sxs-lookup"><span data-stu-id="6ac13-106">DRM_INDIVIDUALIZATION_STATUS enumeration (Wmdrmsdk.h)</span></span>

<span data-ttu-id="6ac13-107">El tipo de enumeración **\_ \_ Estado de individualización de DRM** define los Estados válidos para la individualización DRM.</span><span class="sxs-lookup"><span data-stu-id="6ac13-107">The **DRM\_INDIVIDUALIZATION\_STATUS** enumeration type defines the valid states for DRM individualization.</span></span>

## <a name="syntax"></a><span data-ttu-id="6ac13-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6ac13-108">Syntax</span></span>


```C++
typedef enum DRM_INDIVIDUALIZATION_STATUS { 
  INDI_UNDEFINED  = 0x0000,
  INDI_BEGIN      = 0x0001,
  INDI_SUCCEED    = 0x0002,
  INDI_FAIL       = 0x0004,
  INDI_CANCEL     = 0x0008,
  INDI_DOWNLOAD   = 0x0010,
  INDI_INSTALL    = 0x0020
} ;
```



## <a name="constants"></a><span data-ttu-id="6ac13-109">Constantes</span><span class="sxs-lookup"><span data-stu-id="6ac13-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6ac13-110"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDIr \_ sin definir**</span><span class="sxs-lookup"><span data-stu-id="6ac13-110"><span id="INDI_UNDEFINED"></span><span id="indi_undefined"></span>**INDI\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="6ac13-111">Este valor está reservado para uso futuro.</span><span class="sxs-lookup"><span data-stu-id="6ac13-111">This value is reserved for future use.</span></span>

</dd> <dt>

<span data-ttu-id="6ac13-112"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**Inicio de INDI \_**</span><span class="sxs-lookup"><span data-stu-id="6ac13-112"><span id="INDI_BEGIN"></span><span id="indi_begin"></span>**INDI\_BEGIN**</span></span>
</dt> <dd>

<span data-ttu-id="6ac13-113">Indica el inicio del proceso de individualización.</span><span class="sxs-lookup"><span data-stu-id="6ac13-113">Indicates the start of the individualization process.</span></span>

</dd> <dt>

<span data-ttu-id="6ac13-114"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI \_ correctamente**</span><span class="sxs-lookup"><span data-stu-id="6ac13-114"><span id="INDI_SUCCEED"></span><span id="indi_succeed"></span>**INDI\_SUCCEED**</span></span>
</dt> <dd>

<span data-ttu-id="6ac13-115">Indica que se ha completado el proceso de individualización.</span><span class="sxs-lookup"><span data-stu-id="6ac13-115">Indicates that the individualization process has been completed.</span></span>

</dd> <dt>

<span data-ttu-id="6ac13-116"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**error de INDI \_**</span><span class="sxs-lookup"><span data-stu-id="6ac13-116"><span id="INDI_FAIL"></span><span id="indi_fail"></span>**INDI\_FAIL**</span></span>
</dt> <dd>

<span data-ttu-id="6ac13-117">Indica que se ha producido un error en el proceso de individualización.</span><span class="sxs-lookup"><span data-stu-id="6ac13-117">Indicates that the individualization process failed.</span></span>

</dd> <dt>

<span data-ttu-id="6ac13-118"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**cancelación de INDI \_**</span><span class="sxs-lookup"><span data-stu-id="6ac13-118"><span id="INDI_CANCEL"></span><span id="indi_cancel"></span>**INDI\_CANCEL**</span></span>
</dt> <dd>

<span data-ttu-id="6ac13-119">Indica que la aplicación canceló el proceso de individualización.</span><span class="sxs-lookup"><span data-stu-id="6ac13-119">Indicates that the individualization process was canceled by the application.</span></span>

</dd> <dt>

<span data-ttu-id="6ac13-120"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**descarga de INDI \_**</span><span class="sxs-lookup"><span data-stu-id="6ac13-120"><span id="INDI_DOWNLOAD"></span><span id="indi_download"></span>**INDI\_DOWNLOAD**</span></span>
</dt> <dd>

<span data-ttu-id="6ac13-121">Indica que se está descargando la actualización de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6ac13-121">Indicates that the security upgrade is being downloaded.</span></span>

</dd> <dt>

<span data-ttu-id="6ac13-122"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**instalación de INDI \_**</span><span class="sxs-lookup"><span data-stu-id="6ac13-122"><span id="INDI_INSTALL"></span><span id="indi_install"></span>**INDI\_INSTALL**</span></span>
</dt> <dd>

<span data-ttu-id="6ac13-123">Indica que se está instalando la actualización de seguridad.</span><span class="sxs-lookup"><span data-stu-id="6ac13-123">Indicates that the security upgrade is being installed.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6ac13-124">Observaciones</span><span class="sxs-lookup"><span data-stu-id="6ac13-124">Remarks</span></span>

<span data-ttu-id="6ac13-125">Esta enumeración se usa en la estructura de [**\_ \_ Estado**](drmwm-individualize-status.md) de la función de WM.</span><span class="sxs-lookup"><span data-stu-id="6ac13-125">This enumeration is used by the [**WM\_INDIVIDUALIZE\_STATUS**](drmwm-individualize-status.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ac13-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6ac13-126">Requirements</span></span>



| <span data-ttu-id="6ac13-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6ac13-127">Requirement</span></span> | <span data-ttu-id="6ac13-128">Value</span><span class="sxs-lookup"><span data-stu-id="6ac13-128">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6ac13-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6ac13-129">Header</span></span><br/> | <dl> <span data-ttu-id="6ac13-130"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="6ac13-130"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6ac13-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="6ac13-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6ac13-132">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="6ac13-132">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> </dl>

 

 





