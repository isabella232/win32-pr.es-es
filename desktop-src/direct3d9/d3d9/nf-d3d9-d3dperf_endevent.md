---
title: D3DPERF_EndEvent función)
description: Marca el final de un evento definido por el usuario. PIX puede utilizar este evento para desencadenar una acción.
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
- D3DPERF_EndEvent
targetos: Windows
ms.openlocfilehash: 91c2a6a19b926cd9f5549fae084ce8973432b0f2
ms.sourcegitcommit: 517a888e0370b9ec64c451635f12d60245ff5ae3
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/08/2020
ms.locfileid: "104420399"
---
# <a name="d3dperf_endevent-function"></a><span data-ttu-id="a4601-104">D3DPERF_EndEvent función)</span><span class="sxs-lookup"><span data-stu-id="a4601-104">D3DPERF_EndEvent function</span></span>

<span data-ttu-id="a4601-105">Marca el final de un evento definido por el usuario.</span><span class="sxs-lookup"><span data-stu-id="a4601-105">Marks the end of a user-defined event.</span></span> <span data-ttu-id="a4601-106">PIX puede utilizar este evento para desencadenar una acción.</span><span class="sxs-lookup"><span data-stu-id="a4601-106">PIX can use this event to trigger an action.</span></span>

## <a name="syntax"></a><span data-ttu-id="a4601-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="a4601-107">Syntax</span></span>

```cpp
int WINAPI D3DPERF_EndEvent(void);
```

## <a name="return-value"></a><span data-ttu-id="a4601-108">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a4601-108">Return value</span></span>

<span data-ttu-id="a4601-109">Nivel de la jerarquía en la que el evento finaliza.</span><span class="sxs-lookup"><span data-stu-id="a4601-109">The level of the hierarchy in which the event is ending.</span></span> <span data-ttu-id="a4601-110">Si se produce un error, este valor es negativo.</span><span class="sxs-lookup"><span data-stu-id="a4601-110">If an error occurs, this value is negative.</span></span>

## <a name="requirements"></a><span data-ttu-id="a4601-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a4601-111">Requirements</span></span>
| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="a4601-112">**Plataforma de destino**</span><span class="sxs-lookup"><span data-stu-id="a4601-112">**Target Platform**</span></span> | <span data-ttu-id="a4601-113">Windows</span><span class="sxs-lookup"><span data-stu-id="a4601-113">Windows</span></span> |
| <span data-ttu-id="a4601-114">**Header**</span><span class="sxs-lookup"><span data-stu-id="a4601-114">**Header**</span></span> | <span data-ttu-id="a4601-115">d3d9. h</span><span class="sxs-lookup"><span data-stu-id="a4601-115">d3d9.h</span></span> |
| <span data-ttu-id="a4601-116">**Library**</span><span class="sxs-lookup"><span data-stu-id="a4601-116">**Library**</span></span> | <span data-ttu-id="a4601-117">d3d9. lib</span><span class="sxs-lookup"><span data-stu-id="a4601-117">d3d9.lib</span></span> |
| <span data-ttu-id="a4601-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="a4601-118">**DLL**</span></span> | <span data-ttu-id="a4601-119">d3d9.dll</span><span class="sxs-lookup"><span data-stu-id="a4601-119">d3d9.dll</span></span> |