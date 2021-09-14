---
title: Función UninitializeNapAgentNotifier (NapUtil.h)
description: Cancela la suscripción del proceso de llamada a las notificaciones de cambio de estado de NapAgent y a las notificaciones de cambio de estado de cuarentena.
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- Función NAP uninitializeNapAgentNotifier
topic_type:
- apiref
api_name:
- UninitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5d68b43fba64be82908d73803113f871b08c93c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161236"
---
# <a name="uninitializenapagentnotifier-function"></a>Función UninitializeNapAgentNotifier

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **función UninitializeNapAgentNotifier** cancela la suscripción al proceso de llamada de las notificaciones de cambio de estado de NapAgent y las notificaciones de cambio de estado de cuarentena. El servicio NapAgent proporciona estas notificaciones.

## <a name="syntax"></a>Sintaxis


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*type* \[ En\]
</dt> <dd>

Valor [**napNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) que especifica el tipo de notificaciones de servicio de las que se cancela la suscripción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no tiene valores devueltos.

## <a name="remarks"></a>Observaciones

Esta función no es segura para los subprocesos.

Cada proceso suscrito a las notificaciones del  servicio NapAgent del tipo especificado debe llamar **a UninitializeNapAgentNotifier** para cancelar la suscripción a las notificaciones. Si un proceso se suscribe a más de un tipo de notificación, debe llamar a **UninitializeNapAgentNotifier** una vez para cada tipo de notificación.

Esta función producirá un error en modo silencioso si el proceso no había llamado previamente [**a InitializeNapAgentNotifier**](initializenapagentnotifier.md) para el tipo de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**InitializeNapAgentNotifier**](initializenapagentnotifier.md)
</dt> </dl>

 

 





