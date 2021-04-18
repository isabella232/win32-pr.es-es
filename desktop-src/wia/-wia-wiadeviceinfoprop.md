---
description: Las propiedades de información de dispositivos son propiedades que describen la instalación y la instalación del dispositivo.
ms.assetid: ff6771ac-491e-4765-8cfe-11c7efc1c971
title: Constantes de propiedad de información del dispositivo (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DIP_DEV_ID
- WIA_DIP_VEND_DESC
- WIA_DIP_DEV_DESC
- WIA_DIP_DEV_TYPE
- WIA_DIP_PORT_NAME
- WIA_DIP_DEV_NAME
- WIA_DIP_SERVER_NAME
- WIA_DIP_REMOTE_DEV_ID
- WIA_DIP_UI_CLSID
- WIA_DIP_HW_CONFIG
- WIA_DIP_BAUDRATE
- WIA_DIP_STI_GEN_CAPABILITIES
- WIA_DIP_WIA_VERSION
- WIA_DIP_DRIVER_VERSION
- WIA_DIP_PNP_ID
- WIA_DIP_STI_DRIVER_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 18c44bb310c2dcee5bb227e0885a71b58f5b362e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105715169"
---
# <a name="device-information-property-constants"></a><span data-ttu-id="e9eb0-103">Constantes de propiedades de información del dispositivo</span><span class="sxs-lookup"><span data-stu-id="e9eb0-103">Device Information Property Constants</span></span>

<span data-ttu-id="e9eb0-104">Las propiedades de información de dispositivos son propiedades que describen la instalación y la instalación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-104">Device Information Properties are properties that describe the setup and installation of the device.</span></span> <span data-ttu-id="e9eb0-105">Estas propiedades están disponibles a través de las interfaces [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) y también a través del elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-105">These properties are available through the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interfaces and also through the root item.</span></span> <span data-ttu-id="e9eb0-106">Las propiedades de información del dispositivo tienen el prefijo "WIA \_ DIP \_ " (propiedad de información del dispositivo) y se proporcionan mediante la adquisición de imágenes de Windows (WIA).</span><span class="sxs-lookup"><span data-stu-id="e9eb0-106">Device information properties are prefixed with "WIA\_DIP\_" (Device Information Property) and are supplied by Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="e9eb0-107">Con fines de scripting, estas constantes usan el prefijo "DeviceInfo" y forman parte del tipo enumerado [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="e9eb0-107">For scripting purposes, these constants use the prefix "DeviceInfo" and are part of the [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) enumerated type.</span></span> <span data-ttu-id="e9eb0-108">El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis al lado del nombre de la constante de C/C++ en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-108">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="e9eb0-109">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="e9eb0-109">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="e9eb0-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9eb0-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <span data-ttu-id="e9eb0-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eb0-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e9eb0-112">Cadena de identificador de dispositivo para el minicontrolador WIA.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-112">The device ID string for the WIA minidriver.</span></span> <span data-ttu-id="e9eb0-113">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-113">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="e9eb0-114">Tipo: VT_BSTR, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9eb0-114">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <span data-ttu-id="e9eb0-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eb0-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e9eb0-116">Cadena de Descripción del proveedor para el minicontrolador WIA.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-116">The vendor description string for the WIA minidriver.</span></span> <span data-ttu-id="e9eb0-117">La descripción del proveedor se obtiene del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-117">The vendor description is obtained from the INF file.</span></span> <span data-ttu-id="e9eb0-118">Una aplicación Lee esta propiedad para obtener una descripción del proveedor del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-118">An application reads this property to get a description of the device vendor.</span></span> <span data-ttu-id="e9eb0-119">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-119">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="e9eb0-120">Tipo: VT_BSTR, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9eb0-120">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <span data-ttu-id="e9eb0-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eb0-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e9eb0-122">Cadena de Descripción del dispositivo para el minicontrolador WIA.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-122">The device description string for the WIA minidriver.</span></span> <span data-ttu-id="e9eb0-123">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-123">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9eb0-124">La cadena de Descripción del dispositivo que contiene esta propiedad se obtiene del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-124">The device description string this property contains is obtained from the INF file.</span></span> <span data-ttu-id="e9eb0-125">Una aplicación Lee esta propiedad para obtener una descripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-125">An application reads this property to get a description of the device.</span></span><br/> <span data-ttu-id="e9eb0-126">Tipo: VT_BSTR, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9eb0-126">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <span data-ttu-id="e9eb0-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eb0-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="e9eb0-128">El tipo de dispositivo y el subtipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-128">The device type and device subtype.</span></span> <span data-ttu-id="e9eb0-129">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-129">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9eb0-130">Use la macro GET_STIDEVICE_TYPE para obtener el tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-130">Use the GET_STIDEVICE_TYPE macro to get the device type.</span></span> <span data-ttu-id="e9eb0-131">El tipo de dispositivo y el subtipo se obtienen del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-131">The device type and subtype are obtained from the INF file.</span></span> <span data-ttu-id="e9eb0-132">Una aplicación Lee esta propiedad para determinar si usa un escáner, cámara o dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-132">An application reads this property to determine whether it is using a scanner, camera, or video device.</span></span><br/> <span data-ttu-id="e9eb0-133">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9eb0-133">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="e9eb0-134">Actualmente, los tipos de dispositivo se definen como se indica a continuación.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-134">Currently, device types are defined as follows.</span></span> <span data-ttu-id="e9eb0-135">El asterisco \* indica que el tipo de dispositivo no es compatible con Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-135">The asterisk \* indicates that the device type is not supported by Windows Vista and later.</span></span> <span data-ttu-id="e9eb0-136">El doble asterisco \* \* indica que el tipo de dispositivo no es compatible con Windows Server 2003, Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-136">The double asterisk \*\* indicates that the device type is not supported by either Windows Server 2003, Windows Vista, or later.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e9eb0-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="e9eb0-137">Type</span></span></th>
<th><span data-ttu-id="e9eb0-138">Value</span><span class="sxs-lookup"><span data-stu-id="e9eb0-138">Value</span></span></th>
<th><span data-ttu-id="e9eb0-139">Definición</span><span class="sxs-lookup"><span data-stu-id="e9eb0-139">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9eb0-140">StiDeviceTypeDefault</span><span class="sxs-lookup"><span data-stu-id="e9eb0-140">StiDeviceTypeDefault</span></span></td>
<td><span data-ttu-id="e9eb0-141">0x0000</span><span class="sxs-lookup"><span data-stu-id="e9eb0-141">0x0000</span></span></td>
<td><span data-ttu-id="e9eb0-142">Dispositivo predeterminado</span><span class="sxs-lookup"><span data-stu-id="e9eb0-142">Default device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9eb0-143">StiDeviceTypeScanner</span><span class="sxs-lookup"><span data-stu-id="e9eb0-143">StiDeviceTypeScanner</span></span></td>
<td><span data-ttu-id="e9eb0-144">0x0001</span><span class="sxs-lookup"><span data-stu-id="e9eb0-144">0x0001</span></span></td>
<td><span data-ttu-id="e9eb0-145">Dispositivo de escáner (vea la <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> para determinar si el escáner está plano o está alimentado por hojas).</span><span class="sxs-lookup"><span data-stu-id="e9eb0-145">Scanner device (See the <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> to determine if the scanner is flatbed or sheet-fed.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e9eb0-146">StiDeviceTypeDigitalCamera\*</span><span class="sxs-lookup"><span data-stu-id="e9eb0-146">StiDeviceTypeDigitalCamera\*</span></span></td>
<td><span data-ttu-id="e9eb0-147">0x0002</span><span class="sxs-lookup"><span data-stu-id="e9eb0-147">0x0002</span></span></td>
<td><span data-ttu-id="e9eb0-148">Dispositivo de cámara</span><span class="sxs-lookup"><span data-stu-id="e9eb0-148">Camera device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9eb0-149">StiDeviceTypeStreamingVideo\*\*</span><span class="sxs-lookup"><span data-stu-id="e9eb0-149">StiDeviceTypeStreamingVideo\*\*</span></span></td>
<td><span data-ttu-id="e9eb0-150">0x0003</span><span class="sxs-lookup"><span data-stu-id="e9eb0-150">0x0003</span></span></td>
<td><span data-ttu-id="e9eb0-151">Dispositivo de vídeo</span><span class="sxs-lookup"><span data-stu-id="e9eb0-151">Video device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <span data-ttu-id="e9eb0-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eb0-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9eb0-153">El nombre de puerto del dispositivo instalado, asignado por el controlador de modo kernel que funciona el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-153">The installed device's port name, which is assigned by the kernel-mode driver that operates the device.</span></span> <span data-ttu-id="e9eb0-154">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-154">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9eb0-155">Una aplicación Lee esta propiedad para determinar el nombre del puerto.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-155">An application reads this property to determine the port name.</span></span></p>
<p><span data-ttu-id="e9eb0-156">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9eb0-156">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <span data-ttu-id="e9eb0-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eb0-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9eb0-158">Nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-158">The name of the device.</span></span> <span data-ttu-id="e9eb0-159">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-159">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9eb0-160">El nombre del dispositivo incluido en esta propiedad se obtiene del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-160">The device name contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="e9eb0-161">Una aplicación Lee esta propiedad para obtener el nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-161">An application reads this property to obtain the name of the device.</span></span></p>
<p><span data-ttu-id="e9eb0-162">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9eb0-162">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <span data-ttu-id="e9eb0-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eb0-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9eb0-164">Nombre del servidor en el que se está ejecutando el minicontrolador WIA.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-164">The name of the server that the WIA minidriver is running on.</span></span> <span data-ttu-id="e9eb0-165">Esta propiedad es opcional para Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-165">This property is optional for Windows XP and later.</span></span></p>
<p><span data-ttu-id="e9eb0-166">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9eb0-166">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <span data-ttu-id="e9eb0-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eb0-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9eb0-168">El identificador de dispositivo del dispositivo WIA instalado en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-168">The device ID of the WIA device that is installed on a remote computer.</span></span> <span data-ttu-id="e9eb0-169">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-169">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9eb0-170">El servicio WIA solo lo usa internamente.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-170">It is only used internally by the WIA service.</span></span></p>
<p><span data-ttu-id="e9eb0-171">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9eb0-171">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <span data-ttu-id="e9eb0-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eb0-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9eb0-173">El CLSID proporcionado por el proveedor para cualquier objeto COM de extensión de la interfaz de usuario que se instala con el minicontrolador WIA.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-173">The vendor-supplied CLSID for any UI extension COM object that is installed with the WIA minidriver.</span></span> <span data-ttu-id="e9eb0-174">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-174">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9eb0-175">El valor CLSID de la interfaz de usuario contenido en esta propiedad se obtiene del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-175">The UI CLSID value contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="e9eb0-176">Si no se especifica ningún CLSID de interfaz de usuario, el servicio WIA proporciona un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-176">If no UI CLSID is specified, the WIA service supplies a default value.</span></span> <span data-ttu-id="e9eb0-177">Esta propiedad solo la usa internamente el servicio WIA cuando se muestra la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-177">This property is only used internally by the WIA service when UI is being displayed.</span></span></p>
<p><span data-ttu-id="e9eb0-178">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9eb0-178">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <span data-ttu-id="e9eb0-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eb0-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9eb0-180">El tipo de conexión que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-180">The type of connection that the device is using.</span></span> <span data-ttu-id="e9eb0-181">El servicio WIA crea y mantiene esta propiedad y solo el servicio WIA puede cambiarla.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-181">The WIA service creates and maintains this property, and only the WIA service can change it.</span></span></p>
<p><span data-ttu-id="e9eb0-182">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9eb0-182">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="e9eb0-183">La propiedad puede tener los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-183">The property can have the following possible values.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="e9eb0-184">Value</span><span class="sxs-lookup"><span data-stu-id="e9eb0-184">Value</span></span></th>
<th><span data-ttu-id="e9eb0-185">Definición</span><span class="sxs-lookup"><span data-stu-id="e9eb0-185">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e9eb0-186">1</span><span class="sxs-lookup"><span data-stu-id="e9eb0-186">1</span></span></td>
<td><span data-ttu-id="e9eb0-187">Dispositivo WDM genérico</span><span class="sxs-lookup"><span data-stu-id="e9eb0-187">Generic WDM device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9eb0-188">2</span><span class="sxs-lookup"><span data-stu-id="e9eb0-188">2</span></span></td>
<td><span data-ttu-id="e9eb0-189">Dispositivo SCSI</span><span class="sxs-lookup"><span data-stu-id="e9eb0-189">SCSI device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e9eb0-190">4</span><span class="sxs-lookup"><span data-stu-id="e9eb0-190">4</span></span></td>
<td><span data-ttu-id="e9eb0-191">Dispositivo USB</span><span class="sxs-lookup"><span data-stu-id="e9eb0-191">USB device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e9eb0-192">8</span><span class="sxs-lookup"><span data-stu-id="e9eb0-192">8</span></span></td>
<td><span data-ttu-id="e9eb0-193">Dispositivo serie</span><span class="sxs-lookup"><span data-stu-id="e9eb0-193">Serial device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e9eb0-194">16</span><span class="sxs-lookup"><span data-stu-id="e9eb0-194">16</span></span></td>
<td><span data-ttu-id="e9eb0-195">Dispositivo paralelo</span><span class="sxs-lookup"><span data-stu-id="e9eb0-195">Parallel device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <span data-ttu-id="e9eb0-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eb0-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9eb0-197">La configuración de la velocidad en baudios actual para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-197">The current baud rate setting for the device.</span></span> <span data-ttu-id="e9eb0-198">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-198">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9eb0-199">El valor debe estar &quot; vacío &quot; si el dispositivo no está conectado mediante un cable serie.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-199">The value should be &quot;Empty&quot; if the device is not connected by a serial cable.</span></span></p>
<p><span data-ttu-id="e9eb0-200">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9eb0-200">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <span data-ttu-id="e9eb0-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eb0-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9eb0-202">Las capacidades de STI genéricas para el dispositivo que se obtienen del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-202">The generic STI capabilities for the device as obtained from the INF file.</span></span> <span data-ttu-id="e9eb0-203">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-203">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9eb0-204">Una aplicación Lee esta propiedad para determinar las funciones STI genéricas del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-204">An application reads this property to determine the generic STI capabilities of the device.</span></span></p>
<p><span data-ttu-id="e9eb0-205">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9eb0-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <span data-ttu-id="e9eb0-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eb0-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9eb0-207">Número (como cadena) de la versión de WIA actual que está instalada en el sistema.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-207">The number (as a string) of the current WIA version that is installed on the system.</span></span> <span data-ttu-id="e9eb0-208">Una aplicación Lee esta propiedad para determinar la versión de WIA que está instalada en el sistema.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-208">An application reads this property to determine the version of WIA that is installed on the system.</span></span> <span data-ttu-id="e9eb0-209">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-209">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9eb0-210">Esta propiedad está disponible en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-210">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="e9eb0-211">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9eb0-211">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <span data-ttu-id="e9eb0-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eb0-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9eb0-213">Versión del archivo DLL actual del minicontrolador WIA.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-213">The current DLL version of the WIA minidriver.</span></span> <span data-ttu-id="e9eb0-214">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-214">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9eb0-215">Esta propiedad está disponible en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-215">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="e9eb0-216">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9eb0-216">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <span data-ttu-id="e9eb0-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eb0-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9eb0-218">Identificador de PnP actual para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-218">The current PnP id for the device.</span></span> <span data-ttu-id="e9eb0-219">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-219">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9eb0-220">Esta propiedad está disponible en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-220">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="e9eb0-221">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9eb0-221">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <span data-ttu-id="e9eb0-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="e9eb0-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="e9eb0-223">Versión del controlador STI genérico.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-223">The generic STI driver version.</span></span> <span data-ttu-id="e9eb0-224">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-224">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="e9eb0-225">Una aplicación Lee esta propiedad para determinar la versión del controlador STI genérico.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-225">An application reads this property to determine the generic STI driver version.</span></span> <span data-ttu-id="e9eb0-226">Esta propiedad está disponible en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="e9eb0-226">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="e9eb0-227">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="e9eb0-227">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="e9eb0-228">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9eb0-228">Requirements</span></span>



| <span data-ttu-id="e9eb0-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9eb0-229">Requirement</span></span> | <span data-ttu-id="e9eb0-230">Value</span><span class="sxs-lookup"><span data-stu-id="e9eb0-230">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e9eb0-231">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9eb0-231">Minimum supported client</span></span><br/> | <span data-ttu-id="e9eb0-232">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="e9eb0-232">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="e9eb0-233">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="e9eb0-233">Minimum supported server</span></span><br/> | <span data-ttu-id="e9eb0-234">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="e9eb0-234">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e9eb0-235">Encabezado</span><span class="sxs-lookup"><span data-stu-id="e9eb0-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="e9eb0-236"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="e9eb0-236"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




