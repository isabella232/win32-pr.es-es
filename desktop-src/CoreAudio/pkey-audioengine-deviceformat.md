---
description: La propiedad PKEY AudioEngine DeviceFormat especifica el formato del dispositivo, que es el formato que el usuario ha seleccionado para la secuencia que fluye entre el motor de audio y el dispositivo de punto de conexión de audio cuando el dispositivo funciona en modo \_ \_ compartido.
ms.assetid: eb3c734f-0bb8-47cc-a01f-99569f472cde
title: PKEY_AudioEngine_DeviceFormat (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6ebb80fefd59fbc4067ce4a075d27b88de3d96c1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164897"
---
# <a name="pkey_audioengine_deviceformat"></a>PKEY \_ AudioEngine \_ DeviceFormat

La propiedad **PKEY \_ AudioEngine \_ DeviceFormat** especifica el formato del dispositivo, que es el formato que el usuario ha seleccionado para la secuencia que fluye entre el motor de audio y el dispositivo de punto de conexión de audio cuando el dispositivo funciona en modo compartido. Es posible que este formato no sea el mejor formato predeterminado para que lo use una aplicación en modo exclusivo. Normalmente, una aplicación en modo exclusivo busca un formato de dispositivo adecuado realizando algunas llamadas al método [**IAudioClient::IsFormatSupported.**](/windows/desktop/api/Audioclient/nf-audioclient-iaudioclient-isformatsupported) Para obtener más información, vea [Formatos de dispositivo.](device-formats.md)

El **miembro vt** de la estructura **PROPVARIANT** se establece en VT \_ BLOB.

El **miembro de blob** de la estructura **PROPVARIANT** es una estructura de tipo **BLOB** que contiene dos miembros. El **miembro blob.cbSize** es **un DWORD** que especifica el número de bytes en la descripción del formato. El **miembro blob.pBlobData** apunta a una **estructura DE FORMA DEDATOX** que contiene la descripción del formato. Para obtener más información sobre **BLOB,** consulte la documentación Windows SDK. Para obtener más información sobre **LA FORMA DE ONDAATEX,** consulte la documentación Windows DDK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Encabezado<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades del punto de conexión de audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propiedades de audio principal](core-audio-properties.md)
</dt> </dl>

 

 




