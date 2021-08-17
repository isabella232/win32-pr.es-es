---
title: Propiedad IsUSBDevice de IMsRdpDeviceV2
description: Especifica si el dispositivo es para el redireccionamiento USB.
ms.assetid: df4c9764-ad96-4f35-9537-3890293a944c
ms.tgt_platform: multiple
keywords:
- Propiedad IsUSBDevice Servicios de Escritorio remoto
- Propiedad IsUSBDevice Servicios de Escritorio remoto , interfaz IMsRdpDeviceV2
- Interfaz IMsRdpDeviceV2 Servicios de Escritorio remoto , propiedad IsUSBDevice
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsUSBDevice
- IMsRdpDeviceV2.get_IsUSBDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e03e2572912487cb924f65350dbdd7818d07d2a7b172d18cb28fab87335a00dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138568"
---
# <a name="imsrdpdevicev2isusbdevice-property"></a>Propiedad IMsRdpDeviceV2::IsUSBDevice

Especifica si el dispositivo es para el redireccionamiento USB.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_IsUSBDevice(
  [out, retval] VARIANT_BOOL *pvboolUSBDevice
);
```



## <a name="property-value"></a>Valor de propiedad

**true** si el dispositivo es para el redireccionamiento USB; de lo contrario, **false**.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7 con SP1<br/>                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2 con SP1<br/>                                             |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 se define como 5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





