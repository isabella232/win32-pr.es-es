---
title: Propiedad WarnAboutSendingCredentials de IMsRdpClientNonScriptable3
description: Especifica o recupera si el cuadro de diálogo Advertencia de seguridad debe incluir una advertencia sobre el envío de credenciales al servidor remoto antes de iniciar una sesión.
ms.assetid: b97baef5-4a51-4e5c-bd53-10cff175533c
ms.tgt_platform: multiple
keywords:
- Servicios de Escritorio remoto de la propiedad WarnAboutSendingCredentials
- Propiedad WarnAboutSendingCredentials Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable3
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable3, propiedad WarnAboutSendingCredentials
- Propiedad WarnAboutSendingCredentials Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable4
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable4, propiedad WarnAboutSendingCredentials
- Propiedad WarnAboutSendingCredentials Servicios de Escritorio remoto, interfaz IMsRdpClientNonScriptable5
- Servicios de Escritorio remoto de la interfaz IMsRdpClientNonScriptable5, propiedad WarnAboutSendingCredentials
- Servicios de Escritorio remoto de la propiedad WarnAboutSendingCredentials, objeto MsRdpClient5
- Servicios de Escritorio remoto de objeto MsRdpClient5, propiedad WarnAboutSendingCredentials
- Servicios de Escritorio remoto de la propiedad WarnAboutSendingCredentials, objeto MsRdpClient6
- Servicios de Escritorio remoto de objeto MsRdpClient6, propiedad WarnAboutSendingCredentials
- Servicios de Escritorio remoto de la propiedad WarnAboutSendingCredentials, objeto MsRdpClient7
- Servicios de Escritorio remoto de objeto MsRdpClient7, propiedad WarnAboutSendingCredentials
- Servicios de Escritorio remoto de la propiedad WarnAboutSendingCredentials, objeto MsRdpClient8
- Servicios de Escritorio remoto de objeto MsRdpClient8, propiedad WarnAboutSendingCredentials
- Servicios de Escritorio remoto de la propiedad WarnAboutSendingCredentials, objeto MsRdpClient9
- Servicios de Escritorio remoto de objeto MsRdpClient9, propiedad WarnAboutSendingCredentials
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable3.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable3.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable4.put_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.get_WarnAboutSendingCredentials
- IMsRdpClientNonScriptable5.put_WarnAboutSendingCredentials
- MsRdpClient5.WarnAboutSendingCredentials
- MsRdpClient6.WarnAboutSendingCredentials
- MsRdpClient7.WarnAboutSendingCredentials
- MsRdpClient8.WarnAboutSendingCredentials
- MsRdpClient9.WarnAboutSendingCredentials
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29d9d2fcfe158f5a0bb6812002bfcc160f1c9009
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "105685926"
---
# <a name="imsrdpclientnonscriptable3warnaboutsendingcredentials-property"></a>IMsRdpClientNonScriptable3:: WarnAboutSendingCredentials (propiedad)

Especifica o recupera si el cuadro de diálogo Advertencia de seguridad debe incluir una advertencia sobre el envío de credenciales al servidor remoto antes de iniciar una sesión.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_WarnAboutSendingCredentials(
  [in]  VARIANT_BOOL fWarn
);

HRESULT get_WarnAboutSendingCredentials(
  [out] VARIANT_BOOL *pfWarn
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica si el cuadro de diálogo Advertencia de seguridad debe incluir una advertencia sobre el envío de credenciales al servidor remoto antes de iniciar una sesión.

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

 

 





