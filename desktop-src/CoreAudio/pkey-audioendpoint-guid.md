---
description: La propiedad PKEY AudioEndpoint GUID proporciona el identificador de dispositivo \_ \_ DirectSound que corresponde al dispositivo de punto de conexión de audio.
ms.assetid: d3119504-9b6a-47b8-b3c6-15cb329929cb
title: PKEY_AudioEndpoint_GUID (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 357531a76316381e9ae39f867a5b6cfa0a055a04f41b0cba5fab95fcccbcc7fb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120104365"
---
# <a name="pkey_audioendpoint_guid"></a>PKEY \_ AudioEndpoint \_ GUID

La **propiedad PKEY \_ AudioEndpoint \_ GUID** proporciona el identificador de dispositivo DirectSound que corresponde al dispositivo de punto de conexión de audio. El valor de propiedad es un GUID que el cliente puede proporcionar como identificador de dispositivo a la función **DirectSoundCreate** o **DirectSoundCaptureCreate** en DirectSound API. Este valor identifica de forma única el dispositivo de punto de conexión de audio en todos los dispositivos de punto de conexión de audio del sistema. Para más información sobre DirectSound, consulte la documentación del SDK de DirectX.

El **miembro vt** de la estructura **PROPVARIANT** se establece en VT \_ LPWSTR.

El **miembro pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en NULL que contiene un GUID que identifica el dispositivo de punto de conexión de audio en DirectSound.

Como se explicó anteriormente, [MMDevice API admite roles](mmdevice-api.md) [de dispositivo](device-roles.md). Aunque DirectSound no admite directamente roles de dispositivo, un cliente de DirectSound puede usar la propiedad GUID audioEndpoint PKEY para seleccionar un dispositivo de representación o captura de DirectSound en función de su rol \_ \_ de dispositivo.

Por ejemplo, una aplicación DirectSound realiza los pasos siguientes para crear un dispositivo DirectSound que se corresponda con el dispositivo de punto de conexión de representación al que el usuario ha asignado el rol eMultimedia:

1.  Llame al [**método IMMDeviceEnumerator::GetDefaultAudioEndpoint**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdeviceenumerator-getdefaultaudioendpoint) para obtener la interfaz [**IMMDevice**](/windows/desktop/api/Mmdeviceapi/nn-mmdeviceapi-immdevice) del dispositivo de punto de conexión de representación que tiene el rol eMultimedia.
2.  Llame al [**método IMMDevice::OpenPropertyStore**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) para obtener la **interfaz IPropertyStore** del dispositivo eMultimedia. Para obtener más información sobre **IPropertyStore,** consulte la documentación Windows SDK.
3.  Llame al **método IPropertyStore::GetValue** para obtener el valor de la propiedad \_ GUID audioEndpoint de \_ PKEY.
4.  Convierta el valor de propiedad de un GUID en formato de cadena en una estructura GUID de 16 bytes.
5.  Llame a **la función DirectSoundCreate** con el GUID para crear el dispositivo con el rol eMultimedia.

> [!Note]  
> **PKEY \_ El \_ GUID de AudioEndpoint** es una propiedad de solo lectura independientemente del modo de acceso de almacenamiento solicitado por la aplicación en [**IMMDevice::OpenPropertyStore.**](/windows/desktop/api/Mmdeviceapi/nf-mmdeviceapi-immdevice-openpropertystore) Si una aplicación intenta establecer un valor mediante **IPropertyStore::SetValue**, se produce un error en esta llamada con el código de \_ error E ACCESSDENIED.

 

Tenga en cuenta que el GUID de 16 bytes generado en el paso 4 coincide con el GUID del dispositivo que identifica el dispositivo durante la enumeración del dispositivo DirectSound. La **función DirectSoundEnumerate** enumera los dispositivos de punto de conexión de representación y la función **DirectSoundCaptureEnumerate** enumera los dispositivos de punto de conexión de captura. En cualquier caso, el GUID del dispositivo es el primer parámetro pasado a la función de devolución de llamada de enumeración. Para más información sobre la enumeración DirectSound, consulte la documentación del SDK de DirectX.

Para obtener un ejemplo de código que usa la propiedad PKEY AudioEndpoint GUID, vea Roles de dispositivo \_ \_ para aplicaciones [DirectSound.](device-roles-for-directsound-applications.md)

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades del punto de conexión de audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propiedades de audio principal](core-audio-properties.md)
</dt> </dl>

 

 




