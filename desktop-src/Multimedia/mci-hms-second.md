---
title: Macro MCI_HMS_SECOND (Mciapi. h)
description: La \_ macro MCI HMS \_ Second recupera el componente de segundos de un parámetro que contiene información de horas/minutos/segundos empaquetados (HMS).
ms.assetid: b6895bec-524f-4345-ae65-e75168855df2
keywords:
- MCI_HMS_SECOND de macros de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 30b869141d6480ba0d986450ce950097ba240009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905623"
---
# <a name="mci_hms_second-macro"></a><span data-ttu-id="1cf1a-104">MCI \_ HMS \_ segunda macro</span><span class="sxs-lookup"><span data-stu-id="1cf1a-104">MCI\_HMS\_SECOND macro</span></span>

<span data-ttu-id="1cf1a-105">La macro **MCI \_ HMS \_ Second** recupera el componente de segundos de un parámetro que contiene información de horas/minutos/segundos empaquetados (HMS).</span><span class="sxs-lookup"><span data-stu-id="1cf1a-105">The **MCI\_HMS\_SECOND** macro retrieves the seconds component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="1cf1a-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1cf1a-106">Syntax</span></span>


```C++
BYTE MCI_HMS_SECOND(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="1cf1a-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1cf1a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1cf1a-108">*dwHMS*</span><span class="sxs-lookup"><span data-stu-id="1cf1a-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="1cf1a-109">Hora en formato HMS.</span><span class="sxs-lookup"><span data-stu-id="1cf1a-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1cf1a-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1cf1a-110">Return value</span></span>

<span data-ttu-id="1cf1a-111">Devuelve el componente de segundos de la información de HMS especificada.</span><span class="sxs-lookup"><span data-stu-id="1cf1a-111">Returns the seconds component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="1cf1a-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1cf1a-112">Remarks</span></span>

<span data-ttu-id="1cf1a-113">La hora en formato HMS se expresa como un valor **DWORD** con el byte menos significativo que contiene las horas, el siguiente byte menos significativo que contiene los minutos y el siguiente byte menos significativo que contiene los segundos.</span><span class="sxs-lookup"><span data-stu-id="1cf1a-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="1cf1a-114">El byte más significativo no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="1cf1a-114">The most significant byte is unused.</span></span>

<span data-ttu-id="1cf1a-115">La macro **MCI \_ HMS \_ Second** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="1cf1a-115">The **MCI\_HMS\_SECOND** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_SECOND(hms) ((BYTE)((hms) >> 16)) 
```



## <a name="requirements"></a><span data-ttu-id="1cf1a-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1cf1a-116">Requirements</span></span>



| <span data-ttu-id="1cf1a-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1cf1a-117">Requirement</span></span> | <span data-ttu-id="1cf1a-118">Value</span><span class="sxs-lookup"><span data-stu-id="1cf1a-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="1cf1a-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cf1a-119">Minimum supported client</span></span><br/> | <span data-ttu-id="1cf1a-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1cf1a-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="1cf1a-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1cf1a-121">Minimum supported server</span></span><br/> | <span data-ttu-id="1cf1a-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1cf1a-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="1cf1a-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1cf1a-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="1cf1a-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="1cf1a-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1cf1a-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="1cf1a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1cf1a-126">MCI</span><span class="sxs-lookup"><span data-stu-id="1cf1a-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="1cf1a-127">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="1cf1a-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





