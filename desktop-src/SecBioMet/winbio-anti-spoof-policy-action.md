---
title: Enumeración WINBIO_ANTI_SPOOF_POLICY_ACTION (Winbio \_ Types. h)
description: Especifica los tipos de acciones que se realizan para la Directiva de antifalsificación de un usuario.
ms.assetid: 846C0725-1796-49E4-883C-44AC7D618317
keywords:
- WINBIO_ANTI_SPOOF_POLICY_ACTION enumeración Plataforma de biometría de Windows API
- PWINBIO_ANTI_SPOOF_POLICY de puntero de enumeración Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY_ACTION
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5905624bad252475cdde12c003f31a734e64dd2e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996615"
---
# <a name="winbio_anti_spoof_policy_action-enumeration"></a><span data-ttu-id="38d14-105">\_ \_ \_ Enumeración de acciones de directiva de WINBIO anti spoofing \_</span><span class="sxs-lookup"><span data-stu-id="38d14-105">WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION enumeration</span></span>

<span data-ttu-id="38d14-106">Especifica los tipos de acciones que se realizan para la Directiva de antifalsificación de un usuario.</span><span class="sxs-lookup"><span data-stu-id="38d14-106">Specifies the types of actions you take for the antispoofing policy of a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="38d14-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="38d14-107">Syntax</span></span>


```C++
typedef enum _WINBIO_ANTI_SPOOF_POLICY_ACTION { 
  WINBIO_ANTI_SPOOF_DISABLE  = 0x00000000,
  WINBIO_ANTI_SPOOF_ENABLE   = 0x00000001,
  WINBIO_ANTI_SPOOF_REMOVE   = 0x00000002
} WINBIO_ANTI_SPOOF_POLICY_ACTION, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="constants"></a><span data-ttu-id="38d14-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="38d14-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="38d14-109"><span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**Deshabilitación de WINBIO \_ anti \_ Spoofing \_**</span><span class="sxs-lookup"><span data-stu-id="38d14-109"><span id="WINBIO_ANTI_SPOOF_DISABLE"></span><span id="winbio_anti_spoof_disable"></span>**WINBIO\_ANTI\_SPOOF\_DISABLE**</span></span>
</dt> <dd>

<span data-ttu-id="38d14-110">Desactiva la detección de suplantación de identidad para un factor biométrico.</span><span class="sxs-lookup"><span data-stu-id="38d14-110">Turns off the detection of spoofing for a biometric factor.</span></span>

</dd> <dt>

<span data-ttu-id="38d14-111"><span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**\_ \_ habilitación de WINBIO antispoofing \_**</span><span class="sxs-lookup"><span data-stu-id="38d14-111"><span id="WINBIO_ANTI_SPOOF_ENABLE"></span><span id="winbio_anti_spoof_enable"></span>**WINBIO\_ANTI\_SPOOF\_ENABLE**</span></span>
</dt> <dd>

<span data-ttu-id="38d14-112">Activa la detección de suplantación de identidad para un factor biométrico.</span><span class="sxs-lookup"><span data-stu-id="38d14-112">Turns on the detection of spoofing for a biometric factor.</span></span>

</dd> <dt>

<span data-ttu-id="38d14-113"><span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**\_quitar la \_ suplantación de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="38d14-113"><span id="WINBIO_ANTI_SPOOF_REMOVE"></span><span id="winbio_anti_spoof_remove"></span>**WINBIO\_ANTI\_SPOOF\_REMOVE**</span></span>
</dt> <dd>

<span data-ttu-id="38d14-114">Quita la Directiva de antifalsificación completa del factor biométrico de la cuenta.</span><span class="sxs-lookup"><span data-stu-id="38d14-114">Removes the entire antispoofing policy for the biometric factor from the account.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="38d14-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="38d14-115">Requirements</span></span>



| <span data-ttu-id="38d14-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="38d14-116">Requirement</span></span> | <span data-ttu-id="38d14-117">Value</span><span class="sxs-lookup"><span data-stu-id="38d14-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="38d14-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38d14-118">Minimum supported client</span></span><br/> | <span data-ttu-id="38d14-119">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="38d14-119">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="38d14-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="38d14-120">Minimum supported server</span></span><br/> | <span data-ttu-id="38d14-121">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="38d14-121">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="38d14-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="38d14-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="38d14-123"><dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="38d14-123"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="38d14-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="38d14-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38d14-125">**acción de directiva de WINBIO \_ anti \_ Spoofing \_ \_**</span><span class="sxs-lookup"><span data-stu-id="38d14-125">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[<span data-ttu-id="38d14-126">**\_origen de directiva de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="38d14-126">**WINBIO\_POLICY\_SOURCE**</span></span>](winbio-policy-source.md)
</dt> </dl>

 

 





