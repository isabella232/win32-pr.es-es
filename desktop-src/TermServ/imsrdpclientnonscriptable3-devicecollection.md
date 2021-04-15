---
title: Propiedad recopilación de IMsRdpClientNonScriptable3
description: Recupera la colección de objetos de dispositivo Plug and Play (PnP) que se van a redirigir.
ms.assetid: dd5fe4c7-58bf-4e7a-b066-59278419ea6f
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad recopilación
- Propiedad recopilación Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad recopilación
- Propiedad recopilación Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad recopilación
- Propiedad recopilación Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad recopilación
- Servicios de Escritorio remoto de la propiedad recopilación, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad recopilación
- Servicios de Escritorio remoto de la propiedad recopilación, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad recopilación
- Servicios de Escritorio remoto de la propiedad recopilación, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad recopilación
- Servicios de Escritorio remoto de la propiedad recopilación, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad recopilación
- Servicios de Escritorio remoto de la propiedad recopilación, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad recopilación
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.DeviceCollection
- IMsRdpClientNonScriptable3.get_DeviceCollection
- IMsRdpClientNonScriptable4.DeviceCollection
- IMsRdpClientNonScriptable4.get_DeviceCollection
- IMsRdpClientNonScriptable5.DeviceCollection
- IMsRdpClientNonScriptable5.get_DeviceCollection
- MsRdpClient5.DeviceCollection
- MsRdpClient6.DeviceCollection
- MsRdpClient7.DeviceCollection
- MsRdpClient8.DeviceCollection
- MsRdpClient9.DeviceCollection
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a545d2f4aaae2af68c14dd6531a2c57cf73711dc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422073"
---
# <a name="imsrdpclientnonscriptable3devicecollection-property"></a>IMsRdpClientNonScriptable3::D propiedad eviceCollection

Recupera la colección de objetos de dispositivo Plug and Play (PnP) que se van a redirigir.

Esta propiedad es de solo lectura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_DeviceCollection(
  [out] IMSRdpDeviceCollection **ppDeviceCollection
);
```



## <a name="property-value"></a>Valor de propiedad

Recupera la colección de objetos de dispositivo PnP de tipo [**IMSRdpDevice**](imsrdpdevice.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                                      |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                                |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable3 se define como b3378d90-0728-45c7-8ed7-b6159fb92219<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable4**](imsrdpclientnonscriptable4.md)
</dt> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> <dt>

[**IMsRdpClientNonScriptable3**](imsrdpclientnonscriptable3.md)
</dt> </dl>

 

 





