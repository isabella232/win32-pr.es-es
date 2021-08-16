---
title: Propiedad ActiveBasicDevice MaxVolume (PlayToDevice.h)
description: Obtiene el volumen máximo admitido por el dispositivo.
ms.assetid: EA0EC323-4A18-4CC1-8FA4-7BD302318863
keywords:
- Propiedad MaxVolume de Media Streaming API
- MaxVolume, propiedad Media Streaming API, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice Media Streaming API, propiedad MaxVolume
topic_type:
- apiref
api_name:
- ActiveBasicDevice.MaxVolume
- ActiveBasicDevice.get_MaxVolume
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 803e2e66306bce0d6fd308501edece61668d5f2e0d8041273d508b662f6cd66f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736201"
---
# <a name="activebasicdevicemaxvolume-property"></a>Propiedad ActiveBasicDevice::MaxVolume

Obtiene el volumen máximo admitido por el dispositivo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MaxVolume(
  [out] boolean *UINT32
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a un **UINT32** que especifica el volumen máximo admitido por el dispositivo.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | \[Windows 8.1 solo aplicaciones de escritorio\]<br/>                                                |
| Servidor mínimo compatible<br/> | Windows Server 2012 Solo aplicaciones \[ de escritorio R2\]<br/>                                     |
| Header<br/>                   | <dl> <dt>PlayToDevice.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>PlayToDevice.idl</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Playtodevice.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ActiveBasicDevice**](/previous-versions/windows/desktop/legacy/dn385755(v=vs.85))
</dt> </dl>

 

