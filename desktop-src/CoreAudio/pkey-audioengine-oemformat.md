---
description: La propiedad PKEY AudioEngine OEMFormat especifica el formato predeterminado del dispositivo que se usa para representar o \_ \_ capturar una secuencia. El OEM rellena los valores en un archivo .inf.
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: PKEY_AudioEngine_OEMFormat (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7ed65ae8a7bd717992b13dc7b5517a5725b241
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164894"
---
# <a name="pkey_audioengine_oemformat"></a>PKEY \_ AudioEngine \_ OEMFormat

La propiedad PKEY AudioEngine OEMFormat especifica el formato predeterminado del dispositivo que se usa para representar o \_ \_ capturar una secuencia. El OEM rellena los valores en un archivo .inf.

El **miembro vt** de la estructura **PROPVARIANT** se establece en VT \_ BLOB.

El **miembro blob** de la estructura **PROPVARIANT** es una estructura de tipo **BLOB** que contiene dos miembros. El **miembro blob.cbSize** es **un DWORD** que especifica el número de bytes en la descripción del formato. El **miembro blob.pBlobData** apunta a una estructura **DE FORMADETEATEX** que contiene la descripción del formato. Para más información sobre BLOB, consulte la documentación Windows SDK. Para obtener más información acerca **de LAATEX,** consulte la documentación Windows DDK.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**Propiedades del punto de conexión de audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propiedades de audio principal](core-audio-properties.md)
</dt> </dl>

 

 




