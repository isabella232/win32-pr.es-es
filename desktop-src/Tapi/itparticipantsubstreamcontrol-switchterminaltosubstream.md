---
description: El método SwitchTerminalToSubStream establece un terminal en la subsección participante.
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: Método ITParticipantSubStreamControl::SwitchTerminalToSubStream (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41f211d4f3ff0f01801fb5497d36d81fa46e43397d8b69227180b022c9e74a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774655"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a>ItParticipantSubStreamControl::SwitchTerminalToSubStream (método)

\[**SwitchTerminalToSubStream** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

El **método SwitchTerminalToSubStream** establece un terminal en la subsección participante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pITTerminal* \[ En\]
</dt> <dd>

Puntero a [**la interfaz ITTerminal.**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)

</dd> <dt>

*pITSubStream* \[ En\]
</dt> <dd>

Puntero a [**la interfaz ITSubStream.**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                     | Descripción                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ OK**</dt> </dl>            | El método se realizó correctamente.<br/>                                                                       |
| <dl> <dt>**E \_ UNEXPECTED**</dt> </dl>    | No se pudo acceder a la información del participante para la secuencia.<br/>                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>    | El *parámetro pParticipant* o *pITSubStream* no apunta a una interfaz válida.<br/> |
| <dl> <dt>**TAPI \_ E \_ NOITEMS**</dt> </dl> | La subsección no está lista.<br/>                                                             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | No existe memoria suficiente para realizar la operación.<br/>                                    |



 

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
</dt> <dt>

[**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal)
</dt> </dl>

 

