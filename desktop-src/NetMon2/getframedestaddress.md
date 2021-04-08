---
description: Recupera la dirección de destino de un marco.
ms.assetid: f19a6753-37d8-4ec7-a7d4-ced0292d453c
title: Función GetFrameDestAddress (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDestAddress
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: afec32f0e0fc66ccd5a1d78cc9769b0e742f1e6f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000935"
---
# <a name="getframedestaddress-function"></a><span data-ttu-id="a89c0-103">GetFrameDestAddress función)</span><span class="sxs-lookup"><span data-stu-id="a89c0-103">GetFrameDestAddress function</span></span>

<span data-ttu-id="a89c0-104">La función **GetFrameDestAddress** recupera la dirección de destino de un marco.</span><span class="sxs-lookup"><span data-stu-id="a89c0-104">The **GetFrameDestAddress** function retrieves the destination address of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="a89c0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a89c0-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameDestAddress(
   HFRAME    hFrame,
   LPADDRESS lpAddress,
   DWORD     AddressType,
   DWORD     Flags
);
```



## <a name="parameters"></a><span data-ttu-id="a89c0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a89c0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a89c0-107">*hFrame*</span><span class="sxs-lookup"><span data-stu-id="a89c0-107">*hFrame*</span></span> 
</dt> <dd>

<span data-ttu-id="a89c0-108">Identificador del marco al que se va a obtener un puntero.</span><span class="sxs-lookup"><span data-stu-id="a89c0-108">A handle of the frame to get a pointer to.</span></span>

</dd> <dt>

<span data-ttu-id="a89c0-109">*lpAddress*</span><span class="sxs-lookup"><span data-stu-id="a89c0-109">*lpAddress*</span></span> 
</dt> <dd>

<span data-ttu-id="a89c0-110">Búfer de retorno que almacena la dirección de destino del marco.</span><span class="sxs-lookup"><span data-stu-id="a89c0-110">A return buffer that stores the frame destination address.</span></span>

</dd> <dt>

<span data-ttu-id="a89c0-111">*AddressType*</span><span class="sxs-lookup"><span data-stu-id="a89c0-111">*AddressType*</span></span> 
</dt> <dd>

<span data-ttu-id="a89c0-112">Un tipo de dirección, como el tipo de dirección \_ \_ Ethernet o el tipo de dirección \_ \_ IP.</span><span class="sxs-lookup"><span data-stu-id="a89c0-112">A type of address, such as ADDRESS\_TYPE\_ETHERNET or ADDRESS\_TYPE\_IP.</span></span>

</dd> <dt>

<span data-ttu-id="a89c0-113">*Marcas*</span><span class="sxs-lookup"><span data-stu-id="a89c0-113">*Flags*</span></span> 
</dt> <dd>

<span data-ttu-id="a89c0-114">Marcas usadas para modificar los datos devueltos de la dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="a89c0-114">The flags used to modify returned destination address data.</span></span>



| <span data-ttu-id="a89c0-115">Value</span><span class="sxs-lookup"><span data-stu-id="a89c0-115">Value</span></span>                                                                                                                                                                                                           | <span data-ttu-id="a89c0-116">Significado</span><span class="sxs-lookup"><span data-stu-id="a89c0-116">Meaning</span></span>                                                          |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <span id="ADDRESSTYPE_FLAGS_NORMALIZE"></span><span id="addresstype_flags_normalize"></span><dl> <span data-ttu-id="a89c0-117"><dt>**marcas de ADDRESSTYPE ( \_ \_ normalizar)**</dt></span><span class="sxs-lookup"><span data-stu-id="a89c0-117"><dt>**ADDRESSTYPE\_FLAGS\_NORMALIZE**</dt></span></span> </dl>        | <span data-ttu-id="a89c0-118">Cancela los BITs de enrutamiento y grupo.</span><span class="sxs-lookup"><span data-stu-id="a89c0-118">Cancels the routing and group BITs.</span></span><br/>                   |
| <span id="ADDRESSTYPE_FLAGS_BIT_REVERSE"></span><span id="addresstype_flags_bit_reverse"></span><dl> <span data-ttu-id="a89c0-119"><dt>**BIT de las \_ marcas ADDRESSTYPE \_ \_ inverso**</dt></span><span class="sxs-lookup"><span data-stu-id="a89c0-119"><dt>**ADDRESSTYPE\_FLAGS\_BIT\_REVERSE**</dt></span></span> </dl> | <span data-ttu-id="a89c0-120">Vuelve a convertir las direcciones de red de token ring en normal.</span><span class="sxs-lookup"><span data-stu-id="a89c0-120">Converts token ring network addresses back to normal.</span></span><br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a89c0-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a89c0-121">Return value</span></span>

<span data-ttu-id="a89c0-122">Si la función es correcta, el valor de *lpAddress* es válido y el valor devuelto es BHERR \_ Success.</span><span class="sxs-lookup"><span data-stu-id="a89c0-122">If the function is successful, the *lpAddress* value is valid, and the return value is BHERR\_SUCCESS.</span></span>

<span data-ttu-id="a89c0-123">Si la función no es correcta, el valor devuelto es un código de error.</span><span class="sxs-lookup"><span data-stu-id="a89c0-123">If the function is unsuccessful, the return value is an error code.</span></span>



| <span data-ttu-id="a89c0-124">Código devuelto</span><span class="sxs-lookup"><span data-stu-id="a89c0-124">Return code</span></span>                                                                                                | <span data-ttu-id="a89c0-125">Descripción</span><span class="sxs-lookup"><span data-stu-id="a89c0-125">Description</span></span>                                                                                |
|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="a89c0-126"><dt>**\_ \_ no \_ se encontró el protocolo BHERR**</dt></span><span class="sxs-lookup"><span data-stu-id="a89c0-126"><dt>**BHERR\_PROTOCOL\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="a89c0-127">El protocolo especificado en el parámetro *AddressType* no es válido para el marco.</span><span class="sxs-lookup"><span data-stu-id="a89c0-127">The specified protocol in the *AddressType* parameter is invalid for the frame.</span></span><br/> |
| <dl> <span data-ttu-id="a89c0-128"><dt>**BHERR \_ no válido \_ HFRAME**</dt></span><span class="sxs-lookup"><span data-stu-id="a89c0-128"><dt>**BHERR\_INVALID\_HFRAME**</dt></span></span> </dl>      | <span data-ttu-id="a89c0-129">El valor de *hFrame* no es válido.</span><span class="sxs-lookup"><span data-stu-id="a89c0-129">The *hFrame* value is invalid.</span></span><br/>                                                  |



 

## <a name="remarks"></a><span data-ttu-id="a89c0-130">Observaciones</span><span class="sxs-lookup"><span data-stu-id="a89c0-130">Remarks</span></span>

<span data-ttu-id="a89c0-131">Se permite el tipo de dirección buscar el tipo de dirección **\_ \_ \_ más alto** .</span><span class="sxs-lookup"><span data-stu-id="a89c0-131">The **ADDRESS\_TYPE\_FIND\_HIGHEST** address type is allowed.</span></span> <span data-ttu-id="a89c0-132">Cuando se usa este tipo de dirección, la función busca la dirección IP de IPX, XNS, IP o VINEs antes de devolver la dirección ETHERNET, TOKENRING o FDDI.</span><span class="sxs-lookup"><span data-stu-id="a89c0-132">When this address type is used, the function searches for the IPX, XNS, IP, or VINES IP address before returning the ETHERNET, TOKENRING, or FDDI address.</span></span> <span data-ttu-id="a89c0-133">Este enfoque es útil para los protocolos y en entornos en los que se pueden multiplexar dos NIC en una sola dirección de servidor.</span><span class="sxs-lookup"><span data-stu-id="a89c0-133">This approach is useful for protocols and in environments where two NICs can be multiplexed under a single server address.</span></span>

## <a name="requirements"></a><span data-ttu-id="a89c0-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a89c0-134">Requirements</span></span>



| <span data-ttu-id="a89c0-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="a89c0-135">Requirement</span></span> | <span data-ttu-id="a89c0-136">Value</span><span class="sxs-lookup"><span data-stu-id="a89c0-136">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="a89c0-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a89c0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a89c0-138">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="a89c0-138">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="a89c0-139">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="a89c0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a89c0-140">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="a89c0-140">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a89c0-141">Encabezado</span><span class="sxs-lookup"><span data-stu-id="a89c0-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="a89c0-142"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="a89c0-142"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="a89c0-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a89c0-143">Library</span></span><br/>                  | <dl> <span data-ttu-id="a89c0-144"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="a89c0-144"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="a89c0-145">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="a89c0-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a89c0-146"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a89c0-146"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




