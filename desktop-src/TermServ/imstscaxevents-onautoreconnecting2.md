---
title: Método IMsTscAxEvents OnAutoReconnecting2
description: Se llama cuando un cliente está en proceso de volver a conectar automáticamente una sesión con un servidor Escritorio remoto host de sesión (host de sesión de Escritorio remoto). | Método IMsTscAxEvents OnAutoReconnecting2
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- Método OnAutoReconnecting2 Servicios de Escritorio remoto
- Método OnAutoReconnecting2 Servicios de Escritorio remoto , interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto método , OnAutoReconnecting2
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnAutoReconnecting2
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 194c21fc8ddc6f93ac4816752956f8de5a1d5df71b3af98ddadf8aba48e421a2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119512495"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a>Método IMsTscAxEvents::OnAutoReconnecting2

Se llama cuando un cliente está en proceso de volver a conectar automáticamente una sesión con un servidor Escritorio remoto host de sesión (host de sesión de Escritorio remoto). Se trata de una versión mejorada del [**método OnAutoReconnecting.**](-imstscaxevents--onautoreconnecting.md)

## <a name="syntax"></a>Sintaxis


```C++
void OnAutoReconnecting2(
  [in] LONG         disconnectReason,
  [in] VARIANT_BOOL networkAvailable,
  [in] LONG         attemptCount,
  [in] LONG         maxAttemptCount
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*disconnectReason* \[ En\]
</dt> <dd>

Código que describe el motivo de la última desconexión de sesión.

</dd> <dt>

*networkAvailable* \[ En\]
</dt> <dd>

Especifica si la red está disponible.

</dd> <dt>

*attemptCount* \[ En\]
</dt> <dd>

Número de intentos realizados en el proceso de reconexión automática actual. Este recuento aumenta en uno por cada intento realizado.

</dd> <dt>

*maxAttemptCount* \[ En\]
</dt> <dd>

Número máximo de intentos que se realizarán en el proceso de reconexión automática actual.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método no devuelve ningún valor.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows 8<br/>                                                                   |
| Servidor mínimo compatible<br/> | Windows Server 2012<br/>                                                         |
| Biblioteca de tipos<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**IMsTscAxEvents**](imstscaxevents-interface.md)
</dt> </dl>

 

 





