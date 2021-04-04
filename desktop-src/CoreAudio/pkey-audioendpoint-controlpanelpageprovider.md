---
description: La \_ propiedad ControlPanelPageProvider de AudioEndpoint de PKEY \_ especifica el CLSID del proveedor registrado de la extensión de propiedades de dispositivo para el dispositivo de punto de conexión de audio.
ms.assetid: 429a7572-b609-46fd-946e-ee34ddd6cc5e
title: PKEY_AudioEndpoint_ControlPanelPageProvider (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 205ccdfba799652d9b09af21eefbedd3c3049533
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907242"
---
# <a name="pkey_audioendpoint_controlpanelpageprovider"></a>PKEY \_ AudioEndpoint \_ ControlPanelPageProvider

La **propiedad \_ \_ ControlPanelPageProvider de AudioEndpoint de PKEY** especifica el CLSID del proveedor registrado de la extensión de propiedades de dispositivo para el dispositivo de punto de conexión de audio. La extensión proporciona las propiedades del punto de conexión de audio que se muestran en la página Propiedades del dispositivo del panel de control multimedia de Windows, Mmsys.cpl. Para obtener más información acerca de Mmsys.cpl, consulte la documentación de DDK de Windows.

El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ LPWStr.

El miembro **pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en null que contiene un GUID que identifica el proveedor de la extensión del panel de control.

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

 

 




