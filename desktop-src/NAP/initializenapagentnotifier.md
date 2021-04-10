---
title: Función InitializeNapAgentNotifier (NapUtil. h)
description: Suscribe el proceso de llamada a las notificaciones de cambio de estado NapAgent y las notificaciones de cambio de estado de cuarentena.
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- InitializeNapAgentNotifier función NAP
topic_type:
- apiref
api_name:
- InitializeNapAgentNotifier
api_location:
- qutil.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f59c4c342f693038040f374bbdbcdb8ab226f74d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 12/12/2020
ms.locfileid: "103996175"
---
# <a name="initializenapagentnotifier-function"></a>InitializeNapAgentNotifier función)

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La función **InitializeNapAgentNotifier** suscribe el proceso de llamada a las notificaciones de cambio de estado NapAgent y notificaciones de cambio de estado de cuarentena. Estas notificaciones las proporciona el servicio NapAgent.

## <a name="syntax"></a>Sintaxis


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*tipo* \[ de de\]
</dt> <dd>

Valor [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) que especifica el tipo de notificaciones de servicio que se van a recibir.

</dd> <dt>

*hNotifyEvent* \[ de\]
</dt> <dd>

Identificador de eventos que se usa para la notificación. El autor de la llamada debe pasar un identificador abierto al parámetro *hNotifyEvent* . El llamador también debe cerrar el controlador de eventos cuando ya no se necesite.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto



| Código devuelto                                                                                                | Descripción                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>                       | La inicialización se completó correctamente.<br/>                                                         |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                     | Error de inicialización.<br/>                                                                         |
| <dl> <dt>**ERROR \_ ya \_ inicializado**</dt> </dl> | El proceso ya se ha suscrito a las notificaciones de servicio de NapAgent del *tipo* especificado. <br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Se pasó un argumento no válido. <br/>                                                               |



 

## <a name="remarks"></a>Observaciones

Esta función no es segura para los subprocesos.

Cada proceso que requiere una suscripción a las notificaciones de servicio de NapAgent del *tipo* especificado debe llamar a **InitializeNapAgentNotifier** para suscribirse a las notificaciones. Si un proceso debe suscribirse a más de un tipo de notificación, debe llamar a **InitializeNapAgentNotifier** una vez para cada tipo de notificación.

Una vez que un proceso no requiere más notificaciones, el proceso debe llamar a [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) para el *tipo* especificado.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Vista \[\]<br/>                                       |
| Servidor mínimo compatible<br/> | Solo aplicaciones de escritorio de Windows Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>NapUtil. h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md)
</dt> </dl>

 

 





