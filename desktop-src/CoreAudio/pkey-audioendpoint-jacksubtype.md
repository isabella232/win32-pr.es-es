---
description: La propiedad PKEY \_ AudioEndpoint \_ JackSubType contiene un GUID de categoría de salida para un dispositivo de punto de conexión de audio.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a95ca24d48a35299144f36d052ceea2e2d0d12c56fbc03b58a993fd95772c9e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120053735"
---
# <a name="pkey_audioendpoint_jacksubtype"></a>PKEY \_ AudioEndpoint \_ JackSubType

La **propiedad PKEY \_ AudioEndpoint \_ JackSubType** contiene un GUID de categoría de salida para un dispositivo de punto de conexión de audio. El archivo de encabezado Ksmedia.h define los GUID; cada GUID especifica el tipo de conexión. Estos GUID también tienen categorías de pin asociadas. Por ejemplo, el archivo de encabezado Ksmedia.h define el GUID **KSNODETYPE \_ DISPLAYPORT \_ INTERFACE** para un puerto de presentación que se conecta con el pin KS definido por el GUID **PINNAME \_ DISPLAYPORT \_ OUT**.

Para obtener más información, consulte la descripción de las propiedades de la categoría de anclar en Windows documentación de DDK.

El **miembro vt** de la estructura **PROPVARIANT** se establece en **VT \_ LPWSTR**.

El **miembro pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en NULL que contiene un GUID de categoría.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades del punto de conexión de audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propiedades de audio principal](core-audio-properties.md)
</dt> </dl>

 

 




