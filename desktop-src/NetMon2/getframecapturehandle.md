---
description: La función GetFrameCaptureHandle devuelve un identificador a la captura basada en un fotograma determinado.
ms.assetid: 71b32799-194c-40f8-8438-36aebaba31c7
title: Función GetFrameCaptureHandle (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetFrameCaptureHandle
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: 3770ad0fd3db7d1c076b5d1f286c1fdbdc2707a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907671"
---
# <a name="getframecapturehandle-function"></a><span data-ttu-id="b1363-103">GetFrameCaptureHandle función)</span><span class="sxs-lookup"><span data-stu-id="b1363-103">GetFrameCaptureHandle function</span></span>

<span data-ttu-id="b1363-104">La función **GetFrameCaptureHandle** devuelve un identificador a la captura basada en un fotograma determinado.</span><span class="sxs-lookup"><span data-stu-id="b1363-104">The **GetFrameCaptureHandle** function returns a handle to the capture based on a given frame.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1363-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b1363-105">Syntax</span></span>


```C++
HCAPTURE WINAPI GetFrameCaptureHandle(
  _In_ HFRAME hFrame
);
```



## <a name="parameters"></a><span data-ttu-id="b1363-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b1363-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1363-107">*hFrame* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b1363-107">*hFrame* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1363-108">Identificador de un marco.</span><span class="sxs-lookup"><span data-stu-id="b1363-108">Handle to a frame.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1363-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b1363-109">Return value</span></span>

<span data-ttu-id="b1363-110">Si la función se realiza correctamente, el valor devuelto es un identificador de la captura.</span><span class="sxs-lookup"><span data-stu-id="b1363-110">If the function is successful, the return value is a handle to the capture.</span></span>

<span data-ttu-id="b1363-111">Si la función no se realiza correctamente, el valor devuelto es 0.</span><span class="sxs-lookup"><span data-stu-id="b1363-111">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="b1363-112">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b1363-112">Remarks</span></span>

<span data-ttu-id="b1363-113">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetFrameCaptureHandle** .</span><span class="sxs-lookup"><span data-stu-id="b1363-113">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetFrameCaptureHandle** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1363-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b1363-114">Requirements</span></span>



| <span data-ttu-id="b1363-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="b1363-115">Requirement</span></span> | <span data-ttu-id="b1363-116">Value</span><span class="sxs-lookup"><span data-stu-id="b1363-116">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b1363-117">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1363-117">Minimum supported client</span></span><br/> | <span data-ttu-id="b1363-118">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b1363-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b1363-119">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b1363-119">Minimum supported server</span></span><br/> | <span data-ttu-id="b1363-120">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b1363-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b1363-121">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b1363-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="b1363-122"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b1363-122"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b1363-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b1363-123">Library</span></span><br/>                  | <dl> <span data-ttu-id="b1363-124"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1363-124"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b1363-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b1363-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b1363-126"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b1363-126"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




