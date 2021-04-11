---
description: Define los diferentes Estados preparados de la extensión de origen multimedia.
ms.assetid: 7455B92F-CC2D-4743-935D-F5EBFD834397
title: Enumeración MF_MSE_READY
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MF_MSE_READY
api_type:
- HeaderDef
api_location:
- mfmediaengine.h
ms.openlocfilehash: bff2155a2cb2cb21d4c25d868f95472f47f15b1a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103910202"
---
# <a name="mf_mse_ready-enumeration"></a><span data-ttu-id="23a95-103">\_ \_ Enumeración preparada para MSE de MF</span><span class="sxs-lookup"><span data-stu-id="23a95-103">MF\_MSE\_READY enumeration</span></span>

<span data-ttu-id="23a95-104">Define los diferentes Estados preparados de la extensión de origen multimedia.</span><span class="sxs-lookup"><span data-stu-id="23a95-104">Defines the different ready states of the Media Source Extension.</span></span>

## <a name="syntax"></a><span data-ttu-id="23a95-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="23a95-105">Syntax</span></span>


```C++
typedef enum _MF_MSE_READY { 
  MF_MSE_READY_CLOSED  = 1,
  MF_MSE_READY_OPEN    = 2,
  MF_MSE_READY_ENDED   = 3
} MF_MSE_READY;
```



## <a name="constants"></a><span data-ttu-id="23a95-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="23a95-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="23a95-107"><span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF \_ MSE \_ preparado \_ cerrado**</span><span class="sxs-lookup"><span data-stu-id="23a95-107"><span id="MF_MSE_READY_CLOSED"></span><span id="mf_mse_ready_closed"></span>**MF\_MSE\_READY\_CLOSED**</span></span>
</dt> <dd>

<span data-ttu-id="23a95-108">El origen del medio está cerrado.</span><span class="sxs-lookup"><span data-stu-id="23a95-108">The media source is closed.</span></span>

</dd> <dt>

<span data-ttu-id="23a95-109"><span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**MF \_ MSE \_ listo \_ abierto**</span><span class="sxs-lookup"><span data-stu-id="23a95-109"><span id="MF_MSE_READY_OPEN"></span><span id="mf_mse_ready_open"></span>**MF\_MSE\_READY\_OPEN**</span></span>
</dt> <dd>

<span data-ttu-id="23a95-110">El origen del medio está abierto.</span><span class="sxs-lookup"><span data-stu-id="23a95-110">The media source is open.</span></span>

</dd> <dt>

<span data-ttu-id="23a95-111"><span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**MF \_ MSE \_ preparado \_ terminado**</span><span class="sxs-lookup"><span data-stu-id="23a95-111"><span id="MF_MSE_READY_ENDED"></span><span id="mf_mse_ready_ended"></span>**MF\_MSE\_READY\_ENDED**</span></span>
</dt> <dd>

<span data-ttu-id="23a95-112">El origen de los medios ha finalizado.</span><span class="sxs-lookup"><span data-stu-id="23a95-112">The media source is ended.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="23a95-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="23a95-113">Requirements</span></span>



| <span data-ttu-id="23a95-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="23a95-114">Requirement</span></span> | <span data-ttu-id="23a95-115">Value</span><span class="sxs-lookup"><span data-stu-id="23a95-115">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------|
| <span data-ttu-id="23a95-116">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23a95-116">Minimum supported client</span></span><br/> | <span data-ttu-id="23a95-117">\[Solo aplicaciones de escritorio Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="23a95-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="23a95-118">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="23a95-118">Minimum supported server</span></span><br/> | <span data-ttu-id="23a95-119">Solo aplicaciones de escritorio de Windows Server 2012 R2 \[\]</span><span class="sxs-lookup"><span data-stu-id="23a95-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="23a95-120">IDL</span><span class="sxs-lookup"><span data-stu-id="23a95-120">IDL</span></span><br/>                      | <dl> <span data-ttu-id="23a95-121"><dt>Mfmediaengine. idl</dt></span><span class="sxs-lookup"><span data-stu-id="23a95-121"><dt>Mfmediaengine.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="23a95-122">Vea también</span><span class="sxs-lookup"><span data-stu-id="23a95-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23a95-123">Enumeraciones de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="23a95-123">Media Foundation Enumerations</span></span>](media-foundation-enumerations.md)
</dt> </dl>

 

 




