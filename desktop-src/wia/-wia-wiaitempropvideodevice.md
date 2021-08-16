---
description: El controlador Windows de vídeo de adquisición de imágenes estándar (WIA) (wiavusd.dll) admite las siguientes propiedades para los dispositivos de streaming de vídeo.
ms.assetid: 24fa7e02-c409-49ec-b1a9-309f7c95e292
title: Constantes de propiedad de dispositivo WIA de vídeo (Wiadef.h)
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
ms.openlocfilehash: 9652ac72d6e73a9c44d2f4b299823dad9cc566bb1c7c0129af497ea213a6e5d8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118207373"
---
# <a name="video-wia-device-property-constants"></a>Constantes de propiedad de dispositivo WIA de vídeo

El controlador Windows de vídeo de adquisición de imágenes estándar (WIA) (wiavusd.dll) admite las siguientes propiedades para los dispositivos de streaming de vídeo.

> [!Note]  
> WIA no admite dispositivos de vídeo en Windows Server 2003, Windows Vista o versiones posteriores. Para esas versiones de la Windows, use [DirectShow](/previous-versions//ms783323(v=vs.85)) para adquirir imágenes de vídeo.

 

El prefijo "WIA DPV" indica una propiedad de dispositivo para dispositivos de vídeo y es la convención de nomenclatura usada \_ \_ en C/C++. Con fines de scripting, estas constantes usan el prefijo "VideoDevice" y forman parte del tipo enumerado [WiaItemPropertyId.](-wia-wiaitempropertyid.md) El nombre de miembro correspondiente de esa enumeración de script aparece entre paréntesis junto al nombre de constante de C/C++ en la lista siguiente.



| Constante o valor                                                                                                                                                                                                                                                                           | Descripción                                                                                                                                                                                                                                                                                                                                                                          |
|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WIA_DPV_LAST_PICTURE_TAKEN"></span><span id="wia_dpv_last_picture_taken"></span><dl> <dt>**WIA \_ Vídeo de \_ última \_ imagen \_ de DPVDeviceLastPictureTaken**</dt> <dt></dt> </dl> | Esta propiedad se usa para notificar al controlador WIA que se ha agregado una nueva imagen. Las aplicaciones deben establecer el valor de esta propiedad en el nombre del archivo de imagen creado como resultado de una llamada correcta al método [**IWiaVideo::TakePicture.**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-takepicture) <br/> Tipo: VT \_ BSTR, acceso: lectura y escritura<br/>                                    |
| <span id="WIA_DPV_IMAGES_DIRECTORY"></span><span id="wia_dpv_images_directory"></span><dl> <dt>**WIA \_ DPV \_ IMAGES \_ DIRECTORY**</dt> <dt>VideoDeviceImagesDirectory</dt> </dl>         | Esta propiedad se expone mediante el controlador de modo de usuario de vídeo WIA estándar (wiavusd.dll). El valor de esta propiedad es la ruta de acceso completa del directorio donde el controlador de vídeo WIA coloca imágenes de forma predeterminada. Las aplicaciones deben establecer [**la propiedad IWiaVideo::ImagesDirectory**](/windows/desktop/api/Wiavideo/nf-wiavideo-iwiavideo-get_imagesdirectory) en este valor. <br/> Tipo: VT \_ BSTR, acceso: solo lectura<br/> |
| <span id="WIA_DPV_DSHOW_DEVICE_PATH"></span><span id="wia_dpv_dshow_device_path"></span><dl> <dt>**WIA \_ DPV \_ DSHOW \_ DEVICE \_ PATH**</dt> <dt>VideoDeviceDShowDevicePath</dt> </dl>     | Ruta de acceso completa del DirectShow dispositivo. <br/> Tipo: VT \_ BSTR, acceso: solo lectura<br/>                                                                                                                                                                                                                                                                                     |
| <span id="WIA_DPF_MOUNT_POINT"></span><span id="wia_dpf_mount_point"></span><dl> <dt>**WIA \_ DPF \_ MOUNT \_ POINT FileDeviceMountPoint**</dt> <dt></dt> </dl>                              | Sin implementar. <br/> Tipo: **VT \_ I4,** acceso: solo lectura, valores válidos: [WIA PROP \_ \_ NONE](-wia-property-attributes.md)<br/>                                                                                                                                                                                                                                           |



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 2000 Professional, Windows aplicaciones de escritorio XP \[\]<br/>              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2003 \[\]<br/>                                |
| Header<br/>                   | <dl> <dt>Wiadef.h</dt> </dl> |



 

 
