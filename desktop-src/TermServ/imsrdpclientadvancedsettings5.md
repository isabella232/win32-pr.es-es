---
title: Interfaz IMsRdpClientAdvancedSettings5
description: Administra la configuración de cliente avanzada. Deriva de la interfaz IMsRdpClientAdvancedSettings4.
ms.assetid: a927cd4c-7f70-493e-a4f6-056d0352d56e
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientAdvancedSettings5, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientAdvancedSettings5
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 14e37eb28c1fb7a272291c44661c52ec3548708b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685982"
---
# <a name="imsrdpclientadvancedsettings5-interface"></a><span data-ttu-id="076f4-106">Interfaz IMsRdpClientAdvancedSettings5</span><span class="sxs-lookup"><span data-stu-id="076f4-106">IMsRdpClientAdvancedSettings5 interface</span></span>

<span data-ttu-id="076f4-107">Administra la configuración de cliente avanzada.</span><span class="sxs-lookup"><span data-stu-id="076f4-107">Manages advanced client settings.</span></span> <span data-ttu-id="076f4-108">Deriva de la interfaz [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) .</span><span class="sxs-lookup"><span data-stu-id="076f4-108">Derives from the [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md) interface.</span></span>

<span data-ttu-id="076f4-109">Para obtener una instancia de esta interfaz, use la propiedad [**IMsTscAx:: AdvancedSettings**](imstscax-advancedsettings.md) para obtener un puntero de interfaz [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) .</span><span class="sxs-lookup"><span data-stu-id="076f4-109">To obtain an instance of this interface, use the [**IMsTscAx::AdvancedSettings**](imstscax-advancedsettings.md) property to obtain an [**IMsTscAdvancedSettings**](imstscadvancedsettings-interface.md) interface pointer.</span></span> <span data-ttu-id="076f4-110">A continuación, llame a [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el puntero **IMsTscAdvancedSettings** y pase **IID \_ IMsRdpClientAdvancedSettings5** a **QueryInterface**.</span><span class="sxs-lookup"><span data-stu-id="076f4-110">Then call [**QueryInterface**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the **IMsTscAdvancedSettings** pointer, and pass **IID\_IMsRdpClientAdvancedSettings5** to **QueryInterface**.</span></span>

## <a name="members"></a><span data-ttu-id="076f4-111">Miembros</span><span class="sxs-lookup"><span data-stu-id="076f4-111">Members</span></span>

<span data-ttu-id="076f4-112">La interfaz **IMsRdpClientAdvancedSettings5** hereda de [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md).</span><span class="sxs-lookup"><span data-stu-id="076f4-112">The **IMsRdpClientAdvancedSettings5** interface inherits from [**IMsRdpClientAdvancedSettings4**](imsrdpclientadvancedsettings4.md).</span></span> <span data-ttu-id="076f4-113">**IMsRdpClientAdvancedSettings5** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="076f4-113">**IMsRdpClientAdvancedSettings5** also has these types of members:</span></span>

-   [<span data-ttu-id="076f4-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="076f4-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="076f4-115">Propiedades</span><span class="sxs-lookup"><span data-stu-id="076f4-115">Properties</span></span>

<span data-ttu-id="076f4-116">La interfaz **IMsRdpClientAdvancedSettings5** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="076f4-116">The **IMsRdpClientAdvancedSettings5** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="076f4-117">Propiedad</span><span class="sxs-lookup"><span data-stu-id="076f4-117">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="076f4-118">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="076f4-118">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="076f4-119">Descripción</span><span class="sxs-lookup"><span data-stu-id="076f4-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="076f4-120"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="076f4-120"><a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="076f4-121">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="076f4-121">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="076f4-122">Modo de redirección de audio.</span><span class="sxs-lookup"><span data-stu-id="076f4-122">The audio redirection mode.</span></span> <span data-ttu-id="076f4-123">La propiedad <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a> tiene los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="076f4-123">The <a href="imsrdpclientadvancedsettings5-audioredirectionmode.md"><strong>AudioRedirectionMode</strong></a> property has the following possible values.</span></span><br/><span data-ttu-id="076f4-124">
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (la redirección de audio está habilitada y la opción para la redirección es &quot; traer a este equipo &quot; .</span><span class="sxs-lookup"><span data-stu-id="076f4-124">
<dt><span id="AUDIO_MODE_REDIRECT___0"></span><span id="audio_mode_redirect___0"></span><strong>AUDIO_MODE_REDIRECT 0</strong> (Audio redirection is enabled and the option for redirection is &quot;Bring to this computer&quot;.</span></span> <span data-ttu-id="076f4-125">Este es el modo predeterminado).</span><span class="sxs-lookup"><span data-stu-id="076f4-125">This is the default mode.)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="076f4-126"><dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (la redirección de audio está habilitada y la opción se &quot; deja en el equipo remoto &quot; .</span><span class="sxs-lookup"><span data-stu-id="076f4-126"><dt><span id="AUDIO_MODE_PLAY_ON_SERVER_1"></span><span id="audio_mode_play_on_server_1"></span><strong>AUDIO_MODE_PLAY_ON_SERVER 1</strong> (Audio redirection is enabled and the option is &quot;Leave at remote computer&quot;.</span></span> <span data-ttu-id="076f4-127">La &quot; opción dejar en equipo remoto &quot; solo se admite cuando se conecta de forma remota a un equipo host que ejecuta Windows Vista.</span><span class="sxs-lookup"><span data-stu-id="076f4-127">The &quot;Leave at remote computer&quot; option is supported only when connecting remotely to a host computer that is running Windows Vista.</span></span> <span data-ttu-id="076f4-128">Si la conexión se realiza a un equipo host que ejecuta Windows Server 2008, &quot; se cambia la opción dejar en equipo remoto &quot; a no &quot; reproducir &quot; .</span><span class="sxs-lookup"><span data-stu-id="076f4-128">If the connection is to a host computer that is running Windows Server 2008, the option &quot;Leave at remote computer&quot; is changed to &quot;Do not play&quot;.)</span></span><br/> </dt> <dd></dd> <span data-ttu-id="076f4-129"><dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (la redirección de audio está habilitada y el modo &quot; no se reproduce &quot; ).</span><span class="sxs-lookup"><span data-stu-id="076f4-129"><dt><span id="AUDIO_MODE_NONE_2"></span><span id="audio_mode_none_2"></span><strong>AUDIO_MODE_NONE 2</strong> (Audio redirection is enabled and the mode is &quot;Do not play&quot;.)</span></span><br/> </dt> <dd></dd> </dl></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="076f4-130"><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a></span><span class="sxs-lookup"><span data-stu-id="076f4-130"><a href="imsrdpclientadvancedsettings5-bitmapvirtualcache32bppsize.md"><strong>BitmapVirtualCache32BppSize</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="076f4-131">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="076f4-131">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="076f4-132">Especifica el tamaño del archivo de caché virtual para los mapas de bits de 32 bits por píxel (BPP).</span><span class="sxs-lookup"><span data-stu-id="076f4-132">Specifies the virtual cache file size for 32 bits per pixel (bpp) bitmaps.</span></span> <span data-ttu-id="076f4-133">El valor máximo es 48 megabytes (MB).</span><span class="sxs-lookup"><span data-stu-id="076f4-133">The maximum value is 48 megabytes (MB).</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="076f4-134"><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a></span><span class="sxs-lookup"><span data-stu-id="076f4-134"><a href="imsrdpclientadvancedsettings5-connectionbarshowpinbutton.md"><strong>ConnectionBarShowPinButton</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="076f4-135">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="076f4-135">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="076f4-136">Especifica si se debe mostrar el botón de anclaje en la barra de conexión.</span><span class="sxs-lookup"><span data-stu-id="076f4-136">Specifies whether the pin button should be shown on the connection bar.</span></span> <span data-ttu-id="076f4-137">De forma predeterminada, el valor es <strong>true</strong>.</span><span class="sxs-lookup"><span data-stu-id="076f4-137">By default, the value is <strong>TRUE</strong>.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="076f4-138"><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>PublicMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="076f4-138"><a href="imsrdpclientadvancedsettings5-publicmode.md"><strong>PublicMode</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="076f4-139">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="076f4-139">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="076f4-140">Especifica si el modo público debe estar habilitado o deshabilitado.</span><span class="sxs-lookup"><span data-stu-id="076f4-140">Specifies whether public mode should be enabled or disabled.</span></span> <span data-ttu-id="076f4-141">De forma predeterminada, el modo público está establecido en <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="076f4-141">By default, public mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="076f4-142"><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a></span><span class="sxs-lookup"><span data-stu-id="076f4-142"><a href="imsrdpclientadvancedsettings5-redirectclipboard.md"><strong>RedirectClipboard</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="076f4-143">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="076f4-143">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="076f4-144">Especifica si la redirección del portapapeles debe estar habilitada o deshabilitada.</span><span class="sxs-lookup"><span data-stu-id="076f4-144">Specifies whether clipboard redirection should be enabled or disabled.</span></span> <span data-ttu-id="076f4-145">De forma predeterminada, el modo de redirección del portapapeles se establece en <strong>true</strong> (habilitado).</span><span class="sxs-lookup"><span data-stu-id="076f4-145">By default, clipboard redirection mode is set to <strong>TRUE</strong> (enabled).</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="076f4-146"><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a></span><span class="sxs-lookup"><span data-stu-id="076f4-146"><a href="imsrdpclientadvancedsettings5-redirectdevices.md"><strong>RedirectDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="076f4-147">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="076f4-147">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="076f4-148">Especifica si los dispositivos redirigidos deben estar habilitados o deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="076f4-148">Specifies whether redirected devices should be enabled or disabled.</span></span> <span data-ttu-id="076f4-149">De forma predeterminada, el modo dispositivos redirigidos está establecido en <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="076f4-149">By default, redirected devices mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="076f4-150"><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a></span><span class="sxs-lookup"><span data-stu-id="076f4-150"><a href="imsrdpclientadvancedsettings5-redirectposdevices.md"><strong>RedirectPOSDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="076f4-151">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="076f4-151">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="076f4-152">Especifica si los dispositivos redireccionados de punto de servicio deben estar habilitados o deshabilitados.</span><span class="sxs-lookup"><span data-stu-id="076f4-152">Specifies whether Point of Service redirected devices should be enabled or disabled.</span></span> <span data-ttu-id="076f4-153">De forma predeterminada, el modo de dispositivo redireccionado de punto de servicio está establecido en <strong>false</strong>.</span><span class="sxs-lookup"><span data-stu-id="076f4-153">By default, Point of Service redirected devices mode is set to <strong>FALSE</strong>.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="076f4-154">Observaciones</span><span class="sxs-lookup"><span data-stu-id="076f4-154">Remarks</span></span>

<span data-ttu-id="076f4-155">Esta interfaz se ha extendido mediante las siguientes interfaces, con cada nueva interfaz que hereda todos los métodos y propiedades de las interfaces anteriores:</span><span class="sxs-lookup"><span data-stu-id="076f4-155">This interface has been extended by the following interfaces, with each new interface inheriting all the methods and properties of the previous interfaces:</span></span>

-   [<span data-ttu-id="076f4-156">**IMsRdpClientAdvancedSettings6**</span><span class="sxs-lookup"><span data-stu-id="076f4-156">**IMsRdpClientAdvancedSettings6**</span></span>](imsrdpclientadvancedsettings6.md)
-   [<span data-ttu-id="076f4-157">**IMsRdpClientAdvancedSettings7**</span><span class="sxs-lookup"><span data-stu-id="076f4-157">**IMsRdpClientAdvancedSettings7**</span></span>](imsrdpclientadvancedsettings7.md)
-   [<span data-ttu-id="076f4-158">**IMsRdpClientAdvancedSettings8**</span><span class="sxs-lookup"><span data-stu-id="076f4-158">**IMsRdpClientAdvancedSettings8**</span></span>](imsrdpclientadvancedsettings8.md)

## <a name="requirements"></a><span data-ttu-id="076f4-159">Requisitos</span><span class="sxs-lookup"><span data-stu-id="076f4-159">Requirements</span></span>



| <span data-ttu-id="076f4-160">Requisito</span><span class="sxs-lookup"><span data-stu-id="076f4-160">Requirement</span></span> | <span data-ttu-id="076f4-161">Value</span><span class="sxs-lookup"><span data-stu-id="076f4-161">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------|
| <span data-ttu-id="076f4-162">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="076f4-162">Minimum supported client</span></span><br/> | <span data-ttu-id="076f4-163">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="076f4-163">Windows Vista</span></span><br/>                                                                         |
| <span data-ttu-id="076f4-164">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="076f4-164">Minimum supported server</span></span><br/> | <span data-ttu-id="076f4-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="076f4-165">Windows Server 2008</span></span><br/>                                                                   |
| <span data-ttu-id="076f4-166">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="076f4-166">Type library</span></span><br/>             | <dl> <span data-ttu-id="076f4-167"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="076f4-167"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="076f4-168">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="076f4-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="076f4-169"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="076f4-169"><dt>MsTscAx.dll</dt></span></span> </dl>           |
| <span data-ttu-id="076f4-170">IID</span><span class="sxs-lookup"><span data-stu-id="076f4-170">IID</span></span><br/>                      | <span data-ttu-id="076f4-171">IID \_ IMsRdpClientAdvancedSettings5 se define como FBA7F64E-6783-4405-DA45-FA4A763DABD0</span><span class="sxs-lookup"><span data-stu-id="076f4-171">IID\_IMsRdpClientAdvancedSettings5 is defined as FBA7F64E-6783-4405-DA45-FA4A763DABD0</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="076f4-172">Vea también</span><span class="sxs-lookup"><span data-stu-id="076f4-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="076f4-173">**IMsRdpClientAdvancedSettings4**</span><span class="sxs-lookup"><span data-stu-id="076f4-173">**IMsRdpClientAdvancedSettings4**</span></span>](imsrdpclientadvancedsettings4.md)
</dt> <dt>

[<span data-ttu-id="076f4-174">**IMsRdpClientAdvancedSettings3**</span><span class="sxs-lookup"><span data-stu-id="076f4-174">**IMsRdpClientAdvancedSettings3**</span></span>](imsrdpclientadvancedsettings3.md)
</dt> <dt>

[<span data-ttu-id="076f4-175">**IMsRdpClientAdvancedSettings2**</span><span class="sxs-lookup"><span data-stu-id="076f4-175">**IMsRdpClientAdvancedSettings2**</span></span>](imsrdpclientadvancedsettings2.md)
</dt> <dt>

[<span data-ttu-id="076f4-176">**IMsRdpClientAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="076f4-176">**IMsRdpClientAdvancedSettings**</span></span>](imsrdpclientadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="076f4-177">**IMsTscAdvancedSettings**</span><span class="sxs-lookup"><span data-stu-id="076f4-177">**IMsTscAdvancedSettings**</span></span>](imstscadvancedsettings-interface.md)
</dt> <dt>

[<span data-ttu-id="076f4-178">Referencia de Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="076f4-178">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

