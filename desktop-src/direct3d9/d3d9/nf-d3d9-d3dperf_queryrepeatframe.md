---
title: D3DPERF_QueryRepeatFrame función)
description: Determine si un generador de perfiles de rendimiento solicita que el marco actual se vuelva a enviar a Direct3D para el análisis de rendimiento. Esta función no es compatible actualmente con PIX.
ms.localizationpriority: low
ms.topic: reference
ms.date: 04/06/2020
req.lib: d3d9.lib
req.dll: d3d9.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d9.dll
api_name:
- D3DPERF_QueryRepeatFrame
targetos: Windows
ms.openlocfilehash: c4054a0704fd0258483ee0d3d3d555cb5eabe7f9
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2020
ms.locfileid: "103789046"
---
# <a name="d3dperf_queryrepeatframe-function"></a><span data-ttu-id="99a2f-104">D3DPERF_QueryRepeatFrame función)</span><span class="sxs-lookup"><span data-stu-id="99a2f-104">D3DPERF_QueryRepeatFrame function</span></span>

<span data-ttu-id="99a2f-105">Determine si un generador de perfiles de rendimiento solicita que el marco actual se vuelva a enviar a Direct3D para el análisis de rendimiento.</span><span class="sxs-lookup"><span data-stu-id="99a2f-105">Determine whether a performance profiler is requesting that the current frame be resubmitted to Direct3D for performance analysis.</span></span> <span data-ttu-id="99a2f-106">Esta función no es compatible actualmente con PIX.</span><span class="sxs-lookup"><span data-stu-id="99a2f-106">This function is not currently supported by PIX.</span></span>

## <a name="syntax"></a><span data-ttu-id="99a2f-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="99a2f-107">Syntax</span></span>

```cpp
BOOL WINAPI D3DPERF_QueryRepeatFrame( void );
```

## <a name="return-value"></a><span data-ttu-id="99a2f-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="99a2f-108">Return value</span></span>

<span data-ttu-id="99a2f-109">Si el valor devuelto es TRUE, el llamador debe repetir la misma secuencia de llamadas.</span><span class="sxs-lookup"><span data-stu-id="99a2f-109">If the return value is TRUE, the caller should repeat the same sequence of calls.</span></span> <span data-ttu-id="99a2f-110">Si es FALSE, el llamador debe continuar.</span><span class="sxs-lookup"><span data-stu-id="99a2f-110">If FALSE, the caller should continue.</span></span>

## <a name="remarks"></a><span data-ttu-id="99a2f-111">Observaciones</span><span class="sxs-lookup"><span data-stu-id="99a2f-111">Remarks</span></span>

<span data-ttu-id="99a2f-112">Se debe llamar a la función inmediatamente después de que se llame a **IDirect3DDevice9::P reenviar** .</span><span class="sxs-lookup"><span data-stu-id="99a2f-112">The function should be called immediately after **IDirect3DDevice9::Present** is called.</span></span>

## <a name="requirements"></a><span data-ttu-id="99a2f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="99a2f-113">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="99a2f-114">**Plataforma de destino**</span><span class="sxs-lookup"><span data-stu-id="99a2f-114">**Target Platform**</span></span> | <span data-ttu-id="99a2f-115">Windows</span><span class="sxs-lookup"><span data-stu-id="99a2f-115">Windows</span></span> |
| <span data-ttu-id="99a2f-116">**Header**</span><span class="sxs-lookup"><span data-stu-id="99a2f-116">**Header**</span></span> | <span data-ttu-id="99a2f-117">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="99a2f-117">d3d9.h</span></span> |
| <span data-ttu-id="99a2f-118">**Library**</span><span class="sxs-lookup"><span data-stu-id="99a2f-118">**Library**</span></span> | <span data-ttu-id="99a2f-119">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="99a2f-119">d3d9.lib</span></span> |
| <span data-ttu-id="99a2f-120">**DLL**</span><span class="sxs-lookup"><span data-stu-id="99a2f-120">**DLL**</span></span> | <span data-ttu-id="99a2f-121">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="99a2f-121">d3d9.dll</span></span> |