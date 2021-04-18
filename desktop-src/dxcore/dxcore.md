---
title: DXCore
description: DXCore es una API de enumeración de adaptadores para dispositivos DirectX.
ms.localizationpriority: high
ms.topic: article
ms.date: 06/20/2019
ms.openlocfilehash: 80e93ac7440629a809cb01b4d1d4fa2e73b7ee91
ms.sourcegitcommit: aa021b23d7e8bba2e1df9de93a1c315a17681810
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/10/2020
ms.locfileid: "105720202"
---
# <a name="dxcore"></a><span data-ttu-id="ffdd0-103">DXCore</span><span class="sxs-lookup"><span data-stu-id="ffdd0-103">DXCore</span></span>

<span data-ttu-id="ffdd0-104">DXCore es una API de enumeración de adaptadores para dispositivos de proceso y gráficos, por lo que algunas de sus funciones se superponen con las de [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span><span class="sxs-lookup"><span data-stu-id="ffdd0-104">DXCore is an adapter enumeration API for graphics and compute devices, so some of its facilities overlap with those of [DXGI](../direct3ddxgi/dx-graphics-dxgi.md).</span></span> <span data-ttu-id="ffdd0-105">Direct3D 12 usa DXCore.</span><span class="sxs-lookup"><span data-stu-id="ffdd0-105">DXCore is used by Direct3D 12.</span></span>

<span data-ttu-id="ffdd0-106">Este conjunto de documentación contiene información sobre la programación con DXCore, así como la referencia de DXCore.</span><span class="sxs-lookup"><span data-stu-id="ffdd0-106">This documentation set contains information about programming with DXCore, as well as the DXCore reference.</span></span>

## <a name="requirements"></a><span data-ttu-id="ffdd0-107">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ffdd0-107">Requirements</span></span>

| &nbsp; | &nbsp; |
| ---- |:---- |
| <span data-ttu-id="ffdd0-108">**Entornos de tiempo de ejecución compatibles**</span><span class="sxs-lookup"><span data-stu-id="ffdd0-108">**Supported runtime environments**</span></span> | <span data-ttu-id="ffdd0-109">Windows/C++</span><span class="sxs-lookup"><span data-stu-id="ffdd0-109">Windows/C++</span></span> |
| <span data-ttu-id="ffdd0-110">**Idiomas de programación recomendados**</span><span class="sxs-lookup"><span data-stu-id="ffdd0-110">**Recommended programming languages**</span></span> | <span data-ttu-id="ffdd0-111">C++</span><span class="sxs-lookup"><span data-stu-id="ffdd0-111">C++</span></span> |
| <span data-ttu-id="ffdd0-112">**Cliente mínimo compatible**</span><span class="sxs-lookup"><span data-stu-id="ffdd0-112">**Minimum supported client**</span></span> | <span data-ttu-id="ffdd0-113">Windows 10, versión 2004 (10,0; Compilación 19041)</span><span class="sxs-lookup"><span data-stu-id="ffdd0-113">Windows 10, version 2004 (10.0; Build 19041)</span></span> |
| <span data-ttu-id="ffdd0-114">**Header**</span><span class="sxs-lookup"><span data-stu-id="ffdd0-114">**Header**</span></span> | <span data-ttu-id="ffdd0-115">dxcore. h y dxcore_interface. h</span><span class="sxs-lookup"><span data-stu-id="ffdd0-115">dxcore.h and dxcore_interface.h</span></span> |
| <span data-ttu-id="ffdd0-116">**Library**</span><span class="sxs-lookup"><span data-stu-id="ffdd0-116">**Library**</span></span> | <span data-ttu-id="ffdd0-117">dxcore. lib</span><span class="sxs-lookup"><span data-stu-id="ffdd0-117">dxcore.lib</span></span> |
| <span data-ttu-id="ffdd0-118">**DLL**</span><span class="sxs-lookup"><span data-stu-id="ffdd0-118">**DLL**</span></span> | <span data-ttu-id="ffdd0-119">dxcore.dll</span><span class="sxs-lookup"><span data-stu-id="ffdd0-119">dxcore.dll</span></span> |

## <a name="in-this-section"></a><span data-ttu-id="ffdd0-120">En esta sección</span><span class="sxs-lookup"><span data-stu-id="ffdd0-120">In this section</span></span>

| <span data-ttu-id="ffdd0-121">Tema</span><span class="sxs-lookup"><span data-stu-id="ffdd0-121">Topic</span></span> | <span data-ttu-id="ffdd0-122">Descripción</span><span class="sxs-lookup"><span data-stu-id="ffdd0-122">Description</span></span> |
|-|-|
| [<span data-ttu-id="ffdd0-123">Guía de programación de DXCore</span><span class="sxs-lookup"><span data-stu-id="ffdd0-123">DXCore programming guide</span></span>](dxcore-programming-guide.md) | <span data-ttu-id="ffdd0-124">Instrucciones para programar con DXCore.</span><span class="sxs-lookup"><span data-stu-id="ffdd0-124">Guidance for programming with DXCore.</span></span> |
| [<span data-ttu-id="ffdd0-125">Referencia de DXCore</span><span class="sxs-lookup"><span data-stu-id="ffdd0-125">DXCore reference</span></span>](dxcore-reference.md) | <span data-ttu-id="ffdd0-126">En esta sección se tratan las API de DXCore declaradas en DXCore. h y dxcore_interface. h.</span><span class="sxs-lookup"><span data-stu-id="ffdd0-126">This section covers DXCore APIs declared in dxcore.h and dxcore_interface.h.</span></span> |
