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
# <a name="wpd_device_types-enumeration"></a>\_Enumeración de tipos de dispositivos de WPD \_

El tipo de enumeración de **\_ \_ tipos de dispositivo WPD** describe los distintos tipos de dispositivos portátiles (WPD) de Windows que se usan normalmente para determinar la clasificación básica y el aspecto visual de un dispositivo portátil.

## <a name="syntax"></a>Sintaxis


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



## <a name="constants"></a>Constantes

<dl> <dt>

<span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**tipo de dispositivo de WPD \_ \_ \_ genérico**
</dt> <dd>

Un WPD genérico que incluye dispositivos multifunción que no se encuentran en uno de los otros valores de enumeración de [**\_ \_ tipos de dispositivos de WPD**](wpd-device-types.md) .

</dd> <dt>

<span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**\_cámara de \_ tipo de dispositivo de WPD \_**
</dt> <dd>

Un dispositivo de cámara, como una cámara digital fija.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**\_reproductor de \_ media del tipo de dispositivo WPD \_ \_**
</dt> <dd>

Un dispositivo del reproductor de media que admita la reproducción de audio, vídeo o visualización de imágenes, como un reproductor de música portátil o Portable Media Center. No todas estas funciones se clasifican como un reproductor de \_ media del tipo de dispositivo WPD \_ \_ \_ . Por ejemplo, los dispositivos portátiles de reproducción de música se clasifican como el \_ tipo de dispositivo WPD \_ reproductor de \_ media \_ .

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**tipo de dispositivo de WPD \_ \_ \_ teléfono**
</dt> <dd>

Un dispositivo telefónico, como un teléfono móvil.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**\_vídeo de \_ tipo de dispositivo WPD \_**
</dt> <dd>

Un dispositivo de vídeo.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**\_Administrador de \_ \_ información personal \_ del tipo de dispositivo WPD \_**
</dt> <dd>

Un dispositivo del administrador de información personal.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**\_tipo de dispositivo WPD \_ \_ \_ grabadora de audio**
</dt> <dd>

Un dispositivo de grabadora de audio.

</dd> </dl>

## <a name="remarks"></a>Observaciones

**WPD \_ Los \_ tipos de dispositivos** se leen mediante la interfaz [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) . Las aplicaciones de WPD pueden utilizar estos valores para determinar el aspecto visual genérico del dispositivo. Es decir, se muestra una imagen de cámara para dispositivos similares a la cámara, se muestra una imagen de teléfono móvil para dispositivos similares, etc.

> [!Note]  
> Las aplicaciones de WPD deben usar las capacidades del dispositivo portátil para determinar funcionalmente, no el valor de los **\_ \_ tipos de dispositivos de WPD** .

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




