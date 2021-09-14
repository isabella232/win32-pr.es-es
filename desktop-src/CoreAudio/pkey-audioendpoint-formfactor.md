---
description: La propiedad PKEY \_ AudioEndpoint \_ FormFactor especifica el factor de forma del dispositivo de punto de conexión de audio. El factor de forma indica los atributos físicos del dispositivo de punto de conexión de audio que el usuario manipula.
ms.assetid: f49cb7da-3b50-47e2-90b4-1a885001b5d7
title: PKEY_AudioEndpoint_FormFactor (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5833470e2a2848f9454f3b5eefbf852f452f033
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164926"
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
-   SPDIF
-   HDMI
-   UnknownFormFactor

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

 

 




