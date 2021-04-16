---
title: Interfaces de Servicios de Escritorio remoto AudioEndpoint
description: Las interfaces siguientes se usan con la API de AudioEndpoint.
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de520571c99bf84472760e8a1ca28a52a1d6c32e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105685508"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a>Interfaces de Servicios de Escritorio remoto AudioEndpoint

Las interfaces siguientes se usan con la API de AudioEndpoint.

## <a name="in-this-section"></a>En esta sección

<dl> <dt>

[**IAudioDeviceEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
</dt> <dd>

Inicializa un objeto de punto de conexión de dispositivo y obtiene las funciones del dispositivo que representa.

</dd> <dt>

[**IAudioEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint)
</dt> <dd>

Proporciona información al motor de audio sobre un punto de conexión de audio. Esta interfaz se implementa mediante un punto de conexión de audio.

</dd> <dt>

[**IAudioEndpointControl**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)
</dt> <dd>

Controla el estado de flujo de un punto de conexión.

</dd> <dt>

[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

Obtiene la diferencia entre las posiciones de lectura y escritura actuales en el búfer del extremo.

</dd> <dt>

[**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)
</dt> <dd>

Obtiene el búfer de entrada para cada paso de procesamiento.

</dd> <dt>

[**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)
</dt> <dd>

Obtiene el búfer de salida para cada paso de procesamiento.

</dd> </dl>

## <a name="remarks"></a>Observaciones

La API de Servicios de Escritorio remoto AudioEndpoint es para su uso en escenarios de Escritorio remoto; no es para las aplicaciones cliente.

 

 




