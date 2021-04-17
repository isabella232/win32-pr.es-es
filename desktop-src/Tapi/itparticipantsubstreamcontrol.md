---
description: IPConf MSP implementa la interfaz ITParticipantSubStreamControl.
ms.assetid: d5af0fb1-af18-4efb-9b68-1fa60c1272f6
title: Interfaz ITParticipantSubStreamControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 799b1a85c6619e1175e620f2c5c5ef851005ba50
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105691072"
---
# <a name="itparticipantsubstreamcontrol-interface"></a>Interfaz ITParticipantSubStreamControl

\[**ITParticipantSubStreamControl** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

IPConf MSP implementa la interfaz **ITParticipantSubStreamControl** . Esta interfaz se expone en el objeto de llamada. Esta interfaz proporciona métodos que permiten a una aplicación detectar o controlar la coincidencia del subflujo con el participante. La interfaz **ITParticipantSubStreamControl** se crea llamando a **QueryInterface** en [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).

## <a name="members"></a>Miembros

La interfaz **ITParticipantSubStreamControl** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITParticipantSubStreamControl** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITParticipantSubStreamControl** tiene estos métodos.



| Método                                                                                              | Descripción                                                     |
|:----------------------------------------------------------------------------------------------------|:----------------------------------------------------------------|
| [**obtener \_ ParticipantFromSubStream**](itparticipantsubstreamcontrol-get-participantfromsubstream.md) | Obtiene los participantes asociados a un subflujo determinado.<br/> |
| [**obtener \_ SubStreamFromParticipant**](itparticipantsubstreamcontrol-get-substreamfromparticipant.md) | Obtiene subsecuencias asociadas a un participante determinado.<br/> |
| [**SwitchTerminalToSubStream**](itparticipantsubstreamcontrol-switchterminaltosubstream.md)        | Establece un participante en una subsecuencia.<br/>                   |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Vea también

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> </dl>

 

