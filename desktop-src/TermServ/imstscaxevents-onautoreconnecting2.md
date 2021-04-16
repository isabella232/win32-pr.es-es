---
title: IMsTscAxEvents OnAutoReconnecting2, método
description: Se llama cuando un cliente está en el proceso de volver a conectar automáticamente una sesión con Escritorio remoto un servidor host de sesión de escritorio remoto (host de sesión de RD). | IMsTscAxEvents OnAutoReconnecting2, método
ms.assetid: 20F69798-5397-440C-9D0D-45AE417623A7
ms.tgt_platform: multiple
keywords:
- Método OnAutoReconnecting2 Servicios de Escritorio remoto
- Método OnAutoReconnecting2 Servicios de Escritorio remoto, interfaz IMsTscAxEvents
- Interfaz IMsTscAxEvents Servicios de Escritorio remoto, método OnAutoReconnecting2
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
ms.openlocfilehash: 901bb196922d1772782ab7f1c911c96573c88b36
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/09/2021
ms.locfileid: "105689814"
---
# <a name="imstscaxeventsonautoreconnecting2-method"></a>IMsTscAxEvents:: OnAutoReconnecting2 (método)

Se llama cuando un cliente está en el proceso de volver a conectar automáticamente una sesión con Escritorio remoto un servidor host de sesión de escritorio remoto (host de sesión de RD). Se trata de una versión mejorada del método [**OnAutoReconnecting**](-imstscaxevents--onautoreconnecting.md) .

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

*disconnectReason* \[ de\]
</dt> <dd>

Código que describe el motivo de la última desconexión de la sesión.

</dd> <dt>

*networkAvailable* \[ de\]
</dt> <dd>

Especifica si la red está disponible.

</dd> <dt>

*attemptCount* \[ de\]
</dt> <dd>

Número de intentos realizados en el proceso de reconexión automática actual. Este recuento se incrementa en uno por cada intento realizado.

</dd> <dt>

*maxAttemptCount* \[ de\]
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

 

 





