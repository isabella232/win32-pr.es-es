---
title: Método OnAutoReconnecting de IRemoteDesktopClientEvents
description: Se llama cuando el control de cliente intenta restablecer automáticamente una conexión a una sesión remota.
ms.assetid: 299408A9-ED14-42F4-B324-AF4C86FEDABE
ms.tgt_platform: multiple
keywords:
- Método OnAutoReconnecting Servicios de Escritorio remoto
- Método OnAutoReconnecting Servicios de Escritorio remoto , interfaz IRemoteDesktopClientEvents
- Interfaz IRemoteDesktopClientEvents Servicios de Escritorio remoto método , OnAutoReconnecting
topic_type:
- apiref
api_name:
- IRemoteDesktopClientEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d74c37919384727fdf51aad004349478798a3ffd
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127270484"
---
# <a name="iremotedesktopclienteventsonautoreconnecting-method"></a>IRemoteDesktopClientEvents::OnAutoReconnecting (Método)

Se llama cuando el control de cliente intenta restablecer automáticamente una conexión a una sesión remota.

## <a name="syntax"></a>Sintaxis


```C++
void OnAutoReconnecting(
  [in] long         disconnectReason,
  [in] long         ExtendedDisconnectReason,
  [in] BSTR         disconnectErrorMessage,
  [in] VARIANT_BOOL networkAvailable,
  [in] long         attemptCount,
  [in] long         maxAttemptCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*disconnectReason* \[ En\]
</dt> <dd>

Motivo del evento de desconexión.

</dd> <dt>

*ExtendedDisconnectReason* \[ En\]
</dt> <dd>

Información ampliada para el evento de desconexión.

</dd> <dt>

*disconnectErrorMessage* \[ En\]
</dt> <dd>

Mensaje de error para el evento de desconexión.

</dd> <dt>

*networkAvailable* \[ En\]
</dt> <dd>

Si la red está disponible.

</dd> <dt>

*attemptCount* \[ En\]
</dt> <dd>

¿Cuál es el intento?

</dd> <dt>

*maxAttemptCount* \[ En\]
</dt> <dd>

Se realizará el número máximo de intentos de reconexión.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|------------------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                           |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                                 |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl>         |
| IID<br/>                      | DIID \_ IRemoteDesktopClientEvents se define como 079863B7-6D47-4105-8BFE-0CDCB360E67D<br/> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**IRemoteDesktopClientEvents**](iremotedesktopclientevents.md)
</dt> </dl>

 

 





