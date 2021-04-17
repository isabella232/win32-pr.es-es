---
description: La función BERGetHeader descodifica un encabezado Choice.
ms.assetid: 2574a9b3-c28e-43d1-904f-d45888617584
title: Función BERGetHeader (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BERGetHeader
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 5e2213b15b6b4d2cbaa15b3b9aa9de028e20a62d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105677739"
---
# <a name="bergetheader-function"></a><span data-ttu-id="d85d9-103">BERGetHeader función)</span><span class="sxs-lookup"><span data-stu-id="d85d9-103">BERGetHeader function</span></span>

<span data-ttu-id="d85d9-104">La función **BERGetHeader** descodifica un encabezado Choice.</span><span class="sxs-lookup"><span data-stu-id="d85d9-104">The **BERGetHeader** function decodes a choice header.</span></span>

## <a name="syntax"></a><span data-ttu-id="d85d9-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="d85d9-105">Syntax</span></span>


```C++
BOOL BERGetHeader(
   LPBYTE  pCurrentPointer,
   LPBYTE  pTag,
   LPDWORD pHeaderLength,
   LPDWORD pDataLength,
   LPBYTE  *ppNext
);
```



## <a name="parameters"></a><span data-ttu-id="d85d9-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d85d9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d85d9-107">*pCurrentPointer*</span><span class="sxs-lookup"><span data-stu-id="d85d9-107">*pCurrentPointer*</span></span> 
</dt> <dd>

<span data-ttu-id="d85d9-108">Puntero al encabezado Choice.</span><span class="sxs-lookup"><span data-stu-id="d85d9-108">Pointer to the choice header.</span></span>

</dd> <dt>

<span data-ttu-id="d85d9-109">*pTag*</span><span class="sxs-lookup"><span data-stu-id="d85d9-109">*pTag*</span></span> 
</dt> <dd>

<span data-ttu-id="d85d9-110">Puntero a la etiqueta devuelta.</span><span class="sxs-lookup"><span data-stu-id="d85d9-110">Pointer to the returned tag.</span></span>

</dd> <dt>

<span data-ttu-id="d85d9-111">*pHeaderLength*</span><span class="sxs-lookup"><span data-stu-id="d85d9-111">*pHeaderLength*</span></span> 
</dt> <dd>

<span data-ttu-id="d85d9-112">Puntero a la longitud de encabezado devuelta.</span><span class="sxs-lookup"><span data-stu-id="d85d9-112">Pointer to the returned header length.</span></span>

</dd> <dt>

<span data-ttu-id="d85d9-113">*pDataLength*</span><span class="sxs-lookup"><span data-stu-id="d85d9-113">*pDataLength*</span></span> 
</dt> <dd>

<span data-ttu-id="d85d9-114">Puntero a la longitud de datos devuelta.</span><span class="sxs-lookup"><span data-stu-id="d85d9-114">Pointer to the returned data length.</span></span>

</dd> <dt>

<span data-ttu-id="d85d9-115">*ppNext*</span><span class="sxs-lookup"><span data-stu-id="d85d9-115">*ppNext*</span></span> 
</dt> <dd>

<span data-ttu-id="d85d9-116">Puntero al contenido del encabezado.</span><span class="sxs-lookup"><span data-stu-id="d85d9-116">Pointer to the header contents.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d85d9-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d85d9-117">Return value</span></span>

<span data-ttu-id="d85d9-118">Si la función es correcta (es decir, se encuentra un encabezado de opción BER válido), el valor devuelto es **true**.</span><span class="sxs-lookup"><span data-stu-id="d85d9-118">If the function is successful (that is, a valid BER choice header is found) the return value is **TRUE**.</span></span>

<span data-ttu-id="d85d9-119">Si la función no se realiza correctamente, el valor devuelto es **false**.</span><span class="sxs-lookup"><span data-stu-id="d85d9-119">If the function is unsuccessful, the return value is **FALSE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d85d9-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d85d9-120">Requirements</span></span>



| <span data-ttu-id="d85d9-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d85d9-121">Requirement</span></span> | <span data-ttu-id="d85d9-122">Value</span><span class="sxs-lookup"><span data-stu-id="d85d9-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d85d9-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d85d9-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d85d9-124">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="d85d9-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                            |
| <span data-ttu-id="d85d9-125">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d85d9-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d85d9-126">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="d85d9-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="d85d9-127">Encabezado</span><span class="sxs-lookup"><span data-stu-id="d85d9-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d85d9-128"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="d85d9-128"><dt>Netmon.h</dt></span></span> </dl>   |
| <span data-ttu-id="d85d9-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d85d9-129">Library</span></span><br/>                  | <dl> <span data-ttu-id="d85d9-130"><dt>Analizador. lib</dt></span><span class="sxs-lookup"><span data-stu-id="d85d9-130"><dt>Parser.lib</dt></span></span> </dl> |
| <span data-ttu-id="d85d9-131">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d85d9-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d85d9-132"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d85d9-132"><dt>Nmapi.dll</dt></span></span> </dl>  |



 

 




