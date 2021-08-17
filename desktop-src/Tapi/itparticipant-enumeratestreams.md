---
description: El método EnumerateStreams enumera las secuencias actualmente con los participantes. Este método se proporciona para aplicaciones de C y C++. Las aplicaciones cliente de Automation, como las escritas en Visual Basic, deben usar el método get \_ Secuencias.
ms.assetid: 69db198d-fb4c-482b-bf49-5c636ac2f86b
title: Método ITParticipant::EnumerateStreams (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1ec901c81bb0df666877ee06462b88da965b41bedd961e71cebbf25cd78ee30
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140308"
---
# <a name="itparticipantenumeratestreams-method"></a>ItParticipant::EnumerateStreams (método)

\[**EnumerateStreams** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método EnumerateStreams** enumera las secuencias actualmente con los participantes. Este método se proporciona para aplicaciones de C y C++. Las aplicaciones cliente de Automation, como las escritas en Visual Basic, deben usar el [**método get \_ Secuencias.**](itparticipant-get-streams.md)

## <a name="syntax"></a>Sintaxis


```C++
HRESULT EnumerateStreams(
  [out] IEnumStream **ppEnumStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppEnumStream* \[ out\]
</dt> <dd>

Puntero al [**puntero de interfaz IEnumStream.**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                     | Significado                                                         |
|-------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>      | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl> | El *parámetro ppEnumStream* no es un puntero válido.<br/> |



 

## <a name="remarks"></a>Comentarios

TAPI llama al **método AddRef** en la [**interfaz IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream) devuelta por **ITParticipant::EnumerateStreams**. La aplicación debe llamar **a Release** en la **interfaz IEnumStream** para liberar recursos asociados a ella.

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                |
| Header<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**obtener \_ Secuencias**](itparticipant-get-streams.md)
</dt> <dt>

[**IEnumStream**](/windows/desktop/api/tapi3if/nn-tapi3if-ienumstream)
</dt> </dl>

 

 




