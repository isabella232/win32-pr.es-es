---
title: Método IMsTscAxEvents OnAutoReconnecting
description: Se llama cuando un cliente está en proceso de volver a conectar automáticamente una sesión con un servidor Escritorio remoto de sesión (host de sesión de Escritorio remoto). | Método IMsTscAxEvents OnAutoReconnecting
ms.assetid: 9cb36052-8010-47df-bb46-f4ad81f47a73
ms.tgt_platform: multiple
keywords:
- Método OnAutoReconnecting Servicios de Escritorio remoto
- Método OnAutoReconnecting Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnAutoReconnecting
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a26bb57416cd73f6d838ab08167923c4900b7b923a6a6f411239bbacd3fdbac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119309145"
---
# <a name="imstscaxeventsonautoreconnecting-method"></a>Método IMsTscAxEvents::OnAutoReconnecting

Se llama cuando un cliente está en proceso de volver a conectar automáticamente una sesión con un servidor Escritorio remoto de sesión (host de sesión de Escritorio remoto).

## <a name="syntax"></a>Sintaxis


```C++
void OnAutoReconnecting(
  [in]  LONG                       disconnectReason,
  [in]  LONG                       attemptCount,
  [out] AutoReconnectContinueState *pArcContinueStatus
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*disconnectReason* \[ En\]
</dt> <dd>

Código que describe el motivo de la última desconexión de sesión.

</dd> <dt>

*attemptCount* \[ En\]
</dt> <dd>

Número de intentos realizados en el proceso de reconexión automática actual. Este recuento aumenta en uno por cada intento realizado.

</dd> <dt>

*pIqueContinueStatus* \[ out\]
</dt> <dd>

Puntero a un código devuelto que especifica el estado del proceso de reconexión automática. Este código se puede restablecer para cambiar el estado del proceso de reconexión automática actual.

Para obtener más información sobre cómo restablecer este código, consulte la sección Comentarios.

<dt>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>autoReconnectContinueAutomatic** (0)


</dt> <dd>

El proceso de reconexión se está produciendo automáticamente. Este es el valor predeterminado.

</dd> <dt>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>autoReconnectContinueStop** (1)


</dt> <dd>

Se ha detenido el proceso de reconexión.

</dd> <dt>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>autoReconnectContinueManual** ( 2)


</dt> <dd>

El proceso de reconexión se está produciendo manualmente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Comentarios

Implemente este método en el receptor de eventos para recibir una notificación de que el control restablece una conexión con un servidor host de sesión de Escritorio remoto.

Cuando se cambia el estado del proceso de reconexión automática estableciendo el valor del parámetro *pAsyncContinueStatus* en **autoReconnectContinueAutomatic,** este método funciona en un modo meramente de aviso. Los contenedores pueden escuchar este evento para recibir notificaciones de que el proceso de reconexión automática está en proceso. El control seguirá intentando volver a establecer automáticamente una conexión en función de su propio tiempo interno y recuentos de intentos. Se llama a este método durante cada intento de reconexión automática para notificar al contenedor.

Cuando se cambia el estado del proceso de reconexión automática estableciendo el valor del parámetro *pConnectContinueStatus* en **autoReconnectContinueStop,** se finalizará el intento de reconexión automática actual, se enviará una notificación de desconexión al contenedor y no se emitirán más notificaciones de reconexión automáticas.

> [!Note]  
> Use la [**propiedad EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) para habilitar o deshabilitar la reconexión automática.

 

Cuando se cambia el estado del proceso de reconexión automática estableciendo el valor del parámetro *pControlContinueStatus* en **autoReconnectContinueManual,** el contenedor controlará [](imstscax-disconnect.md) manualmente el proceso de reconexión automática llamando [**a Conectar**](imstscax-connect.md) para desencadenar un intento de conexión o Desconectar para cancelar el proceso de reconexión automática. Una vez establecido en este valor, el control dejará de realizar intentos  de reconexión automática y se convierte en la directiva del contenedor para realizar llamadas Conectar para desencadenar intentos de reconexión automática. Esto se hace cuando el contenedor proporciona un comportamiento personalizado de la interfaz de usuario para la reconexión automática, como reiniciar una conexión RAS o VPN descartada antes del proceso de reconexión automática.

Para obtener más información sobre Conexión web a Escritorio remoto, vea [Requisitos para Conexión web a Escritorio remoto](requirements-for-remote-desktop-web-connection.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Vista<br/>                                                               |
| Servidor mínimo compatible<br/> | Windows Server 2008<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





