---
description: La \_ propiedad DeviceDesc del dispositivo PKEY \_ contiene la descripción del dispositivo de extremo (por ejemplo, &\# 0034; Habla&\# 0034;).
ms.assetid: 23715497-a74d-4dab-aade-c7779fe80aa6
title: PKEY_Device_DeviceDesc (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5eb68f874979e660fec0cd563db9bcaceb7d5b74
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906938"
---
# <a name="pkey_device_devicedesc"></a>\_DeviceDesc de dispositivo PKEY \_

La **propiedad \_ \_ DeviceDesc del dispositivo PKEY** contiene la descripción del dispositivo de extremo (por ejemplo, "altavoces").

El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ LPWStr.

El miembro **pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en null que contiene la descripción del dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Functiondiscoverykeys \_ devpkey. h</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[Propiedades de audio principales](core-audio-properties.md)
</dt> <dt>

[Propiedades de dispositivos](device-properties.md)
</dt> </dl>

 

 




