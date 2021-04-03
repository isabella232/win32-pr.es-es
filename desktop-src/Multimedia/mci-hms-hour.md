---
title: Macro MCI_HMS_HOUR (Mciapi. h)
description: La \_ macro MCI HMS \_ hour recupera el componente de horas de un parámetro que contiene la información empaquetada en horas/minutos/segundos (HMS).
ms.assetid: 55968b2b-2bfe-48ac-a50f-5c8741d11e33
keywords:
- MCI_HMS_HOUR de macros de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_HMS_HOUR
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7ecab8b5de7712a9c1a5ebd5c0a4401b264d7ee
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104079751"
---
# <a name="mci_hms_hour-macro"></a><span data-ttu-id="b92e4-104">MCI \_ HMS \_ hour (macro)</span><span class="sxs-lookup"><span data-stu-id="b92e4-104">MCI\_HMS\_HOUR macro</span></span>

<span data-ttu-id="b92e4-105">La macro **MCI \_ HMS \_ hour** recupera el componente de horas de un parámetro que contiene la información empaquetada en horas/minutos/segundos (HMS).</span><span class="sxs-lookup"><span data-stu-id="b92e4-105">The **MCI\_HMS\_HOUR** macro retrieves the hours component from a parameter containing packed hours/minutes/seconds (HMS) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="b92e4-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b92e4-106">Syntax</span></span>


```C++
BYTE MCI_HMS_HOUR(
   DWORD dwHMS
);
```



## <a name="parameters"></a><span data-ttu-id="b92e4-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b92e4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b92e4-108">*dwHMS*</span><span class="sxs-lookup"><span data-stu-id="b92e4-108">*dwHMS*</span></span> 
</dt> <dd>

<span data-ttu-id="b92e4-109">Hora en formato HMS.</span><span class="sxs-lookup"><span data-stu-id="b92e4-109">Time in HMS format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b92e4-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b92e4-110">Return value</span></span>

<span data-ttu-id="b92e4-111">Devuelve el componente de horas de la información de HMS especificada.</span><span class="sxs-lookup"><span data-stu-id="b92e4-111">Returns the hours component of the specified HMS information.</span></span>

## <a name="remarks"></a><span data-ttu-id="b92e4-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b92e4-112">Remarks</span></span>

<span data-ttu-id="b92e4-113">La hora en formato HMS se expresa como un valor **DWORD** con el byte menos significativo que contiene las horas, el siguiente byte menos significativo que contiene los minutos y el siguiente byte menos significativo que contiene los segundos.</span><span class="sxs-lookup"><span data-stu-id="b92e4-113">Time in HMS format is expressed as a **DWORD** value with the least significant byte containing hours, the next least significant byte containing minutes, and the next least significant byte containing seconds.</span></span> <span data-ttu-id="b92e4-114">El byte más significativo no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="b92e4-114">The most significant byte is unused.</span></span>

<span data-ttu-id="b92e4-115">La macro **MCI \_ HMS \_ hour** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="b92e4-115">The **MCI\_HMS\_HOUR** macro is defined as follows:</span></span>


```C++
#define MCI_HMS_HOUR(hms) ((BYTE)(hms)) 
```



## <a name="requirements"></a><span data-ttu-id="b92e4-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b92e4-116">Requirements</span></span>



| <span data-ttu-id="b92e4-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="b92e4-117">Requirement</span></span> | <span data-ttu-id="b92e4-118">Value</span><span class="sxs-lookup"><span data-stu-id="b92e4-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b92e4-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b92e4-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b92e4-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b92e4-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="b92e4-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b92e4-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b92e4-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b92e4-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b92e4-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b92e4-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="b92e4-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="b92e4-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b92e4-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="b92e4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b92e4-126">MCI</span><span class="sxs-lookup"><span data-stu-id="b92e4-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="b92e4-127">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="b92e4-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





