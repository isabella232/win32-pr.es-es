---
title: D3DPERF_SetRegion función)
description: Marque una serie de fotogramas con el color y el nombre especificados en el archivo PIXRun. Esta función no es compatible actualmente con PIX.
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
- D3DPERF_SetRegion
targetos: Windows
ms.openlocfilehash: 650cc6063865da5ce30b97ed1468c1718ace5da6
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2020
ms.locfileid: "105720137"
---
# <a name="d3dperf_setregion-function"></a><span data-ttu-id="c03ff-104">D3DPERF_SetRegion función)</span><span class="sxs-lookup"><span data-stu-id="c03ff-104">D3DPERF_SetRegion function</span></span>

<span data-ttu-id="c03ff-105">Marque una serie de fotogramas con el color y el nombre especificados en el archivo PIXRun.</span><span class="sxs-lookup"><span data-stu-id="c03ff-105">Mark a series of frames with the specified color and name in the PIXRun file.</span></span> <span data-ttu-id="c03ff-106">Esta función no es compatible actualmente con PIX.</span><span class="sxs-lookup"><span data-stu-id="c03ff-106">This function is not currently supported by PIX.</span></span>

## <a name="syntax"></a><span data-ttu-id="c03ff-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c03ff-107">Syntax</span></span>

```cpp
void WINAPI D3DPERF_SetRegion(
  D3DCOLOR col,
  LPCWSTR wszName
);
```

## <a name="parameters"></a><span data-ttu-id="c03ff-108">Parámetros</span><span class="sxs-lookup"><span data-stu-id="c03ff-108">Parameters</span></span>

`col`

<span data-ttu-id="c03ff-109">Color del evento.</span><span class="sxs-lookup"><span data-stu-id="c03ff-109">Event color.</span></span> <span data-ttu-id="c03ff-110">Este es el color para mostrar el evento en la vista de eventos.</span><span class="sxs-lookup"><span data-stu-id="c03ff-110">This is the color to display the event in the event view.</span></span>

`wszName`

<span data-ttu-id="c03ff-111">Nombre del evento.</span><span class="sxs-lookup"><span data-stu-id="c03ff-111">Event name.</span></span>

## <a name="return-value"></a><span data-ttu-id="c03ff-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="c03ff-112">Return value</span></span>

<span data-ttu-id="c03ff-113">Esta función no devuelve un valor.</span><span class="sxs-lookup"><span data-stu-id="c03ff-113">This function doesn't return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c03ff-114">Observaciones</span><span class="sxs-lookup"><span data-stu-id="c03ff-114">Remarks</span></span>

<span data-ttu-id="c03ff-115">Para facilitar el análisis, el programa de destino puede usar el color para marcar cada nivel de un programa de destino.</span><span class="sxs-lookup"><span data-stu-id="c03ff-115">To make analysis easier, the target program can use color to mark each level of a target program.</span></span>

## <a name="requirements"></a><span data-ttu-id="c03ff-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c03ff-116">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="c03ff-117">**Plataforma de destino**</span><span class="sxs-lookup"><span data-stu-id="c03ff-117">**Target Platform**</span></span> | <span data-ttu-id="c03ff-118">Windows</span><span class="sxs-lookup"><span data-stu-id="c03ff-118">Windows</span></span> |
| <span data-ttu-id="c03ff-119">**Header**</span><span class="sxs-lookup"><span data-stu-id="c03ff-119">**Header**</span></span> | <span data-ttu-id="c03ff-120">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="c03ff-120">d3d9.h</span></span> |
| <span data-ttu-id="c03ff-121">**Library**</span><span class="sxs-lookup"><span data-stu-id="c03ff-121">**Library**</span></span> | <span data-ttu-id="c03ff-122">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="c03ff-122">d3d9.lib</span></span> |
| <span data-ttu-id="c03ff-123">**DLL**</span><span class="sxs-lookup"><span data-stu-id="c03ff-123">**DLL**</span></span> | <span data-ttu-id="c03ff-124">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="c03ff-124">d3d9.dll</span></span> |