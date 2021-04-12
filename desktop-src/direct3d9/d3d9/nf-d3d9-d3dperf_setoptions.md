---
title: D3DPERF_SetOptions función)
description: Establezca las opciones del generador de perfiles especificadas por el programa de destino.
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
- D3DPERF_SetOptions
targetos: Windows
ms.openlocfilehash: 8bd877469864ccdaa833ce80d00eb06ae5fc18de
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2020
ms.locfileid: "104487330"
---
# <a name="d3dperf_setoptions-function"></a><span data-ttu-id="058c8-103">D3DPERF_SetOptions función)</span><span class="sxs-lookup"><span data-stu-id="058c8-103">D3DPERF_SetOptions function</span></span>

<span data-ttu-id="058c8-104">Establezca las opciones del generador de perfiles especificadas por el programa de destino.</span><span class="sxs-lookup"><span data-stu-id="058c8-104">Set profiler options specified by the target program.</span></span>

## <a name="syntax"></a><span data-ttu-id="058c8-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="058c8-105">Syntax</span></span>

```cpp
int WINAPI D3DPERF_SetOptions(
  DWORD dwOptions
);
```

## <a name="parameters"></a><span data-ttu-id="058c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="058c8-106">Parameters</span></span>

`dwOptions`

<span data-ttu-id="058c8-107">Opciones de usuario reconocibles por PIX.</span><span class="sxs-lookup"><span data-stu-id="058c8-107">User options recognizable by PIX.</span></span> <span data-ttu-id="058c8-108">Establézcalo en 1 para notificar a PIX que el programa de destino no concede permiso para el que se va a crear el archivo.</span><span class="sxs-lookup"><span data-stu-id="058c8-108">Set this to 1 to notify PIX that the target program does not give permission to be profiled.</span></span>

## <a name="return-value"></a><span data-ttu-id="058c8-109">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="058c8-109">Return value</span></span>

<span data-ttu-id="058c8-110">Esta función no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="058c8-110">This function doesn't return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="058c8-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="058c8-111">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="058c8-112">**Plataforma de destino**</span><span class="sxs-lookup"><span data-stu-id="058c8-112">**Target Platform**</span></span> | <span data-ttu-id="058c8-113">Windows</span><span class="sxs-lookup"><span data-stu-id="058c8-113">Windows</span></span> |
| <span data-ttu-id="058c8-114">**Header**</span><span class="sxs-lookup"><span data-stu-id="058c8-114">**Header**</span></span> | <span data-ttu-id="058c8-115">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="058c8-115">d3d9.h</span></span> |
| <span data-ttu-id="058c8-116">**Library**</span><span class="sxs-lookup"><span data-stu-id="058c8-116">**Library**</span></span> | <span data-ttu-id="058c8-117">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="058c8-117">d3d9.lib</span></span> |
| <span data-ttu-id="058c8-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="058c8-118">**DLL**</span></span> | <span data-ttu-id="058c8-119">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="058c8-119">d3d9.dll</span></span> |