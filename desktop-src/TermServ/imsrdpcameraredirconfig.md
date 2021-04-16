---
title: Interfaz IMsRdpCameraRedirConfig
description: Representa las configuraciones de una cámara que está disponible para la redirección.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfig
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfig, descrito
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfig
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: fbb0f3344e0653ea4a87c876bb8ca7b8a67e7d21
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104536382"
---
# <a name="imsrdpcameraredirconfig-interface"></a><span data-ttu-id="9e668-105">Interfaz IMsRdpCameraRedirConfig</span><span class="sxs-lookup"><span data-stu-id="9e668-105">IMsRdpCameraRedirConfig interface</span></span>

<span data-ttu-id="9e668-106">Representa las configuraciones de una cámara que está disponible para la redirección.</span><span class="sxs-lookup"><span data-stu-id="9e668-106">Represents the configurations for a camera that is available for redirection.</span></span>

## <a name="members"></a><span data-ttu-id="9e668-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="9e668-107">Members</span></span>

<span data-ttu-id="9e668-108">La interfaz **IMsRdpCameraRedirConfig** hereda de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="9e668-108">The **IMsRdpCameraRedirConfig** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="9e668-109">**IMsRdpCameraRedirConfig** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="9e668-109">**IMsRdpCameraRedirConfig** also has these types of members:</span></span>

- [<span data-ttu-id="9e668-110">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9e668-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9e668-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="9e668-111">Properties</span></span>

<span data-ttu-id="9e668-112">La interfaz **IMsRdpCameraRedirConfig** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="9e668-112">The **IMsRdpCameraRedirConfig** interface has these properties.</span></span>

| <span data-ttu-id="9e668-113">Propiedad</span><span class="sxs-lookup"><span data-stu-id="9e668-113">Property</span></span>         | <span data-ttu-id="9e668-114">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="9e668-114">Access type</span></span>           | <span data-ttu-id="9e668-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e668-115">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="9e668-116">**DeviceExists**</span><span class="sxs-lookup"><span data-stu-id="9e668-116">**DeviceExists**</span></span>](imsrdpcameraredirconfig-deviceexists.md)      | <span data-ttu-id="9e668-117">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e668-117">Read-only</span></span> | <span data-ttu-id="9e668-118">Especifica si el dispositivo de cámara existe actualmente (es decir, si la cámara está conectada).</span><span class="sxs-lookup"><span data-stu-id="9e668-118">Specifies whether or not the camera device currently exists (that is, the camera is connected).</span></span>   |
| [<span data-ttu-id="9e668-119">**FriendlyName**</span><span class="sxs-lookup"><span data-stu-id="9e668-119">**FriendlyName**</span></span>](imsrdpcameraredirconfig-friendlyname.md)                       | <span data-ttu-id="9e668-120">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e668-120">Read-only</span></span> |    <span data-ttu-id="9e668-121">Obtiene el nombre descriptivo de la cámara.</span><span class="sxs-lookup"><span data-stu-id="9e668-121">Gets the camera’s friendly name.</span></span>    |
| [<span data-ttu-id="9e668-122">**ID**</span><span class="sxs-lookup"><span data-stu-id="9e668-122">**InstanceId**</span></span>](imsrdpcameraredirconfig-instanceid.md)      | <span data-ttu-id="9e668-123">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e668-123">Read-only</span></span> |  <span data-ttu-id="9e668-124">Obtiene el identificador de instancia de la cámara.</span><span class="sxs-lookup"><span data-stu-id="9e668-124">Gets the instance ID of the camera.</span></span>  |
| [<span data-ttu-id="9e668-125">**ParentInstanceId**</span><span class="sxs-lookup"><span data-stu-id="9e668-125">**ParentInstanceId**</span></span>](imsrdpcameraredirconfig-parentinstanceid.md)                       | <span data-ttu-id="9e668-126">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e668-126">Read-only</span></span> |    <span data-ttu-id="9e668-127">Obtiene el identificador de instancia del dispositivo primario de la cámara.</span><span class="sxs-lookup"><span data-stu-id="9e668-127">Gets the parent device instance ID of the camera.</span></span>   |
| [<span data-ttu-id="9e668-128">**Redirected**</span><span class="sxs-lookup"><span data-stu-id="9e668-128">**Redirected**</span></span>](imsrdpcameraredirconfig-redirected.md)      | <span data-ttu-id="9e668-129">Lectura/Escritura</span><span class="sxs-lookup"><span data-stu-id="9e668-129">Read/Write</span></span> |  <span data-ttu-id="9e668-130">Especifica si se redirige la cámara.</span><span class="sxs-lookup"><span data-stu-id="9e668-130">Specifies whether or not the camera is redirected.</span></span>  |
| [<span data-ttu-id="9e668-131">**SymbolicLink**</span><span class="sxs-lookup"><span data-stu-id="9e668-131">**SymbolicLink**</span></span>](imsrdpcameraredirconfig-symboliclink.md)                       | <span data-ttu-id="9e668-132">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="9e668-132">Read-only</span></span> |   <span data-ttu-id="9e668-133">Obtiene el vínculo simbólico de la interfaz **KSCATEGORY_VIDEO_CAMERA** de la cámara.</span><span class="sxs-lookup"><span data-stu-id="9e668-133">Gets the symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>   |

## <a name="requirements"></a><span data-ttu-id="9e668-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e668-134">Requirements</span></span>

| <span data-ttu-id="9e668-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e668-135">Requirement</span></span> | <span data-ttu-id="9e668-136">Value</span><span class="sxs-lookup"><span data-stu-id="9e668-136">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="9e668-137">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e668-137">Minimum supported client</span></span>| <span data-ttu-id="9e668-138">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="9e668-138">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="9e668-139">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="9e668-139">Type library</span></span>            | <span data-ttu-id="9e668-140">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="9e668-140">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="9e668-141">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="9e668-141">DLL</span></span>                  | <span data-ttu-id="9e668-142">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="9e668-142">MsTscAx.dll</span></span>     |
| <span data-ttu-id="9e668-143">IID</span><span class="sxs-lookup"><span data-stu-id="9e668-143">IID</span></span>                      | <span data-ttu-id="9e668-144">IID \_ IMsRdpCameraRedirConfig se define como 09750604-D625-47C1-9FCD-F09F735705D7</span><span class="sxs-lookup"><span data-stu-id="9e668-144">IID\_IMsRdpCameraRedirConfig is defined as 09750604-D625-47C1-9FCD-F09F735705D7</span></span>            |

## <a name="see-also"></a><span data-ttu-id="9e668-145">Vea también</span><span class="sxs-lookup"><span data-stu-id="9e668-145">See also</span></span>

- [<span data-ttu-id="9e668-146">**IMsRdpCameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="9e668-146">**IMsRdpCameraRedirConfigCollection**</span></span>](imsrdpcameraredirconfigcollection.md)
- [<span data-ttu-id="9e668-147">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="9e668-147">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)