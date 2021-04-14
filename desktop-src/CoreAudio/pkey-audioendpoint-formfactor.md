---
description: La \_ propiedad PKEY AudioEndpoint \_ FormFactor especifica el factor de forma del dispositivo de extremo de audio. El factor de forma indica los atributos físicos del dispositivo de extremo de audio que manipula el usuario.
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: PKEY_AudioEndpoint_FormFactor (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5833470e2a2848f9454f3b5eefbf852f452f033
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104496516"
---
# <a name="pkey_audioendpoint_formfactor"></a>PKEY \_ AudioEndpoint \_ FormFactor

La propiedad **PKEY \_ AudioEndpoint \_ FormFactor** especifica el factor de forma del dispositivo de extremo de audio. El factor de forma indica los atributos físicos del dispositivo de extremo de audio que manipula el usuario.

El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ UI4.

El miembro **uintVal** de la estructura **PROPVARIANT** contiene un valor de enumeración que se convierte al tipo uint. Se establece en uno de los siguientes valores de enumeración [**EndpointFormFactor**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor) :

-   RemoteNetworkDevice
-   Altavoces
-   LineLevel
-   Auriculares
-   Micrófono
-   Auriculares
-   Auricular
-   UnknownDigitalPassthrough
-   SALIDA
-   HDMI
-   UnknownFormFactor

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

 

 




