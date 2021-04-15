---
description: La función GetFrameDstAddressOffset devuelve el desplazamiento a la dirección de destino de un fotograma determinado.
ms.assetid: 8922d7d0-1a23-47ac-886b-fcc0bcaa6ba7
title: Función GetFrameDstAddressOffset (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameDstAddressOffset
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 8358afdbb303baf623cef6fc32e00d758570d30c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677281"
---
# <a name="getframedstaddressoffset-function"></a><span data-ttu-id="66dc7-103">GetFrameDstAddressOffset función)</span><span class="sxs-lookup"><span data-stu-id="66dc7-103">GetFrameDstAddressOffset function</span></span>

<span data-ttu-id="66dc7-104">La función **GetFrameDstAddressOffset** devuelve el desplazamiento a la dirección de destino de un fotograma determinado.</span><span class="sxs-lookup"><span data-stu-id="66dc7-104">The **GetFrameDstAddressOffset** function returns the offset to the destination address of a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="66dc7-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="66dc7-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameDstAddressOffset(
  _In_ HFRAME  hFrame,
  _In_ DWORD   AddressType,
  _In_ LPDWORD AddressLength
);
```



## <a name="parameters"></a><span data-ttu-id="66dc7-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="66dc7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66dc7-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66dc7-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66dc7-108">Identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="66dc7-108">Handle to the frame.</span></span>

</dd> <dt>

<span data-ttu-id="66dc7-109">*AddressType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66dc7-109">*AddressType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66dc7-110">Tipo de la dirección de destino.</span><span class="sxs-lookup"><span data-stu-id="66dc7-110">Type of the destination address.</span></span> <span data-ttu-id="66dc7-111">Especifique uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="66dc7-111">Specify one of the following values:</span></span>

<span data-ttu-id="66dc7-112">tipo de dirección Ethernet de tipo dirección IP escriba dirección IP tipo de dirección TOKENRING tipo de dirección FDDI tipo de dirección de XNS tipo de dirección \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ \_ IP Vines tipo de dirección \_ IP \_ \_ ATM.</span><span class="sxs-lookup"><span data-stu-id="66dc7-112">ADDRESS\_TYPE\_ETHERNET ADDRESS\_TYPE\_IP ADDRESS\_TYPE\_IPX ADDRESS\_TYPE\_TOKENRING ADDRESS\_TYPE\_FDDI ADDRESS\_TYPE\_XNS ADDRESS\_TYPE\_VINES\_IP ADDRESS\_TYPE\_ATM.</span></span>

</dd> <dt>

<span data-ttu-id="66dc7-113">*AddressLength* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="66dc7-113">*AddressLength* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="66dc7-114">Longitud de la dirección de destino, en bytes.</span><span class="sxs-lookup"><span data-stu-id="66dc7-114">Length of the destination address, in bytes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66dc7-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="66dc7-115">Return value</span></span>

<span data-ttu-id="66dc7-116">Si la función se realiza correctamente, el valor devuelto es el desplazamiento (medido en bytes) al tipo de dirección solicitado.</span><span class="sxs-lookup"><span data-stu-id="66dc7-116">If the function is successful, the return value is the offset (measured in bytes) to the requested address type.</span></span>

<span data-ttu-id="66dc7-117">Si la función no se realiza correctamente, el valor devuelto es menos uno (-1).</span><span class="sxs-lookup"><span data-stu-id="66dc7-117">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="66dc7-118">Observaciones</span><span class="sxs-lookup"><span data-stu-id="66dc7-118">Remarks</span></span>

<span data-ttu-id="66dc7-119">Si el parámetro *AddressType* está establecido en el \_ tipo de dirección \_ Ethernet, el valor devuelto de la función **GetFrameDstAddressOffset** siempre es cero.</span><span class="sxs-lookup"><span data-stu-id="66dc7-119">If the *AddressType* parameter is set to ADDRESS\_TYPE\_ETHERNET, the return value of the **GetFrameDstAddressOffset** function is always zero.</span></span> <span data-ttu-id="66dc7-120">El desplazamiento de una dirección Ethernet siempre es cero.</span><span class="sxs-lookup"><span data-stu-id="66dc7-120">The offset of an Ethernet address is always zero.</span></span>

<span data-ttu-id="66dc7-121">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrameDstAddressOffset** .</span><span class="sxs-lookup"><span data-stu-id="66dc7-121">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameDstAddressOffset** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="66dc7-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66dc7-122">Requirements</span></span>



| <span data-ttu-id="66dc7-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="66dc7-123">Requirement</span></span> | <span data-ttu-id="66dc7-124">Value</span><span class="sxs-lookup"><span data-stu-id="66dc7-124">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="66dc7-125">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66dc7-125">Minimum supported client</span></span><br/> | <span data-ttu-id="66dc7-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="66dc7-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="66dc7-127">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="66dc7-127">Minimum supported server</span></span><br/> | <span data-ttu-id="66dc7-128">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="66dc7-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="66dc7-129">Encabezado</span><span class="sxs-lookup"><span data-stu-id="66dc7-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="66dc7-130"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="66dc7-130"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="66dc7-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66dc7-131">Library</span></span><br/>                  | <dl> <span data-ttu-id="66dc7-132"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="66dc7-132"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="66dc7-133">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="66dc7-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="66dc7-134"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="66dc7-134"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




