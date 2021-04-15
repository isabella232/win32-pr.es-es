---
title: Propiedad ByInstanceId de la interfaz IMsRdpCameraRedirConfigCollection
description: Devuelve un objeto IMsRdpCameraRedirConfig de la colección que corresponde al identificador de instancia especificado.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ByInstanceId
- Propiedad ByInstanceId Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfigCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfigCollection, propiedad ByInstanceId
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByInstanceId
- IMsRdpCameraRedirConfigCollection.get_ByInstanceId
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d90cb7d2f309a3df9e354ace04a840b667e5569b
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104494147"
---
# <a name="imsrdpcameraredirconfigcollectionbyinstanceid-property"></a><span data-ttu-id="3f378-106">IMsRdpCameraRedirConfigCollection:: ByInstanceId (propiedad)</span><span class="sxs-lookup"><span data-stu-id="3f378-106">IMsRdpCameraRedirConfigCollection::ByInstanceId property</span></span>

<span data-ttu-id="3f378-107">Devuelve un objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la colección que corresponde al identificador de instancia especificado.</span><span class="sxs-lookup"><span data-stu-id="3f378-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the specified instance ID.</span></span>

<span data-ttu-id="3f378-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="3f378-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f378-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="3f378-109">Syntax</span></span>

```C++
HRESULT get_ByInstanceId(
    [in]          BSTR instanceId,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="3f378-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="3f378-110">Property value</span></span>

<span data-ttu-id="3f378-111">El objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) que corresponde al identificador de instancia especificado.</span><span class="sxs-lookup"><span data-stu-id="3f378-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified instance ID.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f378-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f378-112">Requirements</span></span>

| <span data-ttu-id="3f378-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f378-113">Requirement</span></span> | <span data-ttu-id="3f378-114">Value</span><span class="sxs-lookup"><span data-stu-id="3f378-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="3f378-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="3f378-115">Minimum supported client</span></span>| <span data-ttu-id="3f378-116">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="3f378-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="3f378-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="3f378-117">Type library</span></span>            | <span data-ttu-id="3f378-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="3f378-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="3f378-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="3f378-119">DLL</span></span>                  | <span data-ttu-id="3f378-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="3f378-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="3f378-121">IID</span><span class="sxs-lookup"><span data-stu-id="3f378-121">IID</span></span>                      | <span data-ttu-id="3f378-122">IID \_ IMsRdpCameraRedirConfigCollection se define como AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="3f378-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="3f378-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="3f378-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f378-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="3f378-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>