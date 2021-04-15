---
title: Interfaz IMsRdpClientAdvancedSettings7
description: Expone métodos y propiedades que administran la configuración avanzada del control ActiveX.
ms.assetid: 2d6848b4-2ce6-4624-b46e-65e7daf2d0f1
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings7, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings7
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eed28c5d26ecf280507ce3cce835a6d0a71fc3bb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105676641"
---
# <a name="imsrdpclientadvancedsettings7-interface"></a><span data-ttu-id="09d29-105">Interfaz IMsRdpClientAdvancedSettings7</span><span class="sxs-lookup"><span data-stu-id="09d29-105">IMsRdpClientAdvancedSettings7 interface</span></span>

<span data-ttu-id="09d29-106">Expone métodos y propiedades que administran la configuración avanzada del control ActiveX.</span><span class="sxs-lookup"><span data-stu-id="09d29-106">Exposes methods and properties that manage advanced settings of the ActiveX control.</span></span>

<span data-ttu-id="09d29-107">Para obtener una instancia de esta interfaz, use la propiedad [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obtener un puntero de interfaz [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="09d29-107">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="09d29-108">A continuación, llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero **IMsTscAdvancedSettings** y pase **IID \_ IMsRdpClientAdvancedSettings7** a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="09d29-108">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings7** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="09d29-109">Miembros</span><span class="sxs-lookup"><span data-stu-id="09d29-109">Members</span></span>

<span data-ttu-id="09d29-110">La interfaz **IMsRdpClientAdvancedSettings7** hereda de **IMsRdpClientAdvancedSettings6**.</span><span class="sxs-lookup"><span data-stu-id="09d29-110">The **IMsRdpClientAdvancedSettings7** interface inherits from **IMsRdpClientAdvancedSettings6**.</span></span> <span data-ttu-id="09d29-111">**IMsRdpClientAdvancedSettings7** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="09d29-111">**IMsRdpClientAdvancedSettings7** also has these types of members:</span></span>

-   [<span data-ttu-id="09d29-112">Propiedades</span><span class="sxs-lookup"><span data-stu-id="09d29-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="09d29-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="09d29-113">Properties</span></span>

<span data-ttu-id="09d29-114">La interfaz **IMsRdpClientAdvancedSettings7** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="09d29-114">The **IMsRdpClientAdvancedSettings7** interface has these properties.</span></span>



| <span data-ttu-id="09d29-115">Propiedad</span><span class="sxs-lookup"><span data-stu-id="09d29-115">Property</span></span>                                                                                                    | <span data-ttu-id="09d29-116">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="09d29-116">Access type</span></span>           | <span data-ttu-id="09d29-117">Descripción</span><span class="sxs-lookup"><span data-stu-id="09d29-117">Description</span></span>                                                                                                                                          |
|:------------------------------------------------------------------------------------------------------------|:----------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="09d29-118">**AudioCaptureRedirectionMode**</span><span class="sxs-lookup"><span data-stu-id="09d29-118">**AudioCaptureRedirectionMode**</span></span>](imsrdpclientadvancedsettings7-audiocaptureredirectionmode.md)<br/> | <span data-ttu-id="09d29-119">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09d29-119">Read/write</span></span><br/> | <span data-ttu-id="09d29-120">Especifica o recupera un valor que indica si el dispositivo de entrada de audio predeterminado se redirige desde el cliente a la sesión remota.</span><span class="sxs-lookup"><span data-stu-id="09d29-120">Specifies or retrieves a value that indicates whether the default audio input device is redirected from the client to the remote session.</span></span><br/> |
| [<span data-ttu-id="09d29-121">**AudioQualityMode**</span><span class="sxs-lookup"><span data-stu-id="09d29-121">**AudioQualityMode**</span></span>](imsrdpclientadvancedsettings7-audioqualitymode.md)<br/>                       | <span data-ttu-id="09d29-122">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09d29-122">Read/write</span></span><br/> | <span data-ttu-id="09d29-123">Especifica o recupera un valor que indica la configuración del modo de calidad de audio para el audio redirigido.</span><span class="sxs-lookup"><span data-stu-id="09d29-123">Specifies or retrieves a value that indicates the audio quality mode setting for redirected audio.</span></span><br/>                                        |
| [<span data-ttu-id="09d29-124">**EnableSuperPan**</span><span class="sxs-lookup"><span data-stu-id="09d29-124">**EnableSuperPan**</span></span>](imsrdpclientadvancedsettings7-enablesuperpan.md)<br/>                           | <span data-ttu-id="09d29-125">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09d29-125">Read/write</span></span><br/> | <span data-ttu-id="09d29-126">Especifica o recupera un valor que indica si SuperPan está habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="09d29-126">Specifies or retrieves a value that indicates whether SuperPan is enabled or disabled.</span></span><br/>                                                    |
| [<span data-ttu-id="09d29-127">**NetworkConnectionType**</span><span class="sxs-lookup"><span data-stu-id="09d29-127">**NetworkConnectionType**</span></span>](imsrdpclientadvancedsettings7-networkconnectiontype.md)<br/>             | <span data-ttu-id="09d29-128">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09d29-128">Read/write</span></span><br/> | <span data-ttu-id="09d29-129">Especifica o recupera un valor que indica el tipo de conexión de red.</span><span class="sxs-lookup"><span data-stu-id="09d29-129">Specifies or retrieves a value that indicates the network connection type.</span></span><br/>                                                                |
| [<span data-ttu-id="09d29-130">**RedirectDirectX**</span><span class="sxs-lookup"><span data-stu-id="09d29-130">**RedirectDirectX**</span></span>](imsrdpclientadvancedsettings7-redirectdirectx.md)<br/>                         | <span data-ttu-id="09d29-131">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09d29-131">Read/write</span></span><br/> | <span data-ttu-id="09d29-132">No se usa esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="09d29-132">This property is not used.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="09d29-133">**SuperPanAccelerationFactor**</span><span class="sxs-lookup"><span data-stu-id="09d29-133">**SuperPanAccelerationFactor**</span></span>](imsrdpclientadvancedsettings7-superpanaccelerationfactor.md)<br/>   | <span data-ttu-id="09d29-134">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09d29-134">Read/write</span></span><br/> | <span data-ttu-id="09d29-135">Especifica o recupera un valor que indica el factor de aceleración de SuperPan.</span><span class="sxs-lookup"><span data-stu-id="09d29-135">Specifies or retrieves a value that indicates the SuperPan acceleration factor.</span></span><br/>                                                           |
| [<span data-ttu-id="09d29-136">**VideoPlaybackMode**</span><span class="sxs-lookup"><span data-stu-id="09d29-136">**VideoPlaybackMode**</span></span>](imsrdpclientadvancedsettings7-videoplaybackmode.md)<br/>                     | <span data-ttu-id="09d29-137">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="09d29-137">Read/write</span></span><br/> | <span data-ttu-id="09d29-138">Especifica o recupera un valor que indica el modo de reproducción de vídeo.</span><span class="sxs-lookup"><span data-stu-id="09d29-138">Specifies or retrieves a value that indicates the video playback mode.</span></span><br/>                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="09d29-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09d29-139">Requirements</span></span>



| <span data-ttu-id="09d29-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="09d29-140">Requirement</span></span> | <span data-ttu-id="09d29-141">Value</span><span class="sxs-lookup"><span data-stu-id="09d29-141">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09d29-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09d29-142">Minimum supported client</span></span><br/> | <span data-ttu-id="09d29-143">Windows 7</span><span class="sxs-lookup"><span data-stu-id="09d29-143">Windows 7</span></span><br/>                                                                             |
| <span data-ttu-id="09d29-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="09d29-144">Minimum supported server</span></span><br/> | <span data-ttu-id="09d29-145">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="09d29-145">Windows Server 2008 R2</span></span><br/>                                                                |
| <span data-ttu-id="09d29-146">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="09d29-146">Type library</span></span><br/>             | <dl> <span data-ttu-id="09d29-147"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09d29-147"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="09d29-148">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="09d29-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="09d29-149"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="09d29-149"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="09d29-150">IID</span><span class="sxs-lookup"><span data-stu-id="09d29-150">IID</span></span><br/>                      | <span data-ttu-id="09d29-151">IID \_ IMsRdpClientAdvancedSettings7 se define como 26036036-4010-4578-8091-0db9a1edf9c3</span><span class="sxs-lookup"><span data-stu-id="09d29-151">IID\_IMsRdpClientAdvancedSettings7 is defined as 26036036-4010-4578-8091-0db9a1edf9c3</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="09d29-152">Vea también</span><span class="sxs-lookup"><span data-stu-id="09d29-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09d29-153">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="09d29-153">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
</dt> <dt>

[<span data-ttu-id="09d29-154">**IMsRdpClientAdvancedSettings5**</span><span class="sxs-lookup"><span data-stu-id="09d29-154">**IMsRdpClientAdvancedSettings5**</span></span>](imsrdpclientadvancedsettings5.md)
</dt> <dt>

[<span data-ttu-id="09d29-155">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="09d29-155">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="09d29-156">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="09d29-156">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="09d29-157">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="09d29-157">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="09d29-158">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="09d29-158">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="09d29-159">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="09d29-159">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> </dl>

 

