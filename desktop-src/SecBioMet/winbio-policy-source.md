---
title: Enumeración WINBIO_POLICY_SOURCE (Winbio \_ Types. h)
description: Enumera los orígenes posibles de información de directiva para la detección de suplantación de los factores biométricos.
ms.assetid: 3DC3BB0B-1FD7-473C-8E0B-B7E0A4A44E9E
keywords:
- WINBIO_POLICY_SOURCE enumeración Plataforma de biometría de Windows API
- PWINBIO_POLICY_SOURCE de puntero de enumeración Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_POLICY_SOURCE
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 866d1d82d939f143c4385caa5d94c68ffe3758f9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104359851"
---
# <a name="winbio_policy_source-enumeration"></a><span data-ttu-id="3203f-105">\_Enumeración de origen de directiva WINBIO \_</span><span class="sxs-lookup"><span data-stu-id="3203f-105">WINBIO\_POLICY\_SOURCE enumeration</span></span>

<span data-ttu-id="3203f-106">Enumera los orígenes posibles de información de directiva para la detección de suplantación de los factores biométricos.</span><span class="sxs-lookup"><span data-stu-id="3203f-106">Lists the possible sources of policy information for the detection of spoofing for biometric factors.</span></span>

## <a name="syntax"></a><span data-ttu-id="3203f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3203f-107">Syntax</span></span>


```C++
typedef enum _WINBIO_POLICY_SOURCE { 
  WINBIO_POLICY_UNKNOWN  = 0x00000000,
  WINBIO_POLICY_DEFAULT  = 0x00000001,
  WINBIO_POLICY_LOCAL    = 0x00000002,
  WINBIO_POLICY_ADMIN    = 0x00000003
} WINBIO_POLICY_SOURCE, *PWINBIO_POLICY_SOURCE;
```



## <a name="constants"></a><span data-ttu-id="3203f-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="3203f-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="3203f-109"><span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**Directiva de WINBIO \_ \_ desconocida**</span><span class="sxs-lookup"><span data-stu-id="3203f-109"><span id="WINBIO_POLICY_UNKNOWN"></span><span id="winbio_policy_unknown"></span>**WINBIO\_POLICY\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="3203f-110">Se desconoce el origen de la Directiva.</span><span class="sxs-lookup"><span data-stu-id="3203f-110">The source of the policy is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="3203f-111"><span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**\_directiva \_ predeterminada de WINBIO**</span><span class="sxs-lookup"><span data-stu-id="3203f-111"><span id="WINBIO_POLICY_DEFAULT"></span><span id="winbio_policy_default"></span>**WINBIO\_POLICY\_DEFAULT**</span></span>
</dt> <dd>

<span data-ttu-id="3203f-112">La Directiva es la directiva predeterminada que proporciona el Plataforma de biometría de Windows.</span><span class="sxs-lookup"><span data-stu-id="3203f-112">The policy is the default policy that the Windows Biometric Framework provides.</span></span>

</dd> <dt>

<span data-ttu-id="3203f-113"><span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**\_Directiva WINBIO \_ local**</span><span class="sxs-lookup"><span data-stu-id="3203f-113"><span id="WINBIO_POLICY_LOCAL"></span><span id="winbio_policy_local"></span>**WINBIO\_POLICY\_LOCAL**</span></span>
</dt> <dd>

<span data-ttu-id="3203f-114">La directiva establecida por el usuario individual para su cuenta mediante la aplicación de **configuración** .</span><span class="sxs-lookup"><span data-stu-id="3203f-114">The policy that the individual user set for their account by using the **Settings** app.</span></span> <span data-ttu-id="3203f-115">Esta directiva invalida la directiva predeterminada.</span><span class="sxs-lookup"><span data-stu-id="3203f-115">This policy overrides the default policy.</span></span>

</dd> <dt>

<span data-ttu-id="3203f-116"><span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**\_Administrador de directivas de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="3203f-116"><span id="WINBIO_POLICY_ADMIN"></span><span id="winbio_policy_admin"></span>**WINBIO\_POLICY\_ADMIN**</span></span>
</dt> <dd>

<span data-ttu-id="3203f-117">Una directiva de grupo establecida por el administrador de TI para la empresa.</span><span class="sxs-lookup"><span data-stu-id="3203f-117">A group policy that the IT administrator set for the enterprise.</span></span> <span data-ttu-id="3203f-118">Los usuarios individuales no pueden invalidar esta Directiva.</span><span class="sxs-lookup"><span data-stu-id="3203f-118">Individual users cannot override this policy.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3203f-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3203f-119">Requirements</span></span>



| <span data-ttu-id="3203f-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="3203f-120">Requirement</span></span> | <span data-ttu-id="3203f-121">Value</span><span class="sxs-lookup"><span data-stu-id="3203f-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3203f-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3203f-122">Minimum supported client</span></span><br/> | <span data-ttu-id="3203f-123">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="3203f-123">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="3203f-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3203f-124">Minimum supported server</span></span><br/> | <span data-ttu-id="3203f-125">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="3203f-125">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="3203f-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="3203f-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="3203f-127"><dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="3203f-127"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3203f-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="3203f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3203f-129">**acción de directiva de WINBIO \_ anti \_ Spoofing \_ \_**</span><span class="sxs-lookup"><span data-stu-id="3203f-129">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> </dl>

 

 





