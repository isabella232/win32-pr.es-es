---
description: La función GetFrameSrcAddressOffset devuelve el desplazamiento de la dirección de origen de los marcos.
ms.assetid: 1c5408d7-cf66-4887-93ee-134c0b8c5eff
title: Función GetFrameSrcAddressOffset (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSrcAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: f7310c0ac2c6f402c37537100cc8060fef9eedd1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "104277979"
---
# <a name="getframesrcaddressoffset-function"></a><span data-ttu-id="b0468-103">GetFrameSrcAddressOffset función)</span><span class="sxs-lookup"><span data-stu-id="b0468-103">GetFrameSrcAddressOffset function</span></span>

<span data-ttu-id="b0468-104">La función **GetFrameSrcAddressOffset** devuelve el desplazamiento de la dirección de origen del marco.</span><span class="sxs-lookup"><span data-stu-id="b0468-104">The **GetFrameSrcAddressOffset** function returns the offset of the frame's source address.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0468-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0468-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameSrcAddressOffset(
   HFRAME  hFrame,
   DWORD   AddressType,
   LPDWORD AddressLength
);
```



## <a name="parameters"></a><span data-ttu-id="b0468-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0468-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b0468-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="b0468-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="b0468-108">Identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="b0468-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="b0468-109">*AddressType*</span><span class="sxs-lookup"><span data-stu-id="b0468-109">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="b0468-110">Tipo de dirección de origen.</span><span class="sxs-lookup"><span data-stu-id="b0468-110">Source address type.</span></span> <span data-ttu-id="b0468-111">El valor del parámetro puede ser uno de los siguientes:</span><span class="sxs-lookup"><span data-stu-id="b0468-111">The parameter value can be one of the following:</span></span>

-   <span data-ttu-id="b0468-112">tipo de dirección \_ \_ Ethernet</span><span class="sxs-lookup"><span data-stu-id="b0468-112">ADDRESS\_TYPE\_ETHERNET</span></span>
-   <span data-ttu-id="b0468-113">tipo de dirección \_ \_ IP</span><span class="sxs-lookup"><span data-stu-id="b0468-113">ADDRESS\_TYPE\_IP</span></span>
-   <span data-ttu-id="b0468-114">tipo de dirección \_ \_ IPX</span><span class="sxs-lookup"><span data-stu-id="b0468-114">ADDRESS\_TYPE\_IPX</span></span>
-   <span data-ttu-id="b0468-115">tipo de dirección \_ \_ TOKENRING</span><span class="sxs-lookup"><span data-stu-id="b0468-115">ADDRESS\_TYPE\_TOKENRING</span></span>
-   <span data-ttu-id="b0468-116">tipo de dirección \_ \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="b0468-116">ADDRESS\_TYPE\_FDDI</span></span>
-   <span data-ttu-id="b0468-117">tipo de dirección \_ \_ XNS</span><span class="sxs-lookup"><span data-stu-id="b0468-117">ADDRESS\_TYPE\_XNS</span></span>
-   <span data-ttu-id="b0468-118">tipo de dirección \_ \_ IP Vines \_</span><span class="sxs-lookup"><span data-stu-id="b0468-118">ADDRESS\_TYPE\_VINES\_IP</span></span>
-   <span data-ttu-id="b0468-119">tipo de dirección \_ \_ ATM</span><span class="sxs-lookup"><span data-stu-id="b0468-119">ADDRESS\_TYPE\_ATM</span></span>

</dd> <dt>

<span data-ttu-id="b0468-120">*AddressLength*</span><span class="sxs-lookup"><span data-stu-id="b0468-120">*AddressLength*</span></span> 
</dt> <dd>

<span data-ttu-id="b0468-121">Puntero a un **valor DWORD**, que, en la devolución, contiene la longitud de la dirección, en bytes.</span><span class="sxs-lookup"><span data-stu-id="b0468-121">Pointer to a **DWORD**, which on return, contains the length of the address, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b0468-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b0468-122">Return value</span></span>

<span data-ttu-id="b0468-123">Si la función se realiza correctamente, el valor devuelto es el desplazamiento de la dirección de origen.</span><span class="sxs-lookup"><span data-stu-id="b0468-123">If the function is successful, the return value is the offset to the source address.</span></span>

<span data-ttu-id="b0468-124">Si la función no se realiza correctamente, el valor devuelto es menos uno (-1).</span><span class="sxs-lookup"><span data-stu-id="b0468-124">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="requirements"></a><span data-ttu-id="b0468-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0468-125">Requirements</span></span>



| <span data-ttu-id="b0468-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0468-126">Requirement</span></span> | <span data-ttu-id="b0468-127">Value</span><span class="sxs-lookup"><span data-stu-id="b0468-127">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b0468-128">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0468-128">Minimum supported client</span></span><br/> | <span data-ttu-id="b0468-129">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b0468-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b0468-130">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b0468-130">Minimum supported server</span></span><br/> | <span data-ttu-id="b0468-131">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b0468-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b0468-132">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0468-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="b0468-133"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0468-133"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b0468-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b0468-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="b0468-135"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b0468-135"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b0468-136">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b0468-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b0468-137"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b0468-137"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




