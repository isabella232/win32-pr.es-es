---
description: Los dispositivos portátiles de Windows admiten las siguientes propiedades de dispositivo.
ms.assetid: 1caf4c1a-ceb6-4aa5-b430-df01c9fb22ce
title: Propiedades del dispositivo (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Device
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 696d5fefd65d194f9bb451b0095ed87b90f8a22c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105671015"
---
# <a name="device-properties-portabledeviceh"></a><span data-ttu-id="b0f4a-103">Propiedades del dispositivo (PortableDevice. h)</span><span class="sxs-lookup"><span data-stu-id="b0f4a-103">Device Properties (PortableDevice.h)</span></span>

<span data-ttu-id="b0f4a-104">Los dispositivos portátiles de Windows admiten las siguientes propiedades de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-104">Windows Portable Devices supports the following device properties.</span></span>



<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b0f4a-105">Propiedad</span><span class="sxs-lookup"><span data-stu-id="b0f4a-105">Property</span></span></th>
<th><span data-ttu-id="b0f4a-106">VarType</span><span class="sxs-lookup"><span data-stu-id="b0f4a-106">VarType</span></span></th>
<th><span data-ttu-id="b0f4a-107">Descripción</span><span class="sxs-lookup"><span data-stu-id="b0f4a-107">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b0f4a-108"><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-108"><span id="wpd_device_datetime"></span><span id="WPD_DEVICE_DATETIME"></span><strong>WPD_DEVICE_DATETIME</strong></span></span></td>
<td><span data-ttu-id="b0f4a-109"><strong>VT_DATE</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-109"><strong>VT_DATE</strong></span></span></td>
<td><span data-ttu-id="b0f4a-110">Fecha y hora actuales del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-110">The current date and time on the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0f4a-111"><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-111"><span id="wpd_device_firmware_version"></span><span id="WPD_DEVICE_FIRMWARE_VERSION"></span><strong>WPD_DEVICE_FIRMWARE_VERSION</strong></span></span></td>
<td><span data-ttu-id="b0f4a-112"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-112"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="b0f4a-113">Versión de firmware del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-113">The device's firmware version.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0f4a-114"><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-114"><span id="wpd_device_functional_unique_id"></span><span id="WPD_DEVICE_FUNCTIONAL_UNIQUE_ID"></span><strong>WPD_DEVICE_FUNCTIONAL_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="b0f4a-115"><strong>VT_VECTOR | VT_UI1</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-115"><strong>VT_VECTOR | VT_UI1</strong></span></span></td>
<td><span data-ttu-id="b0f4a-116">Un identificador único de 16 bytes que es común en varios transportes admitidos por el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-116">A unique 16-byte identifier that is common across multiple transports supported by the device.</span></span> <span data-ttu-id="b0f4a-117">Si un único dispositivo admite varios transportes, esta propiedad se puede usar para asociar los distintos controladores de transporte de WPD a ese dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-117">If a single device supports multiple transports, this property may be used to associate the various transport WPD drivers with that device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0f4a-118"><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-118"><span id="wpd_device_manufacturer"></span><span id="WPD_DEVICE_MANUFACTURER"></span><strong>WPD_DEVICE_MANUFACTURER</strong></span></span></td>
<td><span data-ttu-id="b0f4a-119"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-119"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="b0f4a-120">Un nombre de fabricante de dispositivos legibles para el usuario.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-120">A human-readable device manufacturer name.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0f4a-121"><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-121"><span id="wpd_device_model"></span><span id="WPD_DEVICE_MODEL"></span><strong>WPD_DEVICE_MODEL</strong></span></span></td>
<td><span data-ttu-id="b0f4a-122"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-122"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="b0f4a-123">El modelo del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-123">The device model.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0f4a-124"><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-124"><span id="wpd_device_model_unique_id"></span><span id="WPD_DEVICE_MODEL_UNIQUE_ID"></span><strong>WPD_DEVICE_MODEL_UNIQUE_ID</strong></span></span></td>
<td><span data-ttu-id="b0f4a-125"><strong>VT_VECTOR | VT_UI1</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-125"><strong>VT_VECTOR | VT_UI1</strong></span></span></td>
<td><span data-ttu-id="b0f4a-126">Un identificador único de 16 bytes que se usa para diferenciar entre distintos modelos de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-126">A unique 16-byte identifier used to differentiate among different models of a device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0f4a-127"><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-127"><strong>WPD_DEVICE_NETWORK_IDENTIFIER</strong></span></span></td>
<td><span data-ttu-id="b0f4a-128"><strong>VT_UI8</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-128"><strong>VT_UI8</strong></span></span></td>
<td><span data-ttu-id="b0f4a-129">Valor que especifica el identificador de red EUI-64 del dispositivo; Esta propiedad se utiliza para las operaciones de red fuera de banda. Si el dispositivo tiene direcciones de red física de MAC-48 (típico de redes IPv4), la dirección MAC-48 se codifica en la dirección EUI-64 como las dos mitades de la dirección MAC-48 separada por FF-FF.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-129">A value that specifies the EUI-64 network identifier of the device; this property is used for out-of-band network operations.If the device has MAC-48 physical network addresses (typical of IPv4 networks), the MAC-48 address is encoded in the EUI-64 address as the two halves of the MAC-48 address separated by FF-FF.</span></span> <span data-ttu-id="b0f4a-130">El valor EUI-64 se almacena en &quot; &quot; la red o en &quot; el orden Big-Endian &quot; , donde se colocará una dirección eui-64 de 01-02-03-ff-FF-04-05-06 en el VT_UI8 de modo que el valor decimal sea 72624942021346566.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-130">The EUI-64 value is stored in &quot;network&quot; or &quot;big-endian&quot; order, where an EUI-64 address of 01-02-03-FF-FF-04-05-06 would be placed in the VT_UI8 such that the decimal value is 72624942021346566.</span></span> <span data-ttu-id="b0f4a-131">Esta propiedad es necesaria en cualquier dispositivo que admita la autenticación nominal o segura.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-131">This property is required on any device that supports Nominal or Secure Authentication.</span></span> <span data-ttu-id="b0f4a-132">Esta propiedad se recomienda en los dispositivos que solo admiten la autenticación de cero.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-132">This property is recommended on devices that support only Zero Authentication.</span></span> <span data-ttu-id="b0f4a-133">El host puede usar el valor para establecer automáticamente el acceso al dispositivo sin la intervención del usuario.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-133">The value can be used by the host to automatically establish access to the device without user intervention.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0f4a-134"><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-134"><span id="wpd_device_power_level"></span><span id="WPD_DEVICE_POWER_LEVEL"></span><strong>WPD_DEVICE_POWER_LEVEL</strong></span></span></td>
<td><span data-ttu-id="b0f4a-135"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-135"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="b0f4a-136">Un valor comprendido entre 0 y 100 que especifica el nivel de energía de la batería del dispositivo, donde 0 no es ninguno y 100 se carga por completo.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-136">A value from 0 to 100 that specifies the power level of the device's battery, with 0 being none, and 100 being fully charged.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0f4a-137"><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-137"><span id="wpd_device_power_source"></span><span id="WPD_DEVICE_POWER_SOURCE"></span><strong>WPD_DEVICE_POWER_SOURCE</strong></span></span></td>
<td><span data-ttu-id="b0f4a-138">VT_UI4</span><span class="sxs-lookup"><span data-stu-id="b0f4a-138">VT_UI4</span></span></td>
<td><span data-ttu-id="b0f4a-139">Una enumeración <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> que especifica la fuente de alimentación del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-139">A <a href="wpd-power-sources.md"><strong>WPD_POWER_SOURCES</strong></a> enumeration that specifies the power source of the device.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0f4a-140"><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-140"><span id="wpd_device_protocol"></span><span id="WPD_DEVICE_PROTOCOL"></span><strong>WPD_DEVICE_PROTOCOL</strong></span></span></td>
<td><span data-ttu-id="b0f4a-141"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-141"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="b0f4a-142">El protocolo de dispositivo que se está usando.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-142">The device protocol that is being used.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0f4a-143"><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-143"><span id="wpd_device_serial_number"></span><span id="WPD_DEVICE_SERIAL_NUMBER"></span><strong>WPD_DEVICE_SERIAL_NUMBER</strong></span></span></td>
<td><span data-ttu-id="b0f4a-144"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-144"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="b0f4a-145">El número de serie del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-145">The device's serial number.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0f4a-146"><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-146"><span id="wpd_device_supported_drm_scheme"></span><span id="WPD_DEVICE_SUPPORTED_DRM_SCHEME"></span><strong>WPD_DEVICE_SUPPORTED_DRM_SCHEMES</strong></span></span></td>
<td><span data-ttu-id="b0f4a-147"><strong>VT_UNKNOWN</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-147"><strong>VT_UNKNOWN</strong></span></span></td>
<td><span data-ttu-id="b0f4a-148">Valor que especifica si los formatos admitidos devueltos desde el dispositivo se encuentran en un orden preferido.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-148">A value that specifies whether the supported formats returned from the device are in a preferred order.</span></span> <span data-ttu-id="b0f4a-149">El primer formato de la lista lo prefiere el dispositivo, mientras que el último es el menos preferido. Las aplicaciones pueden usar esta propiedad para determinar si los formatos admitidos de un dispositivo se muestran en un orden preferido.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-149">The first format in the list is most preferred by the device, while the last is the least preferred.Applications may use this property to determine whether a device's supported formats are listed in a preferred order.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0f4a-150"><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-150"><span id="wpd_device_supported_formats_are_ordered"></span><span id="WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED"></span><strong>WPD_DEVICE_SUPPORTED_FORMATS_ARE_ORDERED</strong></span></span></td>
<td><span data-ttu-id="b0f4a-151"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-151"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="b0f4a-152">Valor booleano que especifica si los formatos admitidos devueltos desde el dispositivo se encuentran en un orden preferido; es decir, el primer formato devuelto es más preferido, mientras que el último formato devuelto es el menos preferido.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-152">A Boolean value that specifies whether the supported formats returned from the device are in a preferred order; that is, the first returned format is most preferred while the last returned format is least preferred.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0f4a-153"><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-153"><span id="wpd_device_supports_non_consumable"></span><span id="WPD_DEVICE_SUPPORTS_NON_CONSUMABLE"></span><strong>WPD_DEVICE_SUPPORTS_NON_CONSUMABLE</strong></span></span></td>
<td><span data-ttu-id="b0f4a-154"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-154"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="b0f4a-155">Valor booleano que especifica si el dispositivo admite objetos que no se usan.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-155">A Boolean value that specifies whether the device supports non-consumable objects.</span></span> <span data-ttu-id="b0f4a-156">Se trata de objetos que el dispositivo solo debe almacenar, no reproducir ni usar de ninguna manera.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-156">These are objects that the device is only meant to store, not play or use in any way.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0f4a-157"><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-157"><span id="wpd_device_sync_partner"></span><span id="WPD_DEVICE_SYNC_PARTNER"></span><strong>WPD_DEVICE_SYNC_PARTNER</strong></span></span></td>
<td><span data-ttu-id="b0f4a-158"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-158"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="b0f4a-159">Una descripción inteligible del <em>asociado de sincronización</em>de un dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-159">A human-readable description of a device's <em>synchronization partner</em>.</span></span> <span data-ttu-id="b0f4a-160">Se trata de un dispositivo, una aplicación o un servidor con el que se comunica el dispositivo para mantener un Estado común o un grupo de archivos entre ambos asociados.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-160">This is a device, application, or server that the device communicates with to maintain a common state or group of files between both partners.</span></span> <span data-ttu-id="b0f4a-161">Entre los ejemplos se incluyen programas de correo electrónico y bibliotecas de música.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-161">Examples include e-mail programs and music libraries.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0f4a-162"><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-162"><span id="wpd_device_friendly_name"></span><span id="WPD_DEVICE_FRIENDLY_NAME"></span><strong>WPD_DEVICE_FRIENDLY_NAME</strong></span></span></td>
<td><span data-ttu-id="b0f4a-163"><strong>VT_LPWSTR</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-163"><strong>VT_LPWSTR</strong></span></span></td>
<td><span data-ttu-id="b0f4a-164">Valor que representa el nombre descriptivo establecido por el usuario en el dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-164">A value that represents the friendly name set by the user on the device.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0f4a-165"><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-165"><span id="wpd_device_transport"></span><span id="WPD_DEVICE_TRANSPORT"></span><strong>WPD_DEVICE_TRANSPORT</strong></span></span></td>
<td><span data-ttu-id="b0f4a-166"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-166"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="b0f4a-167">transporte compatible con el dispositivo, como USB, IP o Bluetooth.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-167">the transport supported by the device, such as USB, IP, or Bluetooth.</span></span> <span data-ttu-id="b0f4a-168">Los valores válidos son del tipo de enumeración <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="b0f4a-168">Valid values are of the <a href="wpd-device-transports.md"><strong>WPD_DEVICE_TRANSPORTS</strong></a> enumeration type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b0f4a-169"><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-169"><span id="wpd_device_type"></span><span id="WPD_DEVICE_TYPE"></span><strong>WPD_DEVICE_TYPE</strong></span></span></td>
<td><span data-ttu-id="b0f4a-170"><strong>VT_UI4</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-170"><strong>VT_UI4</strong></span></span></td>
<td><span data-ttu-id="b0f4a-171">Valor que especifica el tipo de dispositivo. las aplicaciones usan esta propiedad solo con fines de representación.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-171">A value that specifies the device type; applications use this property for representation purposes only.</span></span> <span data-ttu-id="b0f4a-172">Las características funcionales del dispositivo se deciden a través de objetos funcionales. Los dispositivos que no proporcionan un icono de dispositivo, por ejemplo, un <strong>WPD_RESOURCE_ICON</strong> para el objeto de dispositivo, se representarán en el espacio de nombres de WPD con un icono genérico.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-172">Functional characteristics of the device are decided through functional objects.Devices that do not supply a device icon, for example, a <strong>WPD_RESOURCE_ICON</strong> for the device object, will be represented in the WPD Namespace with a generic icon.</span></span> <span data-ttu-id="b0f4a-173">Este icono dependerá del tipo de dispositivo especificado, por ejemplo, si el tipo de dispositivo es un teléfono móvil, se usa el icono de teléfono genérico.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-173">This icon will depend on the specified device type, for example, if the device type is a mobile phone, the generic phone icon is used.</span></span> <span data-ttu-id="b0f4a-174">En la primera instalación del dispositivo, el instalador de la clase WPD consultará este valor de propiedad y lo almacenará en el registro de dispositivos en el valor PORTABLE_DEVICE_TYPE como un REG_DWORD.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-174">On first install of the device, the WPD Class Installer will query this property value and store it in the device registry under the PORTABLE_DEVICE_TYPE value as a REG_DWORD.</span></span><br/> <span data-ttu-id="b0f4a-175">Los valores posibles de este parámetro proceden de la enumeración <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> definida en PortableDevice. h.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-175">This parameter's possible values are from the <a href="object-properties.md"><strong>WPD_DEVICE_TYPES</strong></a> enumeration defined in PortableDevice.h.</span></span> <span data-ttu-id="b0f4a-176">Los valores son:</span><span class="sxs-lookup"><span data-stu-id="b0f4a-176">Values are:</span></span><br/> <dl> <span data-ttu-id="b0f4a-177"><strong>WPD_DEVICE_TYPE_GENERIC</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-177"><strong>WPD_DEVICE_TYPE_GENERIC</strong></span></span><br /><span data-ttu-id="b0f4a-178">
<strong>WPD_DEVICE_TYPE_CAMERA</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-178">
<strong>WPD_DEVICE_TYPE_CAMERA</strong></span></span><br /><span data-ttu-id="b0f4a-179">
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-179">
<strong>WPD_DEVICE_TYPE_MEDIA_PLAYER</strong></span></span><br /><span data-ttu-id="b0f4a-180">
<strong>WPD_DEVICE_TYPE_PHONE</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-180">
<strong>WPD_DEVICE_TYPE_PHONE</strong></span></span><br /><span data-ttu-id="b0f4a-181">
<strong>WPD_DEVICE_TYPE_VIDEO</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-181">
<strong>WPD_DEVICE_TYPE_VIDEO</strong></span></span><br /><span data-ttu-id="b0f4a-182">
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-182">
<strong>WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER</strong></span></span><br /><span data-ttu-id="b0f4a-183">
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-183">
<strong>WPD_DEVICE_TYPE_AUDIO_RECORDER</strong></span></span><br />
</dl></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b0f4a-184"><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-184"><span id="wpd_device_use_device_stage"></span><span id="WPD_DEVICE_USE_DEVICE_STAGE"></span><strong>WPD_DEVICE_USE_DEVICE_STAGE</strong></span></span></td>
<td><span data-ttu-id="b0f4a-185"><strong>VT_BOOL</strong></span><span class="sxs-lookup"><span data-stu-id="b0f4a-185"><strong>VT_BOOL</strong></span></span></td>
<td><span data-ttu-id="b0f4a-186">Si esta propiedad existe y está establecida en <strong>true</strong>, el dispositivo se puede usar con la fase de dispositivo.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-186">If this property exists and is set to <strong>TRUE</strong>, the device can be used with Device Stage .</span></span> <span data-ttu-id="b0f4a-187">Esto está pensado para dispositivos que no pueden almacenar metadatos mediante el <strong>Metadata Service del dispositivo</strong>, pero proporcionarán metadatos en los servidores de Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b0f4a-187">This is meant for devices that cannot store metadata using the <strong>Device Metadata Service</strong>, but will provide metadata on the Microsoft servers.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="requirements"></a><span data-ttu-id="b0f4a-188">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b0f4a-188">Requirements</span></span>



| <span data-ttu-id="b0f4a-189">Requisito</span><span class="sxs-lookup"><span data-stu-id="b0f4a-189">Requirement</span></span> | <span data-ttu-id="b0f4a-190">Value</span><span class="sxs-lookup"><span data-stu-id="b0f4a-190">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="b0f4a-191">Encabezado</span><span class="sxs-lookup"><span data-stu-id="b0f4a-191">Header</span></span><br/> | <dl> <span data-ttu-id="b0f4a-192"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="b0f4a-192"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b0f4a-193">Vea también</span><span class="sxs-lookup"><span data-stu-id="b0f4a-193">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b0f4a-194">**Propiedades y atributos de WPD**</span><span class="sxs-lookup"><span data-stu-id="b0f4a-194">**WPD Properties and Attributes**</span></span>](properties-and-attributes.md)
</dt> </dl>

 

 




