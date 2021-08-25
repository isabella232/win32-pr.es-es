---
description: La interfaz ITParticipantSubStreamControl se implementa mediante el MSP de IPConf.
ms.assetid: d5af0fb1-af18-4efb-9b68-1fa60c1272f6
title: Interfaz ITParticipantSubStreamControl (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e910022d45ca9f9516adbe8aeebbdb172d66f28ab1bf8cb23219c2eee80f56cf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774605"
---
# <a name="itparticipantsubstreamcontrol-interface"></a>Interfaz ITParticipantSubStreamControl

\[**ITParticipantSubStreamControl** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz ITParticipantSubStreamControl** se implementa mediante el MSP de IPConf. Esta interfaz se expone en el objeto de llamada. Esta interfaz proporciona métodos que permiten a una aplicación detectar o controlar la coincidencia de substream con el participante. La **interfaz ITParticipantSubStreamControl** se crea llamando **a QueryInterface** en [**ITCallInfo.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)

## <a name="members"></a>Miembros

La **interfaz ITParticipantSubStreamControl** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITParticipantSubStreamControl** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITParticipantSubStreamControl** tiene estos métodos.



| Método                                                                                              | Descripción                                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**get \_ ParticipantFromSubStream**](itparticipantsubstreamcontrol-get-participantfromsubstream.md) | Obtiene los participantes asociados a una subsección determinada.<br/> |
| [**get \_ SubStreamFromParticipant**](itparticipantsubstreamcontrol-get-substreamfromparticipant.md) | Obtiene las subrecciones asociadas a un participante determinado.<br/> |
| [**SwitchTerminalToSubStream**](itparticipantsubstreamcontrol-switchterminaltosubstream.md)        | Establece un participante en una subsección.<br/>                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

