---
description: Además de las propiedades de información de dispositivos, los dispositivos de adquisición de imágenes de Windows (WIA) tienen valores de propiedad almacenados en el registro que las aplicaciones leen y escriben.
ms.assetid: 9948318b-7171-45fa-b46f-48f9357fdb32
title: Constantes de propiedad de dispositivo comunes (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPA_CONNECT_STATUS
- WIA_DPA_DEVICE_TIME
- WIA_DPA_FIRMWARE_VERSION
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 23c8faf8317fa7bf2008baffe3e6bf0e89a27a8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104541891"
---
# <a name="common-device-property-constants"></a><span data-ttu-id="9e86a-103">Constantes de propiedad de dispositivo comunes</span><span class="sxs-lookup"><span data-stu-id="9e86a-103">Common Device Property Constants</span></span>

<span data-ttu-id="9e86a-104">Además de las propiedades de información de dispositivos, los dispositivos de adquisición de imágenes de Windows (WIA) tienen valores de propiedad almacenados en el registro que las aplicaciones leen y escriben.</span><span class="sxs-lookup"><span data-stu-id="9e86a-104">In addition to device information properties, Windows Image Acquisition (WIA) devices have property values stored in the registry that applications read and write.</span></span> <span data-ttu-id="9e86a-105">Están asociados con el objeto [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) o el objeto [**IWiaItem2**](-wia-iwiaitem2.md) .</span><span class="sxs-lookup"><span data-stu-id="9e86a-105">They are associated with the [**IWiaItem**](/windows/desktop/api/wia_xp/nn-wia_xp-iwiaitem) object or [**IWiaItem2**](-wia-iwiaitem2.md) object.</span></span> <span data-ttu-id="9e86a-106">Las propiedades del dispositivo representan información del dispositivo, como el estado de la conexión y la hora del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e86a-106">Device properties represent device information such as connection status and device time.</span></span> <span data-ttu-id="9e86a-107">Cada propiedad de dispositivo tiene una cadena de propiedad de dispositivo asociada.</span><span class="sxs-lookup"><span data-stu-id="9e86a-107">Each device property has an associated device property string.</span></span>

<span data-ttu-id="9e86a-108">Las constantes de propiedad de dispositivo enumeradas aquí son comunes a la mayoría o a todos los dispositivos de hardware WIA.</span><span class="sxs-lookup"><span data-stu-id="9e86a-108">The Device Property Constants listed here are common to most or all WIA hardware devices.</span></span>

<span data-ttu-id="9e86a-109">El prefijo "WIA \_ DPA \_ " indica una propiedad de dispositivo para todos los dispositivos y es la Convención de nomenclatura que se usa en C/C++.</span><span class="sxs-lookup"><span data-stu-id="9e86a-109">The prefix "WIA\_DPA\_" indicates a Device Property for All devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="9e86a-110">Con el fin de crear scripts, estas constantes usan el prefijo "Device" y forman parte del tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="9e86a-110">For scripting purposes these constants use the prefix "Device" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="9e86a-111">El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis al lado del nombre de la constante de C/C++ en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="9e86a-111">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="9e86a-112">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="9e86a-112">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="9e86a-113">Descripción</span><span class="sxs-lookup"><span data-stu-id="9e86a-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_CONNECT_STATUS"></span><span id="wia_dpa_connect_status"></span><dl> <span data-ttu-id="9e86a-114"><dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </span><span class="sxs-lookup"><span data-stu-id="9e86a-114"><dt><strong>WIA_DPA_CONNECT_STATUS</strong></dt> <dt>DeviceConnectStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="9e86a-115">El estado de la conexión actual para el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e86a-115">The current connection status for the device.</span></span> <span data-ttu-id="9e86a-116">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="9e86a-116">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="9e86a-117">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="9e86a-117">Type: <strong>VT_I4</strong>, Access: Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/> <span data-ttu-id="9e86a-118">La propiedad puede tener los siguientes valores posibles.</span><span class="sxs-lookup"><span data-stu-id="9e86a-118">The property can have the following possible values.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="9e86a-119">Estado de conexión</span><span class="sxs-lookup"><span data-stu-id="9e86a-119">Connect Status</span></span></th>
<th><span data-ttu-id="9e86a-120">Definición</span><span class="sxs-lookup"><span data-stu-id="9e86a-120">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9e86a-121">WIA_DEVICE_NOT_CONNECTED</span><span class="sxs-lookup"><span data-stu-id="9e86a-121">WIA_DEVICE_NOT_CONNECTED</span></span></td>
<td><span data-ttu-id="9e86a-122">El dispositivo no está conectado.</span><span class="sxs-lookup"><span data-stu-id="9e86a-122">Device is not connected.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9e86a-123">WIA_DEVICE_CONNECTED</span><span class="sxs-lookup"><span data-stu-id="9e86a-123">WIA_DEVICE_CONNECTED</span></span></td>
<td><span data-ttu-id="9e86a-124">El dispositivo está conectado y operativo.</span><span class="sxs-lookup"><span data-stu-id="9e86a-124">Device is connected and operational.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPA_DEVICE_TIME"></span><span id="wia_dpa_device_time"></span><dl> <span data-ttu-id="9e86a-125"><dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </span><span class="sxs-lookup"><span data-stu-id="9e86a-125"><dt><strong>WIA_DPA_DEVICE_TIME</strong></dt> <dt>DeviceDeviceTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9e86a-126">La hora actual del reloj que está almacenada en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e86a-126">The current clock time that is stored on the device.</span></span> <span data-ttu-id="9e86a-127">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="9e86a-127">The minidriver creates and maintains this property.</span></span></p>
<p><span data-ttu-id="9e86a-128">Tipo: <strong>VT_UI2</strong>  |  <strong>VT_VECTOR</strong>, Access: lectura/escritura o solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="9e86a-128">Type: <strong>VT_UI2</strong> | <strong>VT_VECTOR</strong>, Access: Read/Write or Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="9e86a-129">Esta propiedad solo es compatible con dispositivos que tienen un reloj interno.</span><span class="sxs-lookup"><span data-stu-id="9e86a-129">This property is supported only by devices that have an internal clock.</span></span> <span data-ttu-id="9e86a-130">Si se puede establecer el reloj del dispositivo, esta propiedad es de lectura/escritura; de lo contrario, es de solo lectura.</span><span class="sxs-lookup"><span data-stu-id="9e86a-130">If the device clock can be set, this property is Read/Write; otherwise, it is Read-only.</span></span></p>
<p><span data-ttu-id="9e86a-131">Los dispositivos WIA informan del tiempo en una estructura <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> .</span><span class="sxs-lookup"><span data-stu-id="9e86a-131">WIA devices report time in a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure.</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPA_FIRMWARE_VERSION"></span><span id="wia_dpa_firmware_version"></span><dl> <span data-ttu-id="9e86a-132"><dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </span><span class="sxs-lookup"><span data-stu-id="9e86a-132"><dt><strong>WIA_DPA_FIRMWARE_VERSION</strong></dt> <dt>DeviceFirmwareVersion</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="9e86a-133">Versión de firmware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="9e86a-133">The device firmware version.</span></span> <span data-ttu-id="9e86a-134">Este valor debe ser un valor de cadena, como &quot; 1.0.4 &quot; o &quot; 1.0 ABC &quot; .</span><span class="sxs-lookup"><span data-stu-id="9e86a-134">This value must be a string value, such as &quot;1.0.4&quot; or &quot;1.0abc&quot;.</span></span> <span data-ttu-id="9e86a-135">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="9e86a-135">The minidriver creates and maintains this property.</span></span> <span data-ttu-id="9e86a-136">Si el minicontrolador de WIA no proporciona un recurso de versión, el servicio WIA proporciona el valor &quot; 0.0.0.0 &quot; como valor predeterminado.</span><span class="sxs-lookup"><span data-stu-id="9e86a-136">If the WIA minidriver does not supply a version resource, the WIA service supplies the value &quot;0.0.0.0&quot; as a default.</span></span> <span data-ttu-id="9e86a-137">Una aplicación Lee esta propiedad para determinar la versión de la DLL del minicontrolador de WIA.</span><span class="sxs-lookup"><span data-stu-id="9e86a-137">An application reads this property to determine the version of the WIA minidriver DLL.</span></span></p>
<p><span data-ttu-id="9e86a-138">Tipo: <strong>VT_BSTR</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="9e86a-138">Type: <strong>VT_BSTR</strong>, Access: Read-only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="9e86a-139">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9e86a-139">Requirements</span></span>



| <span data-ttu-id="9e86a-140">Requisito</span><span class="sxs-lookup"><span data-stu-id="9e86a-140">Requirement</span></span> | <span data-ttu-id="9e86a-141">Value</span><span class="sxs-lookup"><span data-stu-id="9e86a-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9e86a-142">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e86a-142">Minimum supported client</span></span><br/> | <span data-ttu-id="9e86a-143">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="9e86a-143">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="9e86a-144">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="9e86a-144">Minimum supported server</span></span><br/> | <span data-ttu-id="9e86a-145">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="9e86a-145">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9e86a-146">Encabezado</span><span class="sxs-lookup"><span data-stu-id="9e86a-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="9e86a-147"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e86a-147"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
