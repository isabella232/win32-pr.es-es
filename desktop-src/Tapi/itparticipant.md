---
description: IPConf MSP implementa la interfaz ITParticipant. Permite que una aplicación recupere información sobre los participantes de la Conferencia y obtenga punteros a las secuencias asociadas a dichos participantes.
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: Interfaz ITParticipant (Ipmsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b7aa9d845d8d2489be0850bcc3fcf3f93ccdac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105680783"
---
# <a name="itparticipant-interface"></a>Interfaz ITParticipant

\[**ITParticipant** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

[IPCONF MSP](ipconf-msp.md)implementa la interfaz **ITParticipant** . Permite que una aplicación recupere información sobre los participantes de la Conferencia y obtenga punteros a las secuencias asociadas a dichos participantes.

Esta interfaz se expone en el objeto de llamada cuando una llamada utiliza la Conferencia de IP. Un puntero se puede obtener llamando a **QueryInterface** mediante un puntero [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo) .

## <a name="members"></a>Miembros

La interfaz **ITParticipant** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITParticipant** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITParticipant** tiene estos métodos.



| Método                                                                      | Descripción                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateStreams**](itparticipant-enumeratestreams.md)                  | Enumera las secuencias asociadas al participante actual.<br/>                                                                                                  |
| [**obtener \_ MediaTypes**](itparticipant-get-mediatypes.md)                     | Obtiene los [**tipos de medios**](tapimediatype--constants.md) asociados a un participante.<br/>                                                                      |
| [**obtener \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) | Obtiene una representación BSTR del tipo de información necesaria, como PTI \_ EmailAddress.<br/>                                                                     |
| [**obtener \_ Estado**](itparticipant-get-status.md)                             | Obtiene el estado del participante.<br/>                                                                                                                          |
| [**obtener \_ secuencias**](itparticipant-get-streams.md)                           | Crea una colección de secuencias asociadas al participante actual. Se proporciona para las aplicaciones cliente de automatización, como las escritas en Visual Basic.<br/> |
| [**Estado de put \_**](itparticipant-put-status.md)                             | Establece si una secuencia asociada al participante está habilitada.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                |
| Encabezado<br/>       | <dl> <dt>Ipmsp. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Vea también

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[Interfaces de IPConf MSP](ipconf-msp-interfaces.md)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 

