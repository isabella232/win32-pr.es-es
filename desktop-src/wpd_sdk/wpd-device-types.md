---
description: El \_ tipo de \_ enumeración de tipos de dispositivo WPD describe los distintos tipos de dispositivos portátiles (WPD) de Windows que se usan normalmente para determinar la clasificación básica y el aspecto visual de un dispositivo portátil.
ms.assetid: 51714e0f-e9b7-4474-a8bb-da3875ef5399
title: Enumeración WPD_DEVICE_TYPES (PortableDevice. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WPD_DEVICE_TYPES
api_type:
- HeaderDef
api_location:
- PortableDevice.h
ms.openlocfilehash: 3e71acf200a95bba05b7298a5824bfa353e4a90b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105698526"
---
# <a name="wpd_device_types-enumeration"></a><span data-ttu-id="06c94-103">\_Enumeración de tipos de dispositivos de WPD \_</span><span class="sxs-lookup"><span data-stu-id="06c94-103">WPD\_DEVICE\_TYPES enumeration</span></span>

<span data-ttu-id="06c94-104">El tipo de enumeración de **\_ \_ tipos de dispositivo WPD** describe los distintos tipos de dispositivos portátiles (WPD) de Windows que se usan normalmente para determinar la clasificación básica y el aspecto visual de un dispositivo portátil.</span><span class="sxs-lookup"><span data-stu-id="06c94-104">The **WPD\_DEVICE\_TYPES** enumeration type describes the different Windows Portable Device (WPD) types commonly used to determine the basic classification and visual appearance of a portable device.</span></span>

## <a name="syntax"></a><span data-ttu-id="06c94-105">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="06c94-105">Syntax</span></span>


```C++
typedef enum tagWPD_DEVICE_TYPES { 
  WPD_DEVICE_TYPE_GENERIC                       = 0,
  WPD_DEVICE_TYPE_CAMERA                        = 1,
  WPD_DEVICE_TYPE_MEDIA_PLAYER                  = 2,
  WPD_DEVICE_TYPE_PHONE                         = 3,
  WPD_DEVICE_TYPE_VIDEO                         = 4,
  WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER  = 5,
  WPD_DEVICE_TYPE_AUDIO_RECORDER                = 6
} WPD_DEVICE_TYPES;
```



## <a name="constants"></a><span data-ttu-id="06c94-106">Constantes</span><span class="sxs-lookup"><span data-stu-id="06c94-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="06c94-107"><span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**tipo de dispositivo de WPD \_ \_ \_ genérico**</span><span class="sxs-lookup"><span data-stu-id="06c94-107"><span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**WPD\_DEVICE\_TYPE\_GENERIC**</span></span>
</dt> <dd>

<span data-ttu-id="06c94-108">Un WPD genérico que incluye dispositivos multifunción que no se encuentran en uno de los otros valores de enumeración de [**\_ \_ tipos de dispositivos de WPD**](wpd-device-types.md) .</span><span class="sxs-lookup"><span data-stu-id="06c94-108">A generic WPD that includes multifunction devices that do not fall into one of the other [**WPD\_DEVICE\_TYPES**](wpd-device-types.md) enumeration values.</span></span>

</dd> <dt>

<span data-ttu-id="06c94-109"><span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**\_cámara de \_ tipo de dispositivo de WPD \_**</span><span class="sxs-lookup"><span data-stu-id="06c94-109"><span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**WPD\_DEVICE\_TYPE\_CAMERA**</span></span>
</dt> <dd>

<span data-ttu-id="06c94-110">Un dispositivo de cámara, como una cámara digital fija.</span><span class="sxs-lookup"><span data-stu-id="06c94-110">A camera device, such as a digital still camera.</span></span>

</dd> <dt>

<span data-ttu-id="06c94-111"><span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**\_reproductor de \_ media del tipo de dispositivo WPD \_ \_**</span><span class="sxs-lookup"><span data-stu-id="06c94-111"><span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER**</span></span>
</dt> <dd>

<span data-ttu-id="06c94-112">Un dispositivo del reproductor de media que admita la reproducción de audio, vídeo o visualización de imágenes, como un reproductor de música portátil o Portable Media Center.</span><span class="sxs-lookup"><span data-stu-id="06c94-112">A media player device that supports playing audio, video, or viewing pictures, such as a portable music player or portable media center.</span></span> <span data-ttu-id="06c94-113">No todas estas funciones se clasifican como un reproductor de \_ media del tipo de dispositivo WPD \_ \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="06c94-113">Not all of this functionally is classified as a WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER.</span></span> <span data-ttu-id="06c94-114">Por ejemplo, los dispositivos portátiles de reproducción de música se clasifican como el \_ tipo de dispositivo WPD \_ reproductor de \_ media \_ .</span><span class="sxs-lookup"><span data-stu-id="06c94-114">For example, portable music player devices are classified as WPD\_DEVICE\_TYPE\_MEDIA\_PLAYER.</span></span>

</dd> <dt>

<span data-ttu-id="06c94-115"><span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**tipo de dispositivo de WPD \_ \_ \_ teléfono**</span><span class="sxs-lookup"><span data-stu-id="06c94-115"><span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**WPD\_DEVICE\_TYPE\_PHONE**</span></span>
</dt> <dd>

<span data-ttu-id="06c94-116">Un dispositivo telefónico, como un teléfono móvil.</span><span class="sxs-lookup"><span data-stu-id="06c94-116">A phone device, such as a mobile phone.</span></span>

</dd> <dt>

<span data-ttu-id="06c94-117"><span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**\_vídeo de \_ tipo de dispositivo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="06c94-117"><span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**WPD\_DEVICE\_TYPE\_VIDEO**</span></span>
</dt> <dd>

<span data-ttu-id="06c94-118">Un dispositivo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="06c94-118">A video device.</span></span>

</dd> <dt>

<span data-ttu-id="06c94-119"><span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**\_Administrador de \_ \_ información personal \_ del tipo de dispositivo WPD \_**</span><span class="sxs-lookup"><span data-stu-id="06c94-119"><span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**WPD\_DEVICE\_TYPE\_PERSONAL\_INFORMATION\_MANAGER**</span></span>
</dt> <dd>

<span data-ttu-id="06c94-120">Un dispositivo del administrador de información personal.</span><span class="sxs-lookup"><span data-stu-id="06c94-120">A personal information manager device.</span></span>

</dd> <dt>

<span data-ttu-id="06c94-121"><span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**\_tipo de dispositivo WPD \_ \_ \_ grabadora de audio**</span><span class="sxs-lookup"><span data-stu-id="06c94-121"><span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**WPD\_DEVICE\_TYPE\_AUDIO\_RECORDER**</span></span>
</dt> <dd>

<span data-ttu-id="06c94-122">Un dispositivo de grabadora de audio.</span><span class="sxs-lookup"><span data-stu-id="06c94-122">An audio recorder device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="06c94-123">Observaciones</span><span class="sxs-lookup"><span data-stu-id="06c94-123">Remarks</span></span>

<span data-ttu-id="06c94-124">**WPD \_ Los \_ tipos de dispositivos** se leen mediante la interfaz [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) .</span><span class="sxs-lookup"><span data-stu-id="06c94-124">**WPD\_DEVICE\_TYPES** are read using the [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) interface.</span></span> <span data-ttu-id="06c94-125">Las aplicaciones de WPD pueden utilizar estos valores para determinar el aspecto visual genérico del dispositivo.</span><span class="sxs-lookup"><span data-stu-id="06c94-125">WPD applications may use these values to determine the generic visual appearance of the device.</span></span> <span data-ttu-id="06c94-126">Es decir, se muestra una imagen de cámara para dispositivos similares a la cámara, se muestra una imagen de teléfono móvil para dispositivos similares, etc.</span><span class="sxs-lookup"><span data-stu-id="06c94-126">That is, a camera picture is displayed for camera-like devices, a mobile phone picture is displayed for phone-like devices, and so on.</span></span>

> [!Note]  
> <span data-ttu-id="06c94-127">Las aplicaciones de WPD deben usar las capacidades del dispositivo portátil para determinar funcionalmente, no el valor de los **\_ \_ tipos de dispositivos de WPD** .</span><span class="sxs-lookup"><span data-stu-id="06c94-127">WPD applications must use the capabilities of the portable device to determine functionally, not the **WPD\_DEVICE\_TYPES** value.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="06c94-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="06c94-128">Requirements</span></span>



| <span data-ttu-id="06c94-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="06c94-129">Requirement</span></span> | <span data-ttu-id="06c94-130">Value</span><span class="sxs-lookup"><span data-stu-id="06c94-130">Value</span></span> |
|-------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="06c94-131">Encabezado</span><span class="sxs-lookup"><span data-stu-id="06c94-131">Header</span></span><br/> | <dl> <span data-ttu-id="06c94-132"><dt>PortableDevice. h</dt></span><span class="sxs-lookup"><span data-stu-id="06c94-132"><dt>PortableDevice.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="06c94-133">Vea también</span><span class="sxs-lookup"><span data-stu-id="06c94-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="06c94-134">**Estructuras y tipos de enumeración**</span><span class="sxs-lookup"><span data-stu-id="06c94-134">**Structures and Enumeration Types**</span></span>](structures-and-enumeration-types.md)
</dt> </dl>

 

 




