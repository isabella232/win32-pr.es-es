---
title: Macro MCI_TMSF_FRAME (Mciapi. h)
description: La \_ \_ macro de Frame TMSF de MCI recupera el componente de fotogramas de un parámetro que contiene información de pistas empaquetadas/minutos/segundos/marcos (TMSF).
ms.assetid: 1ba78d4f-4537-4955-abcc-842976b6b5b9
keywords:
- MCI_TMSF_FRAME de macros de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_TMSF_FRAME
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7c5a6620137aea397c3f1bc04ff7fe821666d837
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801340"
---
# <a name="mci_tmsf_frame-macro"></a><span data-ttu-id="b032e-104">\_TMSF de \_ Marcos MCI</span><span class="sxs-lookup"><span data-stu-id="b032e-104">MCI\_TMSF\_FRAME macro</span></span>

<span data-ttu-id="b032e-105">La macro de **\_ \_ Frame TMSF de MCI** recupera el componente de fotogramas de un parámetro que contiene información de pistas empaquetadas/minutos/segundos/marcos (TMSF).</span><span class="sxs-lookup"><span data-stu-id="b032e-105">The **MCI\_TMSF\_FRAME** macro retrieves the frames component from a parameter containing packed tracks/minutes/seconds/frames (TMSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b032e-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b032e-106">Syntax</span></span>


```C++
BYTE MCI_TMSF_FRAME(
   DWORD dwTMSF
);
```



## <a name="parameters"></a><span data-ttu-id="b032e-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b032e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b032e-108">*dwTMSF*</span><span class="sxs-lookup"><span data-stu-id="b032e-108">*dwTMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="b032e-109">Hora en formato TMSF.</span><span class="sxs-lookup"><span data-stu-id="b032e-109">Time in TMSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b032e-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b032e-110">Return value</span></span>

<span data-ttu-id="b032e-111">Devuelve el componente de marcos de la información de TMSF especificada.</span><span class="sxs-lookup"><span data-stu-id="b032e-111">Returns the frames component of the specified TMSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="b032e-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b032e-112">Remarks</span></span>

<span data-ttu-id="b032e-113">La hora en formato TMSF se expresa como un valor **DWORD** con el byte menos significativo que contiene pistas, el siguiente byte menos significativo que contiene los minutos, el siguiente byte menos significativo que contiene los segundos y el byte más significativo que contiene fotogramas.</span><span class="sxs-lookup"><span data-stu-id="b032e-113">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="b032e-114">La macro **MCI \_ TMSF \_ Frame** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b032e-114">The **MCI\_TMSF\_FRAME** macro is defined as follows:</span></span>


```C++
#define MCI_TMSF_FRAME(tmsf) ((BYTE)((tmsf) >> 24)) 
```



## <a name="requirements"></a><span data-ttu-id="b032e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b032e-115">Requirements</span></span>



| <span data-ttu-id="b032e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b032e-116">Requirement</span></span> | <span data-ttu-id="b032e-117">Value</span><span class="sxs-lookup"><span data-stu-id="b032e-117">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b032e-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b032e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b032e-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b032e-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b032e-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b032e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b032e-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b032e-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b032e-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b032e-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b032e-123"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b032e-123"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b032e-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="b032e-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b032e-125">MCI</span><span class="sxs-lookup"><span data-stu-id="b032e-125">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b032e-126">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="b032e-126">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





