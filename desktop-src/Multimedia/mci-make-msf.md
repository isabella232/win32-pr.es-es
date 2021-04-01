---
title: Macro MCI_MAKE_MSF (Mciapi. h)
description: La \_ macro MCI make de \_ MSF crea un valor de hora en formato empaquetado de minutos/segundos/marcos (MSF) a partir de los minutos, los segundos y los valores de fotogramas dados.
ms.assetid: 8c981d84-b049-4448-a820-bff30896065e
keywords:
- MCI_MAKE_MSF de macros de Windows multimedia
topic_type:
- apiref
api_name:
- MCI_MAKE_MSF
api_location:
- mciapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae7e8566986337d6b9b5161c85bcc62cecc52be0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103997085"
---
# <a name="mci_make_msf-macro"></a><span data-ttu-id="dca4d-104">\_Crear una \_ macro de MSF en MCI</span><span class="sxs-lookup"><span data-stu-id="dca4d-104">MCI\_MAKE\_MSF macro</span></span>

<span data-ttu-id="dca4d-105">La macro **MCI \_ Make de \_ MSF** crea un valor de hora en formato empaquetado de minutos/segundos/marcos (MSF) a partir de los minutos, los segundos y los valores de fotogramas dados.</span><span class="sxs-lookup"><span data-stu-id="dca4d-105">The **MCI\_MAKE\_MSF** macro creates a time value in packed minutes/seconds/frames (MSF) format from the given minutes, seconds, and frame values.</span></span>

## <a name="syntax"></a><span data-ttu-id="dca4d-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="dca4d-106">Syntax</span></span>


```C++
DWORD MCI_MAKE_MSF(
   BYTE minutes,
   BYTE seconds,
   BYTE frames
);
```



## <a name="parameters"></a><span data-ttu-id="dca4d-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="dca4d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dca4d-108">*minutes*</span><span class="sxs-lookup"><span data-stu-id="dca4d-108">*minutes*</span></span> 
</dt> <dd>

<span data-ttu-id="dca4d-109">Número de minutos.</span><span class="sxs-lookup"><span data-stu-id="dca4d-109">Number of minutes.</span></span>

</dd> <dt>

<span data-ttu-id="dca4d-110">*segundos*</span><span class="sxs-lookup"><span data-stu-id="dca4d-110">*seconds*</span></span> 
</dt> <dd>

<span data-ttu-id="dca4d-111">Número de segundos.</span><span class="sxs-lookup"><span data-stu-id="dca4d-111">Number of seconds.</span></span>

</dd> <dt>

<span data-ttu-id="dca4d-112">*marcos*</span><span class="sxs-lookup"><span data-stu-id="dca4d-112">*frames*</span></span> 
</dt> <dd>

<span data-ttu-id="dca4d-113">Número de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="dca4d-113">Number of frames.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dca4d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="dca4d-114">Return value</span></span>

<span data-ttu-id="dca4d-115">Devuelve la hora en formato de MSF empaquetado.</span><span class="sxs-lookup"><span data-stu-id="dca4d-115">Returns the time in packed MSF format.</span></span>

## <a name="remarks"></a><span data-ttu-id="dca4d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="dca4d-116">Remarks</span></span>

<span data-ttu-id="dca4d-117">La hora en formato MSF se expresa como un valor **DWORD** con el byte menos significativo que contiene los minutos, el siguiente byte menos significativo que contiene los segundos y el siguiente byte menos significativo que contiene fotogramas.</span><span class="sxs-lookup"><span data-stu-id="dca4d-117">Time in MSF format is expressed as a **DWORD** value with the least significant byte containing minutes, the next least significant byte containing seconds, and the next least significant byte containing frames.</span></span> <span data-ttu-id="dca4d-118">El byte más significativo no se utiliza.</span><span class="sxs-lookup"><span data-stu-id="dca4d-118">The most significant byte is unused.</span></span>

<span data-ttu-id="dca4d-119">La macro **MCI \_ Make de \_ MSF** se define de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="dca4d-119">The **MCI\_MAKE\_MSF** macro is defined as follows:</span></span>


```C++
#define MCI_MAKE_MSF(m, s, f) ((DWORD)(((BYTE)(m) | \ 
                              ((WORD)(s) << 8)) | \ 
                              (((DWORD)(BYTE)(f)) << 16))) 
```



## <a name="requirements"></a><span data-ttu-id="dca4d-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="dca4d-120">Requirements</span></span>



| <span data-ttu-id="dca4d-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="dca4d-121">Requirement</span></span> | <span data-ttu-id="dca4d-122">Value</span><span class="sxs-lookup"><span data-stu-id="dca4d-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dca4d-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dca4d-123">Minimum supported client</span></span><br/> | <span data-ttu-id="dca4d-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="dca4d-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="dca4d-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="dca4d-125">Minimum supported server</span></span><br/> | <span data-ttu-id="dca4d-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="dca4d-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="dca4d-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="dca4d-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="dca4d-128"><dt>Mciapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="dca4d-128"><dt>Mciapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dca4d-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="dca4d-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dca4d-130">MCI</span><span class="sxs-lookup"><span data-stu-id="dca4d-130">MCI</span></span>](mci.md)
</dt> <dt>

[<span data-ttu-id="dca4d-131">Macros MCI</span><span class="sxs-lookup"><span data-stu-id="dca4d-131">MCI Macros</span></span>](mci-macros.md)
</dt> </dl>

 

 





