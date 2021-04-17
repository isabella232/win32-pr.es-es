---
title: Macro MCI_MAKE_TMSF (Mciapi. h)
description: La macro de TMSF de MCI \_ \_ crea un valor de hora en el formato empaquetado de pistas/minutos/segundos/marcos (TMSF) a partir de los valores de las pistas, los minutos, los segundos y los marcos especificados.
ms.assetid: ff2d6938-0ff7-46d5-92be-42b4b6f35524
keywords:
- MCI_MAKE_TMSF de macros de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_TMSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f06cd6a400f742b49dc29063e8473465ad7e32dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676984"
---
# <a name="mci_make_tmsf-macro"></a><span data-ttu-id="41468-104">\_TMSF de creación de \_ macros</span><span class="sxs-lookup"><span data-stu-id="41468-104">MCI\_MAKE\_TMSF macro</span></span>

<span data-ttu-id="41468-105">La macro de **\_ \_ TMSF de MCI** crea un valor de hora en el formato empaquetado de pistas/minutos/segundos/marcos (TMSF) a partir de los valores de las pistas, los minutos, los segundos y los marcos especificados.</span><span class="sxs-lookup"><span data-stu-id="41468-105">The **MCI\_MAKE\_TMSF** macro creates a time value in packed tracks/minutes/seconds/frames (TMSF) format from the given tracks, minutes, seconds, and frames values.</span></span>

## <a name="syntax"></a><span data-ttu-id="41468-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="41468-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_TMSF(
   BYTE tracks,
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a><span data-ttu-id="41468-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="41468-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="41468-108">*realiza*</span><span class="sxs-lookup"><span data-stu-id="41468-108">*tracks*</span></span> 
</dt> <dd>

<span data-ttu-id="41468-109">Número de pistas.</span><span class="sxs-lookup"><span data-stu-id="41468-109">Number of tracks.</span></span>

</dd> <dt>

<span data-ttu-id="41468-110">*minutes*</span><span class="sxs-lookup"><span data-stu-id="41468-110">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="41468-111">Número de minutos.</span><span class="sxs-lookup"><span data-stu-id="41468-111">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="41468-112">*segundos*</span><span class="sxs-lookup"><span data-stu-id="41468-112">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="41468-113">Número de segundos.</span><span class="sxs-lookup"><span data-stu-id="41468-113">Number of seconds.</span></span>

</dd> <dt>

<span data-ttu-id="41468-114">*marcos*</span><span class="sxs-lookup"><span data-stu-id="41468-114">*frames*</span></span> 
</dt> <dd>

<span data-ttu-id="41468-115">Número de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="41468-115">Number of frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="41468-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="41468-116">Return value</span></span>

<span data-ttu-id="41468-117">Devuelve la hora en formato TMSF empaquetado.</span><span class="sxs-lookup"><span data-stu-id="41468-117">Returns the time in packed TMSF format.</span></span>

## <a name="remarks"></a><span data-ttu-id="41468-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="41468-118">Remarks</span></span>

<span data-ttu-id="41468-119">La hora en formato TMSF se expresa como un valor **DWORD** con el byte menos significativo que contiene pistas, el siguiente byte menos significativo que contiene los minutos, el siguiente byte menos significativo que contiene los segundos y el byte más significativo que contiene fotogramas.</span><span class="sxs-lookup"><span data-stu-id="41468-119">Time in TMSF format is expressed as a **DWORD** value with the least significant byte containing tracks, the next least significant byte containing minutes, the next least significant byte containing seconds, and the most significant byte containing frames.</span></span>

<span data-ttu-id="41468-120">La macro **MCI \_ Make \_ TMSF** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="41468-120">The **MCI\_MAKE\_TMSF** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_TMSF(t, m, s, f) ((DWORD)(((BYTE)(t) | \ 
                                  ((WORD)(m) << 8)) | \ 
                                  (((DWORD)(BYTE)(s) | \ 
                                  ((WORD)(f) << 8)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="41468-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="41468-121">Requirements</span></span>



| <span data-ttu-id="41468-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="41468-122">Requirement</span></span> | <span data-ttu-id="41468-123">Value</span><span class="sxs-lookup"><span data-stu-id="41468-123">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="41468-124">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41468-124">Minimum supported client</span></span><br/> | <span data-ttu-id="41468-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="41468-125">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="41468-126">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="41468-126">Minimum supported server</span></span><br/> | <span data-ttu-id="41468-127">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="41468-127">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="41468-128">Encabezado</span><span class="sxs-lookup"><span data-stu-id="41468-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="41468-129"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="41468-129"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41468-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="41468-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41468-131">MCI</span><span class="sxs-lookup"><span data-stu-id="41468-131">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="41468-132">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="41468-132">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





