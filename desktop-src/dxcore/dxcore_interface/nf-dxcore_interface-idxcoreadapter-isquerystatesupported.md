---
title: IDXCoreAdapter::IsQueryStateSupported
description: Determina si este objeto de adaptador de DXCore y el sistema operativo actual admiten la consulta del valor del estado del adaptador especificado.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: d154597f9b3ddbec24cff230317d881b9595bcde
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149474"
---
# <a name="idxcoreadapterisquerystatesupported-method"></a><span data-ttu-id="f8d8a-103">IDXCoreAdapter:: IsQueryStateSupported (método)</span><span class="sxs-lookup"><span data-stu-id="f8d8a-103">IDXCoreAdapter::IsQueryStateSupported method</span></span>

<span data-ttu-id="f8d8a-104">Determina si este objeto de adaptador de DXCore y el sistema operativo actual admiten la consulta del valor del estado del adaptador especificado.</span><span class="sxs-lookup"><span data-stu-id="f8d8a-104">Determines whether this DXCore adapter object and the current operating system (OS) support querying the value of the specified adapter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8d8a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f8d8a-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsQueryStateSupported( 
  DXCoreAdapterState property) = 0;
```

## <a name="parameters"></a><span data-ttu-id="f8d8a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="f8d8a-106">Parameters</span></span>

### <a name="state"></a><span data-ttu-id="f8d8a-107">state</span><span class="sxs-lookup"><span data-stu-id="f8d8a-107">state</span></span>

<span data-ttu-id="f8d8a-108">Tipo: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span><span class="sxs-lookup"><span data-stu-id="f8d8a-108">Type: **[DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md)**</span></span>

<span data-ttu-id="f8d8a-109">El tipo de elemento de estado que está consultando sobre la compatibilidad con.</span><span class="sxs-lookup"><span data-stu-id="f8d8a-109">The kind of state item that you're querying about support for.</span></span> <span data-ttu-id="f8d8a-110">Vea la tabla en [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) para obtener más información sobre cada tipo de estado del adaptador.</span><span class="sxs-lookup"><span data-stu-id="f8d8a-110">See the table in [DXCoreAdapterState](./ne-dxcore_interface-dxcoreadapterstate.md) for more info about each adapter state kind.</span></span>

## <a name="returns"></a><span data-ttu-id="f8d8a-111">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="f8d8a-111">Returns</span></span>

<span data-ttu-id="f8d8a-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="f8d8a-112">Type: **bool**</span></span>

<span data-ttu-id="f8d8a-113">Devuelve  `true`   si este objeto de adaptador de DXCore y el sistema operativo actual admiten consultas en el estado del adaptador especificado.</span><span class="sxs-lookup"><span data-stu-id="f8d8a-113">Returns `true` if this DXCore adapter object and the current operating system (OS) support querying the specified adapter state.</span></span> <span data-ttu-id="f8d8a-114">De lo contrario, devuelve  `false` .</span><span class="sxs-lookup"><span data-stu-id="f8d8a-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="f8d8a-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="f8d8a-115">See also</span></span>

<span data-ttu-id="f8d8a-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore GUID Attribute GUID](../dxcore-adapter-attribute-guids.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="f8d8a-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>