---
description: La \_ propiedad PKEY \_ AudioEndpoint \_ admite \_ el modo EventDriven indica si el punto de conexión admite el modo basado en eventos.
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: PKEY_AudioEndpoint_Supports_EventDriven_Mode (Mmdeviceapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2707de83721d546040ac878b337faea12f533bb6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104000750"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a>PKEY \_ AudioEndpoint \_ admite \_ el \_ modo EventDriven

La propiedad **PKEY \_ AudioEndpoint admite el \_ \_ \_ modo EventDriven** indica si el punto de conexión admite el modo basado en eventos.

El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ UI4.

El miembro **uintVal** de la estructura **PROPVARIANT** es un **valor DWORD** que indica si el punto de conexión admite el modo basado en eventos.

## <a name="remarks"></a>Observaciones

El valor de esta propiedad se rellena con un OEM de audio en un archivo. inf para indicar que el hardware HDAudio admite el modo basado en eventos según el requisito de WHQL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows 7 \[\]<br/>                                               |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 R2 \[\]<br/>                                  |
| Encabezado<br/>                   | <dl> <dt>Mmdeviceapi. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades de punto de conexión de audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propiedades de audio principales](core-audio-properties.md)
</dt> </dl>

 

 




