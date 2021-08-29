---
title: Propiedad ActiveBasicDevice IsSetNextSourceSupported (PlayToDevice.h)
description: Obtiene un valor que indica si se admite la configuración del siguiente origen.
ms.assetid: 0888A737-D2CC-4259-BC60-9D2B8E8302A0
keywords:
- IsSetNextSourceSupported, propiedad Media Streaming API
- IsSetNextSourceSupported, propiedad Media Streaming API, interfaz ActiveBasicDevice
- ActiveBasicDevice interface Media Streaming API , Propiedad IsSetNextSourceSupported
topic_type:
- apiref
api_name:
- ActiveBasicDevice.IsSetNextSourceSupported
- ActiveBasicDevice.get_IsSetNextSourceSupported
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e7db7bc917ab8f901d32772fdc756f11b74f5dfabc2f31d44bfab12aad023e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119952795"
---
# <a name="activebasicdeviceissetnextsourcesupported-property"></a>Propiedad ActiveBasicDevice::IsSetNextSourceSupported

Obtiene un valor que indica si se admite la configuración del siguiente origen.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_IsSetNextSourceSupported(
  [out] boolean *value
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a un **valor booleano** que indica si se admite la configuración del siguiente origen.

**True** si se admite la configuración del siguiente origen; de lo contrario, **false**.

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

 

