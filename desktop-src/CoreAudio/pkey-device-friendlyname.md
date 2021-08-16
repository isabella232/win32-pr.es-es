---
description: La propiedad PKEY Device FriendlyName contiene el nombre descriptivo del dispositivo del punto de conexión \_ \_ (por ejemplo, &\# 0034; Altavoces (adaptador de audio XYZ)&\# 0034;).
ms.assetid: 3ccd6a78-8bc3-4a46-8f11-7c2ae8a23c63
title: PKEY_Device_FriendlyName (Functiondiscoverykeys \_ devpkey.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 148a9d7f87b32b7175aa794f769d2fa67b42c86c44e8cc7bf773d3fa6b09d106
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118406431"
---
# <a name="pkey_device_friendlyname"></a>PKEY \_ Device \_ FriendlyName

La **propiedad PKEY \_ Device \_ FriendlyName** contiene el nombre descriptivo del dispositivo del punto de conexión (por ejemplo, "Altavoces (adaptador de audio XYZ)").

El **miembro vt** de la estructura **PROPVARIANT** se establece en VT \_ LPWSTR.

El **miembro pwszVal** de la estructura **PROPVARIANT** apunta a una cadena de caracteres anchos terminada en NULL que contiene el nombre descriptivo del dispositivo de punto de conexión.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                                              |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                                        |
| Header<br/>                   | <dl> <dt>Functiondiscoverykeys \_ devpkey.h</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[Propiedades de audio principal](core-audio-properties.md)
</dt> <dt>

[Propiedades de dispositivos](device-properties.md)
</dt> </dl>

 

 




