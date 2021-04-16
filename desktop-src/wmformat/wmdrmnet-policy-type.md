---
title: Enumeración WMDRMNET_POLICY_TYPE (wmdrmsdk. h)
description: El \_ \_ tipo de enumeración de tipo de directiva WMDRMNET muestra los tipos de directivas que están disponibles para las operaciones de Windows Media DRM para dispositivos de red.
ms.assetid: 83e9e247-3bd8-4857-97b6-95b3cd5ad25c
keywords:
- WMDRMNET_POLICY_TYPE enumeración formato de Windows Media
- enumeración Windows Media Format
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_TYPE
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 964a3e938caa312f02f21074f046f3cf88d72de6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649988"
---
# <a name="wmdrmnet_policy_type-enumeration"></a><span data-ttu-id="721ac-105">\_Enumeración de tipo de directiva WMDRMNET \_</span><span class="sxs-lookup"><span data-stu-id="721ac-105">WMDRMNET\_POLICY\_TYPE enumeration</span></span>

<span data-ttu-id="721ac-106">El tipo de enumeración de **\_ \_ tipo de directiva WMDRMNET** muestra los tipos de directivas que están disponibles para las operaciones de Windows Media DRM para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="721ac-106">The **WMDRMNET\_POLICY\_TYPE** enumeration type lists the types of policies that are available for Windows Media DRM for Network Devices operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="721ac-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="721ac-107">Syntax</span></span>


```C++
typedef enum WMDRMNET_POLICY_TYPE { 
  WMDRMNET_POLICY_TYPE_UNDEFINED       = 0x0000,
  WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY  = 0x0001
} ;
```



## <a name="constants"></a><span data-ttu-id="721ac-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="721ac-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="721ac-109"><span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**\_tipo de directiva WMDRMNET \_ sin \_ definir**</span><span class="sxs-lookup"><span data-stu-id="721ac-109"><span id="WMDRMNET_POLICY_TYPE_UNDEFINED"></span><span id="wmdrmnet_policy_type_undefined"></span>**WMDRMNET\_POLICY\_TYPE\_UNDEFINED**</span></span>
</dt> <dd>

<span data-ttu-id="721ac-110">No se admiten tipos de directivas no definidos.</span><span class="sxs-lookup"><span data-stu-id="721ac-110">Undefined policy types are not supported.</span></span>

</dd> <dt>

<span data-ttu-id="721ac-111"><span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**\_tipo de directiva WMDRMNET \_ \_ TRANSCRYPTPLAY**</span><span class="sxs-lookup"><span data-stu-id="721ac-111"><span id="WMDRMNET_POLICY_TYPE_TRANSCRYPTPLAY"></span><span id="wmdrmnet_policy_type_transcryptplay"></span>**WMDRMNET\_POLICY\_TYPE\_TRANSCRYPTPLAY**</span></span>
</dt> <dd>

<span data-ttu-id="721ac-112">La Directiva rige la capacidad de convertir contenido protegido por DRM de Windows Media en Windows Media DRM protegido para los datos de dispositivos de red y reproducirlo en un dispositivo en red.</span><span class="sxs-lookup"><span data-stu-id="721ac-112">The policy governs the ability to convert content protected by Windows Media DRM into protected Windows Media DRM for Network Devices data and play it back on a networked device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="721ac-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="721ac-113">Remarks</span></span>

<span data-ttu-id="721ac-114">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="721ac-114">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="721ac-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="721ac-115">Requirements</span></span>



| <span data-ttu-id="721ac-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="721ac-116">Requirement</span></span> | <span data-ttu-id="721ac-117">Value</span><span class="sxs-lookup"><span data-stu-id="721ac-117">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="721ac-118">Encabezado</span><span class="sxs-lookup"><span data-stu-id="721ac-118">Header</span></span><br/> | <dl> <span data-ttu-id="721ac-119"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="721ac-119"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="721ac-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="721ac-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="721ac-121">**Tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="721ac-121">**Enumeration Types**</span></span>](drm-enumeration-types.md)
</dt> <dt>

[<span data-ttu-id="721ac-122">**\_Directiva WMDRMNET**</span><span class="sxs-lookup"><span data-stu-id="721ac-122">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





