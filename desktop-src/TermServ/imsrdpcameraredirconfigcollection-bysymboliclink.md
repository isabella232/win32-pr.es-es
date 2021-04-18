---
title: Propiedad BySymbolicLink de la interfaz IMsRdpCameraRedirConfigCollection
description: Devuelve un objeto IMsRdpCameraRedirConfig de la colección que corresponde al vínculo simbólico especificado de la interfaz **KSCATEGORY_VIDEO_CAMERA** de la cámara.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad BySymbolicLink
- Propiedad BySymbolicLink Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfigCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfigCollection, propiedad BySymbolicLink
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.BySymbolicLink
- IMsRdpCameraRedirConfigCollection.get_BySymbolicLink
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: d4888c7e468e0522240d8ef922563ab28eb33e77
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "105720242"
---
# <a name="imsrdpcameraredirconfigcollectionbysymboliclink-property"></a><span data-ttu-id="ebe96-106">IMsRdpCameraRedirConfigCollection::. Propiedad BySymbolicLink</span><span class="sxs-lookup"><span data-stu-id="ebe96-106">IMsRdpCameraRedirConfigCollection::.BySymbolicLink property</span></span>

<span data-ttu-id="ebe96-107">Devuelve un objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la colección que corresponde al vínculo simbólico especificado de la interfaz **KSCATEGORY_VIDEO_CAMERA** de la cámara.</span><span class="sxs-lookup"><span data-stu-id="ebe96-107">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the given symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>

<span data-ttu-id="ebe96-108">Esta propiedad es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="ebe96-108">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe96-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ebe96-109">Syntax</span></span>

```C++
HRESULT get_BySymbolicLink(
    [in]          BSTR symbolicLink,
    [out, retval] IMsRdpCameraRedirConfig** ppConfig
);
```

## <a name="property-value"></a><span data-ttu-id="ebe96-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="ebe96-110">Property value</span></span>

<span data-ttu-id="ebe96-111">El objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) que corresponde al vínculo simbólico especificado.</span><span class="sxs-lookup"><span data-stu-id="ebe96-111">The [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object that corresponds to the specified symbolic link.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebe96-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ebe96-112">Requirements</span></span>

| <span data-ttu-id="ebe96-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="ebe96-113">Requirement</span></span> | <span data-ttu-id="ebe96-114">Value</span><span class="sxs-lookup"><span data-stu-id="ebe96-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="ebe96-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="ebe96-115">Minimum supported client</span></span>| <span data-ttu-id="ebe96-116">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="ebe96-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="ebe96-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="ebe96-117">Type library</span></span>            | <span data-ttu-id="ebe96-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="ebe96-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="ebe96-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="ebe96-119">DLL</span></span>                  | <span data-ttu-id="ebe96-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="ebe96-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="ebe96-121">IID</span><span class="sxs-lookup"><span data-stu-id="ebe96-121">IID</span></span>                      | <span data-ttu-id="ebe96-122">IID \_ IMsRdpCameraRedirConfigCollection se define como AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="ebe96-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="ebe96-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="ebe96-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe96-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="ebe96-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>