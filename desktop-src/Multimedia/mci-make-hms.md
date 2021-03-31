---
title: Macro MCI_MAKE_HMS (Mciapi. h)
description: La \_ macro MCI make \_ HMS crea un valor de hora en formato de horas, minutos y segundos empaquetados (HMS) a partir de los valores de horas, minutos y segundos determinados.
ms.assetid: 470e89eb-36e1-4b05-babd-4c986adc88dd
keywords:
- MCI_MAKE_HMS de macros de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_HMS
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f37c95df89ed6a799575e964ae274e01e329ef1c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103803506"
---
# <a name="mci_make_hms-macro"></a><span data-ttu-id="8961f-104">\_HMS de creación de \_ macros</span><span class="sxs-lookup"><span data-stu-id="8961f-104">MCI\_MAKE\_HMS macro</span></span>

<span data-ttu-id="8961f-105">La macro **MCI \_ Make \_ HMS** crea un valor de hora en formato de horas, minutos y segundos empaquetados (HMS) a partir de los valores de horas, minutos y segundos determinados.</span><span class="sxs-lookup"><span data-stu-id="8961f-105">The **MCI\_MAKE\_HMS** macro creates a time value in packed hours/minutes/seconds (HMS) format from the given hours, minutes, and seconds values.</span></span>

## <a name="syntax"></a><span data-ttu-id="8961f-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="8961f-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_HMS(
   BYTE hours,
   BYTE minutes,
   BYTE seconds
);
```



## <a name="parameters"></a><span data-ttu-id="8961f-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8961f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8961f-108">*hours*</span><span class="sxs-lookup"><span data-stu-id="8961f-108">*hours*</span></span> 
</dt> <dd>

<span data-ttu-id="8961f-109">Número de horas.</span><span class="sxs-lookup"><span data-stu-id="8961f-109">Number of hours.</span></span>

</dd> <dt>

<span data-ttu-id="8961f-110">*minutes*</span><span class="sxs-lookup"><span data-stu-id="8961f-110">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="8961f-111">Número de minutos.</span><span class="sxs-lookup"><span data-stu-id="8961f-111">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="8961f-112">*segundos*</span><span class="sxs-lookup"><span data-stu-id="8961f-112">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="8961f-113">Número de segundos.</span><span class="sxs-lookup"><span data-stu-id="8961f-113">Number of seconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8961f-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8961f-114">Return value</span></span>

<span data-ttu-id="8961f-115">Devuelve la hora en formato HMS empaquetado.</span><span class="sxs-lookup"><span data-stu-id="8961f-115">Returns the time in packed HMS format.</span></span>

## <a name="remarks"></a><span data-ttu-id="8961f-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="8961f-116">Remarks</span></span>

<span data-ttu-id="8961f-117">La hora en formato HMS se expresa como un valor **DWORD** con el byte menos significativo que contiene las horas, el siguiente byte menos significativo que contiene los minutos y el siguiente byte menos significativo que contiene los segundos.</span><span class="sxs-lookup"><span data-stu-id="8961f-117">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="8961f-118">El byte más significativo no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="8961f-118">The most significant byte is unused.</span></span>

<span data-ttu-id="8961f-119">La macro **MCI \_ Make \_ HMS** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="8961f-119">The **MCI\_MAKE\_HMS** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_HMS(h, m, s) ((DWORD)(((BYTE)(h) | \ 
                              ((WORD)(m) << 8)) | \ 
                              (((DWORD)(BYTE)(s)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="8961f-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8961f-120">Requirements</span></span>



| <span data-ttu-id="8961f-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="8961f-121">Requirement</span></span> | <span data-ttu-id="8961f-122">Value</span><span class="sxs-lookup"><span data-stu-id="8961f-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="8961f-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8961f-123">Minimum supported client</span></span><br/> | <span data-ttu-id="8961f-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="8961f-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="8961f-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="8961f-125">Minimum supported server</span></span><br/> | <span data-ttu-id="8961f-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="8961f-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="8961f-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="8961f-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="8961f-128"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="8961f-128"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8961f-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="8961f-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8961f-130">MCI</span><span class="sxs-lookup"><span data-stu-id="8961f-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="8961f-131">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="8961f-131">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





