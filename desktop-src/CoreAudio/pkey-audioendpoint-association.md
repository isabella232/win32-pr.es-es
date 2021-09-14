---
description: La propiedad PKEY AudioEndpoint Association asocia una categoría \_ \_ de pin de kernel-streaming (KS) a un dispositivo de punto de conexión de audio.
ms.assetid: a20e082c-eddb-4b81-b851-49350b87e69a
title: PKEY_AudioEndpoint_Association (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe2a7ec4f979e12dd6b548d27e0112c784105074
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164937"
---
# <a name="pkey_audioendpoint_association"></a>PKEY \_ AudioEndpoint \_ Association

La **propiedad PKEY \_ AudioEndpoint \_ Association** asocia una categoría de pin de kernel-streaming (KS) a un dispositivo de punto de conexión de audio. El archivo .inf que instala un adaptador de audio asigna una categoría de pin a cada pin KS del adaptador. Un pin KS en un dispositivo adaptador representa el punto en el que una secuencia de audio entra o sale del dispositivo. Una categoría de pin es un GUID que especifica el tipo de función que realiza un pin de KS. Por ejemplo, el archivo de encabezado Ksmedia.h define el GUID de categoría de pin KSNODETYPE MICROPHONE para indicar un pin KS que se conecta a un micrófono, y \_ KSNODETYPE ESTABILLAS para indicar un pin KS que se conecta a los \_ auriculares. Para obtener más información, consulte la descripción de las propiedades de categoría de anclar en Windows documentación de DDK.

El **miembro vt** de la estructura **PROPVARIANT** se establece en VT \_ LPWSTR.

El **miembro pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en NULL que contiene un GUID de categoría de pin de KS.

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

 

 




