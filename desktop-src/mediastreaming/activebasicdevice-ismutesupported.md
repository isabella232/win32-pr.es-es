---
title: Propiedad ActiveBasicDevice IsMuteSupported (PlayToDevice.h)
description: Obtiene un valor que indica si el dispositivo admite el muting del audio.
ms.assetid: FF4B533F-B416-4DBE-BF86-FA34E785FFA2
keywords:
- Api de streaming multimedia de la propiedad IsMuteSupported
- Propiedad IsMuteSupported de Media Streaming API, interfaz ActiveBasicDevice
- ActiveBasicDevice interface Media Streaming API , IsMuteSupported property
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsMuteSupported
- ActiveBasicDevice.get_IsMuteSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0fad8352504a6c950bb76206f05c77c5baa9f3baed2f1144a1d6c165e380a4b7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236653"
---
# <a name="activebasicdeviceismutesupported-property"></a>Propiedad ActiveBasicDevice::IsMuteSupported

Obtiene un valor que indica si el dispositivo admite el muting del audio.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_IsMuteSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a un **valor booleano** que indica si el dispositivo admite el muting del audio.

**True** si el dispositivo admite el muting del audio; de lo contrario, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
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

 

