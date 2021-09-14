---
description: Estructuras de audio principales
ms.assetid: 92585cd4-baa9-4f75-816e-b83f5badad37
title: Estructuras de audio principales
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 078f49ac7abce8fc2773549df26431b780550c1b
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127165078"
---
# <a name="core-audio-structures"></a>Estructuras de audio principales

En esta sección se describen las estructuras que usan las API de audio principales en Windows Vista y versiones posteriores.



| Estructura                                                                     | Descripción                                                                                                                                                         |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DATOS DE \_ NOTIFICACIÓN DE VOLUMEN DE \_ \_ AUDIO**](/windows/desktop/api/Endpointvolume/ns-endpointvolume-audio_volume_notification_data)   | Describe un cambio en el nivel de volumen o el estado muting de un dispositivo de punto de conexión de audio.                                                                                 |
| [**PARAMS \_ DE ACTIVACIÓN DE AUDIO \_ DIRECTX \_**](/windows/win32/api/mmdeviceapi/ns-mmdeviceapi-directx_audio_activation_params) | Especifica los parámetros de inicialización de una secuencia directSound.                                                                                                   |
| [**DESCRIPCIÓN DE KS \_ JACK**](/windows/win32/api/devicetopology/ns-devicetopology-ksjack_description)                             | Se recupera a [**través de IKsJackDescription::GetJackDescription**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription-getjackdescription); describe un conector de audio.                                 |
| [**KSJACK \_ DESCRIPTION2**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_description2)<br/>                | Se recupera mediante [**IKsJackDescription2::GetJackDescription2**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjackdescription2-getjackdescription2); describe un conector de audio. <br/>                 |
| [**INFORMACIÓN DEL RECEPTOR \_ KSJACK \_**](/windows/desktop/api/Devicetopology/ns-devicetopology-ksjack_sink_information)<br/>       | Se recupera a [**través de IKsJackSinkInformation::GetJackSinkInformation**](/windows/desktop/api/Devicetopology/nf-devicetopology-iksjacksinkinformation-getjacksinkinformation); describe un receptor de conector de audio.<br/> |
| [**LUID**](/windows/desktop/api/Devicetopology/ns-devicetopology-luid)<br/>                                               | Almacena el identificador de puerto de vídeo.<br/>                                                                                                                        |



 

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Referencia de programación](programming-reference.md)
</dt> </dl>

 

 




