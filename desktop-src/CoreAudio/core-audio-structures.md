---
description: Estructuras de audio principales
ms.assetid: 92585cd4-baa9-4f75-816e-b83f5badad37
title: Estructuras de audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ec8ea83d0de4c07c1a3d36bab169d5cb581e82cf60e84e308d04dff49af0dac
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118407219"
---
# <a name="core-audio-structures"></a>Estructuras de audio principales

En esta sección se describen las estructuras que usan core audio API en Windows Vista y versiones posteriores.



| Estructura                                                                     | Descripción                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATOS DE \_ NOTIFICACIÓN DE VOLUMEN DE \_ \_ AUDIO**](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | Describe un cambio en el nivel de volumen o el estado muting de un dispositivo de punto de conexión de audio.                                                                                 |
| [**PARAMS \_ DE ACTIVACIÓN DE AUDIO \_ \_ DE DIRECTX**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | Especifica los parámetros de inicialización para una secuencia de Direct Sound.                                                                                                   |
| [**KS JACK \_ DESCRIPTION**](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | Se recupera mediante [**IKsJackDescription::GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); describe un conector de audio.                                 |
| [**KS JACK \_ DESCRIPTION2**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | Se recupera mediante [**IKsJackDescription2::GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); describe un conector de audio. <br/>                 |
| [**INFORMACIÓN DEL RECEPTOR \_ KS JACK \_**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | Se recupera a [**través de IKs JackSinkInformation::Get JackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); describe un receptor de conector de audio.<br/> |
| [**LUID**](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | Almacena el identificador de puerto de vídeo.<br/>                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación](programming-reference.md)
</dt> </dl>

 

 




