---
description: La propiedad PKEY AudioEndpoint Disable SysFx especifica si los efectos del sistema están habilitados en la secuencia en modo compartido que fluye hacia o desde el dispositivo de punto de \_ \_ conexión de \_ audio.
ms.assetid: 9e73e9b6-1864-49cb-adf8-233cc1f9bfe5
title: PKEY_AudioEndpoint_Disable_SysFx (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a5486222c1c22158c70864b2b9bb0c4c31b5e1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164929"
---
# <a name="pkey_audioendpoint_disable_sysfx"></a>PKEY \_ AudioEndpoint \_ Deshabilitar \_ SysFx

La **propiedad PKEY \_ AudioEndpoint \_ Disable \_ SysFx** especifica si los efectos del sistema están habilitados en la secuencia en modo compartido que fluye hacia o desde el dispositivo de punto de conexión de audio.

Los efectos del sistema se implementan como objetos de procesamiento de audio (APO) que se pueden insertar en una secuencia de audio. Las API son módulos de software que realizan funciones de procesamiento de audio, como el control de volumen y la conversión de formato. Deshabilitar los efectos del sistema para un dispositivo de punto de conexión permite que la secuencia asociada pase a través de las API sin modificar.

Para obtener más información sobre los efectos del sistema en Windows Vista, vea las white papers tituladas "Custom Audio Effects in Windows Vista" (Efectos de audio personalizados en Windows Vista) y "Reusing Windows Vista Audio System Effects" (Volver a Windows Vista Audio System Effects) en el sitio web tecnologías de dispositivos de [audio para Windows.](https://www.microsoft.com/whdc/device/audio/default.mspx)

Esta propiedad solo se aplica a las API de efectos locales y globales instaladas por el archivo .inf que instaló el adaptador de audio al que está conectado el dispositivo de punto de conexión. Además, esta propiedad solo afecta al dispositivo de punto de conexión de destino: no tiene ningún efecto en los efectos del sistema para otros dispositivos de punto de conexión, incluso si se conectan al mismo adaptador.

El **miembro vt** de la estructura **PROPVARIANT** se establece en **VT \_ UI4.**

El **miembro ulVal** de la estructura **PROPVARIANT** se establece en **ENDPOINT \_ SYSFX \_ ENABLED** si los efectos del sistema están habilitados o en **ENDPOINT \_ SYSFX \_ DISABLED** si están deshabilitados.

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

 

 




