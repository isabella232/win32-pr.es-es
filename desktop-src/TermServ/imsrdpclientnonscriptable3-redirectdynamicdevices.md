---
title: Propiedad RedirectDynamicDevices de IMsRdpClientNonScriptable3
description: Especifica o recupera si los dispositivos Plug and Play conectados dinámicamente (PnP) que se enumeran mientras están en una sesión están disponibles para la redirección.
ms.assetid: 8cc5d6a4-108b-4505-8937-f6e790a5c2ba
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDevices
- Propiedad RedirectDynamicDevices Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad RedirectDynamicDevices
- Propiedad RedirectDynamicDevices Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad RedirectDynamicDevices
- Propiedad RedirectDynamicDevices Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad RedirectDynamicDevices
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDevices, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad RedirectDynamicDevices
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDevices, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad RedirectDynamicDevices
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDevices, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad RedirectDynamicDevices
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDevices, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad RedirectDynamicDevices
- Servicios de Escritorio remoto de la propiedad RedirectDynamicDevices, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad RedirectDynamicDevices
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.RedirectDynamicDevices
- IMsRdpClientNonScriptable3.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable3.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.RedirectDynamicDevices
- IMsRdpClientNonScriptable4.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable4.put_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.RedirectDynamicDevices
- IMsRdpClientNonScriptable5.get_RedirectDynamicDevices
- IMsRdpClientNonScriptable5.put_RedirectDynamicDevices
- MsRdpClient5.RedirectDynamicDevices
- MsRdpClient6.RedirectDynamicDevices
- MsRdpClient7.RedirectDynamicDevices
- MsRdpClient8.RedirectDynamicDevices
- MsRdpClient9.RedirectDynamicDevices
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75224d26034e606a7a46943a02845280a092c3b5
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103801448"
---
# <a name="imsrdpclientnonscriptable3redirectdynamicdevices-property"></a>IMsRdpClientNonScriptable3:: RedirectDynamicDevices (propiedad)

Especifica o recupera si los dispositivos Plug and Play conectados dinámicamente (PnP) que se enumeran mientras están en una sesión están disponibles para la redirección.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_RedirectDynamicDevices(
  [in]  VARIANT_BOOL fRedirectDynamicDevices
);

HRESULT get_RedirectDynamicDevices(
  [out] VARIANT_BOOL *pfRedirectDynamicDevices
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica si los dispositivos PnP conectados dinámicamente que se enumeran mientras están en una sesión están disponibles para la redirección.

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

 

 





