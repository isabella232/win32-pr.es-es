---
description: 'Constantes de propiedades de información de dispositivo: las propiedades de información del dispositivo son propiedades que describen la instalación e instalación del dispositivo.'
ms.assetid: ff6771ac-491e-4765-8cfe-11c7efc1c971
title: Constantes de propiedad de información de dispositivo (Wiadef.h)
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
ms.openlocfilehash: aec37ae84eed6b15bc10a4e979a5d95d21be3423
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097243"
---
# <a name="device-information-property-constants"></a><span data-ttu-id="b61f1-103">Constantes de propiedad de información de dispositivo</span><span class="sxs-lookup"><span data-stu-id="b61f1-103">Device Information Property Constants</span></span>

<span data-ttu-id="b61f1-104">Las propiedades de información del dispositivo son propiedades que describen la instalación e instalación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b61f1-104">Device Information Properties are properties that describe the setup and installation of the device.</span></span> <span data-ttu-id="b61f1-105">Estas propiedades están disponibles a través de las interfaces [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) o [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) y también a través del elemento raíz.</span><span class="sxs-lookup"><span data-stu-id="b61f1-105">These properties are available through the [**IWiaDevMgr**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiadevmgr) or [**IWiaDevMgr2**](-wia-iwiadevmgr2.md) interfaces and also through the root item.</span></span> <span data-ttu-id="b61f1-106">Las propiedades de información del dispositivo tienen el prefijo "WIA DIP" (propiedad de información del dispositivo) y se proporcionan mediante adquisición de \_ imágenes de Windows \_ (WIA).</span><span class="sxs-lookup"><span data-stu-id="b61f1-106">Device information properties are prefixed with "WIA\_DIP\_" (Device Information Property) and are supplied by Windows Image Acquisition (WIA).</span></span> <span data-ttu-id="b61f1-107">Con fines de scripting, estas constantes usan el prefijo "DeviceInfo" y forman parte del tipo enumerado [WiaDeviceInfoPropertyId.](-wia-wiadeviceinfopropertyid.md)</span><span class="sxs-lookup"><span data-stu-id="b61f1-107">For scripting purposes, these constants use the prefix "DeviceInfo" and are part of the [WiaDeviceInfoPropertyId](-wia-wiadeviceinfopropertyid.md) enumerated type.</span></span> <span data-ttu-id="b61f1-108">El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis junto al nombre de constante de C/C++ en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="b61f1-108">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="b61f1-109">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="b61f1-109">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="b61f1-110">Descripción</span><span class="sxs-lookup"><span data-stu-id="b61f1-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_ID"></span><span id="wia_dip_dev_id"></span><dl> <span data-ttu-id="b61f1-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span><span class="sxs-lookup"><span data-stu-id="b61f1-111"><dt><strong>WIA_DIP_DEV_ID</strong></dt> <dt>DeviceInfoDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b61f1-112">Cadena de identificador de dispositivo para el minidriver wia.</span><span class="sxs-lookup"><span data-stu-id="b61f1-112">The device ID string for the WIA minidriver.</span></span> <span data-ttu-id="b61f1-113">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b61f1-113">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="b61f1-114">Tipo: VT_BSTR, Acceso: solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b61f1-114">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_VEND_DESC"></span><span id="wia_dip_vend_desc"></span><dl> <span data-ttu-id="b61f1-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span><span class="sxs-lookup"><span data-stu-id="b61f1-115"><dt><strong>WIA_DIP_VEND_DESC</strong></dt> <dt>DeviceInfoVendDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b61f1-116">Cadena de descripción del proveedor para el minidriver de WIA.</span><span class="sxs-lookup"><span data-stu-id="b61f1-116">The vendor description string for the WIA minidriver.</span></span> <span data-ttu-id="b61f1-117">La descripción del proveedor se obtiene del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="b61f1-117">The vendor description is obtained from the INF file.</span></span> <span data-ttu-id="b61f1-118">Una aplicación lee esta propiedad para obtener una descripción del proveedor del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b61f1-118">An application reads this property to get a description of the device vendor.</span></span> <span data-ttu-id="b61f1-119">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b61f1-119">The WIA service creates and maintains this property.</span></span><br/> <span data-ttu-id="b61f1-120">Tipo: VT_BSTR, Acceso: solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b61f1-120">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_DEV_DESC"></span><span id="wia_dip_dev_desc"></span><dl> <span data-ttu-id="b61f1-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span><span class="sxs-lookup"><span data-stu-id="b61f1-121"><dt><strong>WIA_DIP_DEV_DESC</strong></dt> <dt>DeviceInfoDevDesc</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b61f1-122">Cadena de descripción del dispositivo para el minidriver de WIA.</span><span class="sxs-lookup"><span data-stu-id="b61f1-122">The device description string for the WIA minidriver.</span></span> <span data-ttu-id="b61f1-123">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b61f1-123">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="b61f1-124">La cadena de descripción del dispositivo que contiene esta propiedad se obtiene del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="b61f1-124">The device description string this property contains is obtained from the INF file.</span></span> <span data-ttu-id="b61f1-125">Una aplicación lee esta propiedad para obtener una descripción del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b61f1-125">An application reads this property to get a description of the device.</span></span><br/> <span data-ttu-id="b61f1-126">Tipo: VT_BSTR, Acceso: solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b61f1-126">Type: VT_BSTR, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_TYPE"></span><span id="wia_dip_dev_type"></span><dl> <span data-ttu-id="b61f1-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span><span class="sxs-lookup"><span data-stu-id="b61f1-127"><dt><strong>WIA_DIP_DEV_TYPE</strong></dt> <dt>DeviceInfoDevType</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="b61f1-128">El tipo de dispositivo y el subtipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b61f1-128">The device type and device subtype.</span></span> <span data-ttu-id="b61f1-129">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b61f1-129">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="b61f1-130">Use la macro GET_STIDEVICE_TYPE para obtener el tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b61f1-130">Use the GET_STIDEVICE_TYPE macro to get the device type.</span></span> <span data-ttu-id="b61f1-131">El tipo de dispositivo y el subtipo se obtienen del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="b61f1-131">The device type and subtype are obtained from the INF file.</span></span> <span data-ttu-id="b61f1-132">Una aplicación lee esta propiedad para determinar si usa un escáner, una cámara o un dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b61f1-132">An application reads this property to determine whether it is using a scanner, camera, or video device.</span></span><br/> <span data-ttu-id="b61f1-133">Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b61f1-133">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="b61f1-134">Actualmente, los tipos de dispositivo se definen de la manera siguiente.</span><span class="sxs-lookup"><span data-stu-id="b61f1-134">Currently, device types are defined as follows.</span></span> <span data-ttu-id="b61f1-135">El asterisco \* indica que Windows Vista y versiones posteriores no admiten el tipo de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b61f1-135">The asterisk \* indicates that the device type is not supported by Windows Vista and later.</span></span> <span data-ttu-id="b61f1-136">El asterisco doble \*\* indica que el tipo de dispositivo no es compatible con Windows Server 2003, Windows Vista o versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b61f1-136">The double asterisk \*\* indicates that the device type is not supported by either Windows Server 2003, Windows Vista, or later.</span></span> <br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b61f1-137">Tipo</span><span class="sxs-lookup"><span data-stu-id="b61f1-137">Type</span></span></th>
<th><span data-ttu-id="b61f1-138">Value</span><span class="sxs-lookup"><span data-stu-id="b61f1-138">Value</span></span></th>
<th><span data-ttu-id="b61f1-139">Definición</span><span class="sxs-lookup"><span data-stu-id="b61f1-139">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b61f1-140">DeviceTypeDefault</span><span class="sxs-lookup"><span data-stu-id="b61f1-140">StiDeviceTypeDefault</span></span></td>
<td><span data-ttu-id="b61f1-141">0x0000</span><span class="sxs-lookup"><span data-stu-id="b61f1-141">0x0000</span></span></td>
<td><span data-ttu-id="b61f1-142">Dispositivo predeterminado</span><span class="sxs-lookup"><span data-stu-id="b61f1-142">Default device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b61f1-143">DeviceDeviceTypeScanner</span><span class="sxs-lookup"><span data-stu-id="b61f1-143">StiDeviceTypeScanner</span></span></td>
<td><span data-ttu-id="b61f1-144">0x0001</span><span class="sxs-lookup"><span data-stu-id="b61f1-144">0x0001</span></span></td>
<td><span data-ttu-id="b61f1-145">Dispositivo del analizador (vea <a href="-wia-wiaitempropscannerdevice.md"><strong>el WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> para determinar si el analizador está plano o está conectado a hojas).</span><span class="sxs-lookup"><span data-stu-id="b61f1-145">Scanner device (See the <a href="-wia-wiaitempropscannerdevice.md"><strong>WIA_DPS_DOCUMENT_HANDLING_CAPABILITIES</strong></a> to determine if the scanner is flatbed or sheet-fed.)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b61f1-146">DeviceDeviceTypeDigitalCamera\*</span><span class="sxs-lookup"><span data-stu-id="b61f1-146">StiDeviceTypeDigitalCamera\*</span></span></td>
<td><span data-ttu-id="b61f1-147">0x0002</span><span class="sxs-lookup"><span data-stu-id="b61f1-147">0x0002</span></span></td>
<td><span data-ttu-id="b61f1-148">Dispositivo de cámara</span><span class="sxs-lookup"><span data-stu-id="b61f1-148">Camera device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b61f1-149">DeviceDeviceTypeStreamingVideo\*\*</span><span class="sxs-lookup"><span data-stu-id="b61f1-149">StiDeviceTypeStreamingVideo\*\*</span></span></td>
<td><span data-ttu-id="b61f1-150">0x0003</span><span class="sxs-lookup"><span data-stu-id="b61f1-150">0x0003</span></span></td>
<td><span data-ttu-id="b61f1-151">Dispositivo de vídeo</span><span class="sxs-lookup"><span data-stu-id="b61f1-151">Video device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PORT_NAME"></span><span id="wia_dip_port_name"></span><dl> <span data-ttu-id="b61f1-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span><span class="sxs-lookup"><span data-stu-id="b61f1-152"><dt><strong>WIA_DIP_PORT_NAME</strong></dt> <dt>DeviceInfoPortName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b61f1-153">El nombre de puerto del dispositivo instalado, que se asigna mediante el controlador en modo kernel que opera el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b61f1-153">The installed device's port name, which is assigned by the kernel-mode driver that operates the device.</span></span> <span data-ttu-id="b61f1-154">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b61f1-154">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="b61f1-155">Una aplicación lee esta propiedad para determinar el nombre del puerto.</span><span class="sxs-lookup"><span data-stu-id="b61f1-155">An application reads this property to determine the port name.</span></span></p>
<p><span data-ttu-id="b61f1-156">Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b61f1-156">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DEV_NAME"></span><span id="wia_dip_dev_name"></span><dl> <span data-ttu-id="b61f1-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span><span class="sxs-lookup"><span data-stu-id="b61f1-157"><dt><strong>WIA_DIP_DEV_NAME</strong></dt> <dt>DeviceInfoDevName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b61f1-158">Nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b61f1-158">The name of the device.</span></span> <span data-ttu-id="b61f1-159">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b61f1-159">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="b61f1-160">El nombre del dispositivo contenido en esta propiedad se obtiene del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="b61f1-160">The device name contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="b61f1-161">Una aplicación lee esta propiedad para obtener el nombre del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b61f1-161">An application reads this property to obtain the name of the device.</span></span></p>
<p><span data-ttu-id="b61f1-162">Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b61f1-162">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_SERVER_NAME"></span><span id="wia_dip_server_name"></span><dl> <span data-ttu-id="b61f1-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span><span class="sxs-lookup"><span data-stu-id="b61f1-163"><dt><strong>WIA_DIP_SERVER_NAME</strong></dt> <dt>DeviceInfoServerName</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b61f1-164">Nombre del servidor en el que se ejecuta el minidriver de WIA.</span><span class="sxs-lookup"><span data-stu-id="b61f1-164">The name of the server that the WIA minidriver is running on.</span></span> <span data-ttu-id="b61f1-165">Esta propiedad es opcional para Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b61f1-165">This property is optional for Windows XP and later.</span></span></p>
<p><span data-ttu-id="b61f1-166">Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b61f1-166">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_REMOTE_DEV_ID"></span><span id="wia_dip_remote_dev_id"></span><dl> <span data-ttu-id="b61f1-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span><span class="sxs-lookup"><span data-stu-id="b61f1-167"><dt><strong>WIA_DIP_REMOTE_DEV_ID</strong></dt> <dt>DeviceInfoRemoteDevId</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b61f1-168">Identificador de dispositivo del dispositivo WIA que está instalado en un equipo remoto.</span><span class="sxs-lookup"><span data-stu-id="b61f1-168">The device ID of the WIA device that is installed on a remote computer.</span></span> <span data-ttu-id="b61f1-169">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b61f1-169">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="b61f1-170">Solo lo usa internamente el servicio WIA.</span><span class="sxs-lookup"><span data-stu-id="b61f1-170">It is only used internally by the WIA service.</span></span></p>
<p><span data-ttu-id="b61f1-171">Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b61f1-171">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_UI_CLSID"></span><span id="wia_dip_ui_clsid"></span><dl> <span data-ttu-id="b61f1-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span><span class="sxs-lookup"><span data-stu-id="b61f1-172"><dt><strong>WIA_DIP_UI_CLSID</strong></dt> <dt>DeviceInfoUIClsid</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b61f1-173">CLSID proporcionado por el proveedor para cualquier objeto COM de extensión de interfaz de usuario instalado con el minidriver WIA.</span><span class="sxs-lookup"><span data-stu-id="b61f1-173">The vendor-supplied CLSID for any UI extension COM object that is installed with the WIA minidriver.</span></span> <span data-ttu-id="b61f1-174">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b61f1-174">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="b61f1-175">El valor CLSID de la interfaz de usuario contenido en esta propiedad se obtiene del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="b61f1-175">The UI CLSID value contained in this property is obtained from the INF file.</span></span> <span data-ttu-id="b61f1-176">Si no se especifica ningún CLSID de interfaz de usuario, el servicio WIA proporciona un valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="b61f1-176">If no UI CLSID is specified, the WIA service supplies a default value.</span></span> <span data-ttu-id="b61f1-177">El servicio WIA solo usa esta propiedad internamente cuando se muestra la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="b61f1-177">This property is only used internally by the WIA service when UI is being displayed.</span></span></p>
<p><span data-ttu-id="b61f1-178">Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b61f1-178">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_HW_CONFIG"></span><span id="wia_dip_hw_config"></span><dl> <span data-ttu-id="b61f1-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span><span class="sxs-lookup"><span data-stu-id="b61f1-179"><dt><strong>WIA_DIP_HW_CONFIG</strong></dt> <dt>DeviceInfoHwConfig</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b61f1-180">Tipo de conexión que usa el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b61f1-180">The type of connection that the device is using.</span></span> <span data-ttu-id="b61f1-181">El servicio WIA crea y mantiene esta propiedad, y solo el servicio WIA puede cambiarla.</span><span class="sxs-lookup"><span data-stu-id="b61f1-181">The WIA service creates and maintains this property, and only the WIA service can change it.</span></span></p>
<p><span data-ttu-id="b61f1-182">Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b61f1-182">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="b61f1-183">La propiedad puede tener los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="b61f1-183">The property can have the following possible values.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b61f1-184">Value</span><span class="sxs-lookup"><span data-stu-id="b61f1-184">Value</span></span></th>
<th><span data-ttu-id="b61f1-185">Definición</span><span class="sxs-lookup"><span data-stu-id="b61f1-185">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b61f1-186">1</span><span class="sxs-lookup"><span data-stu-id="b61f1-186">1</span></span></td>
<td><span data-ttu-id="b61f1-187">Dispositivo WDM genérico</span><span class="sxs-lookup"><span data-stu-id="b61f1-187">Generic WDM device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b61f1-188">2</span><span class="sxs-lookup"><span data-stu-id="b61f1-188">2</span></span></td>
<td><span data-ttu-id="b61f1-189">Dispositivo SCSI</span><span class="sxs-lookup"><span data-stu-id="b61f1-189">SCSI device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b61f1-190">4</span><span class="sxs-lookup"><span data-stu-id="b61f1-190">4</span></span></td>
<td><span data-ttu-id="b61f1-191">Dispositivo USB</span><span class="sxs-lookup"><span data-stu-id="b61f1-191">USB device</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b61f1-192">8</span><span class="sxs-lookup"><span data-stu-id="b61f1-192">8</span></span></td>
<td><span data-ttu-id="b61f1-193">Dispositivo serie</span><span class="sxs-lookup"><span data-stu-id="b61f1-193">Serial device</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b61f1-194">16</span><span class="sxs-lookup"><span data-stu-id="b61f1-194">16</span></span></td>
<td><span data-ttu-id="b61f1-195">Dispositivo paralelo</span><span class="sxs-lookup"><span data-stu-id="b61f1-195">Parallel device</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_BAUDRATE"></span><span id="wia_dip_baudrate"></span><dl> <span data-ttu-id="b61f1-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span><span class="sxs-lookup"><span data-stu-id="b61f1-196"><dt><strong>WIA_DIP_BAUDRATE</strong></dt> <dt>DeviceInfoBaudRate</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b61f1-197">La configuración actual de velocidad en baudios para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b61f1-197">The current baud rate setting for the device.</span></span> <span data-ttu-id="b61f1-198">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b61f1-198">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="b61f1-199">El valor debe ser &quot; Vacío si el dispositivo no está conectado por un cable &quot; serie.</span><span class="sxs-lookup"><span data-stu-id="b61f1-199">The value should be &quot;Empty&quot; if the device is not connected by a serial cable.</span></span></p>
<p><span data-ttu-id="b61f1-200">Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b61f1-200">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_GEN_CAPABILITIES"></span><span id="wia_dip_sti_gen_capabilities"></span><dl> <span data-ttu-id="b61f1-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span><span class="sxs-lookup"><span data-stu-id="b61f1-201"><dt><strong>WIA_DIP_STI_GEN_CAPABILITIES</strong></dt> <dt>DeviceInfoStiGenCapabilities</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b61f1-202">Las funcionalidades GENÉRICAS PARA EL DISPOSITIVO que se obtienen del archivo INF.</span><span class="sxs-lookup"><span data-stu-id="b61f1-202">The generic STI capabilities for the device as obtained from the INF file.</span></span> <span data-ttu-id="b61f1-203">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b61f1-203">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="b61f1-204">Una aplicación lee esta propiedad para determinar las funcionalidades GENÉRICAS DEL DISPOSITIVO.</span><span class="sxs-lookup"><span data-stu-id="b61f1-204">An application reads this property to determine the generic STI capabilities of the device.</span></span></p>
<p><span data-ttu-id="b61f1-205">Tipo: <strong>VT_I4</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b61f1-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_WIA_VERSION"></span><span id="wia_dip_wia_version"></span><dl> <span data-ttu-id="b61f1-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="b61f1-206"><dt><strong>WIA_DIP_WIA_VERSION</strong></dt> <dt>DeviceInfoWiaVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b61f1-207">Número (como una cadena) de la versión actual de WIA instalada en el sistema.</span><span class="sxs-lookup"><span data-stu-id="b61f1-207">The number (as a string) of the current WIA version that is installed on the system.</span></span> <span data-ttu-id="b61f1-208">Una aplicación lee esta propiedad para determinar la versión de WIA que está instalada en el sistema.</span><span class="sxs-lookup"><span data-stu-id="b61f1-208">An application reads this property to determine the version of WIA that is installed on the system.</span></span> <span data-ttu-id="b61f1-209">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b61f1-209">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="b61f1-210">Esta propiedad está disponible en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b61f1-210">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="b61f1-211">Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b61f1-211">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_DRIVER_VERSION"></span><span id="wia_dip_driver_version"></span><dl> <span data-ttu-id="b61f1-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="b61f1-212"><dt><strong>WIA_DIP_DRIVER_VERSION</strong></dt> <dt>DeviceInfoDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b61f1-213">La versión del archivo DLL actual del minidriver de WIA.</span><span class="sxs-lookup"><span data-stu-id="b61f1-213">The current DLL version of the WIA minidriver.</span></span> <span data-ttu-id="b61f1-214">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b61f1-214">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="b61f1-215">Esta propiedad está disponible en Windows XP y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b61f1-215">This property is available in Windows XP and later.</span></span></p>
<p><span data-ttu-id="b61f1-216">Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b61f1-216">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DIP_PNP_ID"></span><span id="wia_dip_pnp_id"></span><dl> <span data-ttu-id="b61f1-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span><span class="sxs-lookup"><span data-stu-id="b61f1-217"><dt><strong>WIA_DIP_PNP_ID</strong></dt> <dt>DeviceInfoPNPID</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b61f1-218">El identificador pnP actual del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b61f1-218">The current PnP id for the device.</span></span> <span data-ttu-id="b61f1-219">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b61f1-219">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="b61f1-220">Esta propiedad está disponible en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b61f1-220">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="b61f1-221">Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b61f1-221">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DIP_STI_DRIVER_VERSION"></span><span id="wia_dip_sti_driver_version"></span><dl> <span data-ttu-id="b61f1-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="b61f1-222"><dt><strong>WIA_DIP_STI_DRIVER_VERSION</strong></dt> <dt>DeviceInfoStiDriverVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="b61f1-223">Versión genérica del controlador DESTE.</span><span class="sxs-lookup"><span data-stu-id="b61f1-223">The generic STI driver version.</span></span> <span data-ttu-id="b61f1-224">El servicio WIA crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="b61f1-224">The WIA service creates and maintains this property.</span></span> <span data-ttu-id="b61f1-225">Una aplicación lee esta propiedad para determinar la versión genérica del controlador DESTE.</span><span class="sxs-lookup"><span data-stu-id="b61f1-225">An application reads this property to determine the generic STI driver version.</span></span> <span data-ttu-id="b61f1-226">Esta propiedad está disponible en Windows Vista y versiones posteriores.</span><span class="sxs-lookup"><span data-stu-id="b61f1-226">This property is available in Windows Vista and later.</span></span></p>
<p><span data-ttu-id="b61f1-227">Tipo: <strong>VT_BSTR</strong>, Acceso: Solo lectura, Valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="b61f1-227">Type: <strong>VT_BSTR</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="b61f1-228">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b61f1-228">Requirements</span></span>



| <span data-ttu-id="b61f1-229">Requisito</span><span class="sxs-lookup"><span data-stu-id="b61f1-229">Requirement</span></span> | <span data-ttu-id="b61f1-230">Valor</span><span class="sxs-lookup"><span data-stu-id="b61f1-230">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="b61f1-231">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b61f1-231">Minimum supported client</span></span><br/> | <span data-ttu-id="b61f1-232">Windows 2000 Professional, solo aplicaciones de escritorio de Windows \[ XP\]</span><span class="sxs-lookup"><span data-stu-id="b61f1-232">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="b61f1-233">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="b61f1-233">Minimum supported server</span></span><br/> | <span data-ttu-id="b61f1-234">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="b61f1-234">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="b61f1-235">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b61f1-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="b61f1-236"><dt>Wiadef.h</dt></span><span class="sxs-lookup"><span data-stu-id="b61f1-236"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




