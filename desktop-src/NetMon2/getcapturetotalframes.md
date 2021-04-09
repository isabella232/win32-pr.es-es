---
description: La función GetCaptureTotalFrames devuelve el número total de fotogramas de la captura.
ms.assetid: a2b7902c-b80f-4a0a-b12a-2a139df30fca
title: Función GetCaptureTotalFrames (Netmon. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCaptureTotalFrames
api_type:
- DllExport
api_location:
- Nmapi.dll
ms.openlocfilehash: aa7c81e690e9f7eab258c832ae374f18f9b7afc7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907673"
---
# <a name="getcapturetotalframes-function"></a><span data-ttu-id="b2b48-103">GetCaptureTotalFrames función)</span><span class="sxs-lookup"><span data-stu-id="b2b48-103">GetCaptureTotalFrames function</span></span>

<span data-ttu-id="b2b48-104">La función **GetCaptureTotalFrames** devuelve el número total de fotogramas de la captura.</span><span class="sxs-lookup"><span data-stu-id="b2b48-104">The **GetCaptureTotalFrames** function returns the total number of frames in the capture.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2b48-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b2b48-105">Syntax</span></span>


```C++
DWORD WINAPI GetCaptureTotalFrames(
  _In_ HCAPTURE hCapture
);
```



## <a name="parameters"></a><span data-ttu-id="b2b48-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b2b48-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b2b48-107">*hCapture* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="b2b48-107">*hCapture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b2b48-108">Identificador de la captura.</span><span class="sxs-lookup"><span data-stu-id="b2b48-108">Handle to the capture.</span></span> <span data-ttu-id="b2b48-109">Para obtener información acerca de cómo obtener el identificador de captura, vea la sección Comentarios de este tema **GetCaptureTotalFrames** .</span><span class="sxs-lookup"><span data-stu-id="b2b48-109">For information about obtaining the capture handle, see the Remarks section of this **GetCaptureTotalFrames** topic.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b2b48-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b2b48-110">Return value</span></span>

<span data-ttu-id="b2b48-111">Si la función se realiza correctamente, el valor devuelto es el número total de fotogramas de la captura.</span><span class="sxs-lookup"><span data-stu-id="b2b48-111">If the function is successful, the return value is the total number of frames in the capture.</span></span>

<span data-ttu-id="b2b48-112">Si la función no se realiza correctamente, el valor devuelto es 0.</span><span class="sxs-lookup"><span data-stu-id="b2b48-112">If the function is unsuccessful, the return value is 0.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2b48-113">Observaciones</span><span class="sxs-lookup"><span data-stu-id="b2b48-113">Remarks</span></span>

<span data-ttu-id="b2b48-114">Los [*expertos*](e.md) y [*analizadores*](p.md) pueden llamar a la función **GetCaptureTotalFrames** .</span><span class="sxs-lookup"><span data-stu-id="b2b48-114">[*Experts*](e.md) and [*parsers*](p.md) can call the **GetCaptureTotalFrames** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2b48-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2b48-115">Requirements</span></span>



| <span data-ttu-id="b2b48-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2b48-116">Requirement</span></span> | <span data-ttu-id="b2b48-117">Value</span><span class="sxs-lookup"><span data-stu-id="b2b48-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b2b48-118">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2b48-118">Minimum supported client</span></span><br/> | <span data-ttu-id="b2b48-119">\[Solo aplicaciones de escritorio\] de Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="b2b48-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="b2b48-120">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b2b48-120">Minimum supported server</span></span><br/> | <span data-ttu-id="b2b48-121">\[Solo aplicaciones de escritorio\] de Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="b2b48-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="b2b48-122">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b2b48-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="b2b48-123"><dt>Netmon. h</dt></span><span class="sxs-lookup"><span data-stu-id="b2b48-123"><dt>Netmon.h</dt></span></span> </dl>  |
| <span data-ttu-id="b2b48-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2b48-124">Library</span></span><br/>                  | <dl> <span data-ttu-id="b2b48-125"><dt>Nmapi. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b2b48-125"><dt>Nmapi.lib</dt></span></span> </dl> |
| <span data-ttu-id="b2b48-126">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b2b48-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b2b48-127"><dt>Nmapi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b2b48-127"><dt>Nmapi.dll</dt></span></span> </dl> |



 

 




