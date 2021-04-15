---
description: Los dispositivos de hardware de adquisición de imágenes de Windows (WIA) tienen valores de propiedad que se almacenan en el registro de Windows. Para obtener más información, consulte Common Device Property constants.
ms.assetid: 7893137b-194c-4ea1-b15c-59d2f41f972a
title: Constantes de propiedad de dispositivo de cámara (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPC_PICTURES_TAKEN
- WIA_DPC_PICTURES_REMAINING
- WIA_DPC_EXPOSURE_MODE
- WIA_DPC_EXPOSURE_COMP
- WIA_DPC_EXPOSURE_TIME
- WIA_DPC_FNUMBER
- WIA_DPC_FLASH_MODE
- WIA_DPC_FOCUS_MODE
- WIA_DPC_FOCUS_MANUAL_DIST
- WIA_DPC_ZOOM_POSITION
- WIA_DPC_PAN_POSITION
- WIA_DPC_TILT_POSITION
- WIA_DPC_TIMER_MODE
- WIA_DPC_TIMER_VALUE
- WIA_DPC_POWER_MODE
- WIA_DPC_BATTERY_STATUS
- WIA_DPC_THUMB_WIDTH
- WIA_DPC_THUMB_HEIGHT
- WIA_DPC_PICT_WIDTH
- WIA_DPC_PICT_HEIGHT
- WIA_DPC_DIMENSION
- WIA_DPC_COMPRESSION_SETTING
- WIA_DPC_FOCUS_METERING
- WIA_DPC_TIMELAPSE_INTERVAL
- WIA_DPC_TIMELAPSE_NUMBER
- WIA_DPC_BURST_INTERVAL
- WIA_DPC_BURST_NUMBER
- WIA_DPC_EFFECT_MODE
- WIA_DPC_DIGITAL_ZOOM
- WIA_DPC_SHARPNESS
- WIA_DPC_CONTRAST
- WIA_DPC_CAPTURE_MODE
- WIA_DPC_CAPTURE_DELAY
- WIA_DPC_EXPOSURE_INDEX
- WIA_DPC_EXPOSURE_METERING_MODE
- WIA_DPC_FOCUS_METERING_MODE
- WIA_DPC_FOCUS_DISTANCE
- WIA_DPC_FOCAL_LENGTH
- WIA_DPC_RGB_GAIN
- WIA_DPC_WHITE_BALANCE
- WIA_DPC_UPLOAD_URL
- WIA_DPC_ARTIST
- WIA_DPC_COPYRIGHT_INFO
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: 0114fedd7fd4acf811e71db67376afecc2630cfd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104497536"
---
# <a name="camera-device-property-constants"></a><span data-ttu-id="510b8-104">Constantes de propiedades de dispositivo de cámara</span><span class="sxs-lookup"><span data-stu-id="510b8-104">Camera Device Property Constants</span></span>

<span data-ttu-id="510b8-105">Los dispositivos de hardware de adquisición de imágenes de Windows (WIA) tienen valores de propiedad que se almacenan en el registro de Windows.</span><span class="sxs-lookup"><span data-stu-id="510b8-105">Windows Image Acquisition (WIA) hardware devices have property values that are stored in the Windows registry.</span></span> <span data-ttu-id="510b8-106">Para obtener más información, consulte [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).</span><span class="sxs-lookup"><span data-stu-id="510b8-106">For more information, see [**Common Device Property Constants**](-wia-wiaitempropcommondevice.md).</span></span>

<span data-ttu-id="510b8-107">Las siguientes constantes de propiedades de dispositivo, con sus cadenas asociadas, son específicas de las cámaras digitales.</span><span class="sxs-lookup"><span data-stu-id="510b8-107">The following device property constants, with their associated strings, are specific to digital cameras.</span></span> <span data-ttu-id="510b8-108">El prefijo "WIA \_ DPC \_ " indica una propiedad de dispositivo para las cámaras y es la Convención de nomenclatura utilizada en C/C++.</span><span class="sxs-lookup"><span data-stu-id="510b8-108">The prefix "WIA\_DPC\_" indicates a Device Property for Cameras and is the naming convention used in C/C++.</span></span> <span data-ttu-id="510b8-109">Con el fin de crear scripts, estas constantes usan el prefijo "CameraDevice" y forman parte del tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="510b8-109">For scripting purposes these constants use the prefix "CameraDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="510b8-110">El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis al lado del nombre de la constante de C/C++ en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="510b8-110">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>

> [!Note]  
> <span data-ttu-id="510b8-111">WIA no admite cámaras en Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="510b8-111">WIA does not support cameras in Windows Vista or later.</span></span> <span data-ttu-id="510b8-112">En el caso de las versiones de Windows, use la API de dispositivo portátil de Windows (WPD) que se describe en el kit de desarrollo de controladores de Windows (DDK) para adquirir imágenes de cámaras.</span><span class="sxs-lookup"><span data-stu-id="510b8-112">For those versions of the Windows, use the Windows Portable Device (WPD) API described in the Windows Driver Development Kit (DDK) to acquire images from cameras.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="510b8-113">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="510b8-113">Constant/value</span></span></th>
<th style="text-align: left;"><span data-ttu-id="510b8-114">Descripción</span><span class="sxs-lookup"><span data-stu-id="510b8-114">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_TAKEN"></span><span id="wia_dpc_pictures_taken"></span><dl> <span data-ttu-id="510b8-115"><dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-115"><dt><strong>WIA_DPC_PICTURES_TAKEN</strong></dt> <dt>CameraDevicePicturesTaken</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="510b8-116">El número de imágenes que ha tomado la cámara.</span><span class="sxs-lookup"><span data-stu-id="510b8-116">The number of pictures that the camera has taken.</span></span> <span data-ttu-id="510b8-117">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="510b8-117">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="510b8-118">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-118">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICTURES_REMAINING"></span><span id="wia_dpc_pictures_remaining"></span><dl> <span data-ttu-id="510b8-119"><dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-119"><dt><strong>WIA_DPC_PICTURES_REMAINING</strong></dt> <dt>CameraDevicePicturesRemaining</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="510b8-120">El número de imágenes que se pueden tomar, dados los valores de propiedades actuales.</span><span class="sxs-lookup"><span data-stu-id="510b8-120">The number of pictures that can be taken, given the current property settings.</span></span> <span data-ttu-id="510b8-121">Si esta configuración cambia y los cambios afectan al tamaño de las imágenes que genera el dispositivo de cámara, el minicontrolador WIA debe actualizar el número de imágenes restantes.</span><span class="sxs-lookup"><span data-stu-id="510b8-121">If these settings change, and the changes affect the size of the images that the camera device produces, the WIA minidriver should update the number of remaining pictures.</span></span> <span data-ttu-id="510b8-122">El minicontrolador crea y mantiene esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="510b8-122">The minidriver creates and maintains this property.</span></span><br/> <span data-ttu-id="510b8-123">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-123">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_MODE"></span><span id="wia_dpc_exposure_mode"></span><dl> <span data-ttu-id="510b8-124"><dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-124"><dt><strong>WIA_DPC_EXPOSURE_MODE</strong></dt> <dt>CameraDeviceExposureMode</dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="510b8-125">Indica el modo de exposición actual de la cámara.</span><span class="sxs-lookup"><span data-stu-id="510b8-125">Indicates the camera's current exposure mode.</span></span> <span data-ttu-id="510b8-126">Una aplicación cambia esta propiedad para controlar el modo de exposición del dispositivo de cámara.</span><span class="sxs-lookup"><span data-stu-id="510b8-126">An application changes this property to control the exposure mode of the camera device.</span></span><br/> <span data-ttu-id="510b8-127">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="510b8-127">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span><br/> <span data-ttu-id="510b8-128">En la tabla siguiente se incluyen las siete constantes que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="510b8-128">The following table has the seven constants that are valid with this property.</span></span><br/> 
<table>
<thead>
<tr class="header">
<th><span data-ttu-id="510b8-129">Modo de exposición</span><span class="sxs-lookup"><span data-stu-id="510b8-129">Exposure Mode</span></span></th>
<th><span data-ttu-id="510b8-130">Descripción</span><span class="sxs-lookup"><span data-stu-id="510b8-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="510b8-131">EXPOSUREMODE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="510b8-131">EXPOSUREMODE_MANUAL</span></span></td>
<td><span data-ttu-id="510b8-132">El usuario establece la velocidad y la abertura del obturador.</span><span class="sxs-lookup"><span data-stu-id="510b8-132">The shutter speed and aperture are set by the user.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510b8-133">EXPOSUREMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="510b8-133">EXPOSUREMODE_AUTO</span></span></td>
<td><span data-ttu-id="510b8-134">La cámara establece automáticamente la velocidad y la abertura del obturador.</span><span class="sxs-lookup"><span data-stu-id="510b8-134">The shutter speed and aperture are automatically set by the camera.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="510b8-135">EXPOSUREMODE_APERTURE_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="510b8-135">EXPOSUREMODE_APERTURE_PRIORITY</span></span></td>
<td><span data-ttu-id="510b8-136">El usuario establece la abertura y la cámara establece automáticamente la velocidad del obturador.</span><span class="sxs-lookup"><span data-stu-id="510b8-136">The aperture is set by the user, and the camera automatically sets the shutter speed.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510b8-137">EXPOSUREMODE_SHUTTER_PRIORITY</span><span class="sxs-lookup"><span data-stu-id="510b8-137">EXPOSUREMODE_SHUTTER_PRIORITY</span></span></td>
<td><span data-ttu-id="510b8-138">El usuario establece la velocidad del obturador y la cámara establece automáticamente la abertura.</span><span class="sxs-lookup"><span data-stu-id="510b8-138">The shutter speed is set by the user, and the camera automatically sets the aperture.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="510b8-139">EXPOSUREMODE_PROGRAM_CREATIVE</span><span class="sxs-lookup"><span data-stu-id="510b8-139">EXPOSUREMODE_PROGRAM_CREATIVE</span></span></td>
<td><span data-ttu-id="510b8-140">La cámara establece automáticamente la velocidad y la abertura del obturador, optimizadas para seguir siendo importantes.</span><span class="sxs-lookup"><span data-stu-id="510b8-140">The shutter speed and aperture are automatically set by the camera, optimized for still subject matter.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510b8-141">EXPOSUREMODE_PROGRAM_ACTION</span><span class="sxs-lookup"><span data-stu-id="510b8-141">EXPOSUREMODE_PROGRAM_ACTION</span></span></td>
<td><span data-ttu-id="510b8-142">La cámara establece automáticamente la velocidad y la abertura del obturador, optimizadas para escenas que contienen movimiento rápido.</span><span class="sxs-lookup"><span data-stu-id="510b8-142">The shutter speed and aperture are automatically set by the camera, optimized for scenes containing fast motion.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="510b8-143">EXPOSUREMODE_PORTRAIT</span><span class="sxs-lookup"><span data-stu-id="510b8-143">EXPOSUREMODE_PORTRAIT</span></span></td>
<td><span data-ttu-id="510b8-144">La cámara establece automáticamente la velocidad y la abertura del obturador, optimizadas para la fotografía vertical.</span><span class="sxs-lookup"><span data-stu-id="510b8-144">The shutter speed and aperture are automatically set by the camera, optimized for portrait photography.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_COMP"></span><span id="wia_dpc_exposure_comp"></span><dl> <span data-ttu-id="510b8-145"><dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-145"><dt><strong>WIA_DPC_EXPOSURE_COMP</strong></dt> <dt>CameraDeviceExposureComp</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-146">Permite ajustar el punto de establecimiento del control de exposición automática de la cámara digital.</span><span class="sxs-lookup"><span data-stu-id="510b8-146">Allows for the adjustment of the set point of the digital camera's auto-exposure control.</span></span> <span data-ttu-id="510b8-147">Por ejemplo, un valor de cero no cambia el nivel de exposición automática del conjunto de fábrica.</span><span class="sxs-lookup"><span data-stu-id="510b8-147">For example, a setting of zero does not change the factory-set auto-exposure level.</span></span> <span data-ttu-id="510b8-148">Las unidades están en &quot; paradas &quot; que se escalan por un factor de 1000, para permitir valores de detención fraccionarios.</span><span class="sxs-lookup"><span data-stu-id="510b8-148">The units are in &quot;stops&quot; that are scaled by a factor of 1000, to allow for fractional stop values.</span></span> <span data-ttu-id="510b8-149">Un valor de 2000 corresponde a dos detenciones más de exposición (cuatro veces más energía en el sensor), produciendo imágenes más brillantes.</span><span class="sxs-lookup"><span data-stu-id="510b8-149">A setting of 2000 corresponds to two stops more exposure (four times more energy on the sensor), yielding brighter images.</span></span> <span data-ttu-id="510b8-150">Un valor de-1000 corresponde a una parada menos expuesta (la mitad de la energía en el sensor) que produce imágenes más oscuras.</span><span class="sxs-lookup"><span data-stu-id="510b8-150">A setting of -1000 corresponds to one stop less exposure (one-half the energy on the sensor) yielding darker images.</span></span> <span data-ttu-id="510b8-151">Los valores de configuración están en el sistema aditivo de las unidades de exposición fotográfica (vértice).</span><span class="sxs-lookup"><span data-stu-id="510b8-151">The setting values are in Additive System of Photographic Exposure (APEX) units.</span></span> <span data-ttu-id="510b8-152">Esta propiedad se puede expresar como una lista o como un intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="510b8-152">This property may be expressed as either a list or a range of values.</span></span> <span data-ttu-id="510b8-153">Esta propiedad se usa normalmente solo cuando el dispositivo tiene la propiedad <strong>WIA_DPC_EXPOSURE_MODE</strong> establecida en EXPOSUREMODE_MANUAL.</span><span class="sxs-lookup"><span data-stu-id="510b8-153">This property is typically used only when the device has the <strong>WIA_DPC_EXPOSURE_MODE</strong> property set to EXPOSUREMODE_MANUAL.</span></span></p>
<p><span data-ttu-id="510b8-154">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="510b8-154">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_TIME"></span><span id="wia_dpc_exposure_time"></span><dl> <span data-ttu-id="510b8-155"><dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-155"><dt><strong>WIA_DPC_EXPOSURE_TIME</strong></dt> <dt>CameraDeviceExposureTime</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-156">Corresponde a la velocidad del obturador, en segundos, que se escala por 10.000.</span><span class="sxs-lookup"><span data-stu-id="510b8-156">Corresponds to the shutter speed, in seconds that are scaled by 10,000.</span></span> <span data-ttu-id="510b8-157">Normalmente, el dispositivo usa esta propiedad solo cuando la propiedad <strong>WIA_DPC_EXPOSURE_MODE</strong> está establecida en EXPOSUREMODE_MANUAL o EXPOSUREMODE_SHUTTER_PRIORITY.</span><span class="sxs-lookup"><span data-stu-id="510b8-157">Typically, the device uses this property only when the <strong>WIA_DPC_EXPOSURE_MODE</strong> property is set to EXPOSUREMODE_MANUAL or EXPOSUREMODE_SHUTTER_PRIORITY.</span></span></p>
<p><span data-ttu-id="510b8-158">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> o WIA_PROP_LIST</span><span class="sxs-lookup"><span data-stu-id="510b8-158">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_RANGE</a> or WIA_PROP_LIST</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FNUMBER"></span><span id="wia_dpc_fnumber"></span><dl> <span data-ttu-id="510b8-159"><dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-159"><dt><strong>WIA_DPC_FNUMBER</strong></dt> <dt>CameraDeviceFNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-160">Corresponde a la abertura de la lente, en unidades del número de detención de f escalado por 100.</span><span class="sxs-lookup"><span data-stu-id="510b8-160">Corresponds to the aperture of the lens, in units of the f-stop number scaled by 100.</span></span> <span data-ttu-id="510b8-161">Normalmente, la configuración de esta propiedad solo es válida cuando la propiedad <strong>WIA_DPC_EXPOSURE_MODE</strong> está establecida en EXPOSUREMODE_MANUAL o EXPOSUREMODE_APERTURE_PRIORITY.</span><span class="sxs-lookup"><span data-stu-id="510b8-161">The setting of this property is typically valid only when the <strong>WIA_DPC_EXPOSURE_MODE</strong> property is set to EXPOSUREMODE_MANUAL or EXPOSUREMODE_APERTURE_PRIORITY.</span></span></p>
<p><span data-ttu-id="510b8-162">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="510b8-162">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FLASH_MODE"></span><span id="wia_dpc_flash_mode"></span><dl> <span data-ttu-id="510b8-163"><dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-163"><dt><strong>WIA_DPC_FLASH_MODE</strong></dt> <dt>CameraDeviceFlashMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-164">Define la configuración de modo Flash actual para el dispositivo de cámara.</span><span class="sxs-lookup"><span data-stu-id="510b8-164">Defines the current flash mode setting for the camera device.</span></span> <span data-ttu-id="510b8-165">El controlador de dispositivo enumera los valores admitidos de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="510b8-165">The device driver enumerates the supported values of this property.</span></span> <span data-ttu-id="510b8-166">Una aplicación escribe esta propiedad para establecer el modo flash para el dispositivo de cámara.</span><span class="sxs-lookup"><span data-stu-id="510b8-166">An application writes this property to set the flash mode for the camera device.</span></span></p>
<p><span data-ttu-id="510b8-167">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="510b8-167">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="510b8-168">En la tabla siguiente se incluyen las seis constantes que son válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="510b8-168">The following table has the six constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="510b8-169">Modo flash</span><span class="sxs-lookup"><span data-stu-id="510b8-169">Flash Mode</span></span></th>
<th><span data-ttu-id="510b8-170">Definición</span><span class="sxs-lookup"><span data-stu-id="510b8-170">Definition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="510b8-171">FLASHMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="510b8-171">FLASHMODE_AUTO</span></span></td>
<td><span data-ttu-id="510b8-172">El dispositivo de cámara determina la configuración de Flash adecuada.</span><span class="sxs-lookup"><span data-stu-id="510b8-172">The camera device determines the proper flash settings.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510b8-173">FLASHMODE_FILL</span><span class="sxs-lookup"><span data-stu-id="510b8-173">FLASHMODE_FILL</span></span></td>
<td><span data-ttu-id="510b8-174">El dispositivo de cámara está configurado para parpadear independientemente de las condiciones de iluminación actuales.</span><span class="sxs-lookup"><span data-stu-id="510b8-174">The camera device is configured to flash regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="510b8-175">FLASHMODE_OFF</span><span class="sxs-lookup"><span data-stu-id="510b8-175">FLASHMODE_OFF</span></span></td>
<td><span data-ttu-id="510b8-176">El dispositivo de cámara está configurado para <em>no</em> parpadear en ninguna imagen tomada.</span><span class="sxs-lookup"><span data-stu-id="510b8-176">The camera device is configured <em>not</em> to flash for any picture taken.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510b8-177">FLASHMODE_REDEYE_AUTO</span><span class="sxs-lookup"><span data-stu-id="510b8-177">FLASHMODE_REDEYE_AUTO</span></span></td>
<td><span data-ttu-id="510b8-178">El dispositivo de cámara determina la configuración de Flash adecuada mediante la reducción de ojos rojos, independientemente de las condiciones de iluminación actuales.</span><span class="sxs-lookup"><span data-stu-id="510b8-178">The camera device determines the proper flash settings using red-eye reduction, regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="510b8-179">FLASHMODE_REDEYE_FILL</span><span class="sxs-lookup"><span data-stu-id="510b8-179">FLASHMODE_REDEYE_FILL</span></span></td>
<td><span data-ttu-id="510b8-180">El dispositivo de cámara está configurado para usar la reducción de ojos rojos y Flash sin tener en consideración las condiciones de iluminación actuales.</span><span class="sxs-lookup"><span data-stu-id="510b8-180">The camera device is configured to use red-eye reduction and flash regardless of current lighting conditions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510b8-181">FLASHMODE_EXTERNALSYNC</span><span class="sxs-lookup"><span data-stu-id="510b8-181">FLASHMODE_EXTERNALSYNC</span></span></td>
<td><span data-ttu-id="510b8-182">El dispositivo de cámara está configurado para sincronizarse con unidades Flash externas.</span><span class="sxs-lookup"><span data-stu-id="510b8-182">The camera device is configured to synchronize with external flash units.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MODE"></span><span id="wia_dpc_focus_mode"></span><dl> <span data-ttu-id="510b8-183"><dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-183"><dt><strong>WIA_DPC_FOCUS_MODE</strong></dt> <dt>CameraDeviceFocusMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-184">Define la configuración del modo de enfoque actual para el dispositivo de cámara.</span><span class="sxs-lookup"><span data-stu-id="510b8-184">Defines the current focus mode setting for the camera device.</span></span> <span data-ttu-id="510b8-185">El controlador de dispositivo enumera los valores admitidos de esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="510b8-185">The device driver enumerates the supported values of this property.</span></span> <span data-ttu-id="510b8-186">Una aplicación escribe esta propiedad para establecer el modo de enfoque para el dispositivo de cámara.</span><span class="sxs-lookup"><span data-stu-id="510b8-186">An application writes this property to set the focus mode for the camera device.</span></span></p>
<p><span data-ttu-id="510b8-187">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="510b8-187">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="510b8-188">En la tabla siguiente se muestran las tres constantes válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="510b8-188">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="510b8-189">Modo de enfoque</span><span class="sxs-lookup"><span data-stu-id="510b8-189">Focus Mode</span></span></th>
<th><span data-ttu-id="510b8-190">Descripción</span><span class="sxs-lookup"><span data-stu-id="510b8-190">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="510b8-191">FOCUSMODE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="510b8-191">FOCUSMODE_MANUAL</span></span></td>
<td><span data-ttu-id="510b8-192">El dispositivo de cámara está configurado para permitir que el usuario se Centre manualmente.</span><span class="sxs-lookup"><span data-stu-id="510b8-192">The camera device is configured to allow the user to focus manually.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510b8-193">FOCUSMODE_AUTO</span><span class="sxs-lookup"><span data-stu-id="510b8-193">FOCUSMODE_AUTO</span></span></td>
<td><span data-ttu-id="510b8-194">El dispositivo de cámara está configurado para centrarse automáticamente.</span><span class="sxs-lookup"><span data-stu-id="510b8-194">The camera device is configured to focus automatically.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="510b8-195">FOCUSMODE_MACROAUTO</span><span class="sxs-lookup"><span data-stu-id="510b8-195">FOCUSMODE_MACROAUTO</span></span></td>
<td><span data-ttu-id="510b8-196">El dispositivo de cámara está configurado para centrarse automáticamente en el uso de la configuración de macros de rango corto.</span><span class="sxs-lookup"><span data-stu-id="510b8-196">The camera device is configured to focus automatically using short-range macro settings.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_MANUAL_DIST"></span><span id="wia_dpc_focus_manual_dist"></span><dl> <span data-ttu-id="510b8-197"><dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-197"><dt><strong>WIA_DPC_FOCUS_MANUAL_DIST</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-198">Reservado, no usar.</span><span class="sxs-lookup"><span data-stu-id="510b8-198">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="510b8-199">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-199">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ZOOM_POSITION"></span><span id="wia_dpc_zoom_position"></span><dl> <span data-ttu-id="510b8-200"><dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-200"><dt><strong>WIA_DPC_ZOOM_POSITION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-201">Reservado, no usar.</span><span class="sxs-lookup"><span data-stu-id="510b8-201">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="510b8-202">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-202">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PAN_POSITION"></span><span id="wia_dpc_pan_position"></span><dl> <span data-ttu-id="510b8-203"><dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-203"><dt><strong>WIA_DPC_PAN_POSITION</strong></dt> <dt>CameraDevicePanPosition</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-204">Reservado, no usar.</span><span class="sxs-lookup"><span data-stu-id="510b8-204">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="510b8-205">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-205">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TILT_POSITION"></span><span id="wia_dpc_tilt_position"></span><dl> <span data-ttu-id="510b8-206"><dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-206"><dt><strong>WIA_DPC_TILT_POSITION</strong></dt> <dt>CameraDeviceTiltPosition</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-207">Reservado, no usar.</span><span class="sxs-lookup"><span data-stu-id="510b8-207">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="510b8-208">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-208">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_MODE"></span><span id="wia_dpc_timer_mode"></span><dl> <span data-ttu-id="510b8-209"><dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-209"><dt><strong>WIA_DPC_TIMER_MODE</strong></dt> <dt>CameraDeviceTimerMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-210">Reservado, no usar.</span><span class="sxs-lookup"><span data-stu-id="510b8-210">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="510b8-211">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-211">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMER_VALUE"></span><span id="wia_dpc_timer_value"></span><dl> <span data-ttu-id="510b8-212"><dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-212"><dt><strong>WIA_DPC_TIMER_VALUE</strong></dt> <dt>CameraDeviceTimerValue</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-213">Reservado, no usar.</span><span class="sxs-lookup"><span data-stu-id="510b8-213">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="510b8-214">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-214">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_POWER_MODE"></span><span id="wia_dpc_power_mode"></span><dl> <span data-ttu-id="510b8-215"><dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-215"><dt><strong>WIA_DPC_POWER_MODE</strong></dt> <dt>CameraDevicePowerMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-216">Define la fuente de alimentación actual para el dispositivo de cámara.</span><span class="sxs-lookup"><span data-stu-id="510b8-216">Defines the current power source for the camera device.</span></span> <span data-ttu-id="510b8-217">Una aplicación Lee esta propiedad para determinar el origen de energía que está usando la cámara.</span><span class="sxs-lookup"><span data-stu-id="510b8-217">An application reads this property to determine what power source the camera is using.</span></span></p>
<p><span data-ttu-id="510b8-218">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-218">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p>
<p><span data-ttu-id="510b8-219">En la tabla siguiente se muestran las dos constantes válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="510b8-219">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="510b8-220">Modo de energía</span><span class="sxs-lookup"><span data-stu-id="510b8-220">Power Mode</span></span></th>
<th><span data-ttu-id="510b8-221">Descripción</span><span class="sxs-lookup"><span data-stu-id="510b8-221">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="510b8-222">POWERMODE_LINE</span><span class="sxs-lookup"><span data-stu-id="510b8-222">POWERMODE_LINE</span></span></td>
<td><span data-ttu-id="510b8-223">El dispositivo de cámara está funcionando en un adaptador de alimentación.</span><span class="sxs-lookup"><span data-stu-id="510b8-223">The camera device is operating on a power adapter.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510b8-224">POWERMODE_BATTERY</span><span class="sxs-lookup"><span data-stu-id="510b8-224">POWERMODE_BATTERY</span></span></td>
<td><span data-ttu-id="510b8-225">El dispositivo de cámara está funcionando con la energía de la batería.</span><span class="sxs-lookup"><span data-stu-id="510b8-225">The camera device is operating on battery power.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BATTERY_STATUS"></span><span id="wia_dpc_battery_status"></span><dl> <span data-ttu-id="510b8-226"><dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-226"><dt><strong>WIA_DPC_BATTERY_STATUS</strong></dt> <dt>CameraDeviceBatteryStatus</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-227">El porcentaje de energía de la batería que queda para operar el dispositivo de cámara.</span><span class="sxs-lookup"><span data-stu-id="510b8-227">The percentage of battery power that is left to operate the camera device.</span></span> <span data-ttu-id="510b8-228">Este valor debe ser un entero comprendido entre 0 y 100.</span><span class="sxs-lookup"><span data-stu-id="510b8-228">This value should be an integer from 0 through 100.</span></span> <span data-ttu-id="510b8-229">Una aplicación Lee esta propiedad para determinar la duración restante de la batería del dispositivo de cámara.</span><span class="sxs-lookup"><span data-stu-id="510b8-229">An application reads this property to determine the remaining battery life of the camera device.</span></span></p>
<p><span data-ttu-id="510b8-230">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-230">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_WIDTH"></span><span id="wia_dpc_thumb_width"></span><dl> <span data-ttu-id="510b8-231"><dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-231"><dt><strong>WIA_DPC_THUMB_WIDTH</strong></dt> <dt>CameraDeviceThumbWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-232">Ancho, en píxeles, de una imagen en miniatura que se va a usar para las imágenes recién capturadas.</span><span class="sxs-lookup"><span data-stu-id="510b8-232">The width, in pixels, of a thumbnail image to use for newly captured images.</span></span> <span data-ttu-id="510b8-233">Una aplicación Lee este valor para obtener un tamaño estimado para Mostrar miniaturas en su interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="510b8-233">An application reads this value to get an estimated size for displaying thumbnails in its user interface.</span></span></p>
<p><span data-ttu-id="510b8-234">Tipo: <strong>VT_I4</strong>, Access: lectura y escritura (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) o solo lectura (WIA_PROP_NONE), valores válidos: WIA_PROP_LIST o WIA_PROP_NONE</span><span class="sxs-lookup"><span data-stu-id="510b8-234">Type: <strong>VT_I4</strong>, Access: Read/Write (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) or Read Only (WIA_PROP_NONE), Valid values: WIA_PROP_LIST or WIA_PROP_NONE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_THUMB_HEIGHT"></span><span id="wia_dpc_thumb_height"></span><dl> <span data-ttu-id="510b8-235"><dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-235"><dt><strong>WIA_DPC_THUMB_HEIGHT</strong></dt> <dt>CameraDeviceThumbHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-236">Ancho, en píxeles, de una imagen en miniatura que se va a usar para las imágenes recién capturadas.</span><span class="sxs-lookup"><span data-stu-id="510b8-236">The width, in pixels, of a thumbnail image to use for newly captured images.</span></span> <span data-ttu-id="510b8-237">Una aplicación Lee este valor para obtener un tamaño estimado para Mostrar miniaturas en su interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="510b8-237">An application reads this value to get an estimated size for displaying thumbnails in its user interface.</span></span></p>
<p><span data-ttu-id="510b8-238">Tipo: <strong>VT_I4</strong>, Access: lectura y escritura (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) o solo lectura (WIA_PROP_NONE), valores válidos: WIA_PROP_LIST o WIA_PROP_NONE</span><span class="sxs-lookup"><span data-stu-id="510b8-238">Type: <strong>VT_I4</strong>, Access: Read/Write (<a href="-wia-property-attributes.md">WIA_PROP_LIST</a>) or Read Only (WIA_PROP_NONE), Valid values: WIA_PROP_LIST or WIA_PROP_NONE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_PICT_WIDTH"></span><span id="wia_dpc_pict_width"></span><dl> <span data-ttu-id="510b8-239"><dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-239"><dt><strong>WIA_DPC_PICT_WIDTH</strong></dt> <dt>CameraDevicePictWidth</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-240">Ancho en píxeles que se va a usar para las imágenes recién capturadas.</span><span class="sxs-lookup"><span data-stu-id="510b8-240">The width in pixels to use for newly captured images.</span></span> <span data-ttu-id="510b8-241">La lista de valores válidos para esta propiedad tiene una correspondencia uno a uno con la lista de valores válidos para la propiedad <strong>WIA_DPC_PICT_HEIGHT</strong> .</span><span class="sxs-lookup"><span data-stu-id="510b8-241">The list of valid values for this property has a one-to-one correspondence to the list of valid values for the <strong>WIA_DPC_PICT_HEIGHT</strong> property.</span></span> <span data-ttu-id="510b8-242">Si el ancho y el alto individuales se pueden establecer de forma lineal y ortogonal entre sí, se pueden expresar como un intervalo.</span><span class="sxs-lookup"><span data-stu-id="510b8-242">If the individual width and height are linearly settable and orthogonal to each other, they may be expressed as a range.</span></span></p>
<p><span data-ttu-id="510b8-243">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="510b8-243">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_PICT_HEIGHT"></span><span id="wia_dpc_pict_height"></span><dl> <span data-ttu-id="510b8-244"><dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-244"><dt><strong>WIA_DPC_PICT_HEIGHT</strong></dt> <dt>CameraDevicePictHeight</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-245">Alto en píxeles que se va a usar para las imágenes recién capturadas.</span><span class="sxs-lookup"><span data-stu-id="510b8-245">The height in pixels to use for newly captured images.</span></span> <span data-ttu-id="510b8-246">La lista de valores válidos para esta propiedad tiene una correspondencia uno a uno con la lista de valores válidos para la propiedad <strong>WIA_DPC_PICT_WIDTH</strong> .</span><span class="sxs-lookup"><span data-stu-id="510b8-246">The list of valid values for this property has a one-to-one correspondence with the list of valid values for the <strong>WIA_DPC_PICT_WIDTH</strong> property.</span></span> <span data-ttu-id="510b8-247">Si el ancho y el alto individuales se pueden establecer de forma lineal y ortogonal entre sí, se pueden expresar como un intervalo.</span><span class="sxs-lookup"><span data-stu-id="510b8-247">If the individual width and height are linearly settable and orthogonal to each other, they may be expressed as a range.</span></span></p>
<p><span data-ttu-id="510b8-248">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="510b8-248">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIMENSION"></span><span id="wia_dpc_dimension"></span><dl> <span data-ttu-id="510b8-249"><dt><strong>WIA_DPC_DIMENSION</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-249"><dt><strong>WIA_DPC_DIMENSION</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-250">Reservado, no usar.</span><span class="sxs-lookup"><span data-stu-id="510b8-250">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="510b8-251">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-251">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_COMPRESSION_SETTING"></span><span id="wia_dpc_compression_setting"></span><dl> <span data-ttu-id="510b8-252"><dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-252"><dt><strong>WIA_DPC_COMPRESSION_SETTING</strong></dt> <dt>CameraDeviceCompressionSetting</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-253">Diseñado para ser aproximadamente lineal con respecto a la calidad de imagen percibida en una amplia gama de contenido de la escena, y contiene un intervalo o una lista de enteros.</span><span class="sxs-lookup"><span data-stu-id="510b8-253">Intended to be approximately linear with respect to perceived image quality over a broad range of scene content, and it contains either a range or a list of integers.</span></span> <span data-ttu-id="510b8-254">Los enteros más pequeños se utilizan para representar una calidad inferior (es decir, la compresión máxima), mientras que los enteros más grandes se usan para representar una mayor calidad (es decir, compresión mínima).</span><span class="sxs-lookup"><span data-stu-id="510b8-254">Smaller integers are used to represent lower quality (that is, maximum compression), whereas larger integers are used to represent higher quality (that is, minimum compression).</span></span> <span data-ttu-id="510b8-255">Cualquier configuración disponible en un dispositivo solo es relativa a ese dispositivo y, por lo tanto, es específico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="510b8-255">Any available settings on a device are relative only to that device and are therefore device specific.</span></span></p>
<p><span data-ttu-id="510b8-256">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="510b8-256">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING"></span><span id="wia_dpc_focus_metering"></span><dl> <span data-ttu-id="510b8-257"><dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-257"><dt><strong>WIA_DPC_FOCUS_METERING</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-258">Reservado, no usar.</span><span class="sxs-lookup"><span data-stu-id="510b8-258">Reserved, do not use.</span></span></p>
<p><span data-ttu-id="510b8-259">Tipo: <strong>VT_I4</strong>, acceso: solo lectura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-259">Type: <strong>VT_I4</strong>, Access: Read Only, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_INTERVAL"></span><span id="wia_dpc_timelapse_interval"></span><dl> <span data-ttu-id="510b8-260"><dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-260"><dt><strong>WIA_DPC_TIMELAPSE_INTERVAL</strong></dt> <dt>CameraDeviceTimelapseInterval</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-261">El tiempo, en milisegundos, entre las capturas de imagen en una operación de captura de lapso de tiempo.</span><span class="sxs-lookup"><span data-stu-id="510b8-261">The time, in milliseconds, between image captures in a time-lapse capture operation.</span></span></p>
<p><span data-ttu-id="510b8-262">Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="510b8-262">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_TIMELAPSE_NUMBER"></span><span id="wia_dpc_timelapse_number"></span><dl> <span data-ttu-id="510b8-263"><dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-263"><dt><strong>WIA_DPC_TIMELAPSE_NUMBER</strong></dt> <dt>CameraDeviceTimelapseNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-264">El número de imágenes que el dispositivo intenta capturar durante una captura de lapso de tiempo.</span><span class="sxs-lookup"><span data-stu-id="510b8-264">The number of images the device attempts to capture during a time-lapse capture.</span></span></p>
<p><span data-ttu-id="510b8-265">Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="510b8-265">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_BURST_INTERVAL"></span><span id="wia_dpc_burst_interval"></span><dl> <span data-ttu-id="510b8-266"><dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-266"><dt><strong>WIA_DPC_BURST_INTERVAL</strong></dt> <dt>CameraDeviceBurstInterval</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-267">El tiempo, en milisegundos, entre las capturas de la imagen durante una operación de ráfaga.</span><span class="sxs-lookup"><span data-stu-id="510b8-267">The time, in milliseconds, between image captures during a burst operation.</span></span></p>
<p><span data-ttu-id="510b8-268">Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="510b8-268">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_BURST_NUMBER"></span><span id="wia_dpc_burst_number"></span><dl> <span data-ttu-id="510b8-269"><dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-269"><dt><strong>WIA_DPC_BURST_NUMBER</strong></dt> <dt>CameraDeviceBurstNumber</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-270">El número de imágenes que el dispositivo intenta capturar durante una operación de ráfaga.</span><span class="sxs-lookup"><span data-stu-id="510b8-270">The number of images the device attempts to capture during a burst operation.</span></span></p>
<p><span data-ttu-id="510b8-271">Tipo: <strong>VT_I4</strong>, acceso: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="510b8-271">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a>, WIA_PROP_LIST, or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EFFECT_MODE"></span><span id="wia_dpc_effect_mode"></span><dl> <span data-ttu-id="510b8-272"><dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-272"><dt><strong>WIA_DPC_EFFECT_MODE</strong></dt> <dt>CameraDeviceEffectMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-273">Especifica el modo de adquisición de imagen especial de la cámara.</span><span class="sxs-lookup"><span data-stu-id="510b8-273">Specifies the special image acquisition mode of the camera.</span></span></p>
<p><span data-ttu-id="510b8-274">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="510b8-274">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="510b8-275">En la tabla siguiente se muestran las tres constantes válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="510b8-275">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="510b8-276">Modo de efecto</span><span class="sxs-lookup"><span data-stu-id="510b8-276">Effect Mode</span></span></th>
<th><span data-ttu-id="510b8-277">Descripción</span><span class="sxs-lookup"><span data-stu-id="510b8-277">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="510b8-278">EFFECTMODE_STANDARD</span><span class="sxs-lookup"><span data-stu-id="510b8-278">EFFECTMODE_STANDARD</span></span></td>
<td><span data-ttu-id="510b8-279">Capture una imagen en el modo estándar de la cámara.</span><span class="sxs-lookup"><span data-stu-id="510b8-279">Capture an image in the standard mode for the camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510b8-280">EFFECTMODE_BW</span><span class="sxs-lookup"><span data-stu-id="510b8-280">EFFECTMODE_BW</span></span></td>
<td><span data-ttu-id="510b8-281">Capturar una imagen de escala de grises.</span><span class="sxs-lookup"><span data-stu-id="510b8-281">Capture a grayscale image.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="510b8-282">EFFECTMODE_SEPIA</span><span class="sxs-lookup"><span data-stu-id="510b8-282">EFFECTMODE_SEPIA</span></span></td>
<td><span data-ttu-id="510b8-283">Capturar una imagen sepia.</span><span class="sxs-lookup"><span data-stu-id="510b8-283">Capture a sepia image.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_DIGITAL_ZOOM"></span><span id="wia_dpc_digital_zoom"></span><dl> <span data-ttu-id="510b8-284"><dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-284"><dt><strong>WIA_DPC_DIGITAL_ZOOM</strong></dt> <dt>CameraDeviceDigitalZoom</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-285">La relación de zoom efectiva de la imagen adquirida de la cámara digital, escalada por un factor de 10.</span><span class="sxs-lookup"><span data-stu-id="510b8-285">The effective zoom ratio of the digital camera's acquired image, scaled by a factor of 10.</span></span> <span data-ttu-id="510b8-286">Un valor de 10 corresponde a la ausencia del zoom digital (1X), que es el tamaño de la escena estándar capturado por la cámara.</span><span class="sxs-lookup"><span data-stu-id="510b8-286">A value of 10 corresponds to the absence of digital zoom (1X), which is the standard scene size captured by the camera.</span></span> <span data-ttu-id="510b8-287">Un valor de 20 corresponde a un zoom de 2X, donde la cámara captura un cuarto del tamaño de la escena estándar.</span><span class="sxs-lookup"><span data-stu-id="510b8-287">A value of 20 corresponds to a 2X zoom, where one-quarter of the standard scene size is captured by the camera.</span></span></p>
<p><span data-ttu-id="510b8-288">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="510b8-288">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_SHARPNESS"></span><span id="wia_dpc_sharpness"></span><dl> <span data-ttu-id="510b8-289"><dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-289"><dt><strong>WIA_DPC_SHARPNESS</strong></dt> <dt>CameraDeviceSharpness</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-290">Nitidez percibido de una imagen capturada.</span><span class="sxs-lookup"><span data-stu-id="510b8-290">The perceived sharpness of a captured image.</span></span> <span data-ttu-id="510b8-291">Esta propiedad puede utilizar una lista de valores o un intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="510b8-291">This property can use either a list of values or a range of values.</span></span> <span data-ttu-id="510b8-292">El valor mínimo representa la cantidad mínima de nitidez, mientras que el valor máximo representa la nitidez máxima.</span><span class="sxs-lookup"><span data-stu-id="510b8-292">The minimum value represents the least amount of sharpness, whereas the maximum value represents the maximum sharpness.</span></span> <span data-ttu-id="510b8-293">Normalmente, un valor en el centro del intervalo representa la nitidez normal o predeterminada.</span><span class="sxs-lookup"><span data-stu-id="510b8-293">Typically a value in the middle of the range represents normal, or default, sharpness.</span></span></p>
<p><span data-ttu-id="510b8-294">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="510b8-294">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CONTRAST"></span><span id="wia_dpc_contrast"></span><dl> <span data-ttu-id="510b8-295"><dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-295"><dt><strong>WIA_DPC_CONTRAST</strong></dt> <dt>CameraDeviceContrast</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-296">El contraste percibido de una imagen capturada.</span><span class="sxs-lookup"><span data-stu-id="510b8-296">The perceived contrast of a captured image.</span></span> <span data-ttu-id="510b8-297">Esta propiedad puede contener una lista de valores o un intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="510b8-297">This property can contain either a list of values or a range of values.</span></span> <span data-ttu-id="510b8-298">El valor mínimo admitido representa la menor cantidad de contraste, mientras que el valor máximo representa el mayor contraste.</span><span class="sxs-lookup"><span data-stu-id="510b8-298">The minimum supported value represents the least amount of contrast, whereas the maximum value represents the most contrast.</span></span> <span data-ttu-id="510b8-299">Normalmente, un valor en el centro del intervalo representa el contraste normal o predeterminado.</span><span class="sxs-lookup"><span data-stu-id="510b8-299">Typically, a value in the middle of the range represents normal, or default, contrast.</span></span></p>
<p><span data-ttu-id="510b8-300">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="510b8-300">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_MODE"></span><span id="wia_dpc_capture_mode"></span><dl> <span data-ttu-id="510b8-301"><dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-301"><dt><strong>WIA_DPC_CAPTURE_MODE</strong></dt> <dt>CameraDeviceCaptureMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-302">Establece el modo de captura de imagen.</span><span class="sxs-lookup"><span data-stu-id="510b8-302">Sets the image capture mode.</span></span></p>
<p><span data-ttu-id="510b8-303">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="510b8-303">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="510b8-304">En la tabla siguiente se muestran las tres constantes válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="510b8-304">The following table has the three constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="510b8-305">Modo de captura</span><span class="sxs-lookup"><span data-stu-id="510b8-305">Capture Mode</span></span></th>
<th><span data-ttu-id="510b8-306">Descripción</span><span class="sxs-lookup"><span data-stu-id="510b8-306">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="510b8-307">CAPTUREMODE_NORMAL</span><span class="sxs-lookup"><span data-stu-id="510b8-307">CAPTUREMODE_NORMAL</span></span></td>
<td><span data-ttu-id="510b8-308">Modo normal de la cámara.</span><span class="sxs-lookup"><span data-stu-id="510b8-308">Normal mode for the camera.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510b8-309">CAPTUREMODE_BURST</span><span class="sxs-lookup"><span data-stu-id="510b8-309">CAPTUREMODE_BURST</span></span></td>
<td><span data-ttu-id="510b8-310">Capturar más de una imagen en una sucesión rápida según lo definido por los valores de las propiedades <strong>WIA_DPC_BURST_NUMBER</strong> y <strong>WIA_DPC_BURST_INTERVAL</strong> .</span><span class="sxs-lookup"><span data-stu-id="510b8-310">Capture more than one image in quick succession as defined by the values of the <strong>WIA_DPC_BURST_NUMBER</strong> and <strong>WIA_DPC_BURST_INTERVAL</strong> properties.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="510b8-311">CAPTUREMODE_TIMELAPSE</span><span class="sxs-lookup"><span data-stu-id="510b8-311">CAPTUREMODE_TIMELAPSE</span></span></td>
<td><span data-ttu-id="510b8-312">Capturar más de una imagen en sucesión tal y como se define en las propiedades <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> y <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> .</span><span class="sxs-lookup"><span data-stu-id="510b8-312">Capture more than one image in succession as defined by the <strong>WIA_DPC_TIMELAPSE_NUMBER</strong> and <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong> properties.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_CAPTURE_DELAY"></span><span id="wia_dpc_capture_delay"></span><dl> <span data-ttu-id="510b8-313"><dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-313"><dt><strong>WIA_DPC_CAPTURE_DELAY</strong></dt> <dt>CameraDeviceCaptureDelay</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-314">Valor que representa la cantidad de tiempo de retardo, en milisegundos, que se debe insertar entre el desencadenador de captura y el inicio real de la captura de datos.</span><span class="sxs-lookup"><span data-stu-id="510b8-314">The value representing the amount of time delay, in milliseconds, that should be inserted between the capture trigger and the actual initiation of the data capture.</span></span> <span data-ttu-id="510b8-315">Esta propiedad no está pensada para usarse con el fin de describir el tiempo entre fotogramas para la iniciación única, varias capturas, como la ráfaga o el lapso de tiempo, que tienen propiedades de intervalo independientes <strong>WIA_DPC_BURST_INTERVAL</strong> y <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>.</span><span class="sxs-lookup"><span data-stu-id="510b8-315">This property is not intended to be used to describe the time between frames for single-initiation, multiple captures such as burst or time lapse, which have separate interval properties <strong>WIA_DPC_BURST_INTERVAL</strong> and <strong>WIA_DPC_TIMELAPSE_INTERVAL</strong>.</span></span> <span data-ttu-id="510b8-316">En esos casos, todavía actúa como un retraso inicial antes de que se Capture la primera imagen de la serie, independientemente del tiempo entre fotogramas.</span><span class="sxs-lookup"><span data-stu-id="510b8-316">In those cases, it still serves as an initial delay before the first image in the series is captured, independent of the time between frames.</span></span> <span data-ttu-id="510b8-317">En el caso de que no haya retraso en la captura, esta propiedad debe establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="510b8-317">For no precapture delay, this property should be set to zero.</span></span></p>
<p><span data-ttu-id="510b8-318">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="510b8-318">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_INDEX"></span><span id="wia_dpc_exposure_index"></span><dl> <span data-ttu-id="510b8-319"><dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-319"><dt><strong>WIA_DPC_EXPOSURE_INDEX</strong></dt> <dt>CameraDeviceExposureIndex</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-320">Permite la emulación de la configuración de velocidad de película en una cámara digital.</span><span class="sxs-lookup"><span data-stu-id="510b8-320">Allows for the emulation of film speed settings on a digital camera.</span></span> <span data-ttu-id="510b8-321">La configuración corresponde a las designaciones ISO (ASA/DIN).</span><span class="sxs-lookup"><span data-stu-id="510b8-321">The settings correspond to the ISO designations (ASA/DIN).</span></span> <span data-ttu-id="510b8-322">Normalmente, un dispositivo admite valores enumerados discretos, pero es posible el control continuo sobre un intervalo de valores.</span><span class="sxs-lookup"><span data-stu-id="510b8-322">Typically, a device supports discrete enumerated values, but continuous control over a range of values is possible.</span></span> <span data-ttu-id="510b8-323">Un valor de 0xFFFF corresponde a la configuración automática de ISO.</span><span class="sxs-lookup"><span data-stu-id="510b8-323">A value of 0xFFFF corresponds to the Automatic ISO setting.</span></span></p>
<p><span data-ttu-id="510b8-324">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="510b8-324">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_EXPOSURE_METERING_MODE"></span><span id="wia_dpc_exposure_metering_mode"></span><dl> <span data-ttu-id="510b8-325"><dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-325"><dt><strong>WIA_DPC_EXPOSURE_METERING_MODE</strong></dt> <dt>CameraDeviceExposureMeteringMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-326">Especifica el modo que la cámara utiliza para ajustar automáticamente la configuración de exposición.</span><span class="sxs-lookup"><span data-stu-id="510b8-326">Specifies the mode the camera uses to automatically adjust the exposure setting.</span></span></p>
<p><span data-ttu-id="510b8-327">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="510b8-327">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="510b8-328">Modo de medición de exposición</span><span class="sxs-lookup"><span data-stu-id="510b8-328">Exposure Metering Mode</span></span></th>
<th><span data-ttu-id="510b8-329">Descripción</span><span class="sxs-lookup"><span data-stu-id="510b8-329">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="510b8-330">EXPOSUREMETERING_AVERAGE</span><span class="sxs-lookup"><span data-stu-id="510b8-330">EXPOSUREMETERING_AVERAGE</span></span></td>
<td><span data-ttu-id="510b8-331">Establezca la exposición en función de la media de toda la escena.</span><span class="sxs-lookup"><span data-stu-id="510b8-331">Set the exposure based on an average of the entire scene.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510b8-332">EXPOSUREMETERING_CENTERWEIGHT</span><span class="sxs-lookup"><span data-stu-id="510b8-332">EXPOSUREMETERING_CENTERWEIGHT</span></span></td>
<td><span data-ttu-id="510b8-333">Establezca la exposición en función de una media ponderada en el centro.</span><span class="sxs-lookup"><span data-stu-id="510b8-333">Set the exposure based on a center-weighted average.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="510b8-334">EXPOSUREMETERING_MULTISPOT</span><span class="sxs-lookup"><span data-stu-id="510b8-334">EXPOSUREMETERING_MULTISPOT</span></span></td>
<td><span data-ttu-id="510b8-335">Establezca la exposición en función de un patrón de multizona.</span><span class="sxs-lookup"><span data-stu-id="510b8-335">Set the exposure based on a multispot pattern.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510b8-336">EXPOSUREMETERING_CENTERSPOT</span><span class="sxs-lookup"><span data-stu-id="510b8-336">EXPOSUREMETERING_CENTERSPOT</span></span></td>
<td><span data-ttu-id="510b8-337">Establezca la exposición en función de una zona central.</span><span class="sxs-lookup"><span data-stu-id="510b8-337">Set the exposure based on a center spot.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_METERING_MODE"></span><span id="wia_dpc_focus_metering_mode"></span><dl> <span data-ttu-id="510b8-338"><dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-338"><dt><strong>WIA_DPC_FOCUS_METERING_MODE</strong></dt> <dt>CameraDeviceFocusMeteringMode</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-339">Especifica el modo que la cámara utiliza para ajustar automáticamente el foco.</span><span class="sxs-lookup"><span data-stu-id="510b8-339">Specifies the mode the camera uses to automatically adjust the focus.</span></span></p>
<p><span data-ttu-id="510b8-340">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="510b8-340">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="510b8-341">En la tabla siguiente se muestran las dos constantes válidas con esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="510b8-341">The following table has the two constants that are valid with this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="510b8-342">Modo de medición de foco</span><span class="sxs-lookup"><span data-stu-id="510b8-342">Focus Metering Mode</span></span></th>
<th><span data-ttu-id="510b8-343">Descripción</span><span class="sxs-lookup"><span data-stu-id="510b8-343">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="510b8-344">FOCUSMETERING_CENTERSPOT</span><span class="sxs-lookup"><span data-stu-id="510b8-344">FOCUSMETERING_CENTERSPOT</span></span></td>
<td><span data-ttu-id="510b8-345">Ajuste el foco en función de una zona central.</span><span class="sxs-lookup"><span data-stu-id="510b8-345">Adjust the focus based on a center spot.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510b8-346">FOCUSMETERING_MULTISPOT</span><span class="sxs-lookup"><span data-stu-id="510b8-346">FOCUSMETERING_MULTISPOT</span></span></td>
<td><span data-ttu-id="510b8-347">Ajuste el foco en función de un patrón de selección multizona.</span><span class="sxs-lookup"><span data-stu-id="510b8-347">Adjust the focus based on a multispot pattern.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_FOCUS_DISTANCE"></span><span id="wia_dpc_focus_distance"></span><dl> <span data-ttu-id="510b8-348"><dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-348"><dt><strong>WIA_DPC_FOCUS_DISTANCE</strong></dt> <dt>CameraDeviceFocusDistance</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-349">Distancia, en milímetros, entre el plano de captura de imágenes de la cámara digital y el punto de foco.</span><span class="sxs-lookup"><span data-stu-id="510b8-349">The distance, in millimeters, between the image-capturing plane of the digital camera and the point of focus.</span></span> <span data-ttu-id="510b8-350">Un valor de 0xFFFF corresponde a una configuración superior a 655 metros.</span><span class="sxs-lookup"><span data-stu-id="510b8-350">A value of 0xFFFF corresponds to a setting greater than 655 meters.</span></span></p>
<p><span data-ttu-id="510b8-351">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> o WIA_PROP_RANGE</span><span class="sxs-lookup"><span data-stu-id="510b8-351">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a> or WIA_PROP_RANGE</span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_FOCAL_LENGTH"></span><span id="wia_dpc_focal_length"></span><dl> <span data-ttu-id="510b8-352"><dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-352"><dt><strong>WIA_DPC_FOCAL_LENGTH</strong></dt> <dt>CameraDeviceFocalLength</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-353">La longitud focal equivalente de 35mm.</span><span class="sxs-lookup"><span data-stu-id="510b8-353">The 35mm-equivalent focal length.</span></span> <span data-ttu-id="510b8-354">Los valores de esta propiedad se corresponden con la longitud focal en milímetros multiplicada por 100.</span><span class="sxs-lookup"><span data-stu-id="510b8-354">The values of this property correspond to the focal length in millimeters multiplied by 100.</span></span> <span data-ttu-id="510b8-355">La longitud focal determina el zoom óptico.</span><span class="sxs-lookup"><span data-stu-id="510b8-355">The focal length determines the optical zoom.</span></span></p>
<p><span data-ttu-id="510b8-356">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-356">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_RGB_GAIN"></span><span id="wia_dpc_rgb_gain"></span><dl> <span data-ttu-id="510b8-357"><dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-357"><dt><strong>WIA_DPC_RGB_GAIN</strong></dt> <dt>CameraDeviceRGBGain</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-358">Una cadena Unicode terminada en null que representa la ganancia de color rojo, verde y azul aplicada a los datos de imagen, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="510b8-358">A null-terminated Unicode string that represents the red, green, and blue gain applied to image data, respectively.</span></span> <span data-ttu-id="510b8-359">Por ejemplo, &quot; 4:25:50 &quot; representa una ganancia roja de 4, una ganancia verde de 25 y una ganancia azul de 50.</span><span class="sxs-lookup"><span data-stu-id="510b8-359">For example, &quot;4:25:50&quot; represents a red gain of 4, a green gain of 25, and a blue gain of 50.</span></span></p>
<p><span data-ttu-id="510b8-360">Tipo: <strong>VT_BSTR</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-360">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_WHITE_BALANCE"></span><span id="wia_dpc_white_balance"></span><dl> <span data-ttu-id="510b8-361"><dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-361"><dt><strong>WIA_DPC_WHITE_BALANCE</strong></dt> <dt>CameraDeviceWhiteBalance</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-362">Especifica cómo la cámara digital pondera los canales de color.</span><span class="sxs-lookup"><span data-stu-id="510b8-362">Specifies how the digital camera weights color channels.</span></span></p>
<p><span data-ttu-id="510b8-363">Tipo: <strong>VT_I4</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span><span class="sxs-lookup"><span data-stu-id="510b8-363">Type: <strong>VT_I4</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_LIST</a></span></span></p>
<p><span data-ttu-id="510b8-364">A continuación se muestra una lista de los valores posibles para esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="510b8-364">The following is a list of possible values for this property.</span></span></p>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="510b8-365">Balance de blanco</span><span class="sxs-lookup"><span data-stu-id="510b8-365">White Balance</span></span></th>
<th><span data-ttu-id="510b8-366">Descripción</span><span class="sxs-lookup"><span data-stu-id="510b8-366">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="510b8-367">WHITEBALANCE_MANUAL</span><span class="sxs-lookup"><span data-stu-id="510b8-367">WHITEBALANCE_MANUAL</span></span></td>
<td><span data-ttu-id="510b8-368">El balance de blanco se establece directamente mediante la propiedad <strong>WIA_DPC_RGB_GAIN</strong> .</span><span class="sxs-lookup"><span data-stu-id="510b8-368">The white balance is set directly using the <strong>WIA_DPC_RGB_GAIN</strong> property.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510b8-369">WHITEBALANCE_AUTO</span><span class="sxs-lookup"><span data-stu-id="510b8-369">WHITEBALANCE_AUTO</span></span></td>
<td><span data-ttu-id="510b8-370">La cámara utiliza un mecanismo automático para establecer el equilibrio de blanco.</span><span class="sxs-lookup"><span data-stu-id="510b8-370">The camera uses an automatic mechanism to set the white balance.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="510b8-371">WHITEBALANCE_ONEPUSH_AUTO</span><span class="sxs-lookup"><span data-stu-id="510b8-371">WHITEBALANCE_ONEPUSH_AUTO</span></span></td>
<td><span data-ttu-id="510b8-372">La cámara determina el valor de balance de blanco cuando un usuario presiona el botón capturar mientras apunta a la cámara en una superficie blanca.</span><span class="sxs-lookup"><span data-stu-id="510b8-372">The camera determines the white balance setting when a user presses the capture button while pointing the camera at a white surface.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510b8-373">WHITEBALANCE_DAYLIGHT</span><span class="sxs-lookup"><span data-stu-id="510b8-373">WHITEBALANCE_DAYLIGHT</span></span></td>
<td><span data-ttu-id="510b8-374">La cámara establece el balance de blanco con un valor adecuado para su uso en condiciones de horario de verano.</span><span class="sxs-lookup"><span data-stu-id="510b8-374">The camera sets the white balance to a value appropriate for use in daylight conditions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="510b8-375">WHITEBALANCE_FLORESCENT</span><span class="sxs-lookup"><span data-stu-id="510b8-375">WHITEBALANCE_FLORESCENT</span></span></td>
<td><span data-ttu-id="510b8-376">La cámara establece el balance de blanco con un valor adecuado para su uso con una fuente de luz fluorescente.</span><span class="sxs-lookup"><span data-stu-id="510b8-376">The camera sets the white balance to a value appropriate for use with a fluorescent light source.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="510b8-377">WHITEBALANCE_TUNGSTEN</span><span class="sxs-lookup"><span data-stu-id="510b8-377">WHITEBALANCE_TUNGSTEN</span></span></td>
<td><span data-ttu-id="510b8-378">La cámara establece el balance de blanco con un valor adecuado para su uso con una fuente de luz de Tungsten.</span><span class="sxs-lookup"><span data-stu-id="510b8-378">The camera sets the white balance to a value appropriate for use with a tungsten light source.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="510b8-379">WHITEBALANCE_FLASH</span><span class="sxs-lookup"><span data-stu-id="510b8-379">WHITEBALANCE_FLASH</span></span></td>
<td><span data-ttu-id="510b8-380">La cámara establece el balance de blanco con un valor adecuado para su uso con un flash electrónico.</span><span class="sxs-lookup"><span data-stu-id="510b8-380">The camera sets the white balance to a value appropriate for use with an electronic flash.</span></span></td>
</tr>
</tbody>
</table>

<p> </p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_UPLOAD_URL"></span><span id="wia_dpc_upload_url"></span><dl> <span data-ttu-id="510b8-381"><dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-381"><dt><strong>WIA_DPC_UPLOAD_URL</strong></dt> <dt>CameraDeviceUploadURL</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-382">Describe una dirección URL.</span><span class="sxs-lookup"><span data-stu-id="510b8-382">Describes a URL.</span></span> <span data-ttu-id="510b8-383">La dirección URL descrita por este proroperty es aquella en la que se pueden cargar imágenes u objetos, una vez que se han adquirido desde el dispositivo, de acuerdo con uno de los siguientes escenarios.</span><span class="sxs-lookup"><span data-stu-id="510b8-383">The URL described by this proroperty is one that images or objects, after they are acquired from the device, can be uploaded to—according to one of the following scenarios.</span></span></p>
<ul>
<li><span data-ttu-id="510b8-384">Una aplicación WIA Lee esta propiedad y permite al usuario cargar imágenes automáticamente en la dirección URL.</span><span class="sxs-lookup"><span data-stu-id="510b8-384">A WIA application reads this property and allows the user to automatically upload images to the URL.</span></span></li>
<li><span data-ttu-id="510b8-385">Una aplicación establece la dirección URL y otros dispositivos (quioscos, etc.) usan esta propiedad.</span><span class="sxs-lookup"><span data-stu-id="510b8-385">An application sets the URL, and other devices (kiosks and so forth) use this property.</span></span></li>
</ul>
<p><span data-ttu-id="510b8-386">Microsoft Windows no carga imágenes por sí misma.</span><span class="sxs-lookup"><span data-stu-id="510b8-386">Microsoft Windows does not upload images by itself.</span></span></p>
<p><span data-ttu-id="510b8-387">Tipo: <strong>VT_BSTR</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-387">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="WIA_DPC_ARTIST"></span><span id="wia_dpc_artist"></span><dl> <span data-ttu-id="510b8-388"><dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-388"><dt><strong>WIA_DPC_ARTIST</strong></dt> <dt>CameraDeviceArtist</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-389">Nombre del propietario (que es el usuario actual) del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="510b8-389">The name of the owner ( which is the current user) of the device.</span></span> <span data-ttu-id="510b8-390">El dispositivo usa esta propiedad para rellenar el campo artista en cada imagen EXIF que captura.</span><span class="sxs-lookup"><span data-stu-id="510b8-390">The device uses this property to populate the Artist field in every EXIF image that it captures.</span></span></p>
<p><span data-ttu-id="510b8-391">Tipo: <strong>VT_BSTR</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-391">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="WIA_DPC_COPYRIGHT_INFO"></span><span id="wia_dpc_copyright_info"></span><dl> <span data-ttu-id="510b8-392"><dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </span><span class="sxs-lookup"><span data-stu-id="510b8-392"><dt><strong>WIA_DPC_COPYRIGHT_INFO</strong></dt> <dt>CameraDeviceCopyrightInfo</dt> </span></span></dl></td>
<td style="text-align: left;"><p><span data-ttu-id="510b8-393">La notificación de copyright.</span><span class="sxs-lookup"><span data-stu-id="510b8-393">The copyright notification.</span></span> <span data-ttu-id="510b8-394">El dispositivo usa esta propiedad para rellenar el campo copyright en cada imagen EXIF que captura.</span><span class="sxs-lookup"><span data-stu-id="510b8-394">The device uses this property to populate the Copyright field in every EXIF image that it captures.</span></span></p>
<p><span data-ttu-id="510b8-395">Tipo: <strong>VT_BSTR</strong>, Access: lectura/escritura, valores válidos: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span><span class="sxs-lookup"><span data-stu-id="510b8-395">Type: <strong>VT_BSTR</strong>, Access: Read/Write, Valid values: <a href="-wia-property-attributes.md">WIA_PROP_NONE</a></span></span></p></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="510b8-396">Requisitos</span><span class="sxs-lookup"><span data-stu-id="510b8-396">Requirements</span></span>



| <span data-ttu-id="510b8-397">Requisito</span><span class="sxs-lookup"><span data-stu-id="510b8-397">Requirement</span></span> | <span data-ttu-id="510b8-398">Value</span><span class="sxs-lookup"><span data-stu-id="510b8-398">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="510b8-399">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="510b8-399">Minimum supported client</span></span><br/> | <span data-ttu-id="510b8-400">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="510b8-400">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="510b8-401">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="510b8-401">Minimum supported server</span></span><br/> | <span data-ttu-id="510b8-402">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="510b8-402">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="510b8-403">Encabezado</span><span class="sxs-lookup"><span data-stu-id="510b8-403">Header</span></span><br/>                   | <dl> <span data-ttu-id="510b8-404"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="510b8-404"><dt>Wiadef.h</dt></span></span> </dl> |



 

 




