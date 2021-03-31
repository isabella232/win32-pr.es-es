---
title: Enumeración MPRESOLVED_REASON (MpClient. h)
description: Posibles causas de la resolución de un error de corrección.
ms.assetid: 29E875D7-97DA-4129-AB71-B261CD0E682A
keywords:
- MPRESOLVED_REASON enumeración características de entorno heredado de Windows
- PMPRESOLVED_REASON el puntero de enumeración características de entorno heredado de Windows
topic_type:
- apiref
api_name:
- MPRESOLVED_REASON
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab31fc8b734852ccdf15278f535d916228b43976
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079537"
---
# <a name="mpresolved_reason-enumeration"></a><span data-ttu-id="c7b27-105">\_Enumeración de motivo de MPRESOLVED</span><span class="sxs-lookup"><span data-stu-id="c7b27-105">MPRESOLVED\_REASON enumeration</span></span>

<span data-ttu-id="c7b27-106">Posibles causas de la resolución de un error de corrección.</span><span class="sxs-lookup"><span data-stu-id="c7b27-106">Possible reasons for a remediation failure being resolved.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7b27-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7b27-107">Syntax</span></span>


```C++
typedef enum tagMPRESOLVED_REASON { 
  MPRESOLVED_REASON_UNKNOWN    = 0,
  MPRESOLVED_REASON_FULL_SCAN  = 1,
  MPRESOLVED_REASON_TIMED_OUT  = 2
} MPRESOLVED_REASON, *PMPRESOLVED_REASON;
```



## <a name="constants"></a><span data-ttu-id="c7b27-108">Constantes</span><span class="sxs-lookup"><span data-stu-id="c7b27-108">Constants</span></span>

<dl> <dt>

<span data-ttu-id="c7b27-109"><span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**\_motivo MPRESOLVED \_ desconocido**</span><span class="sxs-lookup"><span data-stu-id="c7b27-109"><span id="MPRESOLVED_REASON_UNKNOWN"></span><span id="mpresolved_reason_unknown"></span>**MPRESOLVED\_REASON\_UNKNOWN**</span></span>
</dt> <dd>

<span data-ttu-id="c7b27-110">En un estado de error.</span><span class="sxs-lookup"><span data-stu-id="c7b27-110">In an error state.</span></span>

</dd> <dt>

<span data-ttu-id="c7b27-111"><span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**\_ \_ examen completo del motivo de MPRESOLVED \_**</span><span class="sxs-lookup"><span data-stu-id="c7b27-111"><span id="MPRESOLVED_REASON_FULL_SCAN"></span><span id="mpresolved_reason_full_scan"></span>**MPRESOLVED\_REASON\_FULL\_SCAN**</span></span>
</dt> <dd>

<span data-ttu-id="c7b27-112">Se realizó un examen completo.</span><span class="sxs-lookup"><span data-stu-id="c7b27-112">A full scan was performed.</span></span>

</dd> <dt>

<span data-ttu-id="c7b27-113"><span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**se \_ \_ agotó el tiempo de \_ espera de MPRESOLVED**</span><span class="sxs-lookup"><span data-stu-id="c7b27-113"><span id="MPRESOLVED_REASON_TIMED_OUT"></span><span id="mpresolved_reason_timed_out"></span>**MPRESOLVED\_REASON\_TIMED\_OUT**</span></span>
</dt> <dd>

<span data-ttu-id="c7b27-114">Ha transcurrido el tiempo suficiente.</span><span class="sxs-lookup"><span data-stu-id="c7b27-114">Enough time has passed.</span></span> <span data-ttu-id="c7b27-115">El valor predeterminado es una semana.</span><span class="sxs-lookup"><span data-stu-id="c7b27-115">The default is one week.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c7b27-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c7b27-116">Requirements</span></span>



| <span data-ttu-id="c7b27-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c7b27-117">Requirement</span></span> | <span data-ttu-id="c7b27-118">Value</span><span class="sxs-lookup"><span data-stu-id="c7b27-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c7b27-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7b27-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c7b27-120">Solo aplicaciones de escritorio de Windows 8 \[\]</span><span class="sxs-lookup"><span data-stu-id="c7b27-120">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="c7b27-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="c7b27-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c7b27-122">Solo aplicaciones de escritorio de Windows Server 2012 \[\]</span><span class="sxs-lookup"><span data-stu-id="c7b27-122">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c7b27-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="c7b27-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c7b27-124"><dt>MpClient. h</dt></span><span class="sxs-lookup"><span data-stu-id="c7b27-124"><dt>MpClient.h</dt></span></span> </dl> |



 

 





