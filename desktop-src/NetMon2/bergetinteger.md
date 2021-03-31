---
description: La función BERGetInteger descodifica un entero con codificación BER.
ms.assetid: 1ab0dcec-05cf-4322-a44e-28aa9131495a
title: Función BERGetInteger (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetInteger
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: c89cd5e3f4e4eb35157936f990939154f23966d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "103911645"
---
# <a name="bergetinteger-function"></a><span data-ttu-id="063b3-103">BERGetInteger función)</span><span class="sxs-lookup"><span data-stu-id="063b3-103">BERGetInteger function</span></span>

<span data-ttu-id="063b3-104">La función **BERGetInteger** descodifica un entero con codificación BER.</span><span class="sxs-lookup"><span data-stu-id="063b3-104">The **BERGetInteger** function decodes a BER-encoded integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="063b3-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="063b3-105">Syntax</span></span>


```C++
BOOL BERGetInteger(
   LPBYTE  pCurrentPointer,
   LPBYTE  *ppValuePointer,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="063b3-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="063b3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="063b3-107">*pCurrentPointer*</span><span class="sxs-lookup"><span data-stu-id="063b3-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="063b3-108">Puntero al entero que está descodificado.</span><span class="sxs-lookup"><span data-stu-id="063b3-108">Pointer to the integer that is decoded.</span></span>

</dd> <dt>

<span data-ttu-id="063b3-109">*ppValuePointer*</span><span class="sxs-lookup"><span data-stu-id="063b3-109">*ppValuePointer*</span></span> 
</dt> <dd>

<span data-ttu-id="063b3-110">Puntero al puntero al valor devuelto.</span><span class="sxs-lookup"><span data-stu-id="063b3-110">Pointer to the pointer to returned value.</span></span>

</dd> <dt>

<span data-ttu-id="063b3-111">*pHeaderLength*</span><span class="sxs-lookup"><span data-stu-id="063b3-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="063b3-112">Puntero a la longitud de encabezado devuelta.</span><span class="sxs-lookup"><span data-stu-id="063b3-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="063b3-113">*pDataLength*</span><span class="sxs-lookup"><span data-stu-id="063b3-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="063b3-114">Puntero a la longitud de los datos.</span><span class="sxs-lookup"><span data-stu-id="063b3-114">Pointer to the data length.</span></span>

</dd> <dt>

<span data-ttu-id="063b3-115">*ppNext*</span><span class="sxs-lookup"><span data-stu-id="063b3-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="063b3-116">Puntero al puntero a la entrada siguiente de BER.</span><span class="sxs-lookup"><span data-stu-id="063b3-116">Pointer to the pointer to the next BER entry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="063b3-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="063b3-117">Return value</span></span>

<span data-ttu-id="063b3-118">Si la función es correcta (es decir, si se encuentra y se convierte un entero codificado BER válido), el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="063b3-118">If the function is successful (that is, if a valid BER encoded integer is found and converted), the return value is **TRUE**.</span></span>

<span data-ttu-id="063b3-119">Si la función no es correcta, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="063b3-119">If function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="063b3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="063b3-120">Requirements</span></span>



| <span data-ttu-id="063b3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="063b3-121">Requirement</span></span> | <span data-ttu-id="063b3-122">Value</span><span class="sxs-lookup"><span data-stu-id="063b3-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="063b3-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="063b3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="063b3-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="063b3-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="063b3-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="063b3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="063b3-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="063b3-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="063b3-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="063b3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="063b3-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="063b3-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="063b3-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="063b3-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="063b3-130"><dt>Analizador. lib</dt></span><span class="sxs-lookup"><span data-stu-id="063b3-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="063b3-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="063b3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="063b3-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="063b3-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




