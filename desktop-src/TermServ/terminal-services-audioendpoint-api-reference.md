---
title: Referencia de la API de Servicios de Escritorio remoto AudioEndpoint
description: Admite interfaces para el registro de puntos de conexión de audio y el transporte de datos.
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto, referencia de la API de AudioEndpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1958b21643083a14110ddad77f68024cc464dd36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104418952"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a>Referencia de la API de Servicios de Escritorio remoto AudioEndpoint

Un *punto de conexión de audio* representa un dispositivo de audio, una API de audio o cualquier otro origen o receptor de audio, y se usa para enviar datos al motor de audio o consumir datos del mismo. Un extremo de audio debe estar conectado al motor de audio a través de una *conexión*, y cada conexión solo puede tener un extremo conectado a él. Una vez registrado un extremo, el motor de audio conecta el extremo a la conexión.

Cada objeto de extremo debe implementar las interfaces siguientes:

-   [**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) para permitir que el motor de audio obtenga información sobre el punto de conexión.
-   [**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) para obtener información sobre el búfer de datos antes de realizar un paso de procesamiento y notificar al punto de conexión la finalización de la fase.
-   La interfaz [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) o [**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) , en función de si el objeto de punto de conexión está capturando o representando audio.
-   [**IAudioDeviceEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [**IAudioEndpointControl**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

El motor de audio usa estas interfaces para obtener información sobre los puntos de conexión que están asociados al motor. La implementación del punto de conexión debe proporcionar el mecanismo para enviar o consumir datos del motor de acuerdo con lo especificado en estas interfaces.

La API de Servicios de Escritorio remoto AudioEndpoint admite tipos de enumeración, interfaces y estructuras.

## <a name="in-this-section"></a>En esta sección

-   [Servicios de Escritorio remoto tipos de enumeración AudioEndpoint](terminal-services-audioendpoint-enumeration-types.md)
-   [Servicios de Escritorio remoto funciones AudioEndpoint](remote-desktop-services-audioendpoint-functions.md)
-   [Interfaces de Servicios de Escritorio remoto AudioEndpoint](terminal-services-audioendpoint-interfaces.md)
-   [Servicios de Escritorio remoto estructuras AudioEndpoint](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a>Observaciones

La API de Servicios de Escritorio remoto AudioEndpoint es para su uso en escenarios de Escritorio remoto; no es para las aplicaciones cliente.

 

 




