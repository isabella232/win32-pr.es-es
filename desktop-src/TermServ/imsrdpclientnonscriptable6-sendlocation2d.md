---
title: Método SendLocation2D de la interfaz IMsRdpClientNonScriptable6
description: Envía un valor de latitud y longitud al servidor para que la ubicación geográfica del cliente se pueda reflejar en la sesión remota.
ms.tgt_platform: multiple
keywords:
- Método SendLocation2D Servicios de Escritorio remoto
- Método SendLocation2D Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable6
- Interfaz IMsRdpClientNonScriptable6 Servicios de Escritorio remoto, método SendLocation2D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation2D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: b706fdb35ba8360b294d25021c0c1a18bbe90188
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "103805156"
---
# <a name="imsrdpclientnonscriptable6sendlocation2d-method"></a><span data-ttu-id="7bc24-106">IMsRdpClientNonScriptable6:: SendLocation2D (método)</span><span class="sxs-lookup"><span data-stu-id="7bc24-106">IMsRdpClientNonScriptable6::SendLocation2D method</span></span>

<span data-ttu-id="7bc24-107">Envía un valor de latitud y longitud al servidor para que la ubicación geográfica del cliente se pueda reflejar en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="7bc24-107">Sends a latitude and longitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="7bc24-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="7bc24-108">Syntax</span></span>

```C++
HRESULT SendLocation2D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude
);
```

## <a name="parameters"></a><span data-ttu-id="7bc24-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="7bc24-109">Parameters</span></span>

<span data-ttu-id="7bc24-110">*latitud* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7bc24-110">*latitude* \[in\]</span></span>

<span data-ttu-id="7bc24-111">La latitud de una ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="7bc24-111">The latitude of a geographic location.</span></span> <span data-ttu-id="7bc24-112">El intervalo válido de valores de latitud es de-90,0 a 90,0 grados.</span><span class="sxs-lookup"><span data-stu-id="7bc24-112">The valid range of latitude values is from -90.0 to 90.0 degrees.</span></span>

<span data-ttu-id="7bc24-113">*longitud* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="7bc24-113">*longitude* \[in\]</span></span>

<span data-ttu-id="7bc24-114">Longitud de una ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="7bc24-114">The longitude of a geographic location.</span></span> <span data-ttu-id="7bc24-115">El intervalo válido de valores de latitud es de-180,0 a 180,0 grados.</span><span class="sxs-lookup"><span data-stu-id="7bc24-115">The valid range of latitude values is from -180.0 to 180.0 degrees.</span></span>

## <a name="return-value"></a><span data-ttu-id="7bc24-116">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="7bc24-116">Return value</span></span>

<span data-ttu-id="7bc24-117">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="7bc24-117">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="7bc24-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7bc24-118">Requirements</span></span>

| <span data-ttu-id="7bc24-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="7bc24-119">Requirement</span></span> | <span data-ttu-id="7bc24-120">Value</span><span class="sxs-lookup"><span data-stu-id="7bc24-120">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="7bc24-121">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="7bc24-121">Minimum supported client</span></span>| <span data-ttu-id="7bc24-122">Windows 10, versión 1709 (compilación 16299)</span><span class="sxs-lookup"><span data-stu-id="7bc24-122">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="7bc24-123">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="7bc24-123">Type library</span></span>            | <span data-ttu-id="7bc24-124">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="7bc24-124">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="7bc24-125">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="7bc24-125">DLL</span></span>                  | <span data-ttu-id="7bc24-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="7bc24-126">MsTscAx.dll</span></span>     |
| <span data-ttu-id="7bc24-127">IID</span><span class="sxs-lookup"><span data-stu-id="7bc24-127">IID</span></span>                      | <span data-ttu-id="7bc24-128">IID \_ IMsRdpClientNonScriptable6 se define como 05293249-B28B-4DB8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="7bc24-128">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="7bc24-129">Vea también</span><span class="sxs-lookup"><span data-stu-id="7bc24-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7bc24-130">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="7bc24-130">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
