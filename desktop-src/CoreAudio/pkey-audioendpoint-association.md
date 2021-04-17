---
description: La \_ propiedad de asociación PKEY AudioEndpoint \_ asocia una categoría de PIN de streaming de kernel (KS) con un dispositivo de punto de conexión de audio.
ms.assetid: a20e082c-eddb-4b81-b851-49350b87e69a
title: PKEY_AudioEndpoint_Association (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe2a7ec4f979e12dd6b548d27e0112c784105074
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "105659735"
---
# <a name="pkey_audioendpoint_association"></a>Asociación de PKEY \_ AudioEndpoint \_

La propiedad de **\_ \_ Asociación PKEY AudioEndpoint** asocia una categoría de PIN de streaming de kernel (KS) con un dispositivo de punto de conexión de audio. El archivo. inf que instala un adaptador de audio asigna una categoría de PIN a cada pin de KS en el adaptador. Un PIN de KS en un dispositivo adaptador representa el punto en el que una secuencia de audio entra o sale del dispositivo. Una categoría de PIN es un GUID que especifica el tipo de función que realiza un PIN de KS. Por ejemplo, el archivo de encabezado Ksmedia. h define el KSNODETYPE de GUID de categoría de PIN \_ para indicar un PIN de KS que se conecta a un micrófono y KSNODETYPE \_ auriculares para indicar un PIN de KS que se conecta a los auriculares. Para obtener más información, consulte la descripción de las propiedades de la categoría PIN en la documentación de Windows DDK.

El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ LPWStr.

El miembro **pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en null que contiene un GUID de categoría PIN de KS.

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

 

 




