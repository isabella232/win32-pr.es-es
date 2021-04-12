---
title: D3DPERF_GetStatus función)
description: Determine el estado actual del generador de perfiles desde el programa de destino.
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
- D3DPERF_GetStatus
targetos: Windows
ms.openlocfilehash: 626d56dd449b0a0aa92e85c82dabda119900680d
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2020
ms.locfileid: "104358750"
---
# <a name="d3dperf_getstatus-function"></a><span data-ttu-id="80b0e-103">D3DPERF_GetStatus función)</span><span class="sxs-lookup"><span data-stu-id="80b0e-103">D3DPERF_GetStatus function</span></span>

<span data-ttu-id="80b0e-104">Determine el estado actual del generador de perfiles desde el programa de destino.</span><span class="sxs-lookup"><span data-stu-id="80b0e-104">Determine the current state of the profiler from the target program.</span></span>

## <a name="syntax"></a><span data-ttu-id="80b0e-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="80b0e-105">Syntax</span></span>

```cpp
DWORD WINAPI D3DPERF_GetStatus( void );
```

## <a name="return-value"></a><span data-ttu-id="80b0e-106">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="80b0e-106">Return value</span></span>

<span data-ttu-id="80b0e-107">Un valor distinto de cero cuando PIX está generando perfiles del programa de destino; de lo contrario, es cero.</span><span class="sxs-lookup"><span data-stu-id="80b0e-107">A non-zero value when PIX is profiling the target program; otherwise, zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="80b0e-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="80b0e-108">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="80b0e-109">**Plataforma de destino**</span><span class="sxs-lookup"><span data-stu-id="80b0e-109">**Target Platform**</span></span> | <span data-ttu-id="80b0e-110">Windows</span><span class="sxs-lookup"><span data-stu-id="80b0e-110">Windows</span></span> |
| <span data-ttu-id="80b0e-111">**Header**</span><span class="sxs-lookup"><span data-stu-id="80b0e-111">**Header**</span></span> | <span data-ttu-id="80b0e-112">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="80b0e-112">d3d9.h</span></span> |
| <span data-ttu-id="80b0e-113">**Library**</span><span class="sxs-lookup"><span data-stu-id="80b0e-113">**Library**</span></span> | <span data-ttu-id="80b0e-114">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="80b0e-114">d3d9.lib</span></span> |
| <span data-ttu-id="80b0e-115">**DLL**</span><span class="sxs-lookup"><span data-stu-id="80b0e-115">**DLL**</span></span> | <span data-ttu-id="80b0e-116">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="80b0e-116">d3d9.dll</span></span> |