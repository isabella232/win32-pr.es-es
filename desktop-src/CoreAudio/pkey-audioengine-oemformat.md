---
description: La propiedad PKEY de \_ Audioengine de \_ OEMFormat especifica el formato predeterminado del dispositivo que se usa para representar o capturar un flujo. El OEM rellena los valores en un archivo. inf.
ms.assetid: 3a199ecf-642c-491c-a565-f0083783d180
title: PKEY_AudioEngine_OEMFormat (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be7ed65ae8a7bd717992b13dc7b5517a5725b241
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153401"
---
# <a name="pkey_audioengine_oemformat"></a>PKEY \_ Audioengine \_ OEMFormat

La propiedad PKEY de \_ Audioengine de \_ OEMFormat especifica el formato predeterminado del dispositivo que se usa para representar o capturar un flujo. El OEM rellena los valores en un archivo. inf.

El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ BLOB.

El miembro **BLOB** de la estructura **PROPVARIANT** es una estructura de tipo **BLOB** que contiene dos miembros. Member **BLOB. cbSize** es un **valor DWORD** que especifica el número de bytes en la descripción de formato. Member **BLOB. pBlobData** apunta a una estructura **WAVEFORMATEX** que contiene la descripción del formato. Para obtener más información sobre BLOB, consulte la documentación de Windows SDK. Para obtener más información acerca de **WAVEFORMATEX**, consulte la documentación de DDK de Windows.

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

 

 




