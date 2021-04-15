---
title: Enumeración HealthClassValue (NapProtocol. h)
description: Indica el valor de la clase de mantenimiento TLV.
ms.assetid: af80c27a-a686-494b-8795-73eb366deaa0
keywords:
- NAP de enumeración de HealthClassValue
topic_type:
- apiref
api_name:
- HealthClassValue
api_location:
- NapProtocol.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ade44b74d03a69d6ccf410a042adf3819b8cc782
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104488962"
---
# <a name="healthclassvalue-enumeration"></a><span data-ttu-id="92877-104">Enumeración HealthClassValue</span><span class="sxs-lookup"><span data-stu-id="92877-104">HealthClassValue enumeration</span></span>

> [!Note]  
> <span data-ttu-id="92877-105">La plataforma de protección de acceso a redes no está disponible a partir de Windows 10</span><span class="sxs-lookup"><span data-stu-id="92877-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="92877-106">El tipo de enumeración **HealthClassValue** indica el valor de la clase de mantenimiento TLV.</span><span class="sxs-lookup"><span data-stu-id="92877-106">The **HealthClassValue** enumeration type indicates the value of the health class TLV.</span></span>

## <a name="syntax"></a><span data-ttu-id="92877-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="92877-107">Syntax</span></span>


```C++
typedef enum tagHealthClassValue { 
  healthClassFirewall        = 0,
  healthClassPatchLevel      = 1,
  healthClassAntiVirus       = 2,
  healthClassCriticalUpdate  = 3,
  healthClassReserved        = 128
} HealthClassValue;
```



## <a name="constants"></a><span data-ttu-id="92877-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="92877-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="92877-109"><span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthClassFirewall**</span><span class="sxs-lookup"><span data-stu-id="92877-109"><span id="healthClassFirewall"></span><span id="healthclassfirewall"></span><span id="HEALTHCLASSFIREWALL"></span>**healthClassFirewall**</span></span>
</dt> <dd>

<span data-ttu-id="92877-110">La clase de mantenimiento TLV es Firewall.</span><span class="sxs-lookup"><span data-stu-id="92877-110">The health class TLV is firewall.</span></span>

</dd> <dt>

<span data-ttu-id="92877-111"><span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthClassPatchLevel**</span><span class="sxs-lookup"><span data-stu-id="92877-111"><span id="healthClassPatchLevel"></span><span id="healthclasspatchlevel"></span><span id="HEALTHCLASSPATCHLEVEL"></span>**healthClassPatchLevel**</span></span>
</dt> <dd>

<span data-ttu-id="92877-112">La clase de mantenimiento TLV es el nivel de revisión.</span><span class="sxs-lookup"><span data-stu-id="92877-112">The health class TLV is patch level.</span></span>

</dd> <dt>

<span data-ttu-id="92877-113"><span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthClassAntiVirus**</span><span class="sxs-lookup"><span data-stu-id="92877-113"><span id="healthClassAntiVirus"></span><span id="healthclassantivirus"></span><span id="HEALTHCLASSANTIVIRUS"></span>**healthClassAntiVirus**</span></span>
</dt> <dd>

<span data-ttu-id="92877-114">La clase de estado TLV es antivirus.</span><span class="sxs-lookup"><span data-stu-id="92877-114">The health class TLV is antivirus.</span></span>

</dd> <dt>

<span data-ttu-id="92877-115"><span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthClassCriticalUpdate**</span><span class="sxs-lookup"><span data-stu-id="92877-115"><span id="healthClassCriticalUpdate"></span><span id="healthclasscriticalupdate"></span><span id="HEALTHCLASSCRITICALUPDATE"></span>**healthClassCriticalUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="92877-116">La clase de mantenimiento TLV es una actualización crítica.</span><span class="sxs-lookup"><span data-stu-id="92877-116">The health class TLV is critical update.</span></span>

</dd> <dt>

<span data-ttu-id="92877-117"><span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthClassReserved**</span><span class="sxs-lookup"><span data-stu-id="92877-117"><span id="healthClassReserved"></span><span id="healthclassreserved"></span><span id="HEALTHCLASSRESERVED"></span>**healthClassReserved**</span></span>
</dt> <dd>

<span data-ttu-id="92877-118">Reservado solo para uso del sistema.</span><span class="sxs-lookup"><span data-stu-id="92877-118">Reserved for system use only.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="92877-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="92877-119">Requirements</span></span>



| <span data-ttu-id="92877-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="92877-120">Requirement</span></span> | <span data-ttu-id="92877-121">Value</span><span class="sxs-lookup"><span data-stu-id="92877-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="92877-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92877-122">Minimum supported client</span></span><br/> | <span data-ttu-id="92877-123">Solo aplicaciones de escritorio de Windows Vista \[\]</span><span class="sxs-lookup"><span data-stu-id="92877-123">Windows Vista \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="92877-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="92877-124">Minimum supported server</span></span><br/> | <span data-ttu-id="92877-125">Solo aplicaciones de escritorio de Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="92877-125">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="92877-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="92877-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="92877-127"><dt>NapProtocol. h</dt></span><span class="sxs-lookup"><span data-stu-id="92877-127"><dt>NapProtocol.h</dt></span></span> </dl>   |
| <span data-ttu-id="92877-128">IDL</span><span class="sxs-lookup"><span data-stu-id="92877-128">IDL</span></span><br/>                      | <dl> <span data-ttu-id="92877-129"><dt>NapProtocol. idl</dt></span><span class="sxs-lookup"><span data-stu-id="92877-129"><dt>NapProtocol.idl</dt></span></span> </dl> |



 

 





