---
title: Macro MCI_MSF_SECOND (Mciapi. h)
description: La \_ macro MCI MSF \_ Second recupera el componente de segundos de un parámetro que contiene la información empaquetada en minutos/segundos/marcos (MSF).
ms.assetid: 2d455ce3-1823-46fa-a59e-b9c5c2fe5eb9
keywords:
- MCI_MSF_SECOND de macros de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_MSF_SECOND
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 85dffd36354b335818079ea5b0c88d16752b4501
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103905334"
---
# <a name="mci_msf_second-macro"></a><span data-ttu-id="70f0d-104">Macro MCI de \_ MSF \_ Second</span><span class="sxs-lookup"><span data-stu-id="70f0d-104">MCI\_MSF\_SECOND macro</span></span>

<span data-ttu-id="70f0d-105">La macro **MCI \_ MSF \_ Second** recupera el componente de segundos de un parámetro que contiene la información empaquetada en minutos/segundos/marcos (MSF).</span><span class="sxs-lookup"><span data-stu-id="70f0d-105">The **MCI\_MSF\_SECOND** macro retrieves the seconds component from a parameter containing packed minutes/seconds/frames (MSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="70f0d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="70f0d-106">Syntax</span></span>


```C++
BYTE MCI_MSF_SECOND(
   DWORD dwMSF
);
```



## <a name="parameters"></a><span data-ttu-id="70f0d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="70f0d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="70f0d-108">*dwMSF*</span><span class="sxs-lookup"><span data-stu-id="70f0d-108">*dwMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="70f0d-109">Hora en formato MSF.</span><span class="sxs-lookup"><span data-stu-id="70f0d-109">Time in MSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="70f0d-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="70f0d-110">Return value</span></span>

<span data-ttu-id="70f0d-111">Devuelve el componente de segundos de la información especificada de MSF.</span><span class="sxs-lookup"><span data-stu-id="70f0d-111">Returns the seconds component of the specified MSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="70f0d-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="70f0d-112">Remarks</span></span>

<span data-ttu-id="70f0d-113">La hora en formato MSF se expresa como un valor **DWORD** con el byte menos significativo que contiene los minutos, el siguiente byte menos significativo que contiene los segundos y el siguiente byte menos significativo que contiene fotogramas.</span><span class="sxs-lookup"><span data-stu-id="70f0d-113">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="70f0d-114">El byte más significativo no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="70f0d-114">The most significant byte is unused.</span></span>

<span data-ttu-id="70f0d-115">La macro **MCI \_ MSF \_ Second** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="70f0d-115">The **MCI\_MSF\_SECOND** macro is defined as follows:</span></span>


```C++
#define MCI_MSF_SECOND(msf) ((BYTE)(((WORD)(msf)) >> 8)) 
```



## <a name="requirements"></a><span data-ttu-id="70f0d-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="70f0d-116">Requirements</span></span>



| <span data-ttu-id="70f0d-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="70f0d-117">Requirement</span></span> | <span data-ttu-id="70f0d-118">Value</span><span class="sxs-lookup"><span data-stu-id="70f0d-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="70f0d-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70f0d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="70f0d-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="70f0d-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="70f0d-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="70f0d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="70f0d-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="70f0d-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="70f0d-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="70f0d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="70f0d-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="70f0d-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="70f0d-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="70f0d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="70f0d-126">MCI</span><span class="sxs-lookup"><span data-stu-id="70f0d-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="70f0d-127">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="70f0d-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





