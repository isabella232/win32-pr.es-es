---
description: La propiedad PKEY \_ AudioEndpoint FormFactor especifica el factor de forma del dispositivo de punto \_ de conexión de audio. El factor de forma indica los atributos físicos del dispositivo de punto de conexión de audio que el usuario manipula.
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: PKEY_AudioEndpoint_FormFactor (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e76b53b91a03cda5e8484878f62c3c7a205e422f53ed647d29cca6435e0f14f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119018343"
---
# <a name="pkey_audioendpoint_formfactor"></a>PKEY \_ AudioEndpoint \_ FormFactor

La **propiedad PKEY \_ AudioEndpoint \_ FormFactor** especifica el factor de forma del dispositivo de punto de conexión de audio. El factor de forma indica los atributos físicos del dispositivo de punto de conexión de audio que el usuario manipula.

El **miembro vt** de la estructura **PROPVARIANT** se establece en VT \_ UI4.

El **miembro uintVal** de la **estructura PROPVARIANT** contiene un valor de enumeración que se convierte al tipo UINT. Se establece en uno de los siguientes valores de [**enumeración EndpointFormFactor:**](/windows/win32/api/mmdeviceapi/ne-mmdeviceapi-endpointformfactor)

-   RemoteNetworkDevice
-   Altavoces
-   LineLevel
-   Auriculares
-   Micrófono
-   Auriculares
-   Auricular
-   UnknownDigitalPassthrough
-   Spdif
-   HDMI
-   UnknownFormFactor

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                           |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                     |
| Header<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades del punto de conexión de audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propiedades de audio principal](core-audio-properties.md)
</dt> </dl>

 

 




