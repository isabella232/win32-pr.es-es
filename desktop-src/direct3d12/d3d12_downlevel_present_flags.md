---
title: Enumeración D3D12_DOWNLEVEL_PRESENT_FLAGS
description: Marcas pasadas a ID3D12CommandQueueDownlevel::P método reenviado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/29/2019
topic_type:
- APIRef
api_name:
- D3D12_DOWNLEVEL_PRESENT_FLAGS
api_type:
- HeaderDef
ms.openlocfilehash: 1ce1536945748bae09fc7a0981c14c076fc6394e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/15/2021
ms.locfileid: "105721438"
---
# <a name="d3d12_downlevel_present_flags-enumeration"></a><span data-ttu-id="0406a-103">D3D12 \_ \_ enumeración de marcas de presencia de nivel inferior \_</span><span class="sxs-lookup"><span data-stu-id="0406a-103">D3D12\_DOWNLEVEL\_PRESENT\_FLAGS enumeration</span></span>

<span data-ttu-id="0406a-104">Marcas pasadas a [**ID3D12CommandQueueDownlevel::P función reenviar**](id3d12commandqueuedownlevel-present.md) para modificar el comportamiento.</span><span class="sxs-lookup"><span data-stu-id="0406a-104">Flags passed to the [**ID3D12CommandQueueDownlevel::Present**](id3d12commandqueuedownlevel-present.md) function to modify behavior.</span></span>

## <a name="syntax"></a><span data-ttu-id="0406a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="0406a-105">Syntax</span></span>

```cpp
enum D3D12_DOWNLEVEL_PRESENT_FLAGS
{
    D3D12_DOWNLEVEL_PRESENT_FLAG_NONE = 0,
    D3D12_DOWNLEVEL_PRESENT_FLAG_WAIT_FOR_VBLANK = 1
};
```

## <a name="constants"></a><span data-ttu-id="0406a-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="0406a-106">Constants</span></span>

<span data-ttu-id="0406a-107">**Marca de D3D12 de \_ nivel inferior \_ presente \_ \_ ninguno**</span><span class="sxs-lookup"><span data-stu-id="0406a-107">**D3D12\_DOWNLEVEL\_PRESENT\_FLAG\_NONE**</span></span>

<span data-ttu-id="0406a-108">No hay opciones seleccionadas.</span><span class="sxs-lookup"><span data-stu-id="0406a-108">No options selected.</span></span>

<span data-ttu-id="0406a-109">**D3D12 \_ \_ \_ marca de presentación \_ de nivel inferior \_ de espera para \_ VBLANK**</span><span class="sxs-lookup"><span data-stu-id="0406a-109">**D3D12\_DOWNLEVEL\_PRESENT\_FLAG\_WAIT\_FOR\_VBLANK**</span></span>

<span data-ttu-id="0406a-110">La operación **present** no se realizará hasta que se haya producido una sincronización de errores desde la última vez que **presente** el Ed.</span><span class="sxs-lookup"><span data-stu-id="0406a-110">The **Present** operation won't be done until a VSync has occurred since the last time you **Present** ed.</span></span>

## <a name="requirements"></a><span data-ttu-id="0406a-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0406a-111">Requirements</span></span>

| <span data-ttu-id="0406a-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="0406a-112">Requirement</span></span> | <span data-ttu-id="0406a-113">Value</span><span class="sxs-lookup"><span data-stu-id="0406a-113">Value</span></span> |
|--------|------------------|
| <span data-ttu-id="0406a-114">Encabezado</span><span class="sxs-lookup"><span data-stu-id="0406a-114">Header</span></span> | <span data-ttu-id="0406a-115">d3d12downlevel. h</span><span class="sxs-lookup"><span data-stu-id="0406a-115">d3d12downlevel.h</span></span> |
| <span data-ttu-id="0406a-116">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="0406a-116">DLL</span></span>    | <span data-ttu-id="0406a-117">D3D12.dll (solo Windows 7)</span><span class="sxs-lookup"><span data-stu-id="0406a-117">D3D12.dll (Windows 7 only)</span></span> |

## <a name="see-also"></a><span data-ttu-id="0406a-118">Vea también</span><span class="sxs-lookup"><span data-stu-id="0406a-118">See also</span></span>
* [<span data-ttu-id="0406a-119">ID3D12CommandQueueDownlevel</span><span class="sxs-lookup"><span data-stu-id="0406a-119">ID3D12CommandQueueDownlevel</span></span>](id3d12commandqueuedownlevel.md)
* [<span data-ttu-id="0406a-120">Enumeraciones de Direct3D 12 en Windows 7</span><span class="sxs-lookup"><span data-stu-id="0406a-120">Direct3D 12 On Windows 7 enumerations</span></span>](direct3d-12on7-enumerations.md)
* [<span data-ttu-id="0406a-121">Referencia de Direct3D 12 en Windows 7 (d3d12downlevel. h)</span><span class="sxs-lookup"><span data-stu-id="0406a-121">Direct3D 12 on Windows 7 reference (d3d12downlevel.h)</span></span>](direct3d-12on7-reference.md)
* [<span data-ttu-id="0406a-122">Direct3D 12 en Windows 7</span><span class="sxs-lookup"><span data-stu-id="0406a-122">Direct3D 12 On Windows 7</span></span>](https://devblogs.microsoft.com/directx/porting-directx-12-games-to-windows-7/)
