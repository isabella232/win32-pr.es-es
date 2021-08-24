---
description: La propiedad PKEY \_ AudioEndpoint Supports EventDriven Mode indica si el punto de conexión \_ admite el modo controlado por \_ \_ eventos.
ms.assetid: 9cffd9ae-710b-4d41-aa02-3ab1a065e544
title: PKEY_AudioEndpoint_Supports_EventDriven_Mode (Mmdeviceapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 280be65d4ae8e0b557bd96320ea31f67ba75657ecb5b685608bd2c314e10836d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119758925"
---
# <a name="pkey_audioendpoint_supports_eventdriven_mode"></a>PKEY \_ AudioEndpoint \_ admite el modo \_ EventDriven \_

La **propiedad PKEY \_ AudioEndpoint \_ Supports \_ EventDriven \_ Mode** indica si el punto de conexión admite el modo controlado por eventos.

El **miembro vt** de la estructura **PROPVARIANT** se establece en VT \_ UI4.

El **miembro uintVal** de la estructura **PROPVARIANT** es **un DWORD** que indica si el punto de conexión admite el modo controlado por eventos.

## <a name="remarks"></a>Comentarios

Un OEM de audio rellena este valor de propiedad en un archivo .inf para indicar que el hardware de HDAudio admite el modo controlado por eventos según el requisito de WHQL.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 aplicaciones \[ de escritorio\]<br/>                                               |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[ R2\]<br/>                                  |
| Header<br/>                   | <dl> <dt>Mmdeviceapi.h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**Propiedades del punto de conexión de audio**](audio-endpoint-properties.md)
</dt> <dt>

[Propiedades de audio principal](core-audio-properties.md)
</dt> </dl>

 

 




