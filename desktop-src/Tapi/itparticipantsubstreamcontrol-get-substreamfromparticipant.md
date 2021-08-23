---
description: El método get SubStreamFromParticipant permite que una aplicación detecte qué \_ substreams están asociadas a un participante determinado.
ms.assetid: d45cdd1d-13cf-433a-9b19-193d5c0cba11
title: Método ITParticipantSubStreamControl::get_SubStreamFromParticipant (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae40487bbef7e678722a2710d99bce9ed1ebe2f5192705f0a7dc03f86e10e421
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119621535"
---
# <a name="itparticipantsubstreamcontrolget_substreamfromparticipant-method"></a>ItParticipantSubStreamControl::get \_ SubStreamFromParticipant (método)

\[**get \_ SubStreamFromParticipant** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método get \_ SubStreamFromParticipant** permite que una aplicación detecte qué substreams están asociadas a un participante determinado.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT get_SubStreamFromParticipant(
  [in]  ITParticipant *pParticipant,
  [out] ITSubStream   **ppITSubStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pParticipant* \[ En\]
</dt> <dd>

Puntero a [**la interfaz ITParticipant.**](itparticipant.md)

</dd> <dt>

*ppITSubStream* \[ out\]
</dt> <dd>

Puntero a la matriz de punteros de interfaz [**ITParticipant.**](itparticipant.md)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                   | Descripción                                                                  |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>          | El método se realizó correctamente.<br/>                                                 |
| <dl> <dt>**PUNTERO \_ E**</dt> </dl>     | El *parámetro ppITSubStream* no es un puntero válido.<br/>             |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | El *parámetro pParticipant* no apunta a una interfaz válida.<br/> |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>  | No se pudo acceder a la información del participante de la secuencia.<br/>       |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | No existe memoria suficiente para realizar la operación.<br/>              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipantSubStreamControl**](itparticipantsubstreamcontrol.md)
</dt> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

