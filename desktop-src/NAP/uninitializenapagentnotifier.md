---
title: Función UninitializeNapAgentNotifier (NapUtil. h)
description: Cancela la suscripción del proceso de llamada de las notificaciones de cambio de estado de NapAgent y las notificaciones de cambio de estado de cuarentena.
ms.assetid: b676ee33-caf6-48f0-acf8-5be1b23c62fe
keywords:
- UninitializeNapAgentNotifier función NAP
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
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "104422175"
---
# <a name="uninitializenapagentnotifier-function"></a>UninitializeNapAgentNotifier función)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La función **UninitializeNapAgentNotifier** anula la suscripción del proceso de llamada de las notificaciones de cambio de estado NapAgent y las notificaciones de cambio de estado de cuarentena. Estas notificaciones las proporciona el servicio NapAgent.

## <a name="syntax"></a>Sintaxis


```C++
NAPAPI VOID WINAPI UninitializeNapAgentNotifier(
  _In_ NapNotifyType type
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo* \[ de de\]
</dt> <dd>

Valor [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) que especifica el tipo de notificaciones de servicio del que se va a cancelar la suscripción.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Esta función no tiene valores devueltos.

## <a name="remarks"></a>Observaciones

Esta función no es segura para los subprocesos.

Cada proceso suscrito a notificaciones de servicio de NapAgent del *tipo* especificado debe llamar a **UninitializeNapAgentNotifier** para cancelar la suscripción a las notificaciones. Si un proceso está suscrito a más de un tipo de notificación, debe llamar a **UninitializeNapAgentNotifier** una vez para cada tipo de notificación.

Esta función producirá un error en modo silencioso si el proceso no había llamado previamente a [**InitializeNapAgentNotifier**](initializenapagentnotifier.md) para el tipo de notificación.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**InitializeNapAgentNotifier**](initializenapagentnotifier.md)
</dt> </dl>

 

 





