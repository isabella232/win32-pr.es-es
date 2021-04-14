---
description: La \_ propiedad GUID de PKEY AudioEndpoint \_ proporciona el identificador de dispositivo de DirectSound que corresponde al dispositivo de punto de conexión de audio.
ms.assetid: d3119504-9b6a-47b8-b3c6-15cb329929cb
title: PKEY_AudioEndpoint_GUID (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 45405cd2350777e535b50859e77aa56755d191fc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105648169"
---
# <a name="pkey_audioendpoint_guid"></a>GUID de PKEY \_ AudioEndpoint \_

La **propiedad \_ \_ GUID de PKEY AudioEndpoint** proporciona el identificador de dispositivo de DirectSound que corresponde al dispositivo de punto de conexión de audio. El valor de propiedad es un GUID que el cliente puede proporcionar como identificador de dispositivo a la función **DirectSoundCreate** o **DIRECTSOUNDCAPTURECREATE** en la API de DirectSound. Este valor identifica de forma única el dispositivo de punto de conexión de audio en todos los dispositivos de punto de conexión de audio del sistema. Para obtener más información acerca de DirectSound, consulte la documentación del SDK de DirectX.

El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ LPWStr.

El miembro **pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en null que contiene un GUID que identifica el dispositivo de punto de conexión de audio en DirectSound.

Como se explicó anteriormente, la [API de MMDevice](mmdevice-api.md) admite roles de [dispositivo](device-roles.md). Aunque DirectSound no admite directamente roles de dispositivo, un cliente de DirectSound puede usar la \_ propiedad GUID de PKEY AudioEndpoint \_ para seleccionar un dispositivo de representación o captura de DirectSound en función de su rol de dispositivo.

Por ejemplo, una aplicación DirectSound realiza los pasos siguientes para crear un dispositivo DirectSound que se corresponda con el dispositivo de punto de conexión de representación al que el usuario ha asignado el rol eMultimedia:

1.  Llame al método [**IMMDeviceEnumerator:: GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obtener la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo de punto de conexión de representación que tiene el rol eMultimedia.
2.  Llame al método [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) para obtener la interfaz **IPropertyStore** del dispositivo eMultimedia. Para obtener más información sobre **IPropertyStore**, consulte la documentación de Windows SDK.
3.  Llame al método **IPropertyStore:: GetValue** para obtener el valor de la \_ propiedad GUID de PKEY AudioEndpoint \_ .
4.  Convierta el valor de propiedad de un GUID en formato de cadena en una estructura GUID de 16 bytes.
5.  Llame a la función **DirectSoundCreate** con el GUID para crear el dispositivo con el rol eMultimedia.

> [!Note]  
> **PKEY \_ El \_ GUID de AudioEndpoint** es una propiedad de solo lectura independientemente del modo de acceso al almacenamiento solicitado por la aplicación en [**IMMDevice:: OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore). Si una aplicación intenta establecer un valor mediante **IPropertyStore:: SetValue**, se produce un error en esta llamada con el \_ código de error E ACCESSDENIED.

 

Tenga en cuenta que el GUID de 16 bytes generado en el paso 4 coincide con el GUID del dispositivo que identifica el dispositivo durante la enumeración de dispositivos DirectSound. La función **DirectSoundEnumerate** enumera los dispositivos de punto de conexión de representación y la función **DirectSoundCaptureEnumerate** enumera los dispositivos de punto de conexión de captura. En cualquier caso, el GUID del dispositivo es el primer parámetro que se pasa a la función de devolución de llamada de enumeración. Para obtener más información acerca de la enumeración de DirectSound, consulte la documentación del SDK de DirectX.

Para ver un ejemplo de código que usa \_ la \_ propiedad GUID de PKEY AudioEndpoint, consulte [roles de dispositivo para aplicaciones DirectSound](device-roles-for-directsound-applications.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                           |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de punto de conexión de audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propiedades de audio principales](core-audio-properties.md)
</dt> </dl>

 

 




