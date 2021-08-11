---
title: Propiedad ActiveBasicDevice IsImageSupported (PlayToDevice.h)
description: Obtiene un valor que indica si el dispositivo admite imágenes.
ms.assetid: FC53B87C-D739-4AD4-9DD3-415AC8692224
keywords:
- IsImageSupported, propiedad Media Streaming API
- IsImageSupported, propiedad Media Streaming API, interfaz ActiveBasicDevice
- ActiveBasicDevice interface Media Streaming API , IsImageSupported property
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsImageSupported
- ActiveBasicDevice.get_IsImageSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a147c5156f07c6cc6461cafcf8dc778013a7eb3048d1428f854b844d24f5642a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118236716"
---
# <a name="activebasicdeviceisimagesupported-property"></a>Propiedad ActiveBasicDevice::IsImageSupported

Obtiene un valor que indica si el dispositivo admite imágenes.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_IsImageSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a un **valor booleano** que indica si el dispositivo admite imágenes.

**true** si el dispositivo admite imágenes; de lo contrario, **false**.

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

 

