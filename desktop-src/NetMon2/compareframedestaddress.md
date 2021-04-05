---
description: La función CompareFrameDestAddress compara una dirección con la dirección de destino de un marco.
ms.assetid: 739b3b9f-f989-459d-ac3e-6be7769adc06
title: Función CompareFrameDestAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: a9ce0ff776588c06b8fddc34240e9c2170ceca69
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103909414"
---
# <a name="compareframedestaddress-function"></a><span data-ttu-id="992cc-103">CompareFrameDestAddress función)</span><span class="sxs-lookup"><span data-stu-id="992cc-103">CompareFrameDestAddress function</span></span>

<span data-ttu-id="992cc-104">La función **CompareFrameDestAddress** compara una dirección con la dirección de destino de un marco.</span><span class="sxs-lookup"><span data-stu-id="992cc-104">The **CompareFrameDestAddress** function compares an address to the destination address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="992cc-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="992cc-105">Syntax</span></span>


```C++
BOOL WINAPI CompareFrameDestAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="992cc-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="992cc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="992cc-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="992cc-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="992cc-108">Identificador de un marco.</span><span class="sxs-lookup"><span data-stu-id="992cc-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="992cc-109">*lpAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="992cc-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="992cc-110">Puntero a una dirección.</span><span class="sxs-lookup"><span data-stu-id="992cc-110">Pointer to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="992cc-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="992cc-111">Return value</span></span>

<span data-ttu-id="992cc-112">Si las direcciones son las mismas, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="992cc-112">If the addresses are the same, the return value is **TRUE**.</span></span>

<span data-ttu-id="992cc-113">Si las direcciones no son iguales, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="992cc-113">If the addresses are not the same, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="992cc-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="992cc-114">Remarks</span></span>

<span data-ttu-id="992cc-115">Para que la función **CompareFrameDestAddress** se devuelva correctamente, el tipo de dirección de destino debe coincidir con el tipo de dirección especificado en el parámetro *lpAddress* .</span><span class="sxs-lookup"><span data-stu-id="992cc-115">For the **CompareFrameDestAddress** function to return successfully, the destination address type must match the type of address specified in the *lpAddress* parameter.</span></span>

<span data-ttu-id="992cc-116">Monitor de red proporciona otras dos funciones, [CompareFrameSourceAddress](compareframesourceaddress.md) y [CompareAddresses](compareaddresses.md), que puede usar para comparar direcciones.</span><span class="sxs-lookup"><span data-stu-id="992cc-116">Network Monitor provides two other functions, [CompareFrameSourceAddress](compareframesourceaddress.md) and [CompareAddresses](compareaddresses.md), which you can use to compare addresses.</span></span> <span data-ttu-id="992cc-117">La función **CompareFrameSourceAddress** compara una dirección determinada con la dirección de origen del marco y la función **CompareAddress** compara dos direcciones dadas.</span><span class="sxs-lookup"><span data-stu-id="992cc-117">The **CompareFrameSourceAddress** function compares a given address to the frame's source address, and the **CompareAddress** function compares two given addresses.</span></span>

<span data-ttu-id="992cc-118">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **CompareFrameDestAddress** .</span><span class="sxs-lookup"><span data-stu-id="992cc-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **CompareFrameDestAddress** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="992cc-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="992cc-119">Requirements</span></span>



| <span data-ttu-id="992cc-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="992cc-120">Requirement</span></span> | <span data-ttu-id="992cc-121">Value</span><span class="sxs-lookup"><span data-stu-id="992cc-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="992cc-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="992cc-122">Minimum supported client</span></span><br/> | <span data-ttu-id="992cc-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="992cc-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="992cc-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="992cc-124">Minimum supported server</span></span><br/> | <span data-ttu-id="992cc-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="992cc-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="992cc-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="992cc-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="992cc-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="992cc-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="992cc-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="992cc-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="992cc-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="992cc-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="992cc-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="992cc-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="992cc-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="992cc-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="992cc-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="992cc-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="992cc-133">CompareAddresses</span><span class="sxs-lookup"><span data-stu-id="992cc-133">CompareAddresses</span></span>](compareaddresses.md)
</dt> <dt>

[<span data-ttu-id="992cc-134">CompareFrameSourceAddress</span><span class="sxs-lookup"><span data-stu-id="992cc-134">CompareFrameSourceAddress</span></span>](compareframesourceaddress.md)
</dt> </dl>

 

 




