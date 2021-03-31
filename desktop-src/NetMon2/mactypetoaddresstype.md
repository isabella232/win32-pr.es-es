---
description: La función MacTypeToAddressType convierte un tipo MAC determinado en un tipo de dirección.
ms.assetid: 7ede39a8-9a71-4c7a-8d2d-84a4ea2173bb
title: Función MacTypeToAddressType (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MacTypeToAddressType
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: b0a0eb7a18126062c201fb7f0b122bca3ea8b631
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103908095"
---
# <a name="mactypetoaddresstype-function"></a><span data-ttu-id="7a8fe-103">MacTypeToAddressType función)</span><span class="sxs-lookup"><span data-stu-id="7a8fe-103">MacTypeToAddressType function</span></span>

<span data-ttu-id="7a8fe-104">La función **MacTypeToAddressType** convierte un tipo Mac determinado en un tipo de dirección.</span><span class="sxs-lookup"><span data-stu-id="7a8fe-104">The **MacTypeToAddressType** function converts a given MAC type to an address type.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a8fe-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7a8fe-105">Syntax</span></span>


```C++
DWORD WINAPI MacTypeToAddressType(
  _In_ DWORD MacType
);
```



## <a name="parameters"></a><span data-ttu-id="7a8fe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7a8fe-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a8fe-107">*MacType* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7a8fe-107">*MacType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a8fe-108">Tipo MAC que se va a convertir.</span><span class="sxs-lookup"><span data-stu-id="7a8fe-108">MAC type to be converted.</span></span> <span data-ttu-id="7a8fe-109">Especifique uno de los valores siguientes:</span><span class="sxs-lookup"><span data-stu-id="7a8fe-109">Specify one of the following values:</span></span>

<span data-ttu-id="7a8fe-110">tipo \_ Mac \_ Ethernet Mac \_ tipo \_ TOKENRING Mac \_ tipo \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="7a8fe-110">MAC\_TYPE\_ETHERNET MAC\_TYPE\_TOKENRING MAC\_TYPE\_FDDI</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7a8fe-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7a8fe-111">Return value</span></span>

<span data-ttu-id="7a8fe-112">Si la función se realiza correctamente, el valor devuelto es uno de los siguientes tipos de direcciones.</span><span class="sxs-lookup"><span data-stu-id="7a8fe-112">If the function is successful, the return value is one of the following address types.</span></span>

<span data-ttu-id="7a8fe-113">tipo de dirección \_ \_ Ethernet Dirección tipo \_ \_ TOKENRING \_ tipo de dirección \_ FDDI</span><span class="sxs-lookup"><span data-stu-id="7a8fe-113">ADDRESS\_TYPE\_ETHERNET ADDRESS\_TYPE\_TOKENRING ADDRESS\_TYPE\_FDDI</span></span>

<span data-ttu-id="7a8fe-114">Si la función no es correcta, el tipo MAC es desconocido, el valor devuelto es-1.</span><span class="sxs-lookup"><span data-stu-id="7a8fe-114">If the function is unsuccessful, the MAC type is unknown, the return value is -1.</span></span>

## <a name="remarks"></a><span data-ttu-id="7a8fe-115">Observaciones</span><span class="sxs-lookup"><span data-stu-id="7a8fe-115">Remarks</span></span>

<span data-ttu-id="7a8fe-116">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **MacTypeToAddressType** .</span><span class="sxs-lookup"><span data-stu-id="7a8fe-116">[*Experts*](e.md) and [*parsers*](p.md) can call the **MacTypeToAddressType** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="7a8fe-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7a8fe-117">Requirements</span></span>



| <span data-ttu-id="7a8fe-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7a8fe-118">Requirement</span></span> | <span data-ttu-id="7a8fe-119">Value</span><span class="sxs-lookup"><span data-stu-id="7a8fe-119">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="7a8fe-120">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a8fe-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7a8fe-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7a8fe-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="7a8fe-122">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7a8fe-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7a8fe-123">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7a8fe-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="7a8fe-124">Encabezado</span><span class="sxs-lookup"><span data-stu-id="7a8fe-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="7a8fe-125"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="7a8fe-125"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="7a8fe-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7a8fe-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="7a8fe-127"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="7a8fe-127"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="7a8fe-128">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7a8fe-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a8fe-129"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a8fe-129"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




