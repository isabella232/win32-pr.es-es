---
description: El controlador de vídeo estándar de adquisición de imágenes de Windows (WIA) (wiavusd.dll) admite las siguientes propiedades para la transmisión por secuencias de dispositivos de vídeo.
ms.assetid: 24fa7e02-c409-49ec-b1a9-309f7c95e292
title: Constantes de propiedad de dispositivo WIA de vídeo (Wiadef. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WIA_DPV_LAST_PICTURE_TAKEN
- WIA_DPV_IMAGES_DIRECTORY
- WIA_DPV_DSHOW_DEVICE_PATH
- WIA_DPF_MOUNT_POINT
api_type:
- HeaderDef
api_location:
- wiadef.h
ms.openlocfilehash: f02991cb5c2b8cc15eb89e335ef1e46442c89510
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104154375"
---
# <a name="video-wia-device-property-constants"></a><span data-ttu-id="11877-103">Constantes de propiedad de dispositivo WIA de vídeo</span><span class="sxs-lookup"><span data-stu-id="11877-103">Video WIA Device Property Constants</span></span>

<span data-ttu-id="11877-104">El controlador de vídeo estándar de adquisición de imágenes de Windows (WIA) (wiavusd.dll) admite las siguientes propiedades para la transmisión por secuencias de dispositivos de vídeo.</span><span class="sxs-lookup"><span data-stu-id="11877-104">The standard Windows Image Acquisition (WIA) video driver (wiavusd.dll) supports the following properties for streaming video devices.</span></span>

> [!Note]  
> <span data-ttu-id="11877-105">WIA no admite dispositivos de vídeo en Windows Server 2003, Windows Vista o posterior.</span><span class="sxs-lookup"><span data-stu-id="11877-105">WIA does not support video devices in Windows Server 2003, Windows Vista, or later.</span></span> <span data-ttu-id="11877-106">En el caso de las versiones de Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) para adquirir imágenes del vídeo.</span><span class="sxs-lookup"><span data-stu-id="11877-106">For those versions of the Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) to acquire images from video.</span></span>

 

<span data-ttu-id="11877-107">El prefijo "WIA \_ DPV \_ " indica una propiedad de dispositivo para los dispositivos de vídeo y es la Convención de nomenclatura que se usa en C/C++.</span><span class="sxs-lookup"><span data-stu-id="11877-107">The prefix "WIA\_DPV\_" indicates a Device Property for Video devices and is the naming convention used in C/C++.</span></span> <span data-ttu-id="11877-108">Con fines de scripting, estas constantes usan el prefijo "Device" y forman parte del tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) .</span><span class="sxs-lookup"><span data-stu-id="11877-108">For scripting purposes these constants use the prefix "VideoDevice" and are part of the [WiaItemPropertyId](-wia-wiaitempropertyid.md) enumerated type.</span></span> <span data-ttu-id="11877-109">El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis al lado del nombre de la constante de C/C++ en la lista siguiente.</span><span class="sxs-lookup"><span data-stu-id="11877-109">The corresponding member name from that script enumeration appears in parentheses next to the C/C++ constant name in the following list.</span></span>



| <span data-ttu-id="11877-110">Constante o valor</span><span class="sxs-lookup"><span data-stu-id="11877-110">Constant/value</span></span>                                                                                                                                                                                                                                                                           | <span data-ttu-id="11877-111">Descripción</span><span class="sxs-lookup"><span data-stu-id="11877-111">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <span data-ttu-id="11877-112"><dt>**WIA \_ DPV \_ última \_ imagen \_ tomada**</dt> <dt>VideoDeviceLastPictureTaken</dt></span><span class="sxs-lookup"><span data-stu-id="11877-112"><dt>**WIA\_DPV\_LAST\_PICTURE\_TAKEN**</dt> <dt>VideoDeviceLastPictureTaken</dt></span></span> </dl> | <span data-ttu-id="11877-113">Esta propiedad se utiliza para notificar al controlador WIA que se ha agregado una nueva imagen.</span><span class="sxs-lookup"><span data-stu-id="11877-113">This property is used to notify the WIA driver that a new image has been added.</span></span> <span data-ttu-id="11877-114">Las aplicaciones deben establecer el valor de esta propiedad en el nombre del archivo de imagen creado como resultado de una llamada correcta al método [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) .</span><span class="sxs-lookup"><span data-stu-id="11877-114">Applications should set the value of this property to the name of the image file created as the result of a successful call to the [**IWiaVideo::TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) method.</span></span> <br/> <span data-ttu-id="11877-115">Tipo: VT \_ BSTR, acceso: lectura/escritura</span><span class="sxs-lookup"><span data-stu-id="11877-115">Type: VT\_BSTR, Access: Read/Write</span></span><br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <span data-ttu-id="11877-116"><dt>**WIA \_ \_ \_ Directorio DPV images**</dt> <dt>VideoDeviceImagesDirectory</dt></span><span class="sxs-lookup"><span data-stu-id="11877-116"><dt>**WIA\_DPV\_IMAGES\_DIRECTORY**</dt> <dt>VideoDeviceImagesDirectory</dt></span></span> </dl>         | <span data-ttu-id="11877-117">Esta propiedad se expone mediante el controlador de modo de usuario de vídeo WIA estándar (wiavusd.dll).</span><span class="sxs-lookup"><span data-stu-id="11877-117">This property is exposed by the standard WIA video user-mode driver (wiavusd.dll).</span></span> <span data-ttu-id="11877-118">El valor de esta propiedad es la ruta de acceso completa del directorio donde el controlador de vídeo WIA coloca las imágenes de forma predeterminada.</span><span class="sxs-lookup"><span data-stu-id="11877-118">The value of this property is the full path of the directory where the WIA video driver puts images by default.</span></span> <span data-ttu-id="11877-119">Las aplicaciones deben establecer la propiedad [**IWiaVideo:: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) en este valor.</span><span class="sxs-lookup"><span data-stu-id="11877-119">Applications should set the [**IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) property to this value.</span></span> <br/> <span data-ttu-id="11877-120">Tipo: VT \_ BSTR, acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="11877-120">Type: VT\_BSTR, Access: Read Only</span></span><br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <span data-ttu-id="11877-121"><dt>**WIA \_ \_Ruta de \_ \_ acceso del dispositivo DPV DSHOW**</dt> <dt>VideoDeviceDShowDevicePath</dt></span><span class="sxs-lookup"><span data-stu-id="11877-121"><dt>**WIA\_DPV\_DSHOW\_DEVICE\_PATH**</dt> <dt>VideoDeviceDShowDevicePath</dt></span></span> </dl>     | <span data-ttu-id="11877-122">Ruta de acceso completa del dispositivo DirectShow.</span><span class="sxs-lookup"><span data-stu-id="11877-122">The full path of the DirectShow device.</span></span> <br/> <span data-ttu-id="11877-123">Tipo: VT \_ BSTR, acceso: solo lectura</span><span class="sxs-lookup"><span data-stu-id="11877-123">Type: VT\_BSTR, Access: Read Only</span></span><br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <span data-ttu-id="11877-124"><dt>**WIA \_ FileDeviceMountPoint \_ de \_ punto de montaje de DPF**</dt> <dt></dt></span><span class="sxs-lookup"><span data-stu-id="11877-124"><dt>**WIA\_DPF\_MOUNT\_POINT**</dt> <dt>FileDeviceMountPoint</dt></span></span> </dl>                              | <span data-ttu-id="11877-125">Sin implementar.</span><span class="sxs-lookup"><span data-stu-id="11877-125">Not implemented.</span></span> <br/> <span data-ttu-id="11877-126">Type: **VT \_ I4**, Access: Read Only, valores válidos: [WIA \_ prop \_ None](-wia-property-attributes.md)</span><span class="sxs-lookup"><span data-stu-id="11877-126">Type: **VT\_I4**, Access: Read Only, Valid values: [WIA\_PROP\_NONE](-wia-property-attributes.md)</span></span><br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a><span data-ttu-id="11877-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11877-127">Requirements</span></span>



| <span data-ttu-id="11877-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="11877-128">Requirement</span></span> | <span data-ttu-id="11877-129">Value</span><span class="sxs-lookup"><span data-stu-id="11877-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="11877-130">Cliente mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11877-130">Minimum supported client</span></span><br/> | <span data-ttu-id="11877-131">Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]</span><span class="sxs-lookup"><span data-stu-id="11877-131">Windows 2000 Professional, Windows XP \[desktop apps only\]</span></span><br/>              |
| <span data-ttu-id="11877-132">Servidor mínimo compatible</span><span class="sxs-lookup"><span data-stu-id="11877-132">Minimum supported server</span></span><br/> | <span data-ttu-id="11877-133">Solo aplicaciones de escritorio de Windows Server 2003 \[\]</span><span class="sxs-lookup"><span data-stu-id="11877-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="11877-134">Encabezado</span><span class="sxs-lookup"><span data-stu-id="11877-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="11877-135"><dt>Wiadef. h</dt></span><span class="sxs-lookup"><span data-stu-id="11877-135"><dt>Wiadef.h</dt></span></span> </dl> |



 

 
