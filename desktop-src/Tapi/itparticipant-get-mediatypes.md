---
description: El método get \_ MediaTypes obtiene los tipos de medios asociados a un participante.
ms.assetid: a2323d16-8eec-4c17-b5f2-b6fbd910ba60
title: Método ITParticipant::get_MediaTypes (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e464295f58d72e0b905387f188dc2cf6da9ad609
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160645"
---
# <a name="itparticipantget_mediatypes-method"></a>ItParticipant::get \_ MediaTypes (método)

\[**get \_ MediaTypes** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ MediaTypes** obtiene los [**tipos de medios**](tapimediatype--constants.md) asociados a un participante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MediaTypes(
  [out] long *plMediaType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*plMediaType* \[ out\]
</dt> <dd>

Puntero a marcas de tipo multimedia, como TAPIMEDIATYPE \_ VIDEO.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro plMediaType* no es un puntero válido.<br/>  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                |
| Encabezado<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**tipos de medios**](tapimediatype--constants.md)
</dt> </dl>

 

 




