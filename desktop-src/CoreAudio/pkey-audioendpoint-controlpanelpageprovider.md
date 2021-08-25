---
description: La propiedad PKEY \_ AudioEndpoint ControlPanelPageProvider especifica el CLSID del proveedor registrado de la extensión device-properties para el dispositivo de \_ punto de conexión de audio.
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: PKEY_AudioEndpoint_ControlPanelPageProvider (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6dc39f471649487dcdbfc2fa94371466eabd9ec59a8f9de19bdeafcec9d4283b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119695355"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a>PKEY \_ AudioEndpoint \_ ControlPanelPageProvider

La **propiedad PKEY \_ AudioEndpoint \_ ControlPanelPageProvider** especifica el CLSID del proveedor registrado de la extensión device-properties para el dispositivo de punto de conexión de audio. La extensión proporciona las propiedades del punto de conexión de audio que se muestran en la página propiedades del dispositivo del panel de control multimedia Windows, Mmsys.cpl. Para obtener más información sobre Mmsys.cpl, consulte la documentación Windows DDK.

El **miembro vt** de la estructura **PROPVARIANT** se establece en VT \_ LPWSTR.

El **miembro pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en NULL que contiene un GUID que identifica el proveedor de la extensión del panel de control.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

 




