---
title: BITS_JOB_PROPERTY_VALUE estructura (Deliveryoptimization. h)
description: La Unión BITS_JOB_PROPERTY_VALUE proporciona el valor de propiedad del trabajo DO basándose en el valor de la enumeración BITS_JOB_PROPERTY_ID.
ms.assetid: C24D9EA1-2E72-4403-939A-7B01D7133FE7
keywords:
- Estructura de BITS_JOB_PROPERTY_VALUE
- Estructura de BITS_JOB_PROPERTY_VALUE
topic_type:
- apiref
api_name:
- BITS_JOB_PROPERTY_VALUE
api_location:
- deliveryoptimization.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c48c1fe550db51b6b838379d44df21c95fa95e41
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150280"
---
# <a name="bits_job_property_value-structure"></a><span data-ttu-id="0d0e2-105">Estructura de BITS_JOB_PROPERTY_VALUE</span><span class="sxs-lookup"><span data-stu-id="0d0e2-105">BITS_JOB_PROPERTY_VALUE structure</span></span>

<span data-ttu-id="0d0e2-106">La Unión **BITS_JOB_PROPERTY_VALUE** proporciona el valor de propiedad del trabajo do basándose en el valor de la enumeración [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) .</span><span class="sxs-lookup"><span data-stu-id="0d0e2-106">The **BITS_JOB_PROPERTY_VALUE** union provides the property value of the DO job based on the value of the [**BITS_JOB_PROPERTY_ID**](bits-job-property-id.md) enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d0e2-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0d0e2-107">Syntax</span></span>


```C++
typedef struct {
  DWORD          Dword;
  GUID           ClsID;
  BOOL           Enable;
  UINT64         Uint64;
  BG_AUTH_TARGET Target;
} BITS_JOB_PROPERTY_VALUE;
```



## <a name="members"></a><span data-ttu-id="0d0e2-108">Miembros</span><span class="sxs-lookup"><span data-stu-id="0d0e2-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="0d0e2-109">**DWORD**</span><span class="sxs-lookup"><span data-stu-id="0d0e2-109">**Dword**</span></span>
</dt> <dd>

<span data-ttu-id="0d0e2-110">Este valor se devuelve al utilizar el identificador de la propiedad de enumeración **BITS_JOB_PROPERTY_ID_COST_FLAGS** y se aplica como la [Directiva de transferencia](https://www.bing.com/search?q=transfer+policy) en el trabajo do.</span><span class="sxs-lookup"><span data-stu-id="0d0e2-110">This value is returned when using the enum property ID **BITS_JOB_PROPERTY_ID_COST_FLAGS** and is applied as the [transfer policy](https://www.bing.com/search?q=transfer+policy) on the DO job.</span></span>

</dd> <dt>

<span data-ttu-id="0d0e2-111">**ClsID**</span><span class="sxs-lookup"><span data-stu-id="0d0e2-111">**ClsID**</span></span>
</dt> <dd>

<span data-ttu-id="0d0e2-112">Este valor se devuelve cuando se usa el identificador de la propiedad de enumeración **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** y representa el CLSID del objeto de devolución de llamada que se va a registrar con el trabajo.</span><span class="sxs-lookup"><span data-stu-id="0d0e2-112">This value is returned when using the enum property ID **BITS_JOB_PROPERTY_NOTIFICATION_CLSID** and represents the CLSID of the callback object to register with the DO job.</span></span>

</dd> <dt>

<span data-ttu-id="0d0e2-113">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="0d0e2-113">**Enable**</span></span>
</dt> <dd>

<span data-ttu-id="0d0e2-114">No se admite.</span><span class="sxs-lookup"><span data-stu-id="0d0e2-114">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0d0e2-115">**Uint64**</span><span class="sxs-lookup"><span data-stu-id="0d0e2-115">**Uint64**</span></span>
</dt> <dd>

<span data-ttu-id="0d0e2-116">No se admite.</span><span class="sxs-lookup"><span data-stu-id="0d0e2-116">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="0d0e2-117">**Target**</span><span class="sxs-lookup"><span data-stu-id="0d0e2-117">**Target**</span></span>
</dt> <dd>

<span data-ttu-id="0d0e2-118">No se admite.</span><span class="sxs-lookup"><span data-stu-id="0d0e2-118">Not supported.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0d0e2-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d0e2-119">Requirements</span></span>



| <span data-ttu-id="0d0e2-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d0e2-120">Requirement</span></span> | <span data-ttu-id="0d0e2-121">Value</span><span class="sxs-lookup"><span data-stu-id="0d0e2-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d0e2-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d0e2-122">Minimum supported client</span></span><br/> | <span data-ttu-id="0d0e2-123">Solo aplicaciones de escritorio de Windows 10, versión 1709 \[\]</span><span class="sxs-lookup"><span data-stu-id="0d0e2-123">Windows 10, version 1709 \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="0d0e2-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0d0e2-124">Minimum supported server</span></span><br/> | <span data-ttu-id="0d0e2-125">Windows Server, versión 1709 \[ solo para aplicaciones de escritorio\]</span><span class="sxs-lookup"><span data-stu-id="0d0e2-125">Windows Server, version 1709 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0d0e2-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0d0e2-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="0d0e2-127"><dt>Deliveryoptimization. h</dt></span><span class="sxs-lookup"><span data-stu-id="0d0e2-127"><dt>Deliveryoptimization.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d0e2-128">Vea también</span><span class="sxs-lookup"><span data-stu-id="0d0e2-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d0e2-129">**BITS_JOB_PROPERTY_ID**</span><span class="sxs-lookup"><span data-stu-id="0d0e2-129">**BITS_JOB_PROPERTY_ID**</span></span>](bits-job-property-id.md)
</dt> <dt>

[<span data-ttu-id="0d0e2-130">**BITS_JOB_TRANSFER_POLICY**</span><span class="sxs-lookup"><span data-stu-id="0d0e2-130">**BITS_JOB_TRANSFER_POLICY**</span></span>](bits-job-transfer-policy-.md)
</dt> </dl>

 

 





