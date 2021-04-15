---
description: 'Más información acerca de: PKEY_AudioEndpoint_PhysicalSpeakers'
ms.assetid: 20049071-0a14-421e-8bc5-04af9c7117b0
title: PKEY_AudioEndpoint_PhysicalSpeakers (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6a627ec97dc329f50cc58a15d0df516f598af86
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104539213"
---
# <a name="pkey_audioendpoint_physicalspeakers"></a>PKEY \_ AudioEndpoint \_ PhysicalSpeakers

La **propiedad \_ \_ PhysicalSpeakers de AudioEndpoint de PKEY** especifica la máscara de configuración de canal para el dispositivo de punto de conexión de audio. La máscara indica la configuración física de un conjunto de oradores y especifica la asignación de canales a los altavoces. Para obtener más información acerca de las máscaras de configuración de canal, consulte lo siguiente:

1.  La descripción de la \_ propiedad de configuración de canal de audio KSPROPERTY \_ \_ en la documentación de DDK de Windows.
2.  Las notas del producto titulada "compatibilidad con controladores de audio para las configuraciones de altavoz de Home Theater" en el sitio Web [de tecnologías de dispositivos de audio para Windows](https://www.microsoft.com/whdc/device/audio/default.mspx) .

El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ UI4.

El miembro **uintVal** de la estructura **PROPVARIANT** contiene una máscara de configuración de canal que se convierte al tipo **uint**.

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

 

 




