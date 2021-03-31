---
description: La función GetFrameNumber devuelve el número de un marco.
ms.assetid: 97d343a3-2a1e-47d7-bfc2-b63f8d84b29d
title: Función GetFrameNumber (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameNumber
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: de04fa513fab98b1a82d036f6f40a6c67cdda3ed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000930"
---
# <a name="getframenumber-function"></a><span data-ttu-id="0137f-103">GetFrameNumber función)</span><span class="sxs-lookup"><span data-stu-id="0137f-103">GetFrameNumber function</span></span>

<span data-ttu-id="0137f-104">La función **GetFrameNumber** devuelve el número de un marco.</span><span class="sxs-lookup"><span data-stu-id="0137f-104">The **GetFrameNumber** function returns the number of a frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="0137f-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0137f-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameNumber(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="0137f-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="0137f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0137f-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="0137f-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0137f-108">Identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="0137f-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0137f-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="0137f-109">Return value</span></span>

<span data-ttu-id="0137f-110">Si la función se realiza correctamente, el valor devuelto es un número de marco basado en cero.</span><span class="sxs-lookup"><span data-stu-id="0137f-110">If the function is successful, the return value is a zero-based frame number.</span></span>

<span data-ttu-id="0137f-111">Si la función no es correcta, el valor devuelto es menos uno (-1).</span><span class="sxs-lookup"><span data-stu-id="0137f-111">If the function is not successful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="0137f-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="0137f-112">Remarks</span></span>

<span data-ttu-id="0137f-113">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrameNumber** .</span><span class="sxs-lookup"><span data-stu-id="0137f-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameNumber** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="0137f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0137f-114">Requirements</span></span>



| <span data-ttu-id="0137f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0137f-115">Requirement</span></span> | <span data-ttu-id="0137f-116">Value</span><span class="sxs-lookup"><span data-stu-id="0137f-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="0137f-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0137f-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0137f-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="0137f-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="0137f-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="0137f-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0137f-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="0137f-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="0137f-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0137f-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0137f-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="0137f-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="0137f-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0137f-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="0137f-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="0137f-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="0137f-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0137f-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0137f-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0137f-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




