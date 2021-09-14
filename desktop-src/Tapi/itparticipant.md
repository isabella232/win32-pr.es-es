---
description: La interfaz ITParticipant se implementa mediante el MSP de IPConf. Permite a una aplicación recuperar información sobre los participantes de la conferencia y obtener punteros a las secuencias asociadas a esos participantes.
ms.assetid: 8c3edfc1-3165-48b7-9d83-8892c192498b
title: Interfaz ITParticipant (Ipmsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8b7aa9d845d8d2489be0850bcc3fcf3f93ccdac
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127160636"
---
# <a name="itparticipant-interface"></a>Interfaz ITParticipant

\[**ITParticipant** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz ITParticipant** se implementa mediante el [MSP de IPConf.](ipconf-msp.md) Permite a una aplicación recuperar información sobre los participantes de la conferencia y obtener punteros a las secuencias asociadas a esos participantes.

Esta interfaz se expone en el objeto de llamada cuando una llamada usa la conferencia IP. Un puntero se puede obtener llamando a **QueryInterface** mediante un [**puntero ITCallInfo.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)

## <a name="members"></a>Members

La **interfaz ITParticipant** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITParticipant** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITParticipant** tiene estos métodos.



| Método                                                                      | Descripción                                                                                                                                                             |
|:----------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateStreams**](itparticipant-enumeratestreams.md)                  | Enumera los flujos asociados al participante actual.<br/>                                                                                                  |
| [**obtener \_ MediaTypes**](itparticipant-get-mediatypes.md)                     | Obtiene los [**tipos de medios**](tapimediatype--constants.md) asociados a un participante.<br/>                                                                      |
| [**get \_ ParticipantTypedInfo**](itparticipant-get-participanttypedinfo.md) | Obtiene una representación BSTR del tipo de información necesario, como PTI \_ EMAILADDRESS.<br/>                                                                     |
| [**obtener \_ estado**](itparticipant-get-status.md)                             | Obtiene el estado del participante.<br/>                                                                                                                          |
| [**obtener \_ Secuencias**](itparticipant-get-streams.md)                           | Crea una colección de secuencias asociadas al participante actual. Se proporciona para aplicaciones cliente de Automation, como las escritas en Visual Basic.<br/> |
| [**put \_ Status**](itparticipant-put-status.md)                             | Establece si una secuencia asociada al participante está habilitada.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|--------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                |
| Encabezado<br/>       | <dl> <dt>Ipmsp.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>  |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>Consulte también

<dl> <dt>

[IPConf MSP](ipconf-msp.md)
</dt> <dt>

[IPConf MSP Interfaces](ipconf-msp-interfaces.md)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> </dl>

 

