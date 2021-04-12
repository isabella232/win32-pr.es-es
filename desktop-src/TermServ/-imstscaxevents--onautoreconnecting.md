---
title: IMsTscAxEvents OnAutoReconnecting, método
description: Se llama cuando un cliente está en el proceso de volver a conectar automáticamente una sesión con Escritorio remoto un servidor host de sesión de escritorio remoto (host de sesión de RD). | IMsTscAxEvents OnAutoReconnecting, método
ms.assetid: 9cb36052-8010-47df-bb46-f4ad81f47a73
ms.tgt_platform: multiple
keywords:
- Método OnAutoReconnecting Servicios de Escritorio remoto
- Método OnAutoReconnecting Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnAutoReconnecting
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
ms.openlocfilehash: 3435be46f2bb2c7bcf8ca662b039f3e5ef856d8b
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "104362296"
---
# <a name="imstscaxeventsonautoreconnecting-method"></a>IMsTscAxEvents:: OnAutoReconnecting (método)

Se llama cuando un cliente está en el proceso de volver a conectar automáticamente una sesión con Escritorio remoto un servidor host de sesión de escritorio remoto (host de sesión de RD).

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

*disconnectReason* \[ de\]
</dt> <dd>

Código que describe el motivo de la última desconexión de la sesión.

</dd> <dt>

*attemptCount* \[ de\]
</dt> <dd>

Número de intentos realizados en el proceso de reconexión automática actual. Este recuento se incrementa en uno por cada intento realizado.

</dd> <dt>

*pArcContinueStatus* \[ enuncia\]
</dt> <dd>

Puntero a un código devuelto que especifica el estado del proceso de reconexión automática. Este código se puede restablecer para cambiar el estado del proceso de reconexión automática actual.

Para obtener más información sobre cómo restablecer este código, consulte la sección Comentarios.

<dt>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>

<span id="autoReconnectContinueAutomatic"></span><span id="autoreconnectcontinueautomatic"></span><span id="AUTORECONNECTCONTINUEAUTOMATIC"></span>autoReconnectContinueAutomatic * * * (0)


</dt> <dd>

El proceso de reconexión se está produciendo automáticamente. Este es el valor predeterminado.

</dd> <dt>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>

<span id="autoReconnectContinueStop"></span><span id="autoreconnectcontinuestop"></span><span id="AUTORECONNECTCONTINUESTOP"></span>autoReconnectContinueStop * * * * (1)


</dt> <dd>

Se ha detenido el proceso de reconexión.

</dd> <dt>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>

<span id="autoReconnectContinueManual"></span><span id="autoreconnectcontinuemanual"></span><span id="AUTORECONNECTCONTINUEMANUAL"></span>autoReconnectContinueManual * * * * (2)


</dt> <dd>

El proceso de reconexión se está produciendo manualmente.

</dd> </dl> </dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="remarks"></a>Observaciones

Implemente este método en el receptor de eventos para recibir la notificación de que el control está reestableciendo una conexión con un servidor host de sesión de escritorio remoto.

Cuando se cambia el estado del proceso de reconexión automática estableciendo el valor del parámetro *pArcContinueStatus* en **autoReconnectContinueAutomatic**, este método funciona en un modo meramente consultivo. Los contenedores pueden escuchar este evento en busca de notificaciones que el proceso de reconexión automática está realizando. El control seguirá intentando volver a establecer automáticamente una conexión basándose en sus propios recuentos de tiempo internos e intentos. Se llama a este método durante cada intento de reconexión automática a fin de notificar al contenedor.

Cuando cambie el estado del proceso de reconexión automática estableciendo el valor del parámetro *pArcContinueStatus* en **autoReconnectContinueStop**, se terminará el intento de reconexión automática actual, se enviará una notificación de desconexión al contenedor y no se emitirá ninguna notificación de reconexión automática más.

> [!Note]  
> Use la propiedad [**EnableAutoReconnect**](imsrdpclientadvancedsettings2-enableautoreconnect.md) para habilitar o deshabilitar la reconexión automática.

 

Cuando se cambia el estado del proceso de reconexión automática estableciendo el valor del parámetro *pArcContinueStatus* en **autoReconnectContinueManual**, el contenedor controlará manualmente el proceso de reconexión automática mediante una llamada a [**Connect**](imstscax-connect.md) para desencadenar un intento de conexión o [**desconectar**](imstscax-disconnect.md) para cancelar el proceso de reconexión automática. Una vez establecido este valor, el control dejará de realizar los intentos de reconexión automática y se convertirá en la Directiva del contenedor para **realizar llamadas de conexión para** desencadenar los intentos de reconexión automática. Esto se hace cuando el contenedor proporciona el comportamiento de la interfaz de usuario personalizado para la reconexión automática, como reiniciar una conexión VPN o RAS quitada antes del proceso de reconexión automática.

Para obtener más información acerca de Conexión web a Escritorio remoto, consulte [Requirements for conexión web a escritorio remoto](requirements-for-remote-desktop-web-connection.md).

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

 

 





