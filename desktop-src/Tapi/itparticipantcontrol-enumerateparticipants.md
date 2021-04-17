---
description: El método EnumerateParticipants enumera los participantes asociados a la Conferencia actual.
ms.assetid: 90a2b5f1-8749-42cd-92d4-f5ee4e680eae
title: 'ITParticipantControl:: EnumerateParticipants (método) (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54079860a64f366826cda3a0339424148bff1214
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105689986"
---
# <a name="itparticipantcontrolenumerateparticipants-method"></a>ITParticipantControl:: EnumerateParticipants (método)

\[**EnumerateParticipants** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **EnumerateParticipants** enumera los participantes asociados a la Conferencia actual. Este método se proporciona para las aplicaciones de C y C++. Las aplicaciones cliente de automatización, como las escritas en Visual Basic, deben usar el método [**Get \_ participantes**](itparticipantcontrol-get-participants.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumerateParticipants(
  [out] IEnumParticipant **ppEnumParticipants
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnumParticipants* \[ enuncia\]
</dt> <dd>

Puntero a la interfaz [**IEnumParticipant**](ienumparticipant.md) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                          |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *ppEnumParticipants* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/>       |



 

## <a name="remarks"></a>Observaciones

TAPI llama al método **AddRef** en la interfaz [**IEnumParticipant**](ienumparticipant.md) devuelta por **ITParticipantControl:: EnumerateParticipants**. La aplicación debe llamar a **Release** en la interfaz **IEnumParticipant** para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipantControl**](itparticipantcontrol.md)
</dt> <dt>

[**obtener \_ participantes**](itparticipantcontrol-get-participants.md)
</dt> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




