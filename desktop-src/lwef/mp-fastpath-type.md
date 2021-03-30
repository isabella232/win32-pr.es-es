---
title: Enumeración MP_FASTPATH_TYPE (MpClient. h)
description: Tipo FastPath.
ms.assetid: BD72228F-DCC0-435E-A408-BD7FB02E55E1
keywords:
- MP_FASTPATH_TYPE enumeración características de entorno heredado de Windows
- PMP_FASTPATH_TYPE el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MP_FASTPATH_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e89db79c54b166a833369ff52e47473463e0a2b9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104150985"
---
# <a name="mp_fastpath_type-enumeration"></a><span data-ttu-id="26e0f-105">\_ \_ Enumeración de tipo FASTPATH MP</span><span class="sxs-lookup"><span data-stu-id="26e0f-105">MP\_FASTPATH\_TYPE enumeration</span></span>

<span data-ttu-id="26e0f-106">Tipo FastPath.</span><span class="sxs-lookup"><span data-stu-id="26e0f-106">FastPath type.</span></span>

## <a name="syntax"></a><span data-ttu-id="26e0f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="26e0f-107">Syntax</span></span>


```C++
typedef enum tagMP_FASTPATH_TYPE { 
  MP_FASTPATH_UNKNOWN   = 0,
  MP_FASTPATH_VDM       = 1,
  MP_FASTPATH_DISABLED  = 2
} MP_FASTPATH_TYPE, *PMP_FASTPATH_TYPE;
```



## <a name="constants"></a><span data-ttu-id="26e0f-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="26e0f-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="26e0f-109"><span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**FASTPATH de MP \_ \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="26e0f-109"><span id="MP_FASTPATH_UNKNOWN"></span><span id="mp_fastpath_unknown"></span>**MP\_FASTPATH\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="26e0f-110">Desconocido.</span><span class="sxs-lookup"><span data-stu-id="26e0f-110">Unknown.</span></span>

</dd> <dt>

<span data-ttu-id="26e0f-111"><span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**\_VDM FASTPATH \_ MP**</span><span class="sxs-lookup"><span data-stu-id="26e0f-111"><span id="MP_FASTPATH_VDM"></span><span id="mp_fastpath_vdm"></span>**MP\_FASTPATH\_VDM**</span></span>
</dt> <dd>

<span data-ttu-id="26e0f-112">Actualización de VDM.</span><span class="sxs-lookup"><span data-stu-id="26e0f-112">VDM update.</span></span>

</dd> <dt>

<span data-ttu-id="26e0f-113"><span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**\_FASTPATH MP \_ deshabilitado**</span><span class="sxs-lookup"><span data-stu-id="26e0f-113"><span id="MP_FASTPATH_DISABLED"></span><span id="mp_fastpath_disabled"></span>**MP\_FASTPATH\_DISABLED**</span></span>
</dt> <dd>

<span data-ttu-id="26e0f-114">Notificación de deshabilitación de firma.</span><span class="sxs-lookup"><span data-stu-id="26e0f-114">Signature disable notification.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="26e0f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="26e0f-115">Requirements</span></span>



| <span data-ttu-id="26e0f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="26e0f-116">Requirement</span></span> | <span data-ttu-id="26e0f-117">Value</span><span class="sxs-lookup"><span data-stu-id="26e0f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="26e0f-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26e0f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="26e0f-119">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="26e0f-119">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="26e0f-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="26e0f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="26e0f-121">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="26e0f-121">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="26e0f-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="26e0f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="26e0f-123"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="26e0f-123"><dt>MpClient.h</dt></span></span> </dl> |



 

 





