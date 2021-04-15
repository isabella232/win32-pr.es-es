---
title: Método SendLocation3D de la interfaz IMsRdpClientNonScriptable6
description: Envía un valor de latitud, longitud y altitud al servidor para que la ubicación geográfica del cliente se pueda reflejar en la sesión remota.
ms.tgt_platform: multiple
keywords:
- Método SendLocation3D Servicios de Escritorio remoto
- Método SendLocation3D Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable6
- Interfaz IMsRdpClientNonScriptable6 Servicios de Escritorio remoto, método SendLocation3D
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable6.SendLocation3D
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: c63e779b6d6d090544af40a7ee6d9c05f8c49494
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104494146"
---
# <a name="imsrdpclientnonscriptable6sendlocation3d-method"></a><span data-ttu-id="509a4-106">IMsRdpClientNonScriptable6:: SendLocation3D (método)</span><span class="sxs-lookup"><span data-stu-id="509a4-106">IMsRdpClientNonScriptable6::SendLocation3D method</span></span>

<span data-ttu-id="509a4-107">Envía un valor de latitud, longitud y altitud al servidor para que la ubicación geográfica del cliente se pueda reflejar en la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="509a4-107">Sends a latitude, longitude and altitude value to the server so the client’s geographic location can be reflected in the remote session.</span></span>

## <a name="syntax"></a><span data-ttu-id="509a4-108">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="509a4-108">Syntax</span></span>

```C++
HRESULT SendLocation3D(
  [in] DOUBLE latitude,
  [in] DOUBLE longitude,
  [in] INT32 altitude
);
```

## <a name="parameters"></a><span data-ttu-id="509a4-109">Parámetros</span><span class="sxs-lookup"><span data-stu-id="509a4-109">Parameters</span></span>

<span data-ttu-id="509a4-110">*latitud* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="509a4-110">*latitude* \[in\]</span></span>

<span data-ttu-id="509a4-111">La latitud de una ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="509a4-111">The latitude of a geographic location.</span></span> <span data-ttu-id="509a4-112">El intervalo válido de valores de latitud es de-90,0 a 90,0 grados.</span><span class="sxs-lookup"><span data-stu-id="509a4-112">The valid range of latitude values is from -90.0 to 90.0 degrees.</span></span>

<span data-ttu-id="509a4-113">*longitud* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="509a4-113">*longitude* \[in\]</span></span>

<span data-ttu-id="509a4-114">Longitud de una ubicación geográfica.</span><span class="sxs-lookup"><span data-stu-id="509a4-114">The longitude of a geographic location.</span></span> <span data-ttu-id="509a4-115">El intervalo válido de valores de latitud es de-180,0 a 180,0 grados.</span><span class="sxs-lookup"><span data-stu-id="509a4-115">The valid range of latitude values is from -180.0 to 180.0 degrees.</span></span>

<span data-ttu-id="509a4-116">*altitud* \[ de\]</span><span class="sxs-lookup"><span data-stu-id="509a4-116">*altitude* \[in\]</span></span>

<span data-ttu-id="509a4-117">La altitud de una ubicación geográfica en metros.</span><span class="sxs-lookup"><span data-stu-id="509a4-117">The altitude of a geographic location in meters.</span></span>

## <a name="return-value"></a><span data-ttu-id="509a4-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="509a4-118">Return value</span></span>

<span data-ttu-id="509a4-119">Vuelva **a \_ Aceptar si es** correcto.</span><span class="sxs-lookup"><span data-stu-id="509a4-119">Return **S\_OK** if successful.</span></span>

## <a name="requirements"></a><span data-ttu-id="509a4-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="509a4-120">Requirements</span></span>

| <span data-ttu-id="509a4-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="509a4-121">Requirement</span></span> | <span data-ttu-id="509a4-122">Value</span><span class="sxs-lookup"><span data-stu-id="509a4-122">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="509a4-123">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="509a4-123">Minimum supported client</span></span>| <span data-ttu-id="509a4-124">Windows 10, versión 1709 (compilación 16299)</span><span class="sxs-lookup"><span data-stu-id="509a4-124">Windows 10, version 1709 (build 16299)</span></span>      |
| <span data-ttu-id="509a4-125">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="509a4-125">Type library</span></span>            | <span data-ttu-id="509a4-126">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="509a4-126">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="509a4-127">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="509a4-127">DLL</span></span>                  | <span data-ttu-id="509a4-128">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="509a4-128">MsTscAx.dll</span></span>     |
| <span data-ttu-id="509a4-129">IID</span><span class="sxs-lookup"><span data-stu-id="509a4-129">IID</span></span>                      | <span data-ttu-id="509a4-130">IID \_ IMsRdpClientNonScriptable6 se define como 05293249-B28B-4DB8-BE64-1B2F496B910E</span><span class="sxs-lookup"><span data-stu-id="509a4-130">IID\_IMsRdpClientNonScriptable6 is defined as 05293249-B28B-4DB8-BE64-1B2F496B910E</span></span>            |

## <a name="see-also"></a><span data-ttu-id="509a4-131">Vea también</span><span class="sxs-lookup"><span data-stu-id="509a4-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="509a4-132">**IMsRdpClientNonScriptable6**</span><span class="sxs-lookup"><span data-stu-id="509a4-132">**IMsRdpClientNonScriptable6**</span></span>](imsrdpclientnonscriptable6.md)
</dt> </dl>
