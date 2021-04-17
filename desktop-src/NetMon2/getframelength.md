---
description: La función GetFrameLength devuelve la longitud del marco.
ms.assetid: 30be1f5c-9b13-42ad-944a-92b1aee8a6bc
title: Función GetFrameLength (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameLength
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 29a2a08ac105414a914e14a9ce8e69976725700c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105666281"
---
# <a name="getframelength-function"></a><span data-ttu-id="2f1b0-103">GetFrameLength función)</span><span class="sxs-lookup"><span data-stu-id="2f1b0-103">GetFrameLength function</span></span>

<span data-ttu-id="2f1b0-104">La función **GetFrameLength** devuelve la longitud del marco.</span><span class="sxs-lookup"><span data-stu-id="2f1b0-104">The **GetFrameLength** function returns the length of the frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f1b0-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="2f1b0-105">Syntax</span></span>


```C++
DWORD WINAPI GetFrameLength(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="2f1b0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="2f1b0-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f1b0-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="2f1b0-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f1b0-108">Identificador de un marco.</span><span class="sxs-lookup"><span data-stu-id="2f1b0-108">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f1b0-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2f1b0-109">Return value</span></span>

<span data-ttu-id="2f1b0-110">Si la función se realiza correctamente, el valor devuelto es la longitud del marco en bytes.</span><span class="sxs-lookup"><span data-stu-id="2f1b0-110">If the function is successful, the return value is the length of the frame   in bytes.</span></span>

<span data-ttu-id="2f1b0-111">Si la función no se realiza correctamente, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="2f1b0-111">If the function is unsuccessful, the return value is zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="2f1b0-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="2f1b0-112">Remarks</span></span>

<span data-ttu-id="2f1b0-113">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrameLength** .</span><span class="sxs-lookup"><span data-stu-id="2f1b0-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameLength** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f1b0-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f1b0-114">Requirements</span></span>



| <span data-ttu-id="2f1b0-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f1b0-115">Requirement</span></span> | <span data-ttu-id="2f1b0-116">Value</span><span class="sxs-lookup"><span data-stu-id="2f1b0-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="2f1b0-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f1b0-117">Minimum supported client</span></span><br/> | <span data-ttu-id="2f1b0-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="2f1b0-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="2f1b0-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="2f1b0-119">Minimum supported server</span></span><br/> | <span data-ttu-id="2f1b0-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="2f1b0-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="2f1b0-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="2f1b0-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="2f1b0-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="2f1b0-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="2f1b0-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f1b0-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="2f1b0-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f1b0-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="2f1b0-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="2f1b0-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2f1b0-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2f1b0-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




