---
title: Enumeración MPTHREAT_TYPE (MpClient. h)
description: Posibles tipos de amenaza.
ms.assetid: 56061F12-AA89-4203-BED4-99613E24002A
keywords:
- MPTHREAT_TYPE enumeración características de entorno heredado de Windows
- PMPTHREAT_TYPE el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPTHREAT_TYPE
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8ed823b100c91f259252d7cad71e554099caf6a2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422187"
---
# <a name="mpthreat_type-enumeration"></a><span data-ttu-id="6af3f-105">\_Enumeración de tipo MPTHREAT</span><span class="sxs-lookup"><span data-stu-id="6af3f-105">MPTHREAT\_TYPE enumeration</span></span>

<span data-ttu-id="6af3f-106">Posibles tipos de amenaza.</span><span class="sxs-lookup"><span data-stu-id="6af3f-106">Possible threat types.</span></span>

## <a name="syntax"></a><span data-ttu-id="6af3f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="6af3f-107">Syntax</span></span>


```C++
typedef enum tagMPTHREAT_TYPE { 
  MPTHREAT_TYPE_KNOWNBAD   = 0,
  MPTHREAT_TYPE_BEHAVIOR   = 1,
  MPTHREAT_TYPE_UNKNOWN    = 2,
  MPTHREAT_TYPE_KNOWNGOOD  = 3,
  MPTHREAT_TYPE_NIS        = 4,
  MPTHREAT_TYPE_MAXVALUE   = 4
} MPTHREAT_TYPE, *PMPTHREAT_TYPE;
```



## <a name="constants"></a><span data-ttu-id="6af3f-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="6af3f-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="6af3f-109"><span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**MPTHREAT \_ Type \_ KNOWNBAD**</span><span class="sxs-lookup"><span data-stu-id="6af3f-109"><span id="MPTHREAT_TYPE_KNOWNBAD"></span><span id="mpthreat_type_knownbad"></span>**MPTHREAT\_TYPE\_KNOWNBAD**</span></span>
</dt> <dd>

<span data-ttu-id="6af3f-110">Amenaza desconocida detectada a través de la firma.</span><span class="sxs-lookup"><span data-stu-id="6af3f-110">Known bad threat detected via signature.</span></span>

</dd> <dt>

<span data-ttu-id="6af3f-111"><span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**\_comportamiento del tipo MPTHREAT \_**</span><span class="sxs-lookup"><span data-stu-id="6af3f-111"><span id="MPTHREAT_TYPE_BEHAVIOR"></span><span id="mpthreat_type_behavior"></span>**MPTHREAT\_TYPE\_BEHAVIOR**</span></span>
</dt> <dd>

<span data-ttu-id="6af3f-112">Amenaza sospechosa detectada a través de la supervisión del comportamiento.</span><span class="sxs-lookup"><span data-stu-id="6af3f-112">Suspicious threat detected via behavior monitoring.</span></span>

</dd> <dt>

<span data-ttu-id="6af3f-113"><span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**\_tipo MPTHREAT \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="6af3f-113"><span id="MPTHREAT_TYPE_UNKNOWN"></span><span id="mpthreat_type_unknown"></span>**MPTHREAT\_TYPE\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="6af3f-114">Amenazas desconocidas (sin clasificar).</span><span class="sxs-lookup"><span data-stu-id="6af3f-114">Unknown threats (unclassified).</span></span>

</dd> <dt>

<span data-ttu-id="6af3f-115"><span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**MPTHREAT \_ Type \_ KNOWNGOOD**</span><span class="sxs-lookup"><span data-stu-id="6af3f-115"><span id="MPTHREAT_TYPE_KNOWNGOOD"></span><span id="mpthreat_type_knowngood"></span>**MPTHREAT\_TYPE\_KNOWNGOOD**</span></span>
</dt> <dd>

<span data-ttu-id="6af3f-116">Amenaza buena conocida.</span><span class="sxs-lookup"><span data-stu-id="6af3f-116">Known good threat.</span></span>

</dd> <dt>

<span data-ttu-id="6af3f-117"><span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT \_ tipo \_ NIS**</span><span class="sxs-lookup"><span data-stu-id="6af3f-117"><span id="MPTHREAT_TYPE_NIS"></span><span id="mpthreat_type_nis"></span>**MPTHREAT\_TYPE\_NIS**</span></span>
</dt> <dd>

<span data-ttu-id="6af3f-118">Detección de amenazas de NIS.</span><span class="sxs-lookup"><span data-stu-id="6af3f-118">NIS threat detection.</span></span>

</dd> <dt>

<span data-ttu-id="6af3f-119"><span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**MPTHREAT \_ tipo \_ MAXVALUE**</span><span class="sxs-lookup"><span data-stu-id="6af3f-119"><span id="MPTHREAT_TYPE_MAXVALUE"></span><span id="mpthreat_type_maxvalue"></span>**MPTHREAT\_TYPE\_MAXVALUE**</span></span>
</dt> <dd>

<span data-ttu-id="6af3f-120">Valor máximo posible.</span><span class="sxs-lookup"><span data-stu-id="6af3f-120">Maximum value possible.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="6af3f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6af3f-121">Requirements</span></span>



| <span data-ttu-id="6af3f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="6af3f-122">Requirement</span></span> | <span data-ttu-id="6af3f-123">Value</span><span class="sxs-lookup"><span data-stu-id="6af3f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6af3f-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6af3f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6af3f-125">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="6af3f-125">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="6af3f-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="6af3f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6af3f-127">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="6af3f-127">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="6af3f-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="6af3f-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="6af3f-129"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="6af3f-129"><dt>MpClient.h</dt></span></span> </dl> |



 

 





