---
title: DXCoreHardwareID
description: Representa las partes de identificador de hardware de PnP para un adaptador.
ms.localizationpriority: low
ms.topic: reference
ms.date: 06/20/2019
ms.openlocfilehash: 6882d9aa16bf72fb33f9a254a6434becb37f9cb8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/20/2020
ms.locfileid: "104149339"
---
# <a name="dxcorehardwareid-structure"></a><span data-ttu-id="c7e43-103">Estructura DXCoreHardwareID</span><span class="sxs-lookup"><span data-stu-id="c7e43-103">DXCoreHardwareID structure</span></span>

<span data-ttu-id="c7e43-104">Representa las partes de identificador de hardware de PnP para un adaptador.</span><span class="sxs-lookup"><span data-stu-id="c7e43-104">Represents the PnP hardware ID parts for an adapter.</span></span>

## <a name="syntax"></a><span data-ttu-id="c7e43-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="c7e43-105">Syntax</span></span>

```cpp
struct DXCoreHardwareID
{
  uint32_t vendorID;
  uint32_t deviceID;
  uint32_t subSysID;
  uint32_t revision;
};
```

## <a name="members"></a><span data-ttu-id="c7e43-106">Miembros</span><span class="sxs-lookup"><span data-stu-id="c7e43-106">Members</span></span>

### <a name="vendorid"></a><span data-ttu-id="c7e43-107">vendorId</span><span class="sxs-lookup"><span data-stu-id="c7e43-107">vendorId</span></span>

<span data-ttu-id="c7e43-108">Tipo: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="c7e43-108">Type: **uint32_t\***</span></span>

<span data-ttu-id="c7e43-109">IDENTIFICADOR de PCI del proveedor de hardware del adaptador.</span><span class="sxs-lookup"><span data-stu-id="c7e43-109">The PCI ID of the adapter's hardware vendor.</span></span>

### <a name="deviceid"></a><span data-ttu-id="c7e43-110">deviceId</span><span class="sxs-lookup"><span data-stu-id="c7e43-110">deviceId</span></span>

<span data-ttu-id="c7e43-111">Tipo: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="c7e43-111">Type: **uint32_t\***</span></span>

<span data-ttu-id="c7e43-112">IDENTIFICADOR de PCI del dispositivo de hardware del adaptador.</span><span class="sxs-lookup"><span data-stu-id="c7e43-112">The PCI ID of the adapter's hardware device.</span></span>

### <a name="subsysid"></a><span data-ttu-id="c7e43-113">subSysId</span><span class="sxs-lookup"><span data-stu-id="c7e43-113">subSysId</span></span>

<span data-ttu-id="c7e43-114">Tipo: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="c7e43-114">Type: **uint32_t\***</span></span>

<span data-ttu-id="c7e43-115">IDENTIFICADOR de PCI del subsistema de hardware del adaptador.</span><span class="sxs-lookup"><span data-stu-id="c7e43-115">The PCI ID of the adapter's hardware subsystem.</span></span>

### <a name="revision"></a><span data-ttu-id="c7e43-116">revision</span><span class="sxs-lookup"><span data-stu-id="c7e43-116">revision</span></span>

<span data-ttu-id="c7e43-117">Tipo: **uint32_t \***</span><span class="sxs-lookup"><span data-stu-id="c7e43-117">Type: **uint32_t\***</span></span>

<span data-ttu-id="c7e43-118">IDENTIFICADOR de PCI del número de revisión del adaptador.</span><span class="sxs-lookup"><span data-stu-id="c7e43-118">The PCI ID of the adapter's revision number.</span></span>

## <a name="see-also"></a><span data-ttu-id="c7e43-119">Vea también</span><span class="sxs-lookup"><span data-stu-id="c7e43-119">See also</span></span>

<span data-ttu-id="c7e43-120">[Referencia de DXCore](../dxcore-reference.md), [uso de DXCore para enumerar los adaptadores](../dxcore-enum-adapters.md)</span><span class="sxs-lookup"><span data-stu-id="c7e43-120">[DXCore Reference](../dxcore-reference.md), [Using DXCore to enumerate adapters](../dxcore-enum-adapters.md)</span></span>