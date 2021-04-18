---
title: Propiedad ByIndex de la interfaz IMsRdpCameraRedirConfigCollection
description: Devuelve un objeto IMsRdpCameraRedirConfig por su índice en la colección.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad ByIndex
- Propiedad ByIndex Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfigCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfigCollection, propiedad ByIndex
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.ByIndex
- IMsRdpCameraRedirConfigCollection.get_ByIndex
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 68c179023e93295ee846da22357d5f8efb75b15c
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "105720238"
---
# <a name="imsrdpcameraredirconfigcollectionbyindex-property"></a><span data-ttu-id="f797d-106">IMsRdpCameraRedirConfigCollection:: ByIndex (propiedad)</span><span class="sxs-lookup"><span data-stu-id="f797d-106">IMsRdpCameraRedirConfigCollection::ByIndex property</span></span>

<span data-ttu-id="f797d-107">Devuelve un objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) por su índice en la colección.</span><span class="sxs-lookup"><span data-stu-id="f797d-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object by its index in the collection.</span></span>

<span data-ttu-id="f797d-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="f797d-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="f797d-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="f797d-109">Syntax</span></span>

```C++
HRESULT get_ByIndex(
    [in]            ULONG index,
    [out, retval]   IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="f797d-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="f797d-110">Property value</span></span>

<span data-ttu-id="f797d-111">El objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) que corresponde al índice especificado.</span><span class="sxs-lookup"><span data-stu-id="f797d-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified index.</span></span>

## <a name="requirements"></a><span data-ttu-id="f797d-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f797d-112">Requirements</span></span>

| <span data-ttu-id="f797d-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="f797d-113">Requirement</span></span> | <span data-ttu-id="f797d-114">Value</span><span class="sxs-lookup"><span data-stu-id="f797d-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="f797d-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="f797d-115">Minimum supported client</span></span>| <span data-ttu-id="f797d-116">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="f797d-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="f797d-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="f797d-117">Type library</span></span>            | <span data-ttu-id="f797d-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f797d-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="f797d-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="f797d-119">DLL</span></span>                  | <span data-ttu-id="f797d-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="f797d-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="f797d-121">IID</span><span class="sxs-lookup"><span data-stu-id="f797d-121">IID</span></span>                      | <span data-ttu-id="f797d-122">IID \_ IMsRdpCameraRedirConfigCollection se define como AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="f797d-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="f797d-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="f797d-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f797d-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="f797d-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>