---
UID: ''
title: CaptureStackBackTrace función)
description: Captura un seguimiento de la pila de retroceso recorriendo la pila.
old-location: ''
ms.assetid: na
ms.date: 04/10/2019
ms.keywords: RtlCaptureStackBackTrace
ms.topic: reference
req.header: WinBase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps | UWP apps]
req.kmdf-ver: ''
req.umdf-ver: ''
req.ddi-compliance: ''
req.unicode-ansi: ''
req.idl: ''
req.max-support: ''
req.namespace: ''
req.assembly: ''
req.type-library: ''
req.lib: Kernel32.lib
req.dll: API-MS-Win-Core-rtlsupport-l1-1-0.dll
req.irql: ''
topic_type:
- APIRef
api_type: ''
api_location:
- API-MS-Win-Core-rtlsupport-l1-1-0.dll
api_name:
- CaptureStackBackTrace
targetos: Windows
req.typenames: ''
req.redist: ''
ms.openlocfilehash: 3c9edc9184000d513b82ad4131e3ac05c2ed22d6
ms.sourcegitcommit: 1f6a1bfc1c4bb2641bc3ba44beb1f2727c94681b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2020
ms.locfileid: "105656307"
---
# <a name="capturestackbacktrace-function"></a><span data-ttu-id="97d11-103">CaptureStackBackTrace función)</span><span class="sxs-lookup"><span data-stu-id="97d11-103">CaptureStackBackTrace function</span></span>

## <a name="description"></a><span data-ttu-id="97d11-104">Descripción</span><span class="sxs-lookup"><span data-stu-id="97d11-104">Description</span></span>

<span data-ttu-id="97d11-105">Captura un seguimiento de la pila de retroceso recorriendo la pila y grabando la información de cada fotograma.</span><span class="sxs-lookup"><span data-stu-id="97d11-105">Captures a stack back trace by walking up the stack and recording the information for each frame.</span></span>

```cpp
USHORT WINAPI CaptureStackBackTrace(
  _In_      ULONG  FramesToSkip,
  _In_      ULONG  FramesToCapture,
  _Out_     PVOID  *BackTrace,
  _Out_opt_ PULONG BackTraceHash
);
```

## <a name="parameters"></a><span data-ttu-id="97d11-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97d11-106">Parameters</span></span>

### <a name="framestoskip-in"></a><span data-ttu-id="97d11-107">FramesToSkip [in]</span><span class="sxs-lookup"><span data-stu-id="97d11-107">FramesToSkip [in]</span></span>

<span data-ttu-id="97d11-108">Número de fotogramas que se van a omitir desde el inicio del seguimiento de la copia de seguridad.</span><span class="sxs-lookup"><span data-stu-id="97d11-108">The number of frames to skip from the start of the back trace.</span></span>

### <a name="framestocapture-in"></a><span data-ttu-id="97d11-109">FramesToCapture [in]</span><span class="sxs-lookup"><span data-stu-id="97d11-109">FramesToCapture [in]</span></span>

<span data-ttu-id="97d11-110">Número de fotogramas que se van a capturar.</span><span class="sxs-lookup"><span data-stu-id="97d11-110">The number of frames to be captured.</span></span>
<span data-ttu-id="97d11-111">Puede capturar hasta **MAXUSHORT** fotogramas.</span><span class="sxs-lookup"><span data-stu-id="97d11-111">You can capture up to **MAXUSHORT** frames.</span></span>

<span data-ttu-id="97d11-112">**Windows Server 2003 y Windows XP:**  La suma de los parámetros *FramesToSkip* y *FramesToCapture* debe ser inferior a 63.</span><span class="sxs-lookup"><span data-stu-id="97d11-112">**Windows Server 2003 and Windows XP:**  The sum of the *FramesToSkip* and *FramesToCapture* parameters must be less than 63.</span></span>

### <a name="backtrace-out"></a><span data-ttu-id="97d11-113">Paseguir [out]</span><span class="sxs-lookup"><span data-stu-id="97d11-113">BackTrace [out]</span></span>

<span data-ttu-id="97d11-114">Matriz de punteros capturados del seguimiento de pila actual.</span><span class="sxs-lookup"><span data-stu-id="97d11-114">An array of pointers captured from the current stack trace.</span></span>

### <a name="backtracehash-out-optional"></a><span data-ttu-id="97d11-115">BackTraceHash [out, opcional]</span><span class="sxs-lookup"><span data-stu-id="97d11-115">BackTraceHash [out, optional]</span></span>

<span data-ttu-id="97d11-116">Valor que se puede utilizar para organizar las tablas hash.</span><span class="sxs-lookup"><span data-stu-id="97d11-116">A value that can be used to organize hash tables.</span></span>
<span data-ttu-id="97d11-117">Si este parámetro es **null**, no se calcula ningún valor hash.</span><span class="sxs-lookup"><span data-stu-id="97d11-117">If this parameter is **NULL**, then no hash value is computed.</span></span>

<span data-ttu-id="97d11-118">Este valor se calcula en función de los valores de los punteros devueltos en la matriz de subseguimiento.</span><span class="sxs-lookup"><span data-stu-id="97d11-118">This value is calculated based on the values of the pointers returned in the BackTrace array.</span></span>
<span data-ttu-id="97d11-119">Dos seguimientos de pila idénticos generarán valores hash idénticos.</span><span class="sxs-lookup"><span data-stu-id="97d11-119">Two identical stack traces will generate identical hash values.</span></span>

## <a name="returns"></a><span data-ttu-id="97d11-120">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="97d11-120">Returns</span></span>

<span data-ttu-id="97d11-121">Número de fotogramas capturados.</span><span class="sxs-lookup"><span data-stu-id="97d11-121">The number of captured frames.</span></span>

## <a name="remarks"></a><span data-ttu-id="97d11-122">Observaciones</span><span class="sxs-lookup"><span data-stu-id="97d11-122">Remarks</span></span>

<span data-ttu-id="97d11-123">La función **CaptureStackBackTrace** se define como la función **RtlCaptureStackBackTrace** (la definición se incluye en el Windows SDK a partir de Windows Vista).</span><span class="sxs-lookup"><span data-stu-id="97d11-123">The **CaptureStackBackTrace** function is defined as the **RtlCaptureStackBackTrace** function (the definition is included in the Windows SDK beginning with Windows Vista).</span></span>
<span data-ttu-id="97d11-124">Para obtener más información, vea WinBase. h y Winnt. h.</span><span class="sxs-lookup"><span data-stu-id="97d11-124">For more information, see WinBase.h and WinNT.h.</span></span>

## <a name="see-also"></a><span data-ttu-id="97d11-125">Vea también</span><span class="sxs-lookup"><span data-stu-id="97d11-125">See also</span></span>
