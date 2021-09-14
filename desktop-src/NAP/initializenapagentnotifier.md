---
title: Función InitializeNapAgentNotifier (NapUtil.h)
description: Suscribe el proceso de llamada a las notificaciones de cambio de estado de NapAgent y a las notificaciones de cambio de estado de cuarentena.
ms.assetid: 24180194-50d7-4f54-845d-25402af9cf9a
keywords:
- Función Nap de InitializeNapAgentNotifier
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
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127161270"
---
# <a name="initializenapagentnotifier-function"></a>Función InitializeNapAgentNotifier

> [!Note]  
> La plataforma de protección de acceso a redes no está disponible a partir de Windows 10

 

La **función InitializeNapAgentNotifier** suscribe el proceso de llamada a las notificaciones de cambio de estado de NapAgent y a las notificaciones de cambio de estado de cuarentena. El servicio NapAgent proporciona estas notificaciones.

## <a name="syntax"></a>Sintaxis


```C++
NAPAPI HRESULT WINAPI InitializeNapAgentNotifier(
  _In_ NapNotifyType type,
  _In_ HANDLE        hNotifyEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*type* \[ En\]
</dt> <dd>

Valor [**NapNotifyType**](/windows/win32/api/naptypes/ne-naptypes-napnotifytype) que especifica el tipo de notificaciones de servicio que se recibirán.

</dd> <dt>

*hNotifyEvent* \[ En\]
</dt> <dd>

Identificador de evento que se usa para la notificación. El autor de la llamada debe pasar un identificador abierto al *parámetro hNotifyEvent.* El autor de la llamada también debe cerrar el identificador de eventos cuando ya no sea necesario.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto



| Código devuelto                                                                                                | Descripción                                                                                               |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>                       | La inicialización se completó correctamente.<br/>                                                         |
| <dl> <dt>**E \_ FAIL**</dt> </dl>                     | Error de inicialización.<br/>                                                                         |
| <dl> <dt>**ERROR \_ YA \_ INICIALIZADO**</dt> </dl> | El proceso ya se ha suscrito a las notificaciones del servicio NapAgent del *tipo* especificado. <br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>               | Se pasó un argumento no válido. <br/>                                                               |



 

## <a name="remarks"></a>Observaciones

Esta función no es segura para los subprocesos.

Cada proceso que requiere una suscripción a las  notificaciones del servicio NapAgent del tipo especificado debe llamar a **InitializeNapAgentNotifier** para suscribirse a las notificaciones. Si un proceso debe suscribirse a más de un tipo de notificación, debe llamar a **InitializeNapAgentNotifier** una vez para cada tipo de notificación.

Una vez que un proceso no requiere más notificaciones, el proceso debe llamar a [**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md) para el tipo *especificado.*

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------------------|--------------------------------------------------------------------------------------|
| Cliente mínimo compatible<br/> | Windows Solo \[ aplicaciones de escritorio de Vista\]<br/>                                       |
| Servidor mínimo compatible<br/> | Windows Solo aplicaciones de escritorio de Server 2008 \[\]<br/>                                 |
| Encabezado<br/>                   | <dl> <dt>NapUtil.h</dt> </dl> |
| Archivo DLL<br/>                      | <dl> <dt>Qutil.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**UninitializeNapAgentNotifier**](uninitializenapagentnotifier.md)
</dt> </dl>

 

 





