---
title: Servicios de Escritorio remoto audioEndpoint Interfaces
description: Las interfaces siguientes se usan con audioEndpoint API.
ms.assetid: 615c2d03-c2fb-46f8-aa78-064f8e7b6064
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ec12cd3d4648f3ed357e898f75850e77b3b679d59a92d9f0518f809ba52f58f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000075"
---
# <a name="remote-desktop-services-audioendpoint-interfaces"></a>Servicios de Escritorio remoto audioEndpoint Interfaces

Las interfaces siguientes se usan con audioEndpoint API.

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

Controla el estado de secuencia de un punto de conexión.

</dd> <dt>

[**IAudioEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt)
</dt> <dd>

Obtiene la diferencia entre las posiciones de lectura y escritura actuales en el búfer del punto de conexión.

</dd> <dt>

[**IAudioInputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt)
</dt> <dd>

Obtiene el búfer de entrada para cada paso de procesamiento.

</dd> <dt>

[**IAudioOutputEndpointRT**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt)
</dt> <dd>

Obtiene el búfer de salida para cada paso de procesamiento.

</dd> </dl>

## <a name="remarks"></a>Comentarios

La SERVICIOS DE ESCRITORIO REMOTO AudioEndpoint API es para su uso en Escritorio remoto escenarios; no es para aplicaciones cliente.

 

 




