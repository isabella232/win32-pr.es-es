---
description: La propiedad PKEY \_ AudioEndpoint \_ JackSubType contiene un GUID de categoría de salida para un dispositivo de punto de conexión de audio.
ms.assetid: 5d712823-73e3-4872-a1ea-c166ed41ffa0
title: PKEY_AudioEndpoint_JackSubType (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3546c9741dcfd6065372f0a88a3ce3a921daad8d
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164910"
---
# <a name="pkey_audioendpoint_jacksubtype"></a>PKEY \_ AudioEndpoint \_ JackSubType

La **propiedad PKEY \_ AudioEndpoint \_ JackSubType** contiene un GUID de categoría de salida para un dispositivo de punto de conexión de audio. El archivo de encabezado Ksmedia.h define los GUID; cada GUID especifica el tipo de conexión. Estos GUID también tienen categorías de pin asociadas. Por ejemplo, el archivo de encabezado Ksmedia.h define el GUID **KSNODETYPE \_ DISPLAYPORT \_ INTERFACE** para un puerto de presentación que se conecta con el pin KS definido por el GUID **PINNAME \_ DISPLAYPORT \_ OUT**.

Para obtener más información, consulte la descripción de las propiedades de categoría de anclar en la Windows DDK.

El **miembro vt** de la estructura **PROPVARIANT** se establece en VT **\_ LPWSTR.**

El **miembro pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en NULL que contiene un GUID de categoría.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio solo\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades del punto de conexión de audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propiedades de audio principal](core-audio-properties.md)
</dt> </dl>

 

 




