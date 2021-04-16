---
description: Manipula una descripción de la Conferencia textual.
ms.assetid: b9ce61d1-3fc5-4963-8d2f-586a4b6a159d
title: Interfaz ITConferenceBlob (Sdpblb. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c961b8fb006f1e172f82827216292cb9d12a158f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 03/22/2021
ms.locfileid: "105690436"
---
# <a name="itconferenceblob-interface"></a>Interfaz ITConferenceBlob

\[ Las interfaces y controles de conferencias de telefonía IP de encuentro no están disponibles para su uso en Windows Vista, Windows Server 2008 y las versiones posteriores del sistema operativo. La API de cliente de RTC proporciona una funcionalidad similar.\]

La interfaz **ITConferenceBlob** manipula una descripción de la Conferencia textual. La interfaz está pensada para ser independiente del formato y la sintaxis de la descripción de la Conferencia. Para manipular aspectos específicos de la descripción de la Conferencia, la aplicación debe consultar otra interfaz. Actualmente, solo se admiten las descripciones de la Conferencia SDP; la aplicación debe usar **QueryInterface** para [**ITSdp**](itsdp.md) para tener acceso a los distintos campos de la descripción de la Conferencia SDP. La interfaz **ITConferenceBlob** se crea llamando a **QueryInterface** en [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).

## <a name="members"></a>Miembros

La interfaz **ITConferenceBlob** hereda de la interfaz [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) . **ITConferenceBlob** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La interfaz **ITConferenceBlob** tiene estos métodos.



| Método                                                             | Descripción                                                                                                                                   |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**obtener \_ characterSet**](itconferenceblob-get-characterset.md)     | Obtiene el indicador del [**\_ \_ juego de caracteres de BLOB**](blob-character-set.md) de si los caracteres de BLOB están en ASCII, Unicode, etc.<br/> |
| [**obtener \_ ConferenceBlob**](itconferenceblob-get-conferenceblob.md) | Obtiene un puntero al BLOB de la Conferencia.<br/>                                                                                             |
| [**Smss**](itconferenceblob-init.md)                              | Inicializa el BLOB de la Conferencia.<br/>                                                                                                   |
| [**SetConferenceBlob**](itconferenceblob-setconferenceblob.md)    | Confirma los cambios en el BLOB de la Conferencia.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3,0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb. h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

