---
description: El método EnumerateStreams enumera las secuencias actualmente con los participantes. Este método se proporciona para las aplicaciones de C y C++. Las aplicaciones cliente de automatización, como las escritas en Visual Basic, deben usar el \_ método get streams.
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: 'ITParticipant:: EnumerateStreams (método) (Ipmsp. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fbc92c617ed4baee3ecc33aec65cbdcf50986a27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690622"
---
# <a name="itparticipantenumeratestreams-method"></a>ITParticipant:: EnumerateStreams (método)

\[**EnumerateStreams** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **EnumerateStreams** enumera las secuencias actualmente con los participantes. Este método se proporciona para las aplicaciones de C y C++. Las aplicaciones cliente de automatización, como las escritas en Visual Basic, deben usar el método [**Get \_ streams**](itparticipant-get-streams.md) .

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnumStream* \[ enuncia\]
</dt> <dd>

Puntero al puntero de la interfaz [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                     | Significado                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>      | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**\_puntero E**</dt> </dl> | El parámetro *ppEnumStream* no es un puntero válido.<br/> |



 

## <a name="remarks"></a>Observaciones

TAPI llama al método **AddRef** en la interfaz [**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) devuelta por **ITParticipant:: EnumerateStreams**. La aplicación debe llamar a **Release** en la interfaz **IEnumStream** para liberar recursos asociados a ella.

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

[**obtener \_ secuencias**](itparticipant-get-streams.md)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




