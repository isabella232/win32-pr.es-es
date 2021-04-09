---
description: La \_ \_ propiedad JackSubType de AUDIOENDPOINT de PKEY contiene un GUID de categoría de salida para un dispositivo de punto de conexión de audio.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3546c9741dcfd6065372f0a88a3ce3a921daad8d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153406"
---
# <a name="pkey_audioendpoint_jacksubtype"></a>PKEY \_ AudioEndpoint \_ JackSubType

La **propiedad \_ \_ JackSubType de AudioEndpoint de PKEY** contiene un GUID de categoría de salida para un dispositivo de punto de conexión de audio. El archivo de encabezado Ksmedia. h define los GUID; cada GUID especifica el tipo de conexión. Estos GUID también tienen categorías de PIN asociadas. Por ejemplo, el archivo de encabezado Ksmedia. h define **la \_ \_ interfaz GUID KSNODETYPE DisplayPort** para un puerto de pantalla que se conecta con el PIN de KS definido por el GUID **PINNAME \_ DisplayPort \_ out**.

Para obtener más información, consulte la descripción de las propiedades de la categoría PIN en la documentación de Windows DDK.

El miembro **VT** de la estructura **PROPVARIANT** se establece en **VT \_ LPWStr**.

El miembro **pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en null que contiene un GUID de categoría.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de punto de conexión de audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propiedades de audio principales](core-audio-properties.md)
</dt> </dl>

 

 




