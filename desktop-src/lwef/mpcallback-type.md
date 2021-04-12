---
title: Enumeración MPCALLBACK_TYPE (MpClient. h)
description: Posibles tipos de devolución de llamada.
ms.assetid: 8E4F50B7-0F02-434D-B91E-C9966C92CDC0
keywords:
- MPCALLBACK_TYPE enumeración características de entorno heredado de Windows
- PMPCALLBACK_TYPE el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPCALLBACK_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1a3fd310f3733d36dd92ace1c7a5286bcf73a75f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104490013"
---
# <a name="mpcallback_type-enumeration"></a><span data-ttu-id="1c882-105">\_Enumeración de tipo MPCALLBACK</span><span class="sxs-lookup"><span data-stu-id="1c882-105">MPCALLBACK\_TYPE enumeration</span></span>

<span data-ttu-id="1c882-106">Posibles tipos de devolución de llamada.</span><span class="sxs-lookup"><span data-stu-id="1c882-106">Possible callback types.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c882-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1c882-107">Syntax</span></span>


```C++
typedef enum tagMPCALLBACK_TYPE { 
  MPCALLBACK_UNKNOWN                     = 0,
  MPCALLBACK_STATUS                      = 1,
  MPCALLBACK_THREAT                      = 2,
  MPCALLBACK_SCAN                        = 3,
  MPCALLBACK_CLEAN                       = 4,
  MPCALLBACK_PRECHECK                    = 5,
  MPCALLBACK_SIGUPDATE                   = 6,
  MPCALLBACK_SAMPLE                      = 7,
  MPCALLBACK_RESERVED                    = 8,
  MPCALLBACK_CONFIGURATION_NOTIFICATION  = 9,
  MPCALLBACK_FASTPATH                    = 10,
  MPCALLBACK_PRODUCT_EXPIRATION          = 11,
  MPCALLBACK_NIS_PRIVATE                 = 12,
  MPCALLBACK_HEALTH                      = 13,
  MPCALLBACK_ENDOFLIFE                   = 14,
  MPCALLBACK_MALWARETOAST                = 15,
  MPCALLBACK_MAXVALUE                    = 15
} MPCALLBACK_TYPE, *PMPCALLBACK_TYPE;
```



## <a name="constants"></a><span data-ttu-id="1c882-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="1c882-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="1c882-109"><span id="MPCALLBACK_UNKNOWN"></span><span id="mpcallback_unknown"></span>**MPCALLBACK \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="1c882-109"><span id="MPCALLBACK_UNKNOWN"></span><span id="mpcallback_unknown"></span>**MPCALLBACK\_UNKNOWN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1c882-110"><span id="MPCALLBACK_STATUS"></span><span id="mpcallback_status"></span>**Estado de MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="1c882-110"><span id="MPCALLBACK_STATUS"></span><span id="mpcallback_status"></span>**MPCALLBACK\_STATUS**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1c882-111"><span id="MPCALLBACK_THREAT"></span><span id="mpcallback_threat"></span>**MPCALLBACK \_ amenaza**</span><span class="sxs-lookup"><span data-stu-id="1c882-111"><span id="MPCALLBACK_THREAT"></span><span id="mpcallback_threat"></span>**MPCALLBACK\_THREAT**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1c882-112"><span id="MPCALLBACK_SCAN"></span><span id="mpcallback_scan"></span>**examen de MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="1c882-112"><span id="MPCALLBACK_SCAN"></span><span id="mpcallback_scan"></span>**MPCALLBACK\_SCAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1c882-113"><span id="MPCALLBACK_CLEAN"></span><span id="mpcallback_clean"></span>**MPCALLBACK \_ Clean**</span><span class="sxs-lookup"><span data-stu-id="1c882-113"><span id="MPCALLBACK_CLEAN"></span><span id="mpcallback_clean"></span>**MPCALLBACK\_CLEAN**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1c882-114"><span id="MPCALLBACK_PRECHECK"></span><span id="mpcallback_precheck"></span>**COMPROBACIÓN de MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="1c882-114"><span id="MPCALLBACK_PRECHECK"></span><span id="mpcallback_precheck"></span>**MPCALLBACK\_PRECHECK**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1c882-115"><span id="MPCALLBACK_SIGUPDATE"></span><span id="mpcallback_sigupdate"></span>**MPCALLBACK \_ SIGUPDATE**</span><span class="sxs-lookup"><span data-stu-id="1c882-115"><span id="MPCALLBACK_SIGUPDATE"></span><span id="mpcallback_sigupdate"></span>**MPCALLBACK\_SIGUPDATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1c882-116"><span id="MPCALLBACK_SAMPLE"></span><span id="mpcallback_sample"></span>**ejemplo de MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="1c882-116"><span id="MPCALLBACK_SAMPLE"></span><span id="mpcallback_sample"></span>**MPCALLBACK\_SAMPLE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1c882-117"><span id="MPCALLBACK_RESERVED"></span><span id="mpcallback_reserved"></span>**MPCALLBACK \_ reservado**</span><span class="sxs-lookup"><span data-stu-id="1c882-117"><span id="MPCALLBACK_RESERVED"></span><span id="mpcallback_reserved"></span>**MPCALLBACK\_RESERVED**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1c882-118"><span id="MPCALLBACK_CONFIGURATION_NOTIFICATION"></span><span id="mpcallback_configuration_notification"></span>**\_notificación de configuración de MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="1c882-118"><span id="MPCALLBACK_CONFIGURATION_NOTIFICATION"></span><span id="mpcallback_configuration_notification"></span>**MPCALLBACK\_CONFIGURATION\_NOTIFICATION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1c882-119"><span id="MPCALLBACK_FASTPATH"></span><span id="mpcallback_fastpath"></span>**MPCALLBACK \_ FASTPATH**</span><span class="sxs-lookup"><span data-stu-id="1c882-119"><span id="MPCALLBACK_FASTPATH"></span><span id="mpcallback_fastpath"></span>**MPCALLBACK\_FASTPATH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1c882-120"><span id="MPCALLBACK_PRODUCT_EXPIRATION"></span><span id="mpcallback_product_expiration"></span>**\_expiración del producto MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="1c882-120"><span id="MPCALLBACK_PRODUCT_EXPIRATION"></span><span id="mpcallback_product_expiration"></span>**MPCALLBACK\_PRODUCT\_EXPIRATION**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1c882-121"><span id="MPCALLBACK_NIS_PRIVATE"></span><span id="mpcallback_nis_private"></span>**MPCALLBACK \_ NIS \_ privado**</span><span class="sxs-lookup"><span data-stu-id="1c882-121"><span id="MPCALLBACK_NIS_PRIVATE"></span><span id="mpcallback_nis_private"></span>**MPCALLBACK\_NIS\_PRIVATE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1c882-122"><span id="MPCALLBACK_HEALTH"></span><span id="mpcallback_health"></span>**mantenimiento de MPCALLBACK \_**</span><span class="sxs-lookup"><span data-stu-id="1c882-122"><span id="MPCALLBACK_HEALTH"></span><span id="mpcallback_health"></span>**MPCALLBACK\_HEALTH**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1c882-123"><span id="MPCALLBACK_ENDOFLIFE"></span><span id="mpcallback_endoflife"></span>**MPCALLBACK \_ ENDOFLIFE**</span><span class="sxs-lookup"><span data-stu-id="1c882-123"><span id="MPCALLBACK_ENDOFLIFE"></span><span id="mpcallback_endoflife"></span>**MPCALLBACK\_ENDOFLIFE**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1c882-124"><span id="MPCALLBACK_MALWARETOAST"></span><span id="mpcallback_malwaretoast"></span>**MPCALLBACK \_ MALWARETOAST**</span><span class="sxs-lookup"><span data-stu-id="1c882-124"><span id="MPCALLBACK_MALWARETOAST"></span><span id="mpcallback_malwaretoast"></span>**MPCALLBACK\_MALWARETOAST**</span></span>
</dt> <dd></dd> <dt>

<span data-ttu-id="1c882-125"><span id="MPCALLBACK_MAXVALUE"></span><span id="mpcallback_maxvalue"></span>**MPCALLBACK \_ MAXVALUE**</span><span class="sxs-lookup"><span data-stu-id="1c882-125"><span id="MPCALLBACK_MAXVALUE"></span><span id="mpcallback_maxvalue"></span>**MPCALLBACK\_MAXVALUE**</span></span>
<span data-ttu-id="1c882-126"></dt> <dd></dd> </dl></span><span class="sxs-lookup"><span data-stu-id="1c882-126"></dt> <dd></dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="1c882-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1c882-127">Requirements</span></span>



| <span data-ttu-id="1c882-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="1c882-128">Requirement</span></span> | <span data-ttu-id="1c882-129">Value</span><span class="sxs-lookup"><span data-stu-id="1c882-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="1c882-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c882-130">Minimum supported client</span></span><br/> | <span data-ttu-id="1c882-131">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c882-131">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1c882-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1c882-132">Minimum supported server</span></span><br/> | <span data-ttu-id="1c882-133">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="1c882-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="1c882-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1c882-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="1c882-135"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="1c882-135"><dt>MpClient.h</dt></span></span> </dl> |



 

 





