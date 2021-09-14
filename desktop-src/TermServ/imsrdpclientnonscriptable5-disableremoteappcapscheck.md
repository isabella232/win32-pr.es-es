---
title: IMsRdpClientNonScriptable5 DisableRemoteAppCapsCheck, propiedad
description: Especifica si el control Escritorio remoto ActiveX no debe comprobar las funcionalidades de RemoteApp del servidor.
ms.assetid: dcc44d4b-ece5-4f5b-a00a-f90d7a2fa11a
ms.tgt_platform: multiple
keywords:
- Propiedad DisableRemoteAppCapsCheck Servicios de Escritorio remoto
- Propiedad DisableRemoteAppCapsCheck Servicios de Escritorio remoto interfaz , IMsRdpClientNonScriptable5
- Interfaz IMsRdpClientNonScriptable5 Servicios de Escritorio remoto propiedad , DisableRemoteAppCapsCheck
topic_type:
- apiref
api_name:
- IMsRdpClientNonScriptable5.DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.get_DisableRemoteAppCapsCheck
- IMsRdpClientNonScriptable5.put_DisableRemoteAppCapsCheck
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4f65b0e1b56b3a1152f71aff25d4cf65a4420d1
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127071027"
---
# <a name="imsrdpclientnonscriptable5disableremoteappcapscheck-property"></a>Propiedad IMsRdpClientNonScriptable5::D ableRemoteAppCapsCheck

Especifica si el control Escritorio remoto ActiveX no debe comprobar las funcionalidades de RemoteApp del servidor. Si esta propiedad contiene **VARIANT \_ TRUE**, el control no debe comprobar las funcionalidades de RemoteApp del servidor. Si esta propiedad contiene **VARIANT \_ FALSE,** el control puede comprobar las funcionalidades de RemoteApp del servidor.

Esta propiedad es de lectura y escritura.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT put_DisableRemoteAppCapsCheck(
  [in]          VARIANT_BOOL fDisableRemoteAppCapsCheck
);

HRESULT get_DisableRemoteAppCapsCheck(
  [out, retval] VARIANT_BOOL *pfDisableRemoteAppCapsCheck
);
```



## <a name="property-value"></a>Valor de propiedad

Especifica el nuevo valor de propiedad.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 7<br/>                                                                          |
| Servidor mínimo compatible<br/> | Windows Server 2008 R2<br/>                                                             |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>        |
| IID<br/>                      | IID \_ IMsRdpClientNonScriptable5 se define como 4f6996d5-d7b1-412c-b0ff-063718566907<br/> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsRdpClientNonScriptable5**](imsrdpclientnonscriptable5.md)
</dt> </dl>

 

 





