---
title: Método IConnectionBrokerClient GetTargetInfo (Cbclient. h)
description: Solicita información sobre el equipo de destino al que se debe redirigir la conexión.
ms.assetid: 43970B06-8CBD-4204-94AE-090A63918A90
ms.tgt_platform: multiple
keywords:
- Método GetTargetInfo Servicios de Escritorio remoto
- Método GetTargetInfo Servicios de Escritorio remoto, interfaz IConnectionBrokerClient
- Interfaz IConnectionBrokerClient Servicios de Escritorio remoto, método GetTargetInfo
topic_type:
- apiref
api_name:
- IConnectionBrokerClient.GetTargetInfo
api_location:
- Cbclient.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 366bebf398c5c776e43d5cdee4b99e28e8c580fb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104533754"
---
# <a name="iconnectionbrokerclientgettargetinfo-method"></a>IConnectionBrokerClient:: GetTargetInfo (método)

Solicita información sobre el equipo de destino al que se debe redirigir la conexión. El redirector usa este método para obtener información de redirección de la solicitud de conexión entrante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT GetTargetInfo(
  [in]  CB_CONNECTION_INFO       *pConnectionInfo,
  [in]  DWORD                    Reserved,
  [in]  HANDLE                   hStatusEvent,
  [out] CB_TARGET_INFO           *pTargetInfo,
  [out] DWORD                    *pResult,
  [out] IConnectionBrokerRequest **ppCbReq
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pConnectionInfo* \[ de\]
</dt> <dd>

La dirección de una estructura de [**\_ \_ información de conexión CB**](cb-connection-info.md) que contiene información sobre la solicitud de conexión entrante.

</dd> <dt>

*Reservado* \[ de\]
</dt> <dd>

Este parámetro está reservado para un uso futuro y debe ser cero.

</dd> <dt>

*hStatusEvent* \[ de\]
</dt> <dd>

Identificador de un evento que se establecerá cada vez que se actualice el progreso de la solicitud. Usted es responsable de la creación y el cierre de este evento.

</dd> <dt>

*pTargetInfo* \[ enuncia\]
</dt> <dd>

Dirección de una estructura [**de \_ \_ información del destino CB**](cb-target-info.md) que recibe información sobre el equipo de destino al que se debe redirigir la conexión entrante. Dado que se trata de un método asincrónico, esta memoria debe permanecer disponible hasta que se complete la solicitud. Para obtener más información, vea la sección Comentarios.

</dd> <dt>

*pResult* \[ enuncia\]
</dt> <dd>

Dirección de una variable **DWORD** que recibe un código de resultado. Dado que se trata de un método asincrónico, esta memoria debe permanecer disponible hasta que se complete la solicitud. Para obtener más información, vea la sección Comentarios.

Este código de resultado será uno de los siguientes valores.

<dt>

0
</dt> <dd>

Correcto.

</dd> <dt>

0x0000400
</dt> <dd>

No se pudo encontrar el equipo de destino.

</dd> <dt>

0x0000401
</dt> <dd>

El equipo de destino no está disponible.

</dd> <dt>

0x0000402
</dt> <dd>

Error al cargar el equipo de destino.

</dd> <dt>

0x0000403
</dt> <dd>

Error al poner en conexión el equipo de destino.

</dd> <dt>

0x0000404
</dt> <dd>

Error al redirigir al equipo de destino.

</dd> <dt>

0x0000405
</dt> <dd>

Error al activar la máquina virtual.

</dd> <dt>

0x0000406
</dt> <dd>

Error al arrancar la máquina virtual.

</dd> <dt>

0x0000407
</dt> <dd>

Error al buscar la dirección IP de la máquina virtual.

</dd> <dt>

0x0000408
</dt> <dd>

El agente de sesión no encontró ningún equipo disponible en el grupo.

</dd> <dt>

0x0000409
</dt> <dd>

El agente de sesión canceló la conexión.

</dd> <dt>

0x0000410
</dt> <dd>

El agente de sesión no pudo validar la configuración de conexión.

</dd> </dl> </dd> <dt>

*ppCbReq* \[ enuncia\]
</dt> <dd>

Dirección de un puntero de interfaz [**IConnectionBrokerRequest**](iconnectionbrokerrequest.md) que se usa para obtener las actualizaciones de estado de una operación asincrónica. Esta interfaz se usa junto con el parámetro *hStatusEvent* para esperar y obtener los resultados de esta operación asincrónica.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Devuelve **E \_ pendiente** si se crea la solicitud asincrónica. De lo contrario, devuelve un código de error **HRESULT** .

## <a name="remarks"></a>Observaciones

Este método es asincrónico. Los parámetros *pTargetInfo* y *pResult* deben ser válidos hasta que el método [**IConnectionBrokerRequest:: CheckStatus**](iconnectionbrokerrequest-checkstatus.md) obtenga la **solicitud de \_ Estado CB \_ \_ completada**.

Para obtener más información sobre cómo usar este método, consulte [Cómo usar la API de cliente de conexión a escritorio remoto Broker](use-the-remote-desktop-connection-broker-client-api.md).

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                    |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                          |
| Encabezado<br/>                   | <dl> <dt>Cbclient. h</dt> </dl>   |
| Biblioteca<br/>                  | <dl> <dt>Cbclient. lib</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Cbclient.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IConnectionBrokerClient**](iconnectionbrokerclient.md)
</dt> </dl>

 

 





