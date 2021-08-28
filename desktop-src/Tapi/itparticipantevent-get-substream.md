---
description: Get SubStream obtiene un puntero a una matriz de interfaces ITSubStream que representan las \_ substreams implicadas en el evento.
ms.assetid: 0af9097a-2481-4543-bb3d-35ccd352e992
title: Método ITParticipantEvent::get_SubStream (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f258f68815a5bc7cd201d94ab55199d59ebe6759eb2e279a1c80add91ea6c3d6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774665"
---
# <a name="itparticipanteventget_substream-method"></a>ItParticipantEvent::get \_ SubStream (método)

\[**get \_ SubStream** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

Get **\_ SubStream** obtiene un puntero a una matriz de interfaces [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) que representan las substreams implicadas en el evento.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SubStream(
  [out] ITSubStream **ppSubStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*ppSubStream* \[ out\]
</dt> <dd>

Puntero a la matriz [**de punteros ITSubStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Value                                                                                           | Significado                                                         |
|-------------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | El método se realizó correctamente.<br/>                                    |
| <dl> <dt>**TAPI \_ E \_ NOITEMS**</dt> </dl> | No hay substreams asociados al evento.<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | No existe memoria suficiente para realizar la operación.<br/> |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>       | El *parámetro ppSubStream* no es un puntero válido.<br/>  |



 

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

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

