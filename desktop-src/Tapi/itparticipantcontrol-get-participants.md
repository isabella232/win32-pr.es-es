---
description: El método get \_ Participants crea una colección de participantes asociados a la conferencia actual.
ms.assetid: 643acc3f-3df1-4f3a-a8fe-5d46864f8cf7
title: Método ITParticipantControl::get_Participants (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6e4a99e0efe7702a3358684b00af5e8faa96461c
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160630"
---
# <a name="itparticipantcontrolget_participants-method"></a>ITParticipantControl::get \_ Participants (método)

\[**get \_ Los participantes** no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ Participants** crea una colección de participantes asociados a la conferencia actual. Este método se proporciona para aplicaciones cliente de Automation, como las escritas en Visual Basic. Las aplicaciones de C y C++ deben usar [**el método EnumerateParticipants.**](itparticipantcontrol-enumerateparticipants.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_Participants(
  [out] VARIANT *pVariant
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pVariant* \[ out\]
</dt> <dd>

Puntero a **VARIANT** que contiene [**itcollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection) de punteros de interfaz [**ITParticipant.**](itparticipant.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                         | Significado                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro pVariant* no es un puntero válido.<br/>     |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |



 

## <a name="remarks"></a>Observaciones

TAPI llama al **método AddRef** en la [**interfaz ITParticipant**](itparticipant.md) devuelta por **ITParticipantControl::get \_ Participants**. La aplicación debe llamar **a Release** en la **interfaz ITParticipant** para liberar recursos asociados a ella.

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

[**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md)
</dt> <dt>

[**ITCollection**](/windows/desktop/api/tapi3if/nn-tapi3if-itcollection)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> </dl>

 

 




