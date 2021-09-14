---
title: Método attachEvent de IMsRdpClient9
description: Asocia un evento.
ms.assetid: 3a887aeb-a74f-4477-8cf3-8ac43a31fa26
ms.tgt_platform: multiple
keywords:
- Método attachEvent Servicios de Escritorio remoto
- Método attachEvent Servicios de Escritorio remoto , interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto método , attachEvent
- Método attachEvent Servicios de Escritorio remoto , interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto método , attachEvent
topic_type:
- apiref
api_name:
- IMsRdpClient9.attachEvent
- IMsRdpClient10.attachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f1bd3fd518fba825c209a4170e6b314a7b774a49
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968372"
---
# <a name="imsrdpclient9attachevent-method"></a>IMsRdpClient9::attachEvent (método)

Asocia un evento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT attachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*eventName* \[ En\]
</dt> <dd>

Evento que se adjuntará.

</dd> <dt>

*devolución de llamada* \[ En\]
</dt> <dd>

La devolución de llamada.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Si este método se realiza correctamente, devuelve **S \_ OK**. De lo contrario, devuelve un código de error **HRESULT.**

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8.1<br/>                                                                                                                                                                                                                                                  |
| Servidor mínimo compatible<br/> | Windows Server 2012 R2<br/>                                                                                                                                                                                                                                       |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                  |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>                                                                                                                                                                                  |
| IID<br/>                      | CLSID MsRdpClient9 se define como \_ 301B94BA-5D25-4A12-BFFE-3B6E7A616585<br/> CLSID \_ MsRdpClient9NotSafeForScripting se define como 8B918B82-7985-4C24-89DF-C33AD2BBFBCD<br/> IID IMsRdpClient9 se define como \_ 28904001-04B6-436C-A55B-0AF1A0883DC9<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IMsRdpClient10**](imsrdpclient10.md)
</dt> <dt>

[**IMsRdpClient9**](imsrdpclient9.md)
</dt> </dl>

 

 





