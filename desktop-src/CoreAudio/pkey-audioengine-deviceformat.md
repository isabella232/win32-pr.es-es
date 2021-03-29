---
description: La propiedad PKEY de \_ Audioengine \_ DeviceFormat especifica el formato del dispositivo, que es el formato que el usuario ha seleccionado para la secuencia que fluye entre el motor de audio y el dispositivo de punto de conexión de audio cuando el dispositivo funciona en modo compartido.
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: PKEY_AudioEngine_DeviceFormat (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebb80fefd59fbc4067ce4a075d27b88de3d96c1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103807826"
---
# <a name="pkey_audioengine_deviceformat"></a>PKEY \_ Audioengine \_ DeviceFormat

La propiedad **PKEY de \_ Audioengine \_ DeviceFormat** especifica el formato del dispositivo, que es el formato que el usuario ha seleccionado para la secuencia que fluye entre el motor de audio y el dispositivo de punto de conexión de audio cuando el dispositivo funciona en modo compartido. Es posible que este formato no sea el mejor formato predeterminado para que lo use una aplicación en modo exclusivo. Normalmente, una aplicación de modo exclusivo busca un formato de dispositivo adecuado realizando un número de llamadas al método [**IAudioClient:: IsFormatSupported**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) . Para obtener más información, vea [formatos de dispositivo](device-formats.md).

El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ BLOB.

El miembro **BLOB** de la estructura **PROPVARIANT** es una estructura de tipo **BLOB** que contiene dos miembros. Member **BLOB. cbSize** es un **valor DWORD** que especifica el número de bytes en la descripción de formato. Member **BLOB. pBlobData** apunta a una estructura **WAVEFORMATEX** que contiene la descripción del formato. Para obtener más información sobre **BLOB**, consulte la documentación de Windows SDK. Para obtener más información acerca de **WAVEFORMATEX**, consulte la documentación de DDK de Windows.

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

 

 




