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
# <a name="video-wia-device-property-constants"></a>Constantes de propiedad de dispositivo WIA de vídeo

El controlador de vídeo estándar de adquisición de imágenes de Windows (WIA) (wiavusd.dll) admite las siguientes propiedades para la transmisión por secuencias de dispositivos de vídeo.

> [!Note]  
> WIA no admite dispositivos de vídeo en Windows Server 2003, Windows Vista o posterior. En el caso de las versiones de Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) para adquirir imágenes del vídeo.

 

El prefijo "WIA \_ DPV \_ " indica una propiedad de dispositivo para los dispositivos de vídeo y es la Convención de nomenclatura que se usa en C/C++. Con fines de scripting, estas constantes usan el prefijo "Device" y forman parte del tipo enumerado [WiaItemPropertyId](-wia-wiaitempropertyid.md) . El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis al lado del nombre de la constante de C/C++ en la lista siguiente.



| Constante o valor                                                                                                                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <dt>**WIA \_ DPV \_ última \_ imagen \_ tomada**</dt> <dt>VideoDeviceLastPictureTaken</dt> </dl> | Esta propiedad se utiliza para notificar al controlador WIA que se ha agregado una nueva imagen. Las aplicaciones deben establecer el valor de esta propiedad en el nombre del archivo de imagen creado como resultado de una llamada correcta al método [**IWiaVideo:: TakePicture**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) . <br/> Tipo: VT \_ BSTR, acceso: lectura/escritura<br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <dt>**WIA \_ \_ \_ Directorio DPV images**</dt> <dt>VideoDeviceImagesDirectory</dt> </dl>         | Esta propiedad se expone mediante el controlador de modo de usuario de vídeo WIA estándar (wiavusd.dll). El valor de esta propiedad es la ruta de acceso completa del directorio donde el controlador de vídeo WIA coloca las imágenes de forma predeterminada. Las aplicaciones deben establecer la propiedad [**IWiaVideo:: ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) en este valor. <br/> Tipo: VT \_ BSTR, acceso: solo lectura<br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <dt>**WIA \_ \_Ruta de \_ \_ acceso del dispositivo DPV DSHOW**</dt> <dt>VideoDeviceDShowDevicePath</dt> </dl>     | Ruta de acceso completa del dispositivo DirectShow. <br/> Tipo: VT \_ BSTR, acceso: solo lectura<br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <dt>**WIA \_ FileDeviceMountPoint \_ de \_ punto de montaje de DPF**</dt> <dt></dt> </dl>                              | Sin implementar. <br/> Type: **VT \_ I4**, Access: Read Only, valores válidos: [WIA \_ prop \_ None](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, solo para aplicaciones de escritorio de Windows XP \[\]<br/>              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2003 \[\]<br/>                                |
| Encabezado<br/>                   | <dl> <dt>Wiadef. h</dt> </dl> |



 

 
