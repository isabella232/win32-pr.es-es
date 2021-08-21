---
title: Servicios de Escritorio remoto api audioendpoint
description: Admite interfaces para el registro de puntos de conexión de audio y el transporte de datos.
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto Servicios de Escritorio remoto , referencia de api audioendpoint
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9a7aa83b519ca10128f9bea3b945492f387c0498c81f8b2959cb9830b91dbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000095"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a>Servicios de Escritorio remoto api audioendpoint

Un *punto de conexión de* audio representa un dispositivo de audio, una API de audio o cualquier otro origen o receptor de audio, y se usa para enviar datos al motor de audio o consumir datos desde este. Un punto de conexión de audio debe estar conectado al motor de audio *a* través de una conexión y cada conexión solo puede tener un punto de conexión conectado a él. Una vez registrado un punto de conexión, el motor de audio asocia el punto de conexión a la conexión.

Cada objeto de punto de conexión debe implementar las interfaces siguientes:

-   [**IAudioEndpoint para**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) permitir que el motor de audio obtenga información sobre el punto de conexión.
-   [**IAudioEndpointRT para**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) obtener información sobre el búfer de datos antes de realizar un paso de procesamiento y notificar al punto de conexión cuando se completa el paso.
-   La interfaz [**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) o [**IAudioOutputEndpointRT,**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) dependiendo de si el objeto de punto de conexión captura o representa audio.
-   [**IAudioDeviceEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [**IAudioEndpointControl**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

El motor de audio usa estas interfaces para obtener información sobre los puntos de conexión que están conectados al motor. La implementación del punto de conexión debe proporcionar el mecanismo para entregar datos al motor o consumir datos del motor, tal y como especifican estas interfaces.

La API Servicios de Escritorio remoto AudioEndpoint admite tipos de enumeración, interfaces y estructuras.

## <a name="in-this-section"></a>En esta sección

-   [Servicios de Escritorio remoto enumeración AudioEndpoint](terminal-services-audioendpoint-enumeration-types.md)
-   [Servicios de Escritorio remoto AudioEndpoint Functions](remote-desktop-services-audioendpoint-functions.md)
-   [Servicios de Escritorio remoto interfaces audioendpoint](terminal-services-audioendpoint-interfaces.md)
-   [Servicios de Escritorio remoto AudioEndpoint Structures](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a>Comentarios

La Servicios de Escritorio remoto AudioEndpoint API es para su uso en Escritorio remoto escenarios; no es para las aplicaciones cliente.

 

 




