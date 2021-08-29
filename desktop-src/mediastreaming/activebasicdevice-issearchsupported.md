---
title: Propiedad ActiveBasicDevice IsSearchSupported (PlayToDevice.h)
description: Obtiene un valor que indica si el dispositivo admite la búsqueda.
ms.assetid: 091D467A-1FF6-4635-BF89-4E62AC9C660A
keywords:
- Api de streaming multimedia de la propiedad IsSearchSupported
- IsSearchSupported, propiedad Media Streaming API, interfaz ActiveBasicDevice
- ActiveBasicDevice interface Media Streaming API , Propiedad IsSearchSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSearchSupported
- ActiveBasicDevice.get_IsSearchSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 37aa2d4ce01c058e899a1c15d5672b6578537604b910ac817376fcff49746e4e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120011935"
---
# <a name="activebasicdeviceissearchsupported-property"></a>Propiedad ActiveBasicDevice::IsSearchSupported

Obtiene un valor que indica si el dispositivo admite la búsqueda.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_IsSearchSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a un **valor booleano** que indica si el dispositivo admite la búsqueda.

**True** si el dispositivo admite la búsqueda; de lo contrario, **false**.

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

 

