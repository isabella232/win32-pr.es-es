---
title: WMDRMNET_POLICY_MINIMUM_ENVIRONMENT estructura (wmdrmsdk. h)
description: La \_ estructura de entorno mínima de la Directiva WMDRMNET \_ \_ contiene los requisitos de seguridad mínimos para DRM de Windows Media para dispositivos de red.
ms.assetid: b1bc9a8d-197e-45fe-a152-0b81add977eb
keywords:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT estructura de Windows Media Format
- Formato de Windows Media de estructura
topic_type:
- apiref
api_name:
- WMDRMNET_POLICY_MINIMUM_ENVIRONMENT
api_location:
- Wmdrmsdk.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4bf53fdec186a44eff375dd2e9cf9badfe0ba715
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105699978"
---
# <a name="wmdrmnet_policy_minimum_environment-structure"></a><span data-ttu-id="854f6-105">\_Estructura de \_ entorno mínima de directiva de WMDRMNET \_</span><span class="sxs-lookup"><span data-stu-id="854f6-105">WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT structure</span></span>

<span data-ttu-id="854f6-106">La estructura de **\_ \_ \_ entorno mínima de la Directiva WMDRMNET** contiene los requisitos de seguridad mínimos para DRM de Windows Media para dispositivos de red.</span><span class="sxs-lookup"><span data-stu-id="854f6-106">The **WMDRMNET\_POLICY\_MINIMUM\_ENVIRONMENT** structure contains the minimum security requirements for Windows Media DRM for Network Devices.</span></span>

## <a name="syntax"></a><span data-ttu-id="854f6-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="854f6-107">Syntax</span></span>


```C++
typedef struct WMDRMNET_POLICY_MINIMUM_ENVIRONMENT {
  WORD  wMinimumSecurityLevel;
  DWORD dwMinimumAppRevocationListVersion;
  DWORD dwMinimumDeviceRevocationListVersion;
} ;
```



## <a name="members"></a><span data-ttu-id="854f6-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="854f6-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="854f6-109">**wMinimumSecurityLevel**</span><span class="sxs-lookup"><span data-stu-id="854f6-109">**wMinimumSecurityLevel**</span></span>
</dt> <dd>

<span data-ttu-id="854f6-110">Nivel de seguridad de la aplicación mínimo requerido.</span><span class="sxs-lookup"><span data-stu-id="854f6-110">Minimum application security level required.</span></span>

</dd> <dt>

<span data-ttu-id="854f6-111">**dwMinimumAppRevocationListVersion**</span><span class="sxs-lookup"><span data-stu-id="854f6-111">**dwMinimumAppRevocationListVersion**</span></span>
</dt> <dd>

<span data-ttu-id="854f6-112">Versión de lista de revocación de certificados de aplicación mínima requerida.</span><span class="sxs-lookup"><span data-stu-id="854f6-112">Minimum application certificate revocation list version required.</span></span>

</dd> <dt>

<span data-ttu-id="854f6-113">**dwMinimumDeviceRevocationListVersion**</span><span class="sxs-lookup"><span data-stu-id="854f6-113">**dwMinimumDeviceRevocationListVersion**</span></span>
</dt> <dd>

<span data-ttu-id="854f6-114">Se requiere una lista de revocación de certificados de dispositivo mínima.</span><span class="sxs-lookup"><span data-stu-id="854f6-114">Minimum device certificate revocation list required.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="854f6-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="854f6-115">Remarks</span></span>

<span data-ttu-id="854f6-116">Ninguno.</span><span class="sxs-lookup"><span data-stu-id="854f6-116">None.</span></span>

## <a name="requirements"></a><span data-ttu-id="854f6-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="854f6-117">Requirements</span></span>



| <span data-ttu-id="854f6-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="854f6-118">Requirement</span></span> | <span data-ttu-id="854f6-119">Value</span><span class="sxs-lookup"><span data-stu-id="854f6-119">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="854f6-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="854f6-120">Header</span></span><br/> | <dl> <span data-ttu-id="854f6-121"><dt>Wmdrmsdk. h</dt></span><span class="sxs-lookup"><span data-stu-id="854f6-121"><dt>Wmdrmsdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="854f6-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="854f6-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="854f6-123">**Estructuras**</span><span class="sxs-lookup"><span data-stu-id="854f6-123">**Structures**</span></span>](drm-structures.md)
</dt> <dt>

[<span data-ttu-id="854f6-124">**\_Directiva WMDRMNET**</span><span class="sxs-lookup"><span data-stu-id="854f6-124">**WMDRMNET\_POLICY**</span></span>](wmdrmnet-policy.md)
</dt> </dl>

 

 





