---
title: Estructura de WINBIO_ANTI_SPOOF_POLICY (Winbio \_ Types. h)
description: Representa la Directiva de antifalsificación para un usuario.
ms.assetid: 2B433AE8-21A0-4AF1-853C-9074527DB2E4
keywords:
- Plataforma de biometría de Windows API de WINBIO_ANTI_SPOOF_POLICY Structure
- PWINBIO_ANTI_SPOOF_POLICY de puntero de estructura Plataforma de biometría de Windows API
topic_type:
- apiref
api_name:
- WINBIO_ANTI_SPOOF_POLICY
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3da8b7811afb1de1ad464675125f125ef0ceab73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104491392"
---
# <a name="winbio_anti_spoof_policy-structure"></a><span data-ttu-id="a1977-105">Estructura de directiva de WINBIO \_ anti \_ Spoofing \_</span><span class="sxs-lookup"><span data-stu-id="a1977-105">WINBIO\_ANTI\_SPOOF\_POLICY structure</span></span>

<span data-ttu-id="a1977-106">Representa la Directiva de antifalsificación para un usuario.</span><span class="sxs-lookup"><span data-stu-id="a1977-106">Represents the antispoofing policy for a user.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1977-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1977-107">Syntax</span></span>


```C++
typedef struct _WINBIO_ANTI_SPOOF_POLICY {
  WINBIO_ANTI_SPOOF_POLICY_ACTION Action;
  WINBIO_POLICY_SOURCE            Source;
} WINBIO_ANTI_SPOOF_POLICY, *PWINBIO_ANTI_SPOOF_POLICY;
```



## <a name="members"></a><span data-ttu-id="a1977-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="a1977-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="a1977-109">**Acción**</span><span class="sxs-lookup"><span data-stu-id="a1977-109">**Action**</span></span>
</dt> <dd>

<span data-ttu-id="a1977-110">El tipo de acción que se debe realizar para la Directiva de antifalsificación.</span><span class="sxs-lookup"><span data-stu-id="a1977-110">The type of action to take for the antispoofing policy.</span></span>

</dd> <dt>

<span data-ttu-id="a1977-111">**Origen**</span><span class="sxs-lookup"><span data-stu-id="a1977-111">**Source**</span></span>
</dt> <dd>

<span data-ttu-id="a1977-112">Origen de la Directiva de antifalsificación.</span><span class="sxs-lookup"><span data-stu-id="a1977-112">The source for the antispoofing policy.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1977-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1977-113">Requirements</span></span>



| <span data-ttu-id="a1977-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1977-114">Requirement</span></span> | <span data-ttu-id="a1977-115">Value</span><span class="sxs-lookup"><span data-stu-id="a1977-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1977-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1977-116">Minimum supported client</span></span><br/> | <span data-ttu-id="a1977-117">Solo aplicaciones de escritorio de Windows 10 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1977-117">Windows 10 \[desktop apps only\]</span></span><br/>                                                                                                                              |
| <span data-ttu-id="a1977-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1977-118">Minimum supported server</span></span><br/> | <span data-ttu-id="a1977-119">Solo aplicaciones de escritorio de Windows Server 2016 \[\]</span><span class="sxs-lookup"><span data-stu-id="a1977-119">Windows Server 2016 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="a1977-120">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1977-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1977-121"><dt>Winbio \_ Types. h (incluye Winbio. h para aplicaciones cliente o \_ adaptadores de Winbio. h para adaptadores)</dt></span><span class="sxs-lookup"><span data-stu-id="a1977-121"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1977-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="a1977-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1977-123">**acción de directiva de WINBIO \_ anti \_ Spoofing \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a1977-123">**WINBIO\_ANTI\_SPOOF\_POLICY\_ACTION**</span></span>](winbio-anti-spoof-policy-action.md)
</dt> <dt>

[<span data-ttu-id="a1977-124">**\_origen de directiva de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="a1977-124">**WINBIO\_POLICY\_SOURCE**</span></span>](winbio-policy-source.md)
</dt> <dt>

[<span data-ttu-id="a1977-125">**\_resultado asincrónico de WINBIO \_**</span><span class="sxs-lookup"><span data-stu-id="a1977-125">**WINBIO\_ASYNC\_RESULT**</span></span>](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)
</dt> <dt>

[<span data-ttu-id="a1977-126">**WinBioGetProperty**</span><span class="sxs-lookup"><span data-stu-id="a1977-126">**WinBioGetProperty**</span></span>](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)
</dt> <dt>

[<span data-ttu-id="a1977-127">**WinBioSetProperty**</span><span class="sxs-lookup"><span data-stu-id="a1977-127">**WinBioSetProperty**</span></span>](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)
</dt> </dl>

 

 





