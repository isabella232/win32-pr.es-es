---
title: Método AddConfig de la interfaz IMsRdpCameraRedirConfigCollection
description: Agrega un objeto IMsRdpCameraRedirConfig a la colección (no es necesario que la cámara correspondiente esté conectada).
ms.tgt_platform: multiple
keywords:
- Método AddConfig Servicios de Escritorio remoto
- Método AddConfig Servicios de Escritorio remoto, interfaz IMsRdpCameraRedirConfigCollection
- Interfaz IMsRdpCameraRedirConfigCollection Servicios de Escritorio remoto, método AddConfig
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection.AddConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: e8c954b710c3f35bca9685d461e478104dac9039
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104536381"
---
# <a name="imsrdpcameraredirconfigcollectionaddconfig-method"></a><span data-ttu-id="1edc0-106">IMsRdpCameraRedirConfigCollection:: AddConfig (método)</span><span class="sxs-lookup"><span data-stu-id="1edc0-106">IMsRdpCameraRedirConfigCollection::AddConfig method</span></span>

<span data-ttu-id="1edc0-107">Agrega un objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) a la colección (no es necesario que la cámara correspondiente esté conectada).</span><span class="sxs-lookup"><span data-stu-id="1edc0-107">Adds an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object to the collection (the corresponding camera does not have to be connected).</span></span>

## <a name="syntax"></a><span data-ttu-id="1edc0-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="1edc0-108">Syntax</span></span>

```C++
HRESULT AddConfig(
    [in] BSTR symbolicLink,
    [in] VARIANT_BOOL fRedirected
);
```

## <a name="parameters"></a><span data-ttu-id="1edc0-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1edc0-109">Parameters</span></span>

<span data-ttu-id="1edc0-110">*symbolicLink* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1edc0-110">*symbolicLink* \[in\]</span></span>

<span data-ttu-id="1edc0-111">Vínculo simbólico para el nuevo objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) .</span><span class="sxs-lookup"><span data-stu-id="1edc0-111">The symbolic link for the new [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object.</span></span>

<span data-ttu-id="1edc0-112">*fRedirected* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="1edc0-112">*fRedirected* \[in\]</span></span>

<span data-ttu-id="1edc0-113">Especifica si la nueva cámara se redirige de forma predeterminada o no.</span><span class="sxs-lookup"><span data-stu-id="1edc0-113">Specifies whether or not the new camera gets redirected by default.</span></span>

## <a name="return-value"></a><span data-ttu-id="1edc0-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1edc0-114">Return value</span></span>

<span data-ttu-id="1edc0-115">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="1edc0-115">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="1edc0-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1edc0-116">Requirements</span></span>

| <span data-ttu-id="1edc0-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="1edc0-117">Requirement</span></span> | <span data-ttu-id="1edc0-118">Value</span><span class="sxs-lookup"><span data-stu-id="1edc0-118">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="1edc0-119">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="1edc0-119">Minimum supported client</span></span>| <span data-ttu-id="1edc0-120">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="1edc0-120">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="1edc0-121">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="1edc0-121">Type library</span></span>            | <span data-ttu-id="1edc0-122">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="1edc0-122">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="1edc0-123">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="1edc0-123">DLL</span></span>                  | <span data-ttu-id="1edc0-124">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="1edc0-124">MsTscAx.dll</span></span>     |
| <span data-ttu-id="1edc0-125">IID</span><span class="sxs-lookup"><span data-stu-id="1edc0-125">IID</span></span>                      | <span data-ttu-id="1edc0-126">IID \_ IMsRdpCameraRedirConfigCollection se define como AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="1edc0-126">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>          |

## <a name="see-also"></a><span data-ttu-id="1edc0-127">Vea también</span><span class="sxs-lookup"><span data-stu-id="1edc0-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1edc0-128">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="1edc0-128">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
</dt> </dl>