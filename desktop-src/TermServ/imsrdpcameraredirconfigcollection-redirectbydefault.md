---
title: Propiedad RedirectByDefault de la interfaz IMsRdpCameraRedirConfigCollection
description: Especifica si cualquier cámara nueva se redirige de forma predeterminada.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectByDefault
- Propiedad RedirectByDefault Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfigCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfigCollection, propiedad RedirectByDefault
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.RedirectByDefault
- IMsRdpCameraRedirConfigCollection.put_RedirectByDefault
- IMsRdpCameraRedirConfigCollection.get_RedirectByDefault
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 810af200eefee0008aea21af684c02b6d31325eb
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104151924"
---
# <a name="imsrdpcameraredirconfigcollectionredirectbydefault-property"></a><span data-ttu-id="9ea83-106">IMsRdpCameraRedirConfigCollection:: RedirectByDefault (propiedad)</span><span class="sxs-lookup"><span data-stu-id="9ea83-106">IMsRdpCameraRedirConfigCollection::RedirectByDefault property</span></span>

<span data-ttu-id="9ea83-107">Especifica si cualquier cámara nueva se redirige de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9ea83-107">Specifies whether or not any new camera gets redirected by default.</span></span>

<span data-ttu-id="9ea83-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="9ea83-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ea83-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="9ea83-109">Syntax</span></span>

```C++
HRESULT put_RedirectByDefault(
    [in] VARIANT_BOOL fRedirect
);

HRESULT get_RedirectByDefault(
    [out, retval] VARIANT_BOOL* pfRedirect
);
```

## <a name="property-value"></a><span data-ttu-id="9ea83-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="9ea83-110">Property value</span></span>

<span data-ttu-id="9ea83-111">Un valor que indica si cualquier cámara nueva se redirige de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="9ea83-111">A value that indicates whether or not any new camera gets redirected by default.</span></span>

## <a name="requirements"></a><span data-ttu-id="9ea83-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9ea83-112">Requirements</span></span>

| <span data-ttu-id="9ea83-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="9ea83-113">Requirement</span></span> | <span data-ttu-id="9ea83-114">Value</span><span class="sxs-lookup"><span data-stu-id="9ea83-114">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="9ea83-115">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9ea83-115">Minimum supported client</span></span>| <span data-ttu-id="9ea83-116">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="9ea83-116">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="9ea83-117">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9ea83-117">Type library</span></span>            | <span data-ttu-id="9ea83-118">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="9ea83-118">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="9ea83-119">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9ea83-119">DLL</span></span>                  | <span data-ttu-id="9ea83-120">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="9ea83-120">MsTscAx.dll</span></span>     |
| <span data-ttu-id="9ea83-121">IID</span><span class="sxs-lookup"><span data-stu-id="9ea83-121">IID</span></span>                      | <span data-ttu-id="9ea83-122">IID \_ IMsRdpCameraRedirConfigCollection se define como AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="9ea83-122">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="9ea83-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="9ea83-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ea83-124">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="9ea83-124">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>