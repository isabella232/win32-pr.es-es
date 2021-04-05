---
title: Interfaz IMsRdpClientNonScriptable3
description: Proporciona acceso a las propiedades que no admiten scripts de la sesión remota de un cliente en el control ActiveX Escritorio remoto. Deriva de la interfaz IMsRdpClientNonScriptable2.
ms.assetid: 40cfcd8e-5dd7-497d-8c57-da1f542136b8
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, descrito
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c456393ee00c06bcd16135a7fbc73b0f1686259f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996597"
---
# <a name="imsrdpclientnonscriptable3-interface"></a><span data-ttu-id="d0645-106">Interfaz IMsRdpClientNonScriptable3</span><span class="sxs-lookup"><span data-stu-id="d0645-106">IMsRdpClientNonScriptable3 interface</span></span>

<span data-ttu-id="d0645-107">Proporciona acceso a las propiedades que no admiten scripts de la sesión remota de un cliente en el control ActiveX Escritorio remoto.</span><span class="sxs-lookup"><span data-stu-id="d0645-107">Provides access to the nonscriptable properties of a client's remote session on the Remote Desktop ActiveX control.</span></span> <span data-ttu-id="d0645-108">Deriva de la interfaz [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) .</span><span class="sxs-lookup"><span data-stu-id="d0645-108">Derives from the [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md) interface.</span></span> <span data-ttu-id="d0645-109">Solo se puede tener acceso a los métodos de esta interfaz a través de vtable; no están disponibles para los clientes con scripts.</span><span class="sxs-lookup"><span data-stu-id="d0645-109">Methods of this interface can only be accessed through the vtable; they are not available for use to scriptable clients.</span></span>

## <a name="members"></a><span data-ttu-id="d0645-110">Miembros</span><span class="sxs-lookup"><span data-stu-id="d0645-110">Members</span></span>

<span data-ttu-id="d0645-111">La interfaz **IMsRdpClientNonScriptable3** hereda de [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md).</span><span class="sxs-lookup"><span data-stu-id="d0645-111">The **IMsRdpClientNonScriptable3** interface inherits from [**IMsRdpClientNonScriptable2**](imsrdpclientnonscriptable2.md).</span></span> <span data-ttu-id="d0645-112">**IMsRdpClientNonScriptable3** también tiene estos tipos de miembros:</span><span class="sxs-lookup"><span data-stu-id="d0645-112">**IMsRdpClientNonScriptable3** also has these types of members:</span></span>

-   [<span data-ttu-id="d0645-113">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d0645-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d0645-114">Propiedades</span><span class="sxs-lookup"><span data-stu-id="d0645-114">Properties</span></span>

<span data-ttu-id="d0645-115">La interfaz **IMsRdpClientNonScriptable3** tiene estas propiedades.</span><span class="sxs-lookup"><span data-stu-id="d0645-115">The **IMsRdpClientNonScriptable3** interface has these properties.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="d0645-116">Propiedad</span><span class="sxs-lookup"><span data-stu-id="d0645-116">Property</span></span></th>
<th style="text-align: left;"><span data-ttu-id="d0645-117">Tipo de acceso</span><span class="sxs-lookup"><span data-stu-id="d0645-117">Access type</span></span></th>
<th style="text-align: left;"><span data-ttu-id="d0645-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="d0645-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d0645-119"><a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0645-119"><a href="imsrdpclientnonscriptable3-connectionbartext.md"><strong>ConnectionBarText</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-120">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d0645-120">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-121">Cadena de texto que se va a mostrar para la barra de conexión.</span><span class="sxs-lookup"><span data-stu-id="d0645-121">The text string to display for the connection bar.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d0645-122"><a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>Recopilación</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0645-122"><a href="imsrdpclientnonscriptable3-devicecollection.md"><strong>DeviceCollection</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-123">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0645-123">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-124">La colección de dispositivos PnP que están disponibles para la redirección.</span><span class="sxs-lookup"><span data-stu-id="d0645-124">The collection of PnP devices that are available for redirection.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d0645-125"><a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0645-125"><a href="imsrdpclientnonscriptable3-drivecollection.md"><strong>DriveCollection</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-126">Solo lectura</span><span class="sxs-lookup"><span data-stu-id="d0645-126">Read-only</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-127">La colección de unidades de disco que está disponible para la redirección.</span><span class="sxs-lookup"><span data-stu-id="d0645-127">The collection of disk drives that is available for redirection.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d0645-128"><a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0645-128"><a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>EnableCredSspSupport</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-129">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d0645-129">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-130">Especifica si CredSSP está habilitado para esta conexión.</span><span class="sxs-lookup"><span data-stu-id="d0645-130">Specifies whether CredSSP is enabled for this connection.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d0645-131"><a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0645-131"><a href="imsrdpclientnonscriptable3-negotiatesecuritylayer.md"><strong>NegotiateSecurityLayer</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-132">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d0645-132">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-133">Especifica si la configuración NegotiateSecurityLayer es compatible con esta conexión.</span><span class="sxs-lookup"><span data-stu-id="d0645-133">Specifies whether the NegotiateSecurityLayer setting is supported for this connection.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d0645-134">Cuando <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> está habilitado y presente en el cliente, o cuando capa de sockets seguros (SSL) está habilitado con la autenticación de usuario, NegotiateSecurityLayer se omite.</span><span class="sxs-lookup"><span data-stu-id="d0645-134">When <a href="imsrdpclientnonscriptable3-enablecredsspsupport.md"><strong>CredSspSupport</strong></a> is enabled and present on the client, or when Secure Sockets Layer (SSL) is enabled with user authentication, NegotiateSecurityLayer is ignored.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d0645-135"><a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0645-135"><a href="imsrdpclientnonscriptable3-promptforcredentials.md"><strong>PromptForCredentials</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-136">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d0645-136">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-137">Especifica si se debe mostrar el cuadro de diálogo solicitar credenciales.</span><span class="sxs-lookup"><span data-stu-id="d0645-137">Specifies whether the prompt for credentials dialog box should be shown.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d0645-138"><a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0645-138"><a href="imsrdpclientnonscriptable3-redirectdynamicdevices.md"><strong>RedirectDynamicDevices</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-139">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d0645-139">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-140">Especifica si los dispositivos PnP conectados dinámicamente que se enumeran mientras están en una sesión están disponibles para la redirección.</span><span class="sxs-lookup"><span data-stu-id="d0645-140">Specifies whether dynamically attached PnP devices that are enumerated while in a session are available for redirection.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d0645-141"><a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0645-141"><a href="imsrdpclientnonscriptable3-redirectdynamicdrives.md"><strong>RedirectDynamicDrives</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-142">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d0645-142">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-143">Especifica si las unidades PnP conectadas dinámicamente que se enumeran mientras están en una sesión están disponibles para la redirección.</span><span class="sxs-lookup"><span data-stu-id="d0645-143">Specifies whether dynamically attached PnP drives that are enumerated while in a session are available for redirection.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d0645-144"><a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0645-144"><a href="imsrdpclientnonscriptable3-showredirectionwarningdialog.md"><strong>ShowRedirectionWarningDialog</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-145">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d0645-145">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-146">Especifica si se debe mostrar el cuadro de diálogo Advertencia de seguridad de redirección antes de iniciar una sesión.</span><span class="sxs-lookup"><span data-stu-id="d0645-146">Specifies whether the redirection security warning dialog box should be shown before starting a session.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span data-ttu-id="d0645-147"><a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0645-147"><a href="imsrdpclientnonscriptable3-warnaboutclipboardredirection.md"><strong>WarnAboutClipboardRedirection</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-148">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d0645-148">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-149">Especifica si el cuadro de diálogo Advertencia de seguridad debe incluir una advertencia sobre la redirección del portapapeles antes de iniciar una sesión.</span><span class="sxs-lookup"><span data-stu-id="d0645-149">Specifies whether the security warning dialog box should include a warning about clipboard redirection before starting a session.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span data-ttu-id="d0645-150"><a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a></span><span class="sxs-lookup"><span data-stu-id="d0645-150"><a href="imsrdpclientnonscriptable3-warnaboutsendingcredentials.md"><strong>WarnAboutSendingCredentials</strong></a></span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-151">Lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="d0645-151">Read/write</span></span><br/></td>
<td style="text-align: left;"><span data-ttu-id="d0645-152">Especifica si la advertencia de seguridad debe incluir una advertencia sobre el envío de credenciales al servidor remoto antes de iniciar una sesión.</span><span class="sxs-lookup"><span data-stu-id="d0645-152">Specifies whether the security warning should include a warning about sending credentials to the remote server before starting a session.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="d0645-153">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d0645-153">Requirements</span></span>



| <span data-ttu-id="d0645-154">Requisito</span><span class="sxs-lookup"><span data-stu-id="d0645-154">Requirement</span></span> | <span data-ttu-id="d0645-155">Value</span><span class="sxs-lookup"><span data-stu-id="d0645-155">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0645-156">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0645-156">Minimum supported client</span></span><br/> | <span data-ttu-id="d0645-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d0645-157">Windows Vista</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span data-ttu-id="d0645-158">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="d0645-158">Minimum supported server</span></span><br/> | <span data-ttu-id="d0645-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d0645-159">Windows Server 2008</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span data-ttu-id="d0645-160">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="d0645-160">Type library</span></span><br/>             | <dl> <span data-ttu-id="d0645-161"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0645-161"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d0645-162">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="d0645-162">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0645-163"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d0645-163"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| <span data-ttu-id="d0645-164">CLSID</span><span class="sxs-lookup"><span data-stu-id="d0645-164">CLSID</span></span><br/>                    | <span data-ttu-id="d0645-165">CLSID \_ MsRdpClient10 se define como C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span><span class="sxs-lookup"><span data-stu-id="d0645-165">CLSID\_MsRdpClient10 is defined as C0EFA91A-EEB7-41C7-97FA-F0ED645EFB24</span></span><br/> <span data-ttu-id="d0645-166">CLSID \_ MsRdpClient10NotSafeForScripting se define como A0C63C30-F08D-4AB4-907C-34905D770C7D</span><span class="sxs-lookup"><span data-stu-id="d0645-166">CLSID\_MsRdpClient10NotSafeForScripting is defined as A0C63C30-F08D-4AB4-907C-34905D770C7D</span></span><br/> <span data-ttu-id="d0645-167">CLSID \_ MsRdpClient5 se define como 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span><span class="sxs-lookup"><span data-stu-id="d0645-167">CLSID\_MsRdpClient5 is defined as 4EB89FF4-7F78-4A0F-8B8D-2BF02E94E4B2</span></span><br/> <span data-ttu-id="d0645-168">CLSID \_ MsRdpClient5NotSafeForScripting se define como 4EB2F086-C818-447E-B32C-C51CE2B30D31</span><span class="sxs-lookup"><span data-stu-id="d0645-168">CLSID\_MsRdpClient5NotSafeForScripting is defined as 4EB2F086-C818-447E-B32C-C51CE2B30D31</span></span><br/> <span data-ttu-id="d0645-169">CLSID \_ MsRdpClient6 se define como 7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span><span class="sxs-lookup"><span data-stu-id="d0645-169">CLSID\_MsRdpClient6 is defined as 7390F3D8-0439-4C05-91E3-CF5CB290C3D0</span></span><br/> <span data-ttu-id="d0645-170">CLSID \_ MsRdpClient6NotSafeForScripting se define como D2EA46A7-C2BF-426B-AF24-E19C44456399</span><span class="sxs-lookup"><span data-stu-id="d0645-170">CLSID\_MsRdpClient6NotSafeForScripting is defined as D2EA46A7-C2BF-426B-AF24-E19C44456399</span></span><br/> <span data-ttu-id="d0645-171">CLSID \_ MsRdpClient7 se define como A9D7038D-B5ED-472E-9C47-94BEA90A5910</span><span class="sxs-lookup"><span data-stu-id="d0645-171">CLSID\_MsRdpClient7 is defined as A9D7038D-B5ED-472E-9C47-94BEA90A5910</span></span><br/> <span data-ttu-id="d0645-172">CLSID \_ MsRdpClient7NotSafeForScripting se define como 54D38BF7-B1EF-4479-9674-1BD6EA465258</span><span class="sxs-lookup"><span data-stu-id="d0645-172">CLSID\_MsRdpClient7NotSafeForScripting is defined as 54D38BF7-B1EF-4479-9674-1BD6EA465258</span></span><br/> <span data-ttu-id="d0645-173">CLSID \_ MsRdpClient8 se define como 5F681803-2900-4C43-A1CC-CF405404A676</span><span class="sxs-lookup"><span data-stu-id="d0645-173">CLSID\_MsRdpClient8 is defined as 5F681803-2900-4C43-A1CC-CF405404A676</span></span><br/> <span data-ttu-id="d0645-174">CLSID \_ MsRdpClient8NotSafeForScripting se define como A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="d0645-174">CLSID\_MsRdpClient8NotSafeForScripting is defined as A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span><br/> <span data-ttu-id="d0645-175">CLSID \_ MsRdpClient9 se define como 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span><span class="sxs-lookup"><span data-stu-id="d0645-175">CLSID\_MsRdpClient9 is defined as 301B94BA-5D25-4A12-BFFE-3B6E7A616585</span></span><br/> <span data-ttu-id="d0645-176">CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="d0645-176">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> |
| <span data-ttu-id="d0645-177">IID</span><span class="sxs-lookup"><span data-stu-id="d0645-177">IID</span></span><br/>                      | <span data-ttu-id="d0645-178">IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219</span><span class="sxs-lookup"><span data-stu-id="d0645-178">IID\_IMsRdpClientNonScriptable3 is defined as b3378d90-0728-45c7-8ed7-b6159fb92219</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |



## <a name="see-also"></a><span data-ttu-id="d0645-179">Vea también</span><span class="sxs-lookup"><span data-stu-id="d0645-179">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0645-180">**IMsRdpClientNonScriptable2**</span><span class="sxs-lookup"><span data-stu-id="d0645-180">**IMsRdpClientNonScriptable2**</span></span>](imsrdpclientnonscriptable2.md)
</dt> <dt>

[<span data-ttu-id="d0645-181">**IMsRdpClientNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="d0645-181">**IMsRdpClientNonScriptable**</span></span>](imsrdpclientnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="d0645-182">**IMsTscNonScriptable**</span><span class="sxs-lookup"><span data-stu-id="d0645-182">**IMsTscNonScriptable**</span></span>](imstscnonscriptable-interface.md)
</dt> <dt>

[<span data-ttu-id="d0645-183">Referencia de Conexión web a Escritorio remoto</span><span class="sxs-lookup"><span data-stu-id="d0645-183">Remote Desktop Web Connection Reference</span></span>](remote-desktop-web-connection-reference.md)
</dt> </dl>

 

 





