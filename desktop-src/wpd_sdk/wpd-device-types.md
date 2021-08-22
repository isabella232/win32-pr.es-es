---
description: El tipo de enumeración WPD DEVICE TYPES describe los diferentes tipos de \_ Windows Portable Device (WPD) que se usan normalmente para determinar la clasificación básica y la apariencia visual de un \_ dispositivo portátil.
ms.assetid: 51714e0f-e9b7-4474-a8bb-da3875ef5399
title: WPD_DEVICE_TYPES enumeración (PortableDevice.h)
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
ms.openlocfilehash: 747c4631bc2c24a6550904e36e58a6fc02547bc010da7fa1d08b896c6c17489c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119657465"
---
# <a name="wpd_device_types-enumeration"></a>Enumeración \_ WPD DEVICE \_ TYPES

El tipo de enumeración **\_ WPD DEVICE \_ TYPES** describe los diferentes tipos de Windows Portable Device (WPD) que se usan normalmente para determinar la clasificación básica y la apariencia visual de un dispositivo portátil.

## <a name="syntax"></a>Syntax


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

<span id="WPD_DEVICE_TYPE_GENERIC"></span><span id="wpd_device_type_generic"></span>**TIPO DE DISPOSITIVO WPD \_ \_ \_ GENÉRICO**
</dt> <dd>

Un WPD genérico que incluye dispositivos multifunción que no se incluyen en uno de los otros valores de enumeración [**DE TIPOS DE DISPOSITIVO \_ \_ DE WPD.**](wpd-device-types.md)

</dd> <dt>

<span id="WPD_DEVICE_TYPE_CAMERA"></span><span id="wpd_device_type_camera"></span>**CÁMARA DE TIPO \_ \_ DE DISPOSITIVO \_ WPD**
</dt> <dd>

Un dispositivo de cámara, como una cámara digital.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_MEDIA_PLAYER"></span><span id="wpd_device_type_media_player"></span>**REPRODUCTOR MULTIMEDIA \_ DE TIPO DE DISPOSITIVO \_ \_ \_ WPD**
</dt> <dd>

Un dispositivo de reproductor multimedia que admite la reproducción de audio, vídeo o visualización de imágenes, como un reproductor de música portátil o un centro multimedia portátil. No todo esto se clasifica funcionalmente como un REPRODUCTOR MULTIMEDIA WPD \_ DEVICE \_ \_ \_ TYPE. Por ejemplo, los dispositivos portátiles del reproductor de música se clasifican como WPD \_ DEVICE \_ TYPE MEDIA \_ \_ PLAYER.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PHONE"></span><span id="wpd_device_type_phone"></span>**TELÉFONO DE \_ TIPO \_ DE DISPOSITIVO \_ WPD**
</dt> <dd>

Un dispositivo de teléfono, como un teléfono móvil.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_VIDEO"></span><span id="wpd_device_type_video"></span>**VÍDEO DE \_ TIPO \_ DE DISPOSITIVO \_ WPD**
</dt> <dd>

Un dispositivo de vídeo.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_PERSONAL_INFORMATION_MANAGER"></span><span id="wpd_device_type_personal_information_manager"></span>**ADMINISTRADOR DE \_ INFORMACIÓN PERSONAL DEL TIPO DE DISPOSITIVO \_ \_ \_ \_ WPD**
</dt> <dd>

Un dispositivo de administrador de información personal.

</dd> <dt>

<span id="WPD_DEVICE_TYPE_AUDIO_RECORDER"></span><span id="wpd_device_type_audio_recorder"></span>**GRABADORA DE \_ AUDIO DE TIPO DE DISPOSITIVO \_ \_ \_ WPD**
</dt> <dd>

Un dispositivo de grabadora de audio.

</dd> </dl>

## <a name="remarks"></a>Comentarios

**WPD \_ LOS \_ TIPOS DE** DISPOSITIVO se leen mediante la interfaz [**IPortableDeviceManager.**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager) Las aplicaciones WPD pueden usar estos valores para determinar la apariencia visual genérica del dispositivo. Es decir, se muestra una imagen de cámara para dispositivos parecidos a cámara, se muestra una imagen de teléfono móvil para dispositivos de tipo teléfono, y así sucesivamente.

> [!Note]  
> Las aplicaciones DE WPD deben usar las funciones del dispositivo portátil para determinar funcionalmente, no el valor **\_ DE WPD DEVICE \_ TYPES.**

 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------|---------------------------------------------------------------------------------------------|
| Encabezado<br/> | <dl> <dt>PortableDevice.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Estructuras y tipos de enumeración**](structures-and-enumeration-types.md)
</dt> </dl>

 

 




