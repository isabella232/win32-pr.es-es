---
title: Macro MCI_TMSF_TRACK (Mciapi. h)
description: La \_ macro MCI TMSF \_ Track recupera el componente tracks de un parámetro que contiene información de pistas empaquetadas/minutos/segundos/marcos (TMSF).
ms.assetid: 3455442c-5c66-47c7-b06b-1a2de0e2dfed
keywords:
- MCI_TMSF_TRACK de macros de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_TRACK
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8512169d0e5b3d6892dd1bf615a220143e6d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905306"
---
# <a name="mci_tmsf_track-macro"></a><span data-ttu-id="17b1c-104">\_Macro MCI TMSF \_ Track</span><span class="sxs-lookup"><span data-stu-id="17b1c-104">MCI\_TMSF\_TRACK macro</span></span>

<span data-ttu-id="17b1c-105">La macro **MCI \_ TMSF \_ Track** recupera el componente tracks de un parámetro que contiene información de pistas empaquetadas/minutos/segundos/marcos (TMSF).</span><span class="sxs-lookup"><span data-stu-id="17b1c-105">The **MCI\_TMSF\_TRACK** macro retrieves the tracks component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="17b1c-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="17b1c-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_TRACK(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="17b1c-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="17b1c-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17b1c-108">*dwTMSF*</span><span class="sxs-lookup"><span data-stu-id="17b1c-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="17b1c-109">Hora en formato TMSF.</span><span class="sxs-lookup"><span data-stu-id="17b1c-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17b1c-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="17b1c-110">Return value</span></span>

<span data-ttu-id="17b1c-111">Devuelve el componente de seguimientos de la información de TMSF especificada.</span><span class="sxs-lookup"><span data-stu-id="17b1c-111">Returns the tracks component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="17b1c-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="17b1c-112">Remarks</span></span>

<span data-ttu-id="17b1c-113">La hora en formato TMSF se expresa como un valor **DWORD** con el byte menos significativo que contiene pistas, el siguiente byte menos significativo que contiene los minutos, el siguiente byte menos significativo que contiene los segundos y el byte más significativo que contiene fotogramas.</span><span class="sxs-lookup"><span data-stu-id="17b1c-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="17b1c-114">La macro **MCI \_ TMSF \_ Track** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="17b1c-114">The **MCI\_TMSF\_TRACK** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_TRACK(tmsf) ((BYTE)(tmsf)) 
```



## <a name="requirements"></a><span data-ttu-id="17b1c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17b1c-115">Requirements</span></span>



| <span data-ttu-id="17b1c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="17b1c-116">Requirement</span></span> | <span data-ttu-id="17b1c-117">Value</span><span class="sxs-lookup"><span data-stu-id="17b1c-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="17b1c-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17b1c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="17b1c-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="17b1c-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="17b1c-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="17b1c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="17b1c-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="17b1c-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="17b1c-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="17b1c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="17b1c-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="17b1c-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17b1c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="17b1c-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17b1c-125">MCI</span><span class="sxs-lookup"><span data-stu-id="17b1c-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="17b1c-126">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="17b1c-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





