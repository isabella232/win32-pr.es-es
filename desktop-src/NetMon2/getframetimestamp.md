---
description: La función GetFrameTimeStamp devuelve la marca de tiempo de un fotograma determinado.
ms.assetid: 4ac50400-6674-40fa-9a69-9c0ccb55b92c
title: Función GetFrameTimeStamp (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameTimeStamp
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 37a75f946a5fc0ddb2b32d99334368a272fdf2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/08/2021
ms.locfileid: "105667549"
---
# <a name="getframetimestamp-function"></a><span data-ttu-id="1a2a6-103">GetFrameTimeStamp función)</span><span class="sxs-lookup"><span data-stu-id="1a2a6-103">GetFrameTimeStamp function</span></span>

<span data-ttu-id="1a2a6-104">La función **GetFrameTimeStamp** devuelve la marca de tiempo de un fotograma determinado.</span><span class="sxs-lookup"><span data-stu-id="1a2a6-104">The **GetFrameTimeStamp** function returns the time stamp of a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="1a2a6-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1a2a6-105">Syntax</span></span>


```C++
__int64 WINAPI GetFrameTimeStamp(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="1a2a6-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1a2a6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a2a6-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1a2a6-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1a2a6-108">Identificador del marco.</span><span class="sxs-lookup"><span data-stu-id="1a2a6-108">Handle to the frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a2a6-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1a2a6-109">Return value</span></span>

<span data-ttu-id="1a2a6-110">Si la función se realiza correctamente, el valor devuelto es la marca de tiempo del marco en microsegundos.</span><span class="sxs-lookup"><span data-stu-id="1a2a6-110">If the function is successful, the return value is the time stamp of the frame   in microseconds.</span></span>

<span data-ttu-id="1a2a6-111">Si la función no se realiza correctamente, el valor devuelto es menos uno (-1).</span><span class="sxs-lookup"><span data-stu-id="1a2a6-111">If the function is unsuccessful, the return value is minus one (-1).</span></span>

## <a name="remarks"></a><span data-ttu-id="1a2a6-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="1a2a6-112">Remarks</span></span>

<span data-ttu-id="1a2a6-113">La función **GetFrameTimeStamp** devuelve una marca de tiempo que muestra el tiempo transcurrido entre el inicio del proceso de captura y la grabación del marco.</span><span class="sxs-lookup"><span data-stu-id="1a2a6-113">The **GetFrameTimeStamp** function returns a time stamp that shows the elapsed time between the start of the capture process, and the recording of the frame.</span></span>

<span data-ttu-id="1a2a6-114">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrameTimeStamp** .</span><span class="sxs-lookup"><span data-stu-id="1a2a6-114">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameTimeStamp** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="1a2a6-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1a2a6-115">Requirements</span></span>



| <span data-ttu-id="1a2a6-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="1a2a6-116">Requirement</span></span> | <span data-ttu-id="1a2a6-117">Value</span><span class="sxs-lookup"><span data-stu-id="1a2a6-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1a2a6-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a2a6-118">Minimum supported client</span></span><br/> | <span data-ttu-id="1a2a6-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1a2a6-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="1a2a6-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1a2a6-120">Minimum supported server</span></span><br/> | <span data-ttu-id="1a2a6-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1a2a6-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="1a2a6-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="1a2a6-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="1a2a6-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="1a2a6-123"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="1a2a6-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1a2a6-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="1a2a6-125"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="1a2a6-125"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="1a2a6-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1a2a6-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1a2a6-127"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1a2a6-127"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




