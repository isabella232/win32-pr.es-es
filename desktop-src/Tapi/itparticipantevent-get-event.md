---
description: El \_ método get Event obtiene un \_ descriptor de eventos de participante del tipo de evento que se ha producido.
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: 'Método ITParticipantEvent:: get_Event (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b6cbfcf709b1f9f3f49047504bf5d9e8c02b159
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690830"
---
# <a name="itparticipanteventget_event-method"></a>ITParticipantEvent:: get ( \_ método de eventos)

\[**obtener \_ El evento** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ Event** obtiene un descriptor de [**\_ eventos de participante**](participant-event.md) del tipo de evento que se ha producido.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Event(
  [out] PARTICIPANT_EVENT *pParticipantEvent
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pParticipantEvent* \[ enuncia\]
</dt> <dd>

Puntero a un descriptor de [**\_ eventos de participante**](participant-event.md) del evento.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/>      |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *pParticipantEvent* no es un puntero válido.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipantEvent**](itparticipantevent.md)
</dt> <dt>

[**evento de participante \_**](participant-event.md)
</dt> </dl>

 

 




