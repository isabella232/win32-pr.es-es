---
description: El método get \_ Event obtiene un descriptor PARTICIPANT EVENT del tipo de evento que se ha \_ producido.
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: Método ITParticipantEvent::get_Event (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d45e8f6aab556eb1b6f5c6dc1b4b0cbadf9653e06fd77f4fb806b7ef89d7813
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118864706"
---
# <a name="itparticipanteventget_event-method"></a>ItParticipantEvent::get \_ (método)

\[**get \_ El** evento no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ Event** obtiene un descriptor [**PARTICIPANT \_ EVENT**](participant-event.md) del tipo de evento que se ha producido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Event(
  [out] PARTICIPANT_EVENT *pParticipantEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pParticipantEvent* \[ out\]
</dt> <dd>

Puntero a un descriptor [**\_ PARTICIPANT EVENT**](participant-event.md) del evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>      |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pParticipantEvent* no es un puntero válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**EVENTO \_ DE PARTICIPANTE**](participant-event.md)
</dt> </dl>

 

 




