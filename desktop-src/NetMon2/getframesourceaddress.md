---
description: Recupera la dirección de origen de un marco.
ms.assetid: 414f9e64-f1b2-46f1-822e-0fffacfad843
title: Función GetFrameSourceAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameSourceAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 6939e5875c4d2f6f41ae33574c7a7240697042ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105686570"
---
# <a name="getframesourceaddress-function"></a><span data-ttu-id="a1604-103">GetFrameSourceAddress función)</span><span class="sxs-lookup"><span data-stu-id="a1604-103">GetFrameSourceAddress function</span></span>

<span data-ttu-id="a1604-104">La función **GetFrameSourceAddress** recupera la dirección de origen de un marco.</span><span class="sxs-lookup"><span data-stu-id="a1604-104">The **GetFrameSourceAddress** function retrieves the source address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1604-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a1604-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameSourceAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="a1604-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1604-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1604-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="a1604-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="a1604-108">Identificador del marco para el que se va a obtener un puntero.</span><span class="sxs-lookup"><span data-stu-id="a1604-108">A handle to the frame for which to get a pointer to.</span></span>

</dd> <dt>

<span data-ttu-id="a1604-109">*lpAddress*</span><span class="sxs-lookup"><span data-stu-id="a1604-109">*lpAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="a1604-110">Búfer de retorno que almacena la dirección de origen del marco.</span><span class="sxs-lookup"><span data-stu-id="a1604-110">A return buffer that stores the frame source address.</span></span>

</dd> <dt>

<span data-ttu-id="a1604-111">*AddressType*</span><span class="sxs-lookup"><span data-stu-id="a1604-111">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="a1604-112">El tipo de dirección que se busca, como el tipo de dirección \_ \_ Ethernet o el tipo de dirección \_ \_ IP.</span><span class="sxs-lookup"><span data-stu-id="a1604-112">The type of address searched for, such as ADDRESS\_TYPE\_ETHERNET or ADDRESS\_TYPE\_IP.</span></span>

</dd> <dt>

<span data-ttu-id="a1604-113">*Marcas*</span><span class="sxs-lookup"><span data-stu-id="a1604-113">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="a1604-114">Marcas usadas para modificar los datos de dirección de origen devueltos.</span><span class="sxs-lookup"><span data-stu-id="a1604-114">The flags used to modify returned source address data.</span></span>



| <span data-ttu-id="a1604-115">Value</span><span class="sxs-lookup"><span data-stu-id="a1604-115">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="a1604-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a1604-116">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <span data-ttu-id="a1604-117"><dt>**marcas de ADDRESSTYPE ( \_ \_ normalizar)**</dt></span><span class="sxs-lookup"><span data-stu-id="a1604-117"><dt>**ADDRESSTYPE\_FLAGS\_NORMALIZE**</dt></span></span> </dl>        | <span data-ttu-id="a1604-118">Cancela los BITs de enrutamiento y grupo.</span><span class="sxs-lookup"><span data-stu-id="a1604-118">Cancels the routing and group BITs.</span></span><br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <span data-ttu-id="a1604-119"><dt>**BIT de las \_ marcas ADDRESSTYPE \_ \_ inverso**</dt></span><span class="sxs-lookup"><span data-stu-id="a1604-119"><dt>**ADDRESSTYPE\_FLAGS\_BIT\_REVERSE**</dt></span></span> </dl> | <span data-ttu-id="a1604-120">Vuelve a convertir las direcciones de red de token ring en normal.</span><span class="sxs-lookup"><span data-stu-id="a1604-120">Converts token ring network addresses back to normal.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1604-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1604-121">Return value</span></span>

<span data-ttu-id="a1604-122">Si la función es correcta, el valor de *lpAddress* es válido y el valor devuelto es BHERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a1604-122">If the function is successful, the *lpAddress* value is valid, and the return value is BHERR\_SUCCESS.</span></span>

<span data-ttu-id="a1604-123">Si la función no es correcta, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="a1604-123">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="a1604-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a1604-124">Return code</span></span>                                                                                                | <span data-ttu-id="a1604-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="a1604-125">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a1604-126"><dt>**\_ \_ no \_ se encontró el protocolo BHERR**</dt></span><span class="sxs-lookup"><span data-stu-id="a1604-126"><dt>**BHERR\_PROTOCOL\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="a1604-127">El protocolo especificado por el parámetro *AddressType* no es válido para el marco.</span><span class="sxs-lookup"><span data-stu-id="a1604-127">The protocol specified by the *AddressType* parameter is invalid for the frame.</span></span><br/> |
| <dl> <span data-ttu-id="a1604-128"><dt>**BHERR \_ no válido \_ HFRAME**</dt></span><span class="sxs-lookup"><span data-stu-id="a1604-128"><dt>**BHERR\_INVALID\_HFRAME**</dt></span></span> </dl>      | <span data-ttu-id="a1604-129">El valor del parámetro *hFrame* no es válido.</span><span class="sxs-lookup"><span data-stu-id="a1604-129">The *hFrame* parameter value is invalid.</span></span><br/>                                        |



 

## <a name="remarks"></a><span data-ttu-id="a1604-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a1604-130">Remarks</span></span>

<span data-ttu-id="a1604-131">Se permite un tipo de dirección de **tipo de dirección \_ \_ Buscar \_ superior** .</span><span class="sxs-lookup"><span data-stu-id="a1604-131">An address type of **ADDRESS\_TYPE\_FIND\_HIGHEST** is allowed.</span></span> <span data-ttu-id="a1604-132">Cuando se usa este tipo de dirección, la función busca la dirección IP de IPX, XNS, IP o VINEs antes de devolver la dirección ETHERNET, TOKENRING o FDDI.</span><span class="sxs-lookup"><span data-stu-id="a1604-132">When this address type is used, the function searches for the IPX, XNS, IP, or VINES IP address before returning the ETHERNET, TOKENRING, or FDDI address.</span></span> <span data-ttu-id="a1604-133">Este enfoque es útil para los protocolos y entornos en los que se pueden multiplexar dos NIC en una sola dirección de servidor.</span><span class="sxs-lookup"><span data-stu-id="a1604-133">This approach is useful for protocols and environments in which two NICs can be multiplexed under a single server address.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1604-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1604-134">Requirements</span></span>



| <span data-ttu-id="a1604-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1604-135">Requirement</span></span> | <span data-ttu-id="a1604-136">Value</span><span class="sxs-lookup"><span data-stu-id="a1604-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a1604-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1604-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a1604-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a1604-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a1604-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a1604-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a1604-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a1604-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a1604-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a1604-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1604-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a1604-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="a1604-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1604-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="a1604-144"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a1604-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a1604-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a1604-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a1604-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a1604-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




