---
description: El método SwitchTerminalToSubStream establece un terminal en la subsecuencia del participante.
ms.assetid: 39e1d4b9-2e39-4b36-9a6a-89e41cd59153
title: 'ITParticipantSubStreamControl:: SwitchTerminalToSubStream (método) (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f10401b2cf1598c76537ebd3a7049d67bf0657
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105681241"
---
# <a name="itparticipantsubstreamcontrolswitchterminaltosubstream-method"></a>ITParticipantSubStreamControl:: SwitchTerminalToSubStream (método)

\[**SwitchTerminalToSubStream** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

El método **SwitchTerminalToSubStream** establece un terminal en la subsecuencia del participante.

## <a name="syntax"></a>Sintaxis


```C++
HRESULT SwitchTerminalToSubStream(
  [in] ITTerminal  *pITTerminal,
  [in] ITSubStream *pITSubStream
);
```



## <a name="parameters"></a>Parámetros

<dl> <dt>

*pITTerminal* \[ de\]
</dt> <dd>

Puntero a la interfaz [**ITTerminal**](/windows/win32/api/tapi3if/nn-tapi3if-itterminal) .

</dd> <dt>

*pITSubStream* \[ de\]
</dt> <dd>

Puntero a la interfaz [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) .

</dd> </dl>

## <a name="return-value"></a>Valor devuelto

Este método puede devolver uno de estos valores.



| Código devuelto                                                                                     | Descripción                                                                                        |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ correcto**</dt> </dl>            | El método se realizó correctamente.<br/>                                                                       |
| <dl> <dt>**E \_ inesperado**</dt> </dl>    | No se pudo tener acceso a la información de los participantes de la secuencia.<br/>                           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>    | Los parámetros *pParticipant* o *pITSubStream* no apuntan a una interfaz válida.<br/> |
| <dl> <dt>**\_elementos TAPI E \_ noitems**</dt> </dl> | La subsecuencia no está lista.<br/>                                                             |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>   | No hay memoria suficiente para realizar la operación.<br/>                                    |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
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

 

