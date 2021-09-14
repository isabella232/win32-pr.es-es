---
description: Propiedad PKEY \_ DeviceInterface \_ FriendlyName.
ms.assetid: beef2153-489f-4ff5-a161-b4e2cd4ac1fa
title: PKEY_DeviceInterface_FriendlyName (Functiondiscoverykeys \_ devpkey.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b7590e9254e336bf9dbfe0fdeb3349bf19c0b8c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127164885"
---
# <a name="pkey_deviceinterface_friendlyname"></a>PKEY \_ DeviceInterface \_ FriendlyName

La **propiedad PKEY \_ DeviceInterface \_ FriendlyName** contiene el nombre descriptivo del adaptador de audio al que está conectado el dispositivo de punto de conexión (por ejemplo, "Adaptador de audio XYZ").

El **miembro vt** de la estructura **PROPVARIANT** se establece en VT \_ LPWSTR.

El **miembro pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en NULL que contiene el nombre descriptivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                        |
| Encabezado<br/>                   | <dl> <dt>Functiondiscoverykeys \_ devpkey.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de audio principal](core-audio-properties.md)
</dt> <dt>

[Propiedades de dispositivos](device-properties.md)
</dt> </dl>

 

 




