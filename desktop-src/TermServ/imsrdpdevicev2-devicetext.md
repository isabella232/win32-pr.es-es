---
title: IMsRdpDeviceV2 DeviceText, propiedad
description: Contiene el texto del dispositivo.
ms.assetid: 2a67e8d4-2af3-4738-ade2-a79800aea4a1
ms.tgt_platform: multiple
keywords:
- Propiedad DeviceText Servicios de Escritorio remoto
- Propiedad DeviceText Servicios de Escritorio remoto interfaz , IMsRdpDeviceV2
- Interfaz IMsRdpDeviceV2 Servicios de Escritorio remoto , propiedad DeviceText
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
ms.openlocfilehash: 8ed156a56215c859455cd16cb5d4ae0396eb24a0b62c8b9ae0ee6d5a43bd2ad3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138608"
---
# <a name="imsrdpdevicev2devicetext-property"></a>IMsRdpDeviceV2::D eviceText

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

 

 





