---
description: La \_ propiedad PKEY AudioEndpoint \_ Disable \_ SysFx especifica si los efectos del sistema están habilitados en la secuencia de modo compartido que fluye hacia o desde el dispositivo de punto de conexión de audio.
ms.assetid: 9e73e9b6-1864-49cb-adf8-233cc1f9bfe5
title: PKEY_AudioEndpoint_Disable_SysFx (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61a5486222c1c22158c70864b2b9bb0c4c31b5e1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104153342"
---
# <a name="pkey_audioendpoint_disable_sysfx"></a>PKEY \_ AudioEndpoint \_ deshabilitar \_ SysFx

La propiedad **PKEY \_ AudioEndpoint \_ Disable \_ SysFx** especifica si los efectos del sistema están habilitados en la secuencia de modo compartido que fluye hacia o desde el dispositivo de punto de conexión de audio.

Los efectos del sistema se implementan como objetos de procesamiento de audio (APOs) que se pueden insertar en una secuencia de audio. APOs son módulos de software que realizan funciones de procesamiento de audio como el control de volumen y la conversión de formato. Deshabilitar los efectos del sistema para un dispositivo de extremo permite que el flujo asociado pase a través de APOs sin modificar.

Para obtener más información acerca de los efectos del sistema en Windows Vista, consulte las notas del producto titulada "efectos de audio personalizados en Windows Vista" y "reutilización de los efectos del sistema de audio de Windows Vista" en el sitio Web [de tecnologías de dispositivos de audio para Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .

Esta propiedad sólo se aplica a los efectos locales y a los efectos globales APOs que instalaron el archivo. inf que instaló el adaptador de audio al que está conectado el dispositivo de extremo. Además, esta propiedad solo afecta al dispositivo de extremo de destino: no tiene ningún efecto en los efectos del sistema para otros dispositivos de extremo, aunque se conecten al mismo adaptador.

El miembro **VT** de la estructura **PROPVARIANT** se establece en **VT \_ UI4**.

El miembro **ulVal** de la estructura **PROPVARIANT** se establece en el **extremo \_ SYSFX \_ habilitado** si se habilitan los efectos del sistema o en el **extremo \_ SYSFX \_ deshabilitado** si están deshabilitados.

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

 

 




