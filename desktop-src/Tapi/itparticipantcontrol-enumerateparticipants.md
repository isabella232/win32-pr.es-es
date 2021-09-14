---
description: El método EnumerateParticipants enumera los participantes asociados a la conferencia actual.
ms.assetid: 90a2b5f1-8749-42cd-92d4-f5ee4e680eae
title: Método ITParticipantControl::EnumerateParticipants (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54079860a64f366826cda3a0339424148bff1214
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160635"
---
# <a name="itparticipantcontrolenumerateparticipants-method"></a>ItParticipantControl::EnumerateParticipants (método)

\[**EnumerateParticipants** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método EnumerateParticipants** enumera los participantes asociados a la conferencia actual. Este método se proporciona para aplicaciones de C y C++. Las aplicaciones cliente de Automation, como las escritas en Visual Basic, deben usar el [**método get \_ Participants.**](itparticipantcontrol-get-participants.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumerateParticipants(
  [out] IEnumParticipant **ppEnumParticipants
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnumParticipants* \[ out\]
</dt> <dd>

Puntero a [**la interfaz IEnumParticipant.**](ienumparticipant.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                               |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                          |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro ppEnumParticipants* no es un puntero válido.<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>       |



 

## <a name="remarks"></a>Observaciones

TAPI llama al **método AddRef** en la [**interfaz IEnumParticipant devuelta**](ienumparticipant.md) por **ITParticipantControl::EnumerateParticipants**. La aplicación debe llamar **a Release** en la **interfaz IEnumParticipant** para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITParticipantControl**](itparticipantcontrol.md)
</dt> <dt>

[**obtener \_ participantes**](itparticipantcontrol-get-participants.md)
</dt> <dt>

[**IEnumParticipant**](ienumparticipant.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




