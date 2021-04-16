---
title: WMDRMNET_POLICY estructura (wmdrmsdk. h)
description: La \_ estructura de directiva WMDRMNET contiene la Directiva que se va a usar para DRM de Windows Media para las operaciones de dispositivos de red.
ms.assetid: 11eaaeb2-3470-4f58-ae1c-53ee0f60bdce
keywords:
- WMDRMNET_POLICY estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 574e37a8c5ee7f68291012b86cda3a89e25949ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105649525"
---
# <a name="wmdrmnet_policy-structure"></a><span data-ttu-id="61525-105">Estructura de directiva de WMDRMNET \_</span><span class="sxs-lookup"><span data-stu-id="61525-105">WMDRMNET\_POLICY structure</span></span>

<span data-ttu-id="61525-106">La estructura de **\_ Directiva WMDRMNET** contiene la Directiva que se va a usar para DRM de Windows Media para las operaciones de dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="61525-106">The **WMDRMNET\_POLICY** structure contains the policy to be used for Windows Media DRM for Network Devices operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="61525-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="61525-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY {
  WMDRMNET_POLICY_TYPE ePolicyType;
  BYTE                 *pbPolicy;
} ;
```



## <a name="members"></a><span data-ttu-id="61525-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="61525-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="61525-109">**ePolicyType**</span><span class="sxs-lookup"><span data-stu-id="61525-109">**ePolicyType**</span></span>
</dt> <dd>

<span data-ttu-id="61525-110">Miembro de la enumeración de [**\_ \_ tipo de directiva WMDRMNET**](wmdrmnet-policy-type.md) que especifica el tipo de directiva.</span><span class="sxs-lookup"><span data-stu-id="61525-110">Member of the [**WMDRMNET\_POLICY\_TYPE**](wmdrmnet-policy-type.md) enumeration that specifies the type of policy.</span></span>

</dd> <dt>

<span data-ttu-id="61525-111">**pbPolicy**</span><span class="sxs-lookup"><span data-stu-id="61525-111">**pbPolicy**</span></span>
</dt> <dd>

<span data-ttu-id="61525-112">Búfer que contiene la Directiva.</span><span class="sxs-lookup"><span data-stu-id="61525-112">Buffer containing the policy.</span></span> <span data-ttu-id="61525-113">El único tipo de directiva que se admite actualmente es el **\_ tipo de directiva WMDRMNET \_ \_ TRANSCRYPTPLAY**.</span><span class="sxs-lookup"><span data-stu-id="61525-113">The only type of policy currently supported is **WMDRMNET\_POLICY\_TYPE\_TRANSCRYPTPLAY**.</span></span> <span data-ttu-id="61525-114">Este miembro es un puntero a una estructura de **\_ \_ TRANSCRYPTPLAY de directiva de WMDRMNET** .</span><span class="sxs-lookup"><span data-stu-id="61525-114">This member is a pointer to a **WMDRMNET\_POLICY\_TRANSCRYPTPLAY** structure.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="61525-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="61525-115">Remarks</span></span>

<span data-ttu-id="61525-116">Esta estructura se usa como parámetro para el método [**IWMDRMNetTransmitter:: GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) .</span><span class="sxs-lookup"><span data-stu-id="61525-116">This structure is used as a parameter for the [**IWMDRMNetTransmitter::GetLeafLicenseResponse**](iwmdrmnettransmitter-getleaflicenseresponse.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="61525-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61525-117">Requirements</span></span>



| <span data-ttu-id="61525-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="61525-118">Requirement</span></span> | <span data-ttu-id="61525-119">Value</span><span class="sxs-lookup"><span data-stu-id="61525-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="61525-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="61525-120">Header</span></span><br/> | <dl> <span data-ttu-id="61525-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="61525-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61525-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="61525-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61525-123">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="61525-123">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="61525-124">**\_ \_ requisitos globales de la Directiva WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="61525-124">**WMDRMNET\_POLICY\_GLOBAL\_REQUIREMENTS**</span></span>](wmdrmnet-policy-global-requirements.md)
</dt> <dt>

[<span data-ttu-id="61525-125">**\_ \_ entorno mínimo de directiva de WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="61525-125">**WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT**</span></span>](wmdrmnet-policy-minimum-environment.md)
</dt> <dt>

[<span data-ttu-id="61525-126">**\_TRANSCRYPTPLAY de directiva de WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="61525-126">**WMDRMNET\_POLICY\_TRANSCRYPTPLAY**</span></span>](wmdrmnet-policy-transcryptplay.md)
</dt> <dt>

[<span data-ttu-id="61525-127">**\_tipo de directiva WMDRMNET \_**</span><span class="sxs-lookup"><span data-stu-id="61525-127">**WMDRMNET\_POLICY\_TYPE**</span></span>](wmdrmnet-policy-type.md)
</dt> </dl>

 

 





