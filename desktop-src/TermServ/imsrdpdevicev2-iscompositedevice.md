---
title: IMsRdpDeviceV2 IsCompositeDevice, propiedad
description: Especifica si el dispositivo es un dispositivo compuesto.
ms.assetid: cc54f3f0-de0b-4f75-b5a1-4f061ac95ab5
ms.tgt_platform: multiple
keywords:
- Propiedad IsCompositeDevice Servicios de Escritorio remoto
- Propiedad IsCompositeDevice Servicios de Escritorio remoto interfaz , IMsRdpDeviceV2
- Interfaz IMsRdpDeviceV2 Servicios de Escritorio remoto , propiedad IsCompositeDevice
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.IsCompositeDevice
- IMsRdpDeviceV2.get_IsCompositeDevice
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c271c78eabd007641033d7171edc4b4ced1a70b9f18eb366fb30a8bac75254f4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119138558"
---
# <a name="imsrdpdevicev2iscompositedevice-property"></a>IMsRdpDeviceV2::IsCompositeDevice, propiedad

Especifica si el dispositivo es un dispositivo compuesto.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_IsCompositeDevice(
  [out, retval] VARIANT_BOOL *pvboolCompositeDevice
);
```



## <a name="property-value"></a>Valor de propiedad

**true** si el dispositivo es un dispositivo compuesto; de lo contrario, **false**.

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

 

 





