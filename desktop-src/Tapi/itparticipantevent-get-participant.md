---
description: El \_ método get participante obtiene un puntero a una matriz de interfaces ITParticipant que representan los participantes implicados en el evento.
ms.assetid: 3c650715-b1c3-4f84-976a-2cb0f7f19f52
title: 'Método ITParticipantEvent:: get_Participant (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc5e9ee84bac69bd77237f1a50b9a008b2830258
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680402"
---
# <a name="itparticipanteventget_participant-method"></a>ITParticipantEvent:: get ( \_ método de participante)

\[**obtener \_ El participante** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ participante** obtiene un puntero a una matriz de interfaces [**ITParticipant**](itparticipant.md) que representan los participantes implicados en el evento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Participant(
  [out] ITParticipant **ppParticipant
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppParticipant* \[ enuncia\]
</dt> <dd>

Puntero a la matriz de interfaces [**ITParticipant**](itparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                           | Significado                                                          |
|-------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>            | El método se realizó correctamente.<br/>                                     |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | No hay memoria suficiente para realizar la operación.<br/>  |
| <dl> <dt>**\_elementos TAPI E \_ noitems**</dt> </dl> | No hay participantes asociados al evento.<br/>  |
| <dl> <dt>**\_puntero E**</dt> </dl>       | El parámetro *ppParticipant* no es un puntero válido.<br/> |



 

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

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




