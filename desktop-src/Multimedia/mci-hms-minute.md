---
title: Macro MCI_HMS_MINUTE (Mciapi. h)
description: La \_ macro MCI HMS \_ minute recupera el componente de minutos de un parámetro que contiene información de horas/minutos/segundos empaquetados (HMS).
ms.assetid: d083f769-9825-48cc-80f9-34ce3ef66ad6
keywords:
- MCI_HMS_MINUTE de macros de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 49c91d2dcb13ea6b206df2a0dbc0d6a2e7096e59
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104151129"
---
# <a name="mci_hms_minute-macro"></a><span data-ttu-id="b0cd6-104">HMS de la \_ macro de minuto de MCI \_</span><span class="sxs-lookup"><span data-stu-id="b0cd6-104">MCI\_HMS\_MINUTE macro</span></span>

<span data-ttu-id="b0cd6-105">La macro **MCI \_ HMS \_ minute** recupera el componente de minutos de un parámetro que contiene información de horas/minutos/segundos empaquetados (HMS).</span><span class="sxs-lookup"><span data-stu-id="b0cd6-105">The **MCI\_HMS\_MINUTE** macro retrieves the minutes component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0cd6-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0cd6-106">Syntax</span></span>


```C++
BYTE MCI_HMS_MINUTE(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="b0cd6-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0cd6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0cd6-108">*dwHMS*</span><span class="sxs-lookup"><span data-stu-id="b0cd6-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="b0cd6-109">Hora en formato HMS.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0cd6-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0cd6-110">Return value</span></span>

<span data-ttu-id="b0cd6-111">Devuelve el componente de minutos de la información de HMS especificada.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-111">Returns the minutes component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="b0cd6-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b0cd6-112">Remarks</span></span>

<span data-ttu-id="b0cd6-113">La hora en formato HMS se expresa como un valor **DWORD** con el byte menos significativo que contiene las horas, el siguiente byte menos significativo que contiene los minutos y el siguiente byte menos significativo que contiene los segundos.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="b0cd6-114">El byte más significativo no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b0cd6-114">The most significant byte is unused.</span></span>

<span data-ttu-id="b0cd6-115">La macro **MCI \_ HMS \_ minute** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b0cd6-115">The **MCI\_HMS\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_MINUTE(hms) ((BYTE)(((WORD)(hms)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="b0cd6-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0cd6-116">Requirements</span></span>



| <span data-ttu-id="b0cd6-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0cd6-117">Requirement</span></span> | <span data-ttu-id="b0cd6-118">Value</span><span class="sxs-lookup"><span data-stu-id="b0cd6-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b0cd6-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0cd6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b0cd6-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b0cd6-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b0cd6-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0cd6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b0cd6-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b0cd6-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b0cd6-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0cd6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0cd6-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0cd6-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0cd6-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0cd6-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0cd6-126">MCI</span><span class="sxs-lookup"><span data-stu-id="b0cd6-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b0cd6-127">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="b0cd6-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





