---
title: Propiedad CmDeviceInstance de IMsRdpDeviceV2
description: Contiene la instancia de dispositivo de Configuration Manager del dispositivo.
ms.assetid: 2a3e7001-7889-417f-8f9d-cc7a1776249f
ms.tgt_platform: multiple
keywords:
- Propiedad CmDeviceInstance Servicios de Escritorio remoto
- Propiedad CmDeviceInstance Servicios de Escritorio remoto interfaz , IMsRdpDeviceV2
- Interfaz IMsRdpDeviceV2 Servicios de Escritorio remoto , propiedad CmDeviceInstance
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmDeviceInstance
- IMsRdpDeviceV2.get_CmDeviceInstance
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 28843563cef37e09a9901a6b78285bf3f30b100e7e578c25666259c62b9eeb60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099375"
---
# <a name="imsrdpdevicev2cmdeviceinstance-property"></a>IMsRdpDeviceV2::CmDeviceInstance, propiedad

Contiene la instancia de dispositivo de Configuration Manager del dispositivo.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_CmDeviceInstance(
  [out, retval] DWORD *pCmDeviceInstance
);
```



## <a name="property-value"></a>Valor de propiedad

Instancia de dispositivo de Configuration Manager del dispositivo.

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

 

 





