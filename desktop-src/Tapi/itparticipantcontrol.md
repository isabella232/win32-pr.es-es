---
description: IPConf MSP implementa la interfaz ITParticipantControl.
ms.assetid: e617f2a4-6be8-4cb1-9f03-470c5100b834
title: Interfaz ITParticipantControl (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 96075748f0c35cbc5af3c6cd07277d15222e0658
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690491"
---
# <a name="itparticipantcontrol-interface"></a>Interfaz ITParticipantControl

\[**ITParticipantControl** no está disponible para su uso en Windows Vista, windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

IPConf MSP implementa la interfaz **ITParticipantControl** . Esta interfaz se expone en el objeto de llamada. Esta interfaz permite que una aplicación recupere punteros a los participantes de una conferencia. La interfaz **ITParticipantControl** se crea llamando a **QueryInterface** en [**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo).

## <a name="members"></a>Miembros

La interfaz **ITParticipantControl** hereda de la interfaz [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITParticipantControl** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITParticipantControl** tiene estos métodos.



| Método                                                                      | Descripción                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) | Enumera los participantes actualmente implicados en la Conferencia.<br/>                                                                                                    |
| [**obtener \_ participantes**](itparticipantcontrol-get-participants.md)          | Crea una colección de participantes asociados a la Conferencia actual. Se proporciona para las aplicaciones cliente de automatización, como las escritas en Visual Basic.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

