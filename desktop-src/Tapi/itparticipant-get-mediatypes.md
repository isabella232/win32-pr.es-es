---
description: El \_ método get MediaTypes obtiene los tipos de medios asociados a un participante.
ms.assetid: a2323d16-8eec-4c17-b5f2-b6fbd910ba60
title: 'Método ITParticipant:: get_MediaTypes (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e464295f58d72e0b905387f188dc2cf6da9ad609
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105678935"
---
# <a name="itparticipantget_mediatypes-method"></a>ITParticipant:: get \_ MediaTypes (método)

\[**obtener \_ MediaTypes** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **Get \_ MediaTypes** obtiene los [**tipos de medios**](tapimediatype--constants.md) asociados a un participante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_MediaTypes(
  [out] long *plMediaType
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*plMediaType* \[ enuncia\]
</dt> <dd>

Puntero a marcas de tipo de medio, como TAPIMEDIATYPE \_ video.

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>          | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No hay memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**\_puntero E**</dt> </dl>     | El parámetro *plMediaType* no es un puntero válido.<br/>  |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**tipos de medios**](tapimediatype--constants.md)
</dt> </dl>

 

 




