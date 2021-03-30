---
title: Propiedad Property de la interfaz IMsRdpExtendedSettings
description: Contiene una propiedad con nombre.
ms.assetid: 3acaeff9-1617-46c3-80c3-b87496b83670
ms.tgt_platform: multiple
keywords:
- Propiedad de propiedad Servicios de Escritorio remoto
- Propiedad de propiedad Servicios de Escritorio remoto, interfaz IMsRdpExtendedSettings
- Servicios de Escritorio remoto de la interfaz IMsRdpExtendedSettings, propiedad propiedad
topic_type:
- apiref
api_name:
- IMsRdpExtendedSettings.Property
- IMsRdpExtendedSettings.get_Property
- IMsRdpExtendedSettings.put_Property
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1eadc8ce59e5a2bd50a4e61ad75b5124b24c21b8
ms.sourcegitcommit: 04e801237156e90b48111d60bddf437f87f5cdfe
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/19/2020
ms.locfileid: "103805162"
---
# <a name="imsrdpextendedsettingsproperty-property"></a><span data-ttu-id="b4d93-106">IMsRdpExtendedSettings::P propiedad filtros</span><span class="sxs-lookup"><span data-stu-id="b4d93-106">IMsRdpExtendedSettings::Property property</span></span>

<span data-ttu-id="b4d93-107">Contiene una propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="b4d93-107">Contains a named property.</span></span>

<span data-ttu-id="b4d93-108">Esta propiedad es de lectura y escritura.</span><span class="sxs-lookup"><span data-stu-id="b4d93-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b4d93-109">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="b4d93-109">Syntax</span></span>


```C++
HRESULT put_Property(
  [in]          BSTR    bstrPropertyName,
  [in]          VARIANT *pValue
);

HRESULT get_Property(
  [in]          BSTR    bstrPropertyName,
  [out, retval] VARIANT *pValue
);
```



## <a name="property-value"></a><span data-ttu-id="b4d93-110">Valor de propiedad</span><span class="sxs-lookup"><span data-stu-id="b4d93-110">Property value</span></span>

<span data-ttu-id="b4d93-111">Valor de la propiedad con nombre.</span><span class="sxs-lookup"><span data-stu-id="b4d93-111">The named property value.</span></span>

| <span data-ttu-id="b4d93-112">Nombre de propiedad</span><span class="sxs-lookup"><span data-stu-id="b4d93-112">Property name</span></span> | <span data-ttu-id="b4d93-113">Tipo de datos</span><span class="sxs-lookup"><span data-stu-id="b4d93-113">Data type</span></span> | <span data-ttu-id="b4d93-114">Access</span><span class="sxs-lookup"><span data-stu-id="b4d93-114">Access</span></span> | <span data-ttu-id="b4d93-115">Se puede cambiar una vez iniciada la conexión</span><span class="sxs-lookup"><span data-stu-id="b4d93-115">Can be changed after connection started</span></span> | <span data-ttu-id="b4d93-116">Descripción</span><span class="sxs-lookup"><span data-stu-id="b4d93-116">Description</span></span> |
|----------|-----------|--------|-----------------------------------------|-------------|
| <span data-ttu-id="b4d93-117">ConnectToChildSession</span><span class="sxs-lookup"><span data-stu-id="b4d93-117">ConnectToChildSession</span></span> | <span data-ttu-id="b4d93-118">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="b4d93-118">**VT\_BOOL**</span></span> | <span data-ttu-id="b4d93-119">Lectura/Escritura</span><span class="sxs-lookup"><span data-stu-id="b4d93-119">Read/Write</span></span> | <span data-ttu-id="b4d93-120">Sí</span><span class="sxs-lookup"><span data-stu-id="b4d93-120">Yes</span></span> | <span data-ttu-id="b4d93-121">Establecer esta propiedad en **true** hace que el control de cliente se conecte a la sesión secundaria en el equipo local en lugar de a un servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="b4d93-121">Setting this property to **True** causes the client control to connect to the child session on the local machine instead of a remote server.</span></span> <span data-ttu-id="b4d93-122">Si esta propiedad se establece en **true**, no se puede conectar a un servidor remoto porque todas las conexiones se redirigen a localhost.</span><span class="sxs-lookup"><span data-stu-id="b4d93-122">If this property is set to **true**, you cannot connect to a remote server because all connections are redirected to localhost.</span></span> <span data-ttu-id="b4d93-123">Para obtener más información sobre las sesiones secundarias, vea [sesiones secundarias](child-sessions.md).</span><span class="sxs-lookup"><span data-stu-id="b4d93-123">For more information about child sessions, see [Child Sessions](child-sessions.md).</span></span> |
| <span data-ttu-id="b4d93-124">DisableCredentialsDelegation</span><span class="sxs-lookup"><span data-stu-id="b4d93-124">DisableCredentialsDelegation</span></span> | <span data-ttu-id="b4d93-125">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="b4d93-125">**VT\_BOOL**</span></span> | <span data-ttu-id="b4d93-126">Lectura/Escritura</span><span class="sxs-lookup"><span data-stu-id="b4d93-126">Read/Write</span></span> | <span data-ttu-id="b4d93-127">No</span><span class="sxs-lookup"><span data-stu-id="b4d93-127">No</span></span> | <span data-ttu-id="b4d93-128">Si **es true**, las credenciales no se envían al servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="b4d93-128">If **True**, credentials are not sent to the remote server.</span></span> |
| <span data-ttu-id="b4d93-129">EnableFrameBufferRedirection</span><span class="sxs-lookup"><span data-stu-id="b4d93-129">EnableFrameBufferRedirection</span></span> | <span data-ttu-id="b4d93-130">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="b4d93-130">**VT\_BOOL**</span></span> | <span data-ttu-id="b4d93-131">Lectura/Escritura</span><span class="sxs-lookup"><span data-stu-id="b4d93-131">Read/Write</span></span> | <span data-ttu-id="b4d93-132">No</span><span class="sxs-lookup"><span data-stu-id="b4d93-132">No</span></span> | <span data-ttu-id="b4d93-133">Si es **true**, se intenta la redirección de búfer de fotogramas.</span><span class="sxs-lookup"><span data-stu-id="b4d93-133">If **True**, frame buffer redirection is attempted.</span></span> <span data-ttu-id="b4d93-134">En el caso de una conexión de bucle invertido (el mismo equipo es el cliente y el servidor), el redireccionamiento de búfer de fotogramas permite compartir la memoria del búfer de fotogramas entre las sesiones.</span><span class="sxs-lookup"><span data-stu-id="b4d93-134">For a loopback connection (the same computer is both client and server) frame buffer redirection allows the memory for the frame buffer to be shared between the sessions.</span></span> |
| <span data-ttu-id="b4d93-135">EnableHardwareMode</span><span class="sxs-lookup"><span data-stu-id="b4d93-135">EnableHardwareMode</span></span> | <span data-ttu-id="b4d93-136">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="b4d93-136">**VT\_BOOL**</span></span>  | <span data-ttu-id="b4d93-137">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="b4d93-137">Write Only</span></span> | <span data-ttu-id="b4d93-138">No</span><span class="sxs-lookup"><span data-stu-id="b4d93-138">No</span></span> | <span data-ttu-id="b4d93-139">Si es **true**, se intenta el hardware de ayuda con la descodificación de gráficos.</span><span class="sxs-lookup"><span data-stu-id="b4d93-139">If **True**, hardware assist with graphics decoding is attempted.</span></span> |
| <span data-ttu-id="b4d93-140">IgnoreCursors</span><span class="sxs-lookup"><span data-stu-id="b4d93-140">IgnoreCursors</span></span> | <span data-ttu-id="b4d93-141">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="b4d93-141">**VT\_BOOL**</span></span> | <span data-ttu-id="b4d93-142">Solo escritura</span><span class="sxs-lookup"><span data-stu-id="b4d93-142">Write Only</span></span> | <span data-ttu-id="b4d93-143">No</span><span class="sxs-lookup"><span data-stu-id="b4d93-143">No</span></span> | <span data-ttu-id="b4d93-144">Si **es true**, se omiten los cursores enviados por el servidor remoto.</span><span class="sxs-lookup"><span data-stu-id="b4d93-144">If **True**, cursors sent by the remote server are ignored.</span></span> |
| <span data-ttu-id="b4d93-145">ManualClipboardSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="b4d93-145">ManualClipboardSyncEnabled</span></span> | <span data-ttu-id="b4d93-146">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="b4d93-146">**VT\_BOOL**</span></span> | <span data-ttu-id="b4d93-147">Lectura/Escritura</span><span class="sxs-lookup"><span data-stu-id="b4d93-147">Read/Write</span></span> | <span data-ttu-id="b4d93-148">Sí</span><span class="sxs-lookup"><span data-stu-id="b4d93-148">Yes</span></span> | <span data-ttu-id="b4d93-149">Establecer esta propiedad en **true** significa que los portapapeles locales y remotos no se mantendrán automáticamente sincronizados. En su lugar, se debe usar la interfaz [**IMsRdpClipboard**](imsrdpclipboard.md) para sincronizar los formatos del Portapapeles desde el portapapeles local con el portapapeles remoto y el portapapeles remoto con el portapapeles local.</span><span class="sxs-lookup"><span data-stu-id="b4d93-149">Setting this property to **True** means that the local and remote clipboards will not be automatically kept in sync. Instead the [**IMsRdpClipboard**](imsrdpclipboard.md) interface must be used to sync clipboard formats from the local clipboard to the remote clipboard and the remote clipboard to the local clipboard.</span></span> |
| <span data-ttu-id="b4d93-150">ZoomLevel (</span><span class="sxs-lookup"><span data-stu-id="b4d93-150">ZoomLevel</span></span> | <span data-ttu-id="b4d93-151">\**_VT \_ UI4_*</span><span class="sxs-lookup"><span data-stu-id="b4d93-151">\**_VT\_UI4_*</span></span> | <span data-ttu-id="b4d93-152">Lectura/Escritura</span><span class="sxs-lookup"><span data-stu-id="b4d93-152">Read/Write</span></span> | <span data-ttu-id="b4d93-153">Sí</span><span class="sxs-lookup"><span data-stu-id="b4d93-153">Yes</span></span> | <span data-ttu-id="b4d93-154">Implementa la característica de zoom mediante el control ActiveX RDP.</span><span class="sxs-lookup"><span data-stu-id="b4d93-154">Implements the Zoom feature by using the RDP ActiveX control.</span></span> <span data-ttu-id="b4d93-155">La característica de zoom está disponible en el menú **sistema** de RDP.</span><span class="sxs-lookup"><span data-stu-id="b4d93-155">The Zoom feature is available from the **System** menu of RDP.</span></span> <span data-ttu-id="b4d93-156">La propiedad **zoomLevel (** no tiene ningún efecto en el modo RemoteApp y en el modo de pantalla completa.</span><span class="sxs-lookup"><span data-stu-id="b4d93-156">The **ZoomLevel** property has no effect in RemoteApp mode and full-screen mode.</span></span> <span data-ttu-id="b4d93-157">[**IMsRdpClientAdvancedSettings:: SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) y **zoomLevel (** se excluyen mutuamente.</span><span class="sxs-lookup"><span data-stu-id="b4d93-157">[**IMsRdpClientAdvancedSettings::SmartSizing**](imsrdpclientadvancedsettings-smartsizing.md) and **ZoomLevel** are mutually exclusive.</span></span> |

## <a name="requirements"></a><span data-ttu-id="b4d93-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b4d93-158">Requirements</span></span>



| <span data-ttu-id="b4d93-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="b4d93-159">Requirement</span></span> | <span data-ttu-id="b4d93-160">Value</span><span class="sxs-lookup"><span data-stu-id="b4d93-160">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b4d93-161">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4d93-161">Minimum supported client</span></span><br/> | <span data-ttu-id="b4d93-162">Windows 8</span><span class="sxs-lookup"><span data-stu-id="b4d93-162">Windows 8</span></span><br/>                                                                                                                                                                                                                                                                                           |
| <span data-ttu-id="b4d93-163">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b4d93-163">Minimum supported server</span></span><br/> | <span data-ttu-id="b4d93-164">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="b4d93-164">Windows Server 2012</span></span><br/>                                                                                                                                                                                                                                                                                 |
| <span data-ttu-id="b4d93-165">Biblioteca de tipos</span><span class="sxs-lookup"><span data-stu-id="b4d93-165">Type library</span></span><br/>             | <dl> <span data-ttu-id="b4d93-166"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4d93-166"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                         |
| <span data-ttu-id="b4d93-167">Archivo DLL</span><span class="sxs-lookup"><span data-stu-id="b4d93-167">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b4d93-168"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b4d93-168"><dt>MsTscAx.dll</dt></span></span> </dl>                                                                                                                                                                                                                         |
| <span data-ttu-id="b4d93-169">CLSID</span><span class="sxs-lookup"><span data-stu-id="b4d93-169">CLSID</span></span><br/>                    | <span data-ttu-id="b4d93-170">CLSID \_ MsRdpClient7NotSafeForScripting se define como 54d38bf7-b1ef-4479-9674-1bd6ea465258</span><span class="sxs-lookup"><span data-stu-id="b4d93-170">CLSID\_MsRdpClient7NotSafeForScripting is defined as 54d38bf7-b1ef-4479-9674-1bd6ea465258</span></span><br/> <span data-ttu-id="b4d93-171">CLSID \_ MsRdpClient8NotSafeForScripting se define como A3BC03A0-041D-42E3-AD22-882B7865C9C5</span><span class="sxs-lookup"><span data-stu-id="b4d93-171">CLSID\_MsRdpClient8NotSafeForScripting is defined as A3BC03A0-041D-42E3-AD22-882B7865C9C5</span></span><br/> <span data-ttu-id="b4d93-172">CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span><span class="sxs-lookup"><span data-stu-id="b4d93-172">CLSID\_MsRdpClient9NotSafeForScripting is defined as 8B918B82-7985-4C24-89DF-C33AD2BBFBCD</span></span><br/> |
| <span data-ttu-id="b4d93-173">IID</span><span class="sxs-lookup"><span data-stu-id="b4d93-173">IID</span></span><br/>                      | <span data-ttu-id="b4d93-174">IID \_ IMsRdpExtendedSettings se define como 302D8188-0052-4807-806A-362B628F9AC5</span><span class="sxs-lookup"><span data-stu-id="b4d93-174">IID\_IMsRdpExtendedSettings is defined as 302D8188-0052-4807-806A-362B628F9AC5</span></span><br/>                                                                                                                                                                                                                      |



## <a name="see-also"></a><span data-ttu-id="b4d93-175">Vea también</span><span class="sxs-lookup"><span data-stu-id="b4d93-175">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b4d93-176">**IMsRdpExtendedSettings**</span><span class="sxs-lookup"><span data-stu-id="b4d93-176">**IMsRdpExtendedSettings**</span></span>](imsrdpextendedsettings.md)
</dt> </dl>

 

 





