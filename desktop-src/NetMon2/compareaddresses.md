---
description: La función CompareAddresses compara dos direcciones, lo que indica que una de las direcciones es mayor que, menor o igual que la otra dirección.
ms.assetid: 76ff37d2-714f-4bac-adcc-eab78c8f25d3
title: Función CompareAddresses (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CompareAddresses
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: fd72ef0281615c0b56176e86ee9bb3659b498a0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667736"
---
# <a name="compareaddresses-function"></a><span data-ttu-id="ab9ac-103">CompareAddresses función)</span><span class="sxs-lookup"><span data-stu-id="ab9ac-103">CompareAddresses function</span></span>

<span data-ttu-id="ab9ac-104">La función **CompareAddresses** compara dos direcciones, lo que indica que una de las direcciones es mayor que, menor o igual que la otra dirección.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-104">The **CompareAddresses** function compares two addresses, indicating that one of the addresses is greater than, less than, or equal to the other address.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab9ac-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ab9ac-105">Syntax</span></span>


```C++
int WINAPI CompareAddresses(
  _In_ LPADDRESS lpAddress1,
  _In_ LPADDRESS lpAddress2
);
```



## <a name="parameters"></a><span data-ttu-id="ab9ac-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="ab9ac-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab9ac-107">*lpAddress1* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab9ac-107">*lpAddress1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab9ac-108">Puntero a la primera dirección.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-108">Pointer to the first address.</span></span>

</dd> <dt>

<span data-ttu-id="ab9ac-109">*lpAddress2* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="ab9ac-109">*lpAddress2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab9ac-110">Puntero a la segunda dirección.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-110">Pointer to the second address.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab9ac-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ab9ac-111">Return value</span></span>

<span data-ttu-id="ab9ac-112">Si las direcciones son iguales, la función devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-112">If the addresses are the same, the function returns zero.</span></span>

<span data-ttu-id="ab9ac-113">Si el parámetro *lpAddress1* especifica una dirección que es menor que la dirección que especifica el parámetro *lpAddress2* , el valor devuelto es un número negativo.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-113">If the *lpAddress1* parameter specifies an address that is less than the address that the *lpAddress2* parameter specifies, the return value is a negative number.</span></span>

<span data-ttu-id="ab9ac-114">Si el parámetro *lpAddress1* especifica una dirección que es mayor que la dirección que especifica el parámetro *lpAddress2* , el valor devuelto es un número positivo.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-114">If the *lpAddress1* parameter specifies an address that is greater than the address that the *lpAddress2* parameter specifies, the return value is a positive number.</span></span>

## <a name="remarks"></a><span data-ttu-id="ab9ac-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="ab9ac-115">Remarks</span></span>

<span data-ttu-id="ab9ac-116">Una dirección que es menor que otra dirección indica un fotograma anterior.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-116">An address that is less than another address indicates a previous frame.</span></span> <span data-ttu-id="ab9ac-117">Una dirección que es mayor que otra dirección indica un fotograma posterior.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-117">An address that is greater than another address indicates a later frame.</span></span>

<span data-ttu-id="ab9ac-118">Monitor de red proporciona otras dos funciones, [CompareFrameDestAddress](compareframedestaddress.md) y [CompareFrameSourceAddress](compareframesourceaddress.md), que puede usar para comparar direcciones.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-118">Network Monitor provides two other functions, [CompareFrameDestAddress](compareframedestaddress.md) and [CompareFrameSourceAddress](compareframesourceaddress.md), which you can use to compare addresses.</span></span> <span data-ttu-id="ab9ac-119">La función **CompareFrameDestAddress** compara una dirección determinada con la dirección de destino del marco y la función **CompareFrameSourceAddress** compara una dirección determinada con la dirección de origen del marco.</span><span class="sxs-lookup"><span data-stu-id="ab9ac-119">The **CompareFrameDestAddress** function compares a given address to the frame's destination address, and the **CompareFrameSourceAddress** function compares a given address to the frame's source address.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab9ac-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ab9ac-120">Requirements</span></span>



| <span data-ttu-id="ab9ac-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="ab9ac-121">Requirement</span></span> | <span data-ttu-id="ab9ac-122">Value</span><span class="sxs-lookup"><span data-stu-id="ab9ac-122">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ab9ac-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab9ac-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ab9ac-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ab9ac-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="ab9ac-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ab9ac-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ab9ac-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ab9ac-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="ab9ac-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="ab9ac-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab9ac-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="ab9ac-128"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="ab9ac-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ab9ac-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="ab9ac-130"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="ab9ac-130"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="ab9ac-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ab9ac-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab9ac-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab9ac-132"><dt>Nmapi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab9ac-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="ab9ac-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab9ac-134">CompareFrameDestAddress</span><span class="sxs-lookup"><span data-stu-id="ab9ac-134">CompareFrameDestAddress</span></span>](compareframedestaddress.md)
</dt> <dt>

[<span data-ttu-id="ab9ac-135">CompareFrameSourceAddress</span><span class="sxs-lookup"><span data-stu-id="ab9ac-135">CompareFrameSourceAddress</span></span>](compareframesourceaddress.md)
</dt> </dl>

 

 




