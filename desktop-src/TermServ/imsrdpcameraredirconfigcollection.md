---
title: Interfaz IMsRdpCameraRedirConfigCollection
description: Representa la colección de cámaras (y las configuraciones asociadas) que están disponibles para la redirección.
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfigCollection
- Servicios de Escritorio remoto de la interfaz IMsRdpCameraRedirConfigCollection, descrito
topic_type:
- apiref
api_name:
- IMsRdpCameraRedirConfigCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 12/16/2020
ms.openlocfilehash: 3d97249a7485ec024ee3611809c87c5b6ed41143
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "104151923"
---
# <a name="imsrdpcameraredirconfigcollection-interface"></a><span data-ttu-id="e3e3a-105">Interfaz IMsRdpCameraRedirConfigCollection</span><span class="sxs-lookup"><span data-stu-id="e3e3a-105">IMsRdpCameraRedirConfigCollection interface</span></span>

 <span data-ttu-id="e3e3a-106">Representa la colección de cámaras (y las configuraciones asociadas) que están disponibles para la redirección.</span><span class="sxs-lookup"><span data-stu-id="e3e3a-106">Represents the collection of cameras (and the associated configurations) that are available for redirection.</span></span>

## <a name="members"></a><span data-ttu-id="e3e3a-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="e3e3a-107">Members</span></span>

<span data-ttu-id="e3e3a-108">La interfaz **IMsRdpCameraRedirConfigCollection** hereda de **IUnknown**.</span><span class="sxs-lookup"><span data-stu-id="e3e3a-108">The **IMsRdpCameraRedirConfigCollection** interface inherits from **IUnknown**.</span></span> <span data-ttu-id="e3e3a-109">**IMsRdpCameraRedirConfigCollection** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="e3e3a-109">**IMsRdpCameraRedirConfigCollection** also has these types of members:</span></span>

- [<span data-ttu-id="e3e3a-110">Métodos</span><span class="sxs-lookup"><span data-stu-id="e3e3a-110">Methods</span></span>](#methods)
- [<span data-ttu-id="e3e3a-111">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e3e3a-111">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="e3e3a-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="e3e3a-112">Methods</span></span>

<span data-ttu-id="e3e3a-113">La interfaz **IMsRdpCameraRedirConfigCollection** tiene estos métodos.</span><span class="sxs-lookup"><span data-stu-id="e3e3a-113">The **IMsRdpCameraRedirConfigCollection** interface has these methods.</span></span>

| <span data-ttu-id="e3e3a-114">Método</span><span class="sxs-lookup"><span data-stu-id="e3e3a-114">Method</span></span>            | <span data-ttu-id="e3e3a-115">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3e3a-115">Description</span></span>              |
|:------------------|:-------------------------|
| [<span data-ttu-id="e3e3a-116">**AddConfig**</span><span class="sxs-lookup"><span data-stu-id="e3e3a-116">**AddConfig**</span></span>](imsrdpcameraredirconfigcollection-addconfig.md)       |  <span data-ttu-id="e3e3a-117">Agrega un objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) a la colección (no es necesario que la cámara correspondiente esté conectada).</span><span class="sxs-lookup"><span data-stu-id="e3e3a-117">Adds an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object to the collection (the corresponding camera does not have to be connected).</span></span>                   |
| [<span data-ttu-id="e3e3a-118">**Volver a examinar**</span><span class="sxs-lookup"><span data-stu-id="e3e3a-118">**Rescan**</span></span>](imsrdpcameraredirconfigcollection-rescan.md)       |  <span data-ttu-id="e3e3a-119">Enumera los dispositivos de cámara conectados.</span><span class="sxs-lookup"><span data-stu-id="e3e3a-119">Enumerates connected camera devices.</span></span>                   |

### <a name="properties"></a><span data-ttu-id="e3e3a-120">Propiedades</span><span class="sxs-lookup"><span data-stu-id="e3e3a-120">Properties</span></span>

<span data-ttu-id="e3e3a-121">La interfaz **IMsRdpCameraRedirConfigCollection** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="e3e3a-121">The **IMsRdpCameraRedirConfigCollection** interface has these properties.</span></span>

| <span data-ttu-id="e3e3a-122">Propiedad</span><span class="sxs-lookup"><span data-stu-id="e3e3a-122">Property</span></span>         | <span data-ttu-id="e3e3a-123">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="e3e3a-123">Access type</span></span>           | <span data-ttu-id="e3e3a-124">Descripción</span><span class="sxs-lookup"><span data-stu-id="e3e3a-124">Description</span></span>            |
|:-----------------|:----------------------|:-----------------------|
| [<span data-ttu-id="e3e3a-125">**ByIndex**</span><span class="sxs-lookup"><span data-stu-id="e3e3a-125">**ByIndex**</span></span>](imsrdpcameraredirconfigcollection-byindex.md)      | <span data-ttu-id="e3e3a-126">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e3e3a-126">Read-only</span></span> |  <span data-ttu-id="e3e3a-127">Devuelve un objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) por su índice en la colección.</span><span class="sxs-lookup"><span data-stu-id="e3e3a-127">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object by its index in the collection.</span></span>   |
| [<span data-ttu-id="e3e3a-128">**ByInstanceId**</span><span class="sxs-lookup"><span data-stu-id="e3e3a-128">**ByInstanceId**</span></span>](imsrdpcameraredirconfigcollection-byinstanceid.md)                       | <span data-ttu-id="e3e3a-129">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e3e3a-129">Read-only</span></span> |    <span data-ttu-id="e3e3a-130">Devuelve un objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la colección que corresponde al identificador de instancia especificado.</span><span class="sxs-lookup"><span data-stu-id="e3e3a-130">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the specified instance ID.</span></span>    |
| [<span data-ttu-id="e3e3a-131">**BySymbolicLink**</span><span class="sxs-lookup"><span data-stu-id="e3e3a-131">**BySymbolicLink**</span></span>](imsrdpcameraredirconfigcollection-bysymboliclink.md)      | <span data-ttu-id="e3e3a-132">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e3e3a-132">Read-only</span></span> |  <span data-ttu-id="e3e3a-133">Devuelve un objeto [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la colección que corresponde al vínculo simbólico especificado de la interfaz **KSCATEGORY_VIDEO_CAMERA** de la cámara.</span><span class="sxs-lookup"><span data-stu-id="e3e3a-133">Returns an [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) object from the collection that corresponds to the given symbolic link of the **KSCATEGORY_VIDEO_CAMERA** interface for the camera.</span></span>  |
| [<span data-ttu-id="e3e3a-134">**Contabiliza**</span><span class="sxs-lookup"><span data-stu-id="e3e3a-134">**Count**</span></span>](imsrdpcameraredirconfigcollection-count.md)                       | <span data-ttu-id="e3e3a-135">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="e3e3a-135">Read-only</span></span> |    <span data-ttu-id="e3e3a-136">Devuelve el número de objetos [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) de la colección.</span><span class="sxs-lookup"><span data-stu-id="e3e3a-136">Returns the number of [IMsRdpCameraRedirConfig](imsrdpcameraredirconfig.md) objects in the collection.</span></span>   |
| [<span data-ttu-id="e3e3a-137">**EncodeVideo**</span><span class="sxs-lookup"><span data-stu-id="e3e3a-137">**EncodeVideo**</span></span>](imsrdpcameraredirconfigcollection-encodevideo.md)      | <span data-ttu-id="e3e3a-138">Lectura/Escritura</span><span class="sxs-lookup"><span data-stu-id="e3e3a-138">Read/Write</span></span> |  <span data-ttu-id="e3e3a-139">Especifica si la secuencia de vídeo es H. 264 codificada.</span><span class="sxs-lookup"><span data-stu-id="e3e3a-139">Specifies whether or not the video stream is H.264 encoded.</span></span>  |
| [<span data-ttu-id="e3e3a-140">**EncodingQuality**</span><span class="sxs-lookup"><span data-stu-id="e3e3a-140">**EncodingQuality**</span></span>](imsrdpcameraredirconfigcollection-encodingquality.md)                       | <span data-ttu-id="e3e3a-141">Lectura/Escritura</span><span class="sxs-lookup"><span data-stu-id="e3e3a-141">Read/Write</span></span> |    <span data-ttu-id="e3e3a-142">Especifica la calidad de codificación (velocidad de bits).</span><span class="sxs-lookup"><span data-stu-id="e3e3a-142">Specifies the encoding quality (bit rate).</span></span>   |
| [<span data-ttu-id="e3e3a-143">**RedirectByDefault**</span><span class="sxs-lookup"><span data-stu-id="e3e3a-143">**RedirectByDefault**</span></span>](imsrdpcameraredirconfigcollection-redirectbydefault.md)                       | <span data-ttu-id="e3e3a-144">Lectura/Escritura</span><span class="sxs-lookup"><span data-stu-id="e3e3a-144">Read/Write</span></span> |   <span data-ttu-id="e3e3a-145">Especifica si cualquier cámara nueva se redirige de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="e3e3a-145">Specifies whether or not any new camera gets redirected by default.</span></span>    |

## <a name="requirements"></a><span data-ttu-id="e3e3a-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e3e3a-146">Requirements</span></span>

| <span data-ttu-id="e3e3a-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="e3e3a-147">Requirement</span></span> | <span data-ttu-id="e3e3a-148">Value</span><span class="sxs-lookup"><span data-stu-id="e3e3a-148">Value</span></span> |
|-------------------------------------|---------------------------------------|
| <span data-ttu-id="e3e3a-149">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e3e3a-149">Minimum supported client</span></span>| <span data-ttu-id="e3e3a-150">Windows 10, versión 1803 (compilación 17134)</span><span class="sxs-lookup"><span data-stu-id="e3e3a-150">Windows 10, version 1803 (build 17134)</span></span>      |
| <span data-ttu-id="e3e3a-151">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="e3e3a-151">Type library</span></span>            | <span data-ttu-id="e3e3a-152">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="e3e3a-152">MsTscAx.dll</span></span>                        |
| <span data-ttu-id="e3e3a-153">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="e3e3a-153">DLL</span></span>                  | <span data-ttu-id="e3e3a-154">MsTscAx.dll</span><span class="sxs-lookup"><span data-stu-id="e3e3a-154">MsTscAx.dll</span></span>     |
| <span data-ttu-id="e3e3a-155">IID</span><span class="sxs-lookup"><span data-stu-id="e3e3a-155">IID</span></span>                      | <span data-ttu-id="e3e3a-156">IID \_ IMsRdpCameraRedirConfigCollection se define como AE45252B-AAAB-4504-B681-649D6073A37A</span><span class="sxs-lookup"><span data-stu-id="e3e3a-156">IID\_IMsRdpCameraRedirConfigCollection is defined as AE45252B-AAAB-4504-B681-649D6073A37A</span></span>            |

## <a name="see-also"></a><span data-ttu-id="e3e3a-157">Vea también</span><span class="sxs-lookup"><span data-stu-id="e3e3a-157">See also</span></span>

- [<span data-ttu-id="e3e3a-158">**IMsRdpCameraRedirConfig**</span><span class="sxs-lookup"><span data-stu-id="e3e3a-158">**IMsRdpCameraRedirConfig**</span></span>](imsrdpcameraredirconfig.md)
- [<span data-ttu-id="e3e3a-159">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span><span class="sxs-lookup"><span data-stu-id="e3e3a-159">**IMsRdpClientNonScriptable7::CameraRedirConfigCollection**</span></span>](imsrdpclientnonscriptable7-cameraredirconfigcollection.md)
