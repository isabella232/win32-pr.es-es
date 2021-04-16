---
title: Macro MCI_MSF_MINUTE (Mciapi. h)
description: La \_ macro MCI \_ -minute de MSF recupera el componente de minutos de un parámetro que contiene información empaquetada en minutos/segundos/marcos (MSF).
ms.assetid: 60ac6662-d828-4635-a019-2603199523c5
keywords:
- MCI_MSF_MINUTE de macros de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_MSF_MINUTE
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f65f978c13fc1b3fbf86266c35786b21612c4e7c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105651418"
---
# <a name="mci_msf_minute-macro"></a><span data-ttu-id="29ecd-104">Macro MCI- \_ minute de MSF \_</span><span class="sxs-lookup"><span data-stu-id="29ecd-104">MCI\_MSF\_MINUTE macro</span></span>

<span data-ttu-id="29ecd-105">La macro **MCI- \_ \_ minute de MSF** recupera el componente de minutos de un parámetro que contiene información empaquetada en minutos/segundos/marcos (MSF).</span><span class="sxs-lookup"><span data-stu-id="29ecd-105">The **MCI\_MSF\_MINUTE** macro retrieves the minutes component from a parameter containing packed minutes/seconds/frames (MSF) information.</span></span>

## <a name="syntax"></a><span data-ttu-id="29ecd-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="29ecd-106">Syntax</span></span>


```C++
BYTE MCI_MSF_MINUTE(
   DWORD dwMSF
);
```



## <a name="parameters"></a><span data-ttu-id="29ecd-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="29ecd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="29ecd-108">*dwMSF*</span><span class="sxs-lookup"><span data-stu-id="29ecd-108">*dwMSF*</span></span> 
</dt> <dd>

<span data-ttu-id="29ecd-109">Hora en formato MSF.</span><span class="sxs-lookup"><span data-stu-id="29ecd-109">Time in MSF format.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="29ecd-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="29ecd-110">Return value</span></span>

<span data-ttu-id="29ecd-111">Devuelve el componente de minutos de la información de MSF especificada.</span><span class="sxs-lookup"><span data-stu-id="29ecd-111">Returns the minutes component of the specified MSF information.</span></span>

## <a name="remarks"></a><span data-ttu-id="29ecd-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="29ecd-112">Remarks</span></span>

<span data-ttu-id="29ecd-113">La hora en formato MSF se expresa como un valor **DWORD** con el byte menos significativo que contiene los minutos, el siguiente byte menos significativo que contiene los segundos y el siguiente byte menos significativo que contiene fotogramas.</span><span class="sxs-lookup"><span data-stu-id="29ecd-113">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="29ecd-114">El byte más significativo no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="29ecd-114">The most significant byte is unused.</span></span>

<span data-ttu-id="29ecd-115">La macro **MCI de \_ MSF \_ minute** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="29ecd-115">The **MCI\_MSF\_MINUTE** macro is defined as follows:</span></span>


```C++
#define MCI_MSF_MINUTE(msf) ((BYTE)(msf)) 
```



## <a name="requirements"></a><span data-ttu-id="29ecd-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="29ecd-116">Requirements</span></span>



| <span data-ttu-id="29ecd-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="29ecd-117">Requirement</span></span> | <span data-ttu-id="29ecd-118">Value</span><span class="sxs-lookup"><span data-stu-id="29ecd-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="29ecd-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29ecd-119">Minimum supported client</span></span><br/> | <span data-ttu-id="29ecd-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="29ecd-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="29ecd-121">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="29ecd-121">Minimum supported server</span></span><br/> | <span data-ttu-id="29ecd-122">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="29ecd-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="29ecd-123">Encabezado</span><span class="sxs-lookup"><span data-stu-id="29ecd-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="29ecd-124"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="29ecd-124"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29ecd-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="29ecd-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29ecd-126">MCI</span><span class="sxs-lookup"><span data-stu-id="29ecd-126">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="29ecd-127">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="29ecd-127">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





