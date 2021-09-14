---
title: Método IMsRdpClient9 detachEvent
description: Desasocula un evento.
ms.assetid: 6a3ca713-1d5c-4070-a527-ad4f532a4cbf
ms.tgt_platform: multiple
keywords:
- Método detachEvent Servicios de Escritorio remoto
- Método detachEvent Servicios de Escritorio remoto , interfaz IMsRdpClient9
- Interfaz IMsRdpClient9 Servicios de Escritorio remoto método , detachEvent
- Método detachEvent Servicios de Escritorio remoto , interfaz IMsRdpClient10
- Interfaz IMsRdpClient10 Servicios de Escritorio remoto método , detachEvent
topic_type:
- apiref
api_name:
- IMsRdpClient9.detachEvent
- IMsRdpClient10.detachEvent
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 399611ea526338f4cfe40ef3a4d6543bf27f134a
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "126968371"
---
# <a name="imsrdpclient9detachevent-method"></a>IMsRdpClient9::d etachEvent (método)

Desasocula un evento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT detachEvent(
  [in] BSTR      eventName,
  [in] IDispatch *callback
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*eventName* \[ En\]
</dt> <dd>

Nombre del evento.

</dd> <dt>

*devolución de llamada* \[ En\]
</dt> <dd>

Devolución de llamada asociada al evento.

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

 

 





