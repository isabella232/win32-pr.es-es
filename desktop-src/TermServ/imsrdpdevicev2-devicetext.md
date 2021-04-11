---
title: Propiedad DeviceText de IMsRdpDeviceV2
description: Contiene el texto del dispositivo.
ms.assetid: 2a67e8d4-2af3-4738-ade2-a79800aea4a1
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad DeviceText
- Propiedad DeviceText Servicios de Escritorio remoto, interfaz IMsRdpDeviceV2
- Servicios de Escritorio remoto de la interfaz IMsRdpDeviceV2, propiedad DeviceText
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.DeviceText
- IMsRdpDeviceV2.get_DeviceText
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6fb35142a166db7e7c05fa5c0f00f7fdf2e1219c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104274512"
---
# <a name="imsrdpdevicev2devicetext-property"></a>IMsRdpDeviceV2::D propiedad eviceText

Contiene el texto del dispositivo. Este es el nombre que Windows muestra al usuario.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DeviceText(
  [out, retval] BSTR *pDeviceText
);
```



## <a name="property-value"></a>Valor de propiedad

Nombre para mostrar del dispositivo.

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

 

 





