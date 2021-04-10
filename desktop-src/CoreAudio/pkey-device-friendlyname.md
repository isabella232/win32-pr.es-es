---
description: La \_ propiedad FriendlyName del dispositivo PKEY \_ contiene el nombre descriptivo del dispositivo de extremo (por ejemplo, &\# 0034; Altavoces (adaptador de audio XYZ) &\# 0034;).
ms.assetid: 3ccd6a78-8bc3-4a46-8f11-7c2ae8a23c63
title: PKEY_Device_FriendlyName (Functiondiscoverykeys \_ devpkey. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fab8b8f30e04ae66356fb0910e3767d74b7b697a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103906934"
---
# <a name="pkey_device_friendlyname"></a>PKEY el \_ dispositivo \_ FriendlyName

La **propiedad \_ \_ FriendlyName del dispositivo PKEY** contiene el nombre descriptivo del dispositivo del punto de conexión (por ejemplo, "altavoces (adaptador de audio XYZ)").

El miembro **VT** de la estructura **PROPVARIANT** se establece en VT \_ LPWStr.

El miembro **pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en null que contiene el nombre descriptivo del dispositivo de extremo.

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

 

 




