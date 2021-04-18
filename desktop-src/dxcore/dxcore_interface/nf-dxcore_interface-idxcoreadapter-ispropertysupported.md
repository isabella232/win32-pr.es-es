---
title: IDXCoreAdapter::IsPropertySupported
description: Determina si este objeto de adaptador de DXCore y el sistema operativo actual admiten la propiedad de adaptador especificada.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: b960d96515d4aee85520a6def70a8f0e9349e131
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "105720162"
---
# <a name="idxcoreadapterispropertysupported-method"></a><span data-ttu-id="b0a5a-103">IDXCoreAdapter:: IsPropertySupported (método)</span><span class="sxs-lookup"><span data-stu-id="b0a5a-103">IDXCoreAdapter::IsPropertySupported method</span></span>

<span data-ttu-id="b0a5a-104">Determina si este objeto de adaptador de DXCore y el sistema operativo actual admiten la propiedad de adaptador especificada.</span><span class="sxs-lookup"><span data-stu-id="b0a5a-104">Determines whether this DXCore adapter object and the current operating system (OS) support the specified adapter property.</span></span>

## <a name="syntax"></a><span data-ttu-id="b0a5a-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b0a5a-105">Syntax</span></span>

```cpp
virtual bool STDMETHODCALLTYPE IsPropertySupported( 
  DXCoreAdapterProperty property) = 0;
```

## <a name="parameters"></a><span data-ttu-id="b0a5a-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b0a5a-106">Parameters</span></span>

### <a name="property"></a><span data-ttu-id="b0a5a-107">propiedad</span><span class="sxs-lookup"><span data-stu-id="b0a5a-107">property</span></span>

<span data-ttu-id="b0a5a-108">Tipo: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span><span class="sxs-lookup"><span data-stu-id="b0a5a-108">Type: **[DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md)**</span></span>

<span data-ttu-id="b0a5a-109">Tipo de propiedad que se va a consultar sobre la compatibilidad con.</span><span class="sxs-lookup"><span data-stu-id="b0a5a-109">The type of property that you're querying about support for.</span></span> <span data-ttu-id="b0a5a-110">Vea la tabla en [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) para obtener más información sobre cada propiedad del adaptador.</span><span class="sxs-lookup"><span data-stu-id="b0a5a-110">See the table in [DXCoreAdapterProperty](./ne-dxcore_interface-dxcoreadapterproperty.md) for more info about each adapter property.</span></span>

## <a name="returns"></a><span data-ttu-id="b0a5a-111">Devoluciones</span><span class="sxs-lookup"><span data-stu-id="b0a5a-111">Returns</span></span>

<span data-ttu-id="b0a5a-112">Tipo: **bool**</span><span class="sxs-lookup"><span data-stu-id="b0a5a-112">Type: **bool**</span></span>

<span data-ttu-id="b0a5a-113">Devuelve  `true`   si este objeto de adaptador de DXCore y el sistema operativo actual admiten la propiedad de adaptador especificada.</span><span class="sxs-lookup"><span data-stu-id="b0a5a-113">Returns `true` if this DXCore adapter object and the current operating system (OS) support the specified adapter property.</span></span> <span data-ttu-id="b0a5a-114">De lo contrario, devuelve  `false` .</span><span class="sxs-lookup"><span data-stu-id="b0a5a-114">Otherwise, returns `false`.</span></span>

## <a name="see-also"></a><span data-ttu-id="b0a5a-115">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0a5a-115">See also</span></span>

<span data-ttu-id="b0a5a-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore GUID Attribute GUID](../dxcore-adapter-attribute-guids.md), [using DXCore to Enumerate Adapters](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="b0a5a-116">[IDXCoreAdapter](./nn-dxcore_interface-idxcoreadapter.md), [DXCore Reference](../dxcore-reference.md), [DXCore adapter attribute GUIDs](../dxcore-adapter-attribute-guids.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>