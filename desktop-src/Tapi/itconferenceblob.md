---
description: Manipula una descripción textual de la conferencia.
ms.assetid: b9ce61d1-3fc5-4963-8d2f-586a4b6a159d
title: Interfaz ITConferenceBlob (Sdpblb.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c961b8fb006f1e172f82827216292cb9d12a158f
ms.sourcegitcommit: d75fc10b9f0825bbe5ce5045c90d4045e3c53243
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/13/2021
ms.locfileid: "127068747"
---
# <a name="itconferenceblob-interface"></a>Interfaz ITConferenceBlob

\[Los controles e interfaces de conferencia de telefonía IP de Rendezvous no están disponibles para su uso en Windows Vista, Windows Server 2008 y versiones posteriores del sistema operativo. La API de cliente RTC proporciona una funcionalidad similar.\]

La **interfaz ITConferenceBlob** manipula una descripción textual de la conferencia. La interfaz está pensada para ser independiente del formato y la sintaxis de la descripción de la conferencia. Para manipular aspectos específicos de la descripción de la conferencia, la aplicación debe consultar otra interfaz. Actualmente, solo se admiten descripciones de conferencias de SDP; La aplicación debe usar **QueryInterface** para [**ITSdp para**](itsdp.md) acceder a los distintos campos de la descripción de la conferencia de SDP. La **interfaz ITConferenceBlob** se crea llamando a **QueryInterface** en [**ITDirectoryObject**](/windows/desktop/api/Rend/nn-rend-itdirectoryobject).

## <a name="members"></a>Members

La **interfaz ITConferenceBlob** hereda de la [**interfaz IDispatch.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **ITConferenceBlob** también tiene estos tipos de miembros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

La **interfaz ITConferenceBlob** tiene estos métodos.



| Método                                                             | Descripción                                                                                                                                   |
|:-------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------|
| [**get \_ CharacterSet**](itconferenceblob-get-characterset.md)     | Obtiene el [**indicador BLOB \_ CHARACTER \_ SET**](blob-character-set.md) de si los caracteres de blob están en ASCII, Unicode, y así sucesivamente.<br/> |
| [**get \_ ConferenceBlob**](itconferenceblob-get-conferenceblob.md) | Obtiene un puntero al blob de conferencia.<br/>                                                                                             |
| [**Init**](itconferenceblob-init.md)                              | Inicializa el blob de conferencia.<br/>                                                                                                   |
| [**SetConferenceBlob**](itconferenceblob-setconferenceblob.md)    | Confirma los cambios en el blob de conferencia.<br/>                                                                                            |



 

## <a name="requirements"></a>Requisitos



| Requisito | Value |
|-------------------------|---------------------------------------------------------------------------------------|
| Versión de TAPI<br/> | Requiere TAPI 3.0 o posterior<br/>                                                 |
| Encabezado<br/>       | <dl> <dt>Sdpblb.h</dt> </dl>   |
| Biblioteca<br/>      | <dl> <dt>Uuid.lib</dt> </dl>   |
| Archivo DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



 

