---
description: La interfaz ITParticipantControl se implementa mediante el MSP de IPConf.
ms.assetid: e617f2a4-6be8-4cb1-9f03-470c5100b834
title: Interfaz ITParticipantControl (Confpriv.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9e111a298069901a67d8b0ecbff365e0ab03f1885a247d41425afe7eb31085d5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774755"
---
# <a name="itparticipantcontrol-interface"></a>Interfaz ITParticipantControl

\[**ITParticipantControl** no está disponible para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz ITParticipantControl** se implementa mediante el MSP de IPConf. Esta interfaz se expone en el objeto de llamada. Esta interfaz permite a una aplicación recuperar punteros a los participantes en una conferencia. La **interfaz ITParticipantControl** se crea mediante una llamada **a QueryInterface** en [**ITCallInfo.**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)

## <a name="members"></a>Miembros

La **interfaz ITParticipantControl** hereda de la [**interfaz IUnknown.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **ITParticipantControl también** tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITParticipantControl** tiene estos métodos.



| Método                                                                      | Descripción                                                                                                                                                                 |
|:----------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EnumerateParticipants**](itparticipantcontrol-enumerateparticipants.md) | Enumera los participantes que participan actualmente en la conferencia.<br/>                                                                                                    |
| [**obtener \_ participantes**](itparticipantcontrol-get-participants.md)          | Crea una colección de participantes asociados a la conferencia actual. Se proporciona para aplicaciones cliente de Automation, como las escritas en Visual Basic.<br/> |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Header<br/>       | <dl> <dt>Confpriv.h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



 

