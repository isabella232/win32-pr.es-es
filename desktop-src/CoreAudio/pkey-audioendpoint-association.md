---
description: La propiedad PKEY \_ AudioEndpoint Association asocia una categoría de pin de \_ kernel-streaming (KS) con un dispositivo de punto de conexión de audio.
ms.assetid: a20e082c-eddb-4b81-b851-49350b87e69a
title: PKEY_AudioEndpoint_Association (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35f7130ac82341b2da25356158d656051934b77f6006c35c1e812a4779a2e6e5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119698675"
---
# <a name="pkey_audioendpoint_association"></a>PKEY \_ AudioEndpoint \_ Association

La **propiedad PKEY \_ AudioEndpoint \_ Association** asocia una categoría de pin de kernel-streaming (KS) con un dispositivo de punto de conexión de audio. El archivo .inf que instala un adaptador de audio asigna una categoría de pin a cada pin KS del adaptador. Una marca KS en un dispositivo adaptador representa el punto en el que una secuencia de audio entra o sale del dispositivo. Una categoría de pin es un GUID que especifica el tipo de función que realiza un pin de KS. Por ejemplo, el archivo de encabezado Ksmedia.h define el GUID de categoría de pin KSNODETYPE MICROPHONE para indicar un pin KS que se conecta a un micrófono, y \_ KSNODETYPE LODOS PARA indicar un pin KS que se conecta a los \_ micrófonos. Para obtener más información, consulte la descripción de las propiedades de categoría de anclar en la documentación Windows DDK.

El **miembro vt** de la estructura **PROPVARIANT** se establece en VT \_ LPWSTR.

El **miembro pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en NULL que contiene un GUID de categoría de pin de KS.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 




