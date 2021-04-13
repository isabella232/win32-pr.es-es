---
description: La función CompareFrameSourceAddress compara una dirección con la dirección de origen de un marco.
ms.assetid: 7221c0cc-d6c1-4ec9-bf11-3ba1fefb35da
title: Función CompareFrameSourceAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 4a100273c37e25a7b1deba86ed2704886dbfccc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104278145"
---
# <a name="compareframesourceaddress-function"></a><span data-ttu-id="d7f6e-103">CompareFrameSourceAddress función)</span><span class="sxs-lookup"><span data-stu-id="d7f6e-103">CompareFrameSourceAddress function</span></span>

<span data-ttu-id="d7f6e-104">La función **CompareFrameSourceAddress** compara una dirección con la dirección de origen de un marco.</span><span class="sxs-lookup"><span data-stu-id="d7f6e-104">The **CompareFrameSourceAddress** function compares an address to the source address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f6e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d7f6e-105">Syntax</span></span>


```C++
BOOL WINAPI CompareFrameSourceAddress(
  _In_ HFRAME    hFrame,
  _In_ LPADDRESS lpAddress
);
```



## <a name="parameters"></a><span data-ttu-id="d7f6e-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d7f6e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7f6e-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7f6e-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f6e-108">Identificador de un marco.</span><span class="sxs-lookup"><span data-stu-id="d7f6e-108">Handle to a frame.</span></span>

</dd> <dt>

<span data-ttu-id="d7f6e-109">*lpAddress* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="d7f6e-109">*lpAddress* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7f6e-110">Puntero a una dirección.</span><span class="sxs-lookup"><span data-stu-id="d7f6e-110">Pointer to an address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7f6e-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d7f6e-111">Return value</span></span>

<span data-ttu-id="d7f6e-112">Si las direcciones son las mismas, el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="d7f6e-112">If the addresses are the same, the return value is **TRUE**.</span></span>

<span data-ttu-id="d7f6e-113">Si las direcciones no son iguales, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="d7f6e-113">If the addresses are not the same, the return value is **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7f6e-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="d7f6e-114">Remarks</span></span>

<span data-ttu-id="d7f6e-115">Para que la función **CompareFrameSourceAddress** se ejecute correctamente, el tipo de dirección de origen debe coincidir con el tipo de dirección especificado en el parámetro *lpAddress* .</span><span class="sxs-lookup"><span data-stu-id="d7f6e-115">For the **CompareFrameSourceAddress** function to succeed, the source address type must match the type of address specified in the *lpAddress* parameter.</span></span>

<span data-ttu-id="d7f6e-116">Monitor de red proporciona otras dos funciones para comparar direcciones: [CompareFrameDestAddress](compareframedestaddress.md) y [CompareAddresses](compareaddresses.md).</span><span class="sxs-lookup"><span data-stu-id="d7f6e-116">Network Monitor provides two other functions for comparing addresses: [CompareFrameDestAddress](compareframedestaddress.md) and [CompareAddresses](compareaddresses.md).</span></span> <span data-ttu-id="d7f6e-117">La función **CompareFrameDestAddress** compara una dirección determinada con la dirección de destino del marco y la función **CompareAddress** compara dos direcciones dadas.</span><span class="sxs-lookup"><span data-stu-id="d7f6e-117">The **CompareFrameDestAddress** function compares a given address to the frame's destination address, and the **CompareAddress** function compares two given addresses.</span></span>

<span data-ttu-id="d7f6e-118">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **CompareFrameSourceAddress** .</span><span class="sxs-lookup"><span data-stu-id="d7f6e-118">[*Experts*](e.md) and [*parsers*](p.md) can call the **CompareFrameSourceAddress** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f6e-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7f6e-119">Requirements</span></span>



| <span data-ttu-id="d7f6e-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7f6e-120">Requirement</span></span> | <span data-ttu-id="d7f6e-121">Value</span><span class="sxs-lookup"><span data-stu-id="d7f6e-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f6e-122">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7f6e-122">Minimum supported client</span></span><br/> | <span data-ttu-id="d7f6e-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d7f6e-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="d7f6e-124">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d7f6e-124">Minimum supported server</span></span><br/> | <span data-ttu-id="d7f6e-125">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d7f6e-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="d7f6e-126">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d7f6e-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7f6e-127"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d7f6e-127"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="d7f6e-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7f6e-128">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7f6e-129"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7f6e-129"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="d7f6e-130">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d7f6e-130">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7f6e-131"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7f6e-131"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7f6e-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="d7f6e-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f6e-133">CompareAddresses</span><span class="sxs-lookup"><span data-stu-id="d7f6e-133">CompareAddresses</span></span>](compareaddresses.md)
</dt> <dt>

[<span data-ttu-id="d7f6e-134">CompareFrameDestAddress</span><span class="sxs-lookup"><span data-stu-id="d7f6e-134">CompareFrameDestAddress</span></span>](compareframedestaddress.md)
</dt> </dl>

 

 




