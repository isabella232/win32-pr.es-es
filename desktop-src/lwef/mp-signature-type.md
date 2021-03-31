---
title: Enumeración MP_SIGNATURE_TYPE (MpClient. h)
description: Posibles tipos de firma.
ms.assetid: 44B195A8-866D-4B87-9576-54E00658F9B3
keywords:
- MP_SIGNATURE_TYPE enumeración características de entorno heredado de Windows
- PMP_SIGNATURE_TYPE el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MP_SIGNATURE_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b99f7140706e9a6d3fa32e7eb346ef6478f3f26
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490396"
---
# <a name="mp_signature_type-enumeration"></a><span data-ttu-id="68fa7-105">\_Enumeración de tipos de firma de MP \_</span><span class="sxs-lookup"><span data-stu-id="68fa7-105">MP\_SIGNATURE\_TYPE enumeration</span></span>

<span data-ttu-id="68fa7-106">Posibles tipos de firma.</span><span class="sxs-lookup"><span data-stu-id="68fa7-106">Possible signature types.</span></span>

## <a name="syntax"></a><span data-ttu-id="68fa7-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="68fa7-107">Syntax</span></span>


```C++
typedef enum tagMP_SIGNATURE_TYPE { 
  MP_SIGNATURE_ANTIMALWARE     = 0,
  MP_SIGNATURE_ANTIVIRUS       = 1,
  MP_SIGNATURE_ANTISPYWARE     = 2,
  MP_SIGNATURE_NIS             = 3,
  MP_SIGNATURE_TYPES_MAXVALUE  = 3
} MP_SIGNATURE_TYPE, *PMP_SIGNATURE_TYPE;
```



## <a name="constants"></a><span data-ttu-id="68fa7-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="68fa7-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="68fa7-109"><span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**antimalware de firma de MP \_ \_**</span><span class="sxs-lookup"><span data-stu-id="68fa7-109"><span id="MP_SIGNATURE_ANTIMALWARE"></span><span id="mp_signature_antimalware"></span>**MP\_SIGNATURE\_ANTIMALWARE**</span></span>
</dt> <dd>

<span data-ttu-id="68fa7-110">Firmas antivirus y antispyware.</span><span class="sxs-lookup"><span data-stu-id="68fa7-110">Both antivirus and antispyware signatures.</span></span>

</dd> <dt>

<span data-ttu-id="68fa7-111"><span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**\_antivirus de firmas de MP \_**</span><span class="sxs-lookup"><span data-stu-id="68fa7-111"><span id="MP_SIGNATURE_ANTIVIRUS"></span><span id="mp_signature_antivirus"></span>**MP\_SIGNATURE\_ANTIVIRUS**</span></span>
</dt> <dd>

<span data-ttu-id="68fa7-112">Solo firmas de antivirus.</span><span class="sxs-lookup"><span data-stu-id="68fa7-112">Only antivirus signatures.</span></span>

</dd> <dt>

<span data-ttu-id="68fa7-113"><span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**\_AntiSpyware de firma de MP \_**</span><span class="sxs-lookup"><span data-stu-id="68fa7-113"><span id="MP_SIGNATURE_ANTISPYWARE"></span><span id="mp_signature_antispyware"></span>**MP\_SIGNATURE\_ANTISPYWARE**</span></span>
</dt> <dd>

<span data-ttu-id="68fa7-114">Solo firmas de anti spyware.</span><span class="sxs-lookup"><span data-stu-id="68fa7-114">Only antispyware signatures.</span></span>

</dd> <dt>

<span data-ttu-id="68fa7-115"><span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**firma de MP en \_ \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="68fa7-115"><span id="MP_SIGNATURE_NIS"></span><span id="mp_signature_nis"></span>**MP\_SIGNATURE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="68fa7-116">Firmas NIS.</span><span class="sxs-lookup"><span data-stu-id="68fa7-116">NIS signatures.</span></span>

</dd> <dt>

<span data-ttu-id="68fa7-117"><span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**tipos de firma de MP \_ \_ \_ MAXVALUE**</span><span class="sxs-lookup"><span data-stu-id="68fa7-117"><span id="MP_SIGNATURE_TYPES_MAXVALUE"></span><span id="mp_signature_types_maxvalue"></span>**MP\_SIGNATURE\_TYPES\_MAXVALUE**</span></span>
<span data-ttu-id="68fa7-118"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="68fa7-118"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="68fa7-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68fa7-119">Requirements</span></span>



| <span data-ttu-id="68fa7-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="68fa7-120">Requirement</span></span> | <span data-ttu-id="68fa7-121">Value</span><span class="sxs-lookup"><span data-stu-id="68fa7-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="68fa7-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68fa7-122">Minimum supported client</span></span><br/> | <span data-ttu-id="68fa7-123">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="68fa7-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="68fa7-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="68fa7-124">Minimum supported server</span></span><br/> | <span data-ttu-id="68fa7-125">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="68fa7-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="68fa7-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="68fa7-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="68fa7-127"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="68fa7-127"><dt>MpClient.h</dt></span></span> </dl> |



 

 





