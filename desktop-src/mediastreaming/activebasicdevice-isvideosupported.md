---
title: Propiedad ActiveBasicDevice IsVideoSupported (PlayToDevice.h)
description: Obtiene un valor que indica si el dispositivo admite vídeo.
ms.assetid: E8D33A04-748D-42F8-878F-35D973A6B559
keywords:
- Propiedad IsVideoSupported de Media Streaming API
- Propiedad IsVideoSupported de Media Streaming API, interfaz ActiveBasicDevice
- Interfaz ActiveBasicDevice Media Streaming API , propiedad IsVideoSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsVideoSupported
- ActiveBasicDevice.get_IsVideoSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91bb115aad422546746a44824c847bd0ae80c188264e8539e569a26e16eefa93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972524"
---
# <a name="activebasicdeviceisvideosupported-property"></a>Propiedad ActiveBasicDevice::IsVideoSupported

Obtiene un valor que indica si el dispositivo admite vídeo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_IsVideoSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a un **valor booleano** que indica si el dispositivo admite vídeo.

**true** si el dispositivo admite vídeo; de lo contrario, **false**.

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

 

