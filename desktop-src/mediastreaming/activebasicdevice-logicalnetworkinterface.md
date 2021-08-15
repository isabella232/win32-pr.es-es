---
title: Propiedad ActiveBasicDevice LogicalNetworkInterface (PlayToDevice.h)
description: Obtiene el identificador de la interfaz de red lógica.
ms.assetid: 47C2E0BE-D3E3-4A9F-9FC6-873882811506
keywords:
- Propiedad LogicalNetworkInterface de Media Streaming API
- Propiedad LogicalNetworkInterface Media Streaming API, interfaz ActiveBasicDevice
- ActiveBasicDevice interface Media Streaming API , LogicalNetworkInterface property
topic_type:
- apiref
api_name:
- ActiveBasicDevice.LogicalNetworkInterface
- ActiveBasicDevice.get_LogicalNetworkInterface
api_location:
- playtodevice.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41ee3e2b23a43e29daf2438cee517220f895ad601607dbdc6a61497f8ef1afa7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118736391"
---
# <a name="activebasicdevicelogicalnetworkinterface-property"></a>Propiedad ActiveBasicDevice::LogicalNetworkInterface

Obtiene el identificador de la interfaz de red lógica.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_LogicalNetworkInterface(
  [out] GUID *value
);
```



## <a name="property-value"></a>Valor de propiedad

Puntero a un **GUID** que especifica el identificador de la interfaz de red lógica.

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

 

