---
title: Objeto Settings (SDK de Windows Media Player)
description: El objeto de configuración proporciona una manera de modificar diversas opciones de configuración de Windows Media Player mediante el uso de las siguientes propiedades y métodos.
ms.assetid: f22e8c37-f0c6-4268-a6ed-ce03cff5f3e5
keywords:
- Objeto de configuración Windows Media Player
topic_type:
- apiref
api_name:
- Settings Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d01a521dbccb351045f09dc15d71779fd9362cf4
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 11/12/2019
ms.locfileid: "103904271"
---
# <a name="settings-object"></a>Objeto de configuración

El objeto de **configuración** proporciona una manera de modificar diversas opciones de configuración de Windows Media Player mediante el uso de las siguientes propiedades y métodos.

El objeto de **configuración** admite las siguientes propiedades.



| Propiedad                                                  | Descripción                                                                                                                      |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Automáticamente](settings-autostart.md)                       | Especifica o recupera un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente.                           |
| [balancea](settings-balance.md)                           | Especifica o recupera el equilibrio estéreo actual.                                                                               |
| [baseURL](settings-baseurl.md)                           | Especifica o recupera la dirección URL base que se usa para la resolución de la ruta de acceso relativa con comandos de script de dirección URL que están incrustados en archivos multimedia. |
| [defaultAudioLanguage](settings-defaultaudiolanguage.md) | Recupera el identificador de configuración regional (LCID) del idioma de audio predeterminado especificado en Windows Media Player.                          |
| [defaultFrame](settings-defaultframe.md)                 | Especifica o recupera el nombre del marco que se usa para mostrar una dirección URL que se recibe en un evento **comando** .                |
| [enableErrorDialogs](settings-enableerrordialogs.md)     | Especifica o recupera un valor que indica si los cuadros de diálogo de error se muestran automáticamente.                                    |
| [invokeURLs](settings-invokeurls.md)                     | Especifica o recupera un valor que indica si los eventos de dirección URL deben iniciar un explorador Web.                                        |
| [isAvailable](settings-isavailable.md)                   | Recupera si un tipo de información especificado está disponible o se puede realizar una acción especificada.                           |
| [mediaAccessRights](settings-mediaaccessrights.md)       | Recupera un valor que indica los derechos concedidos actualmente para el acceso a la biblioteca.                                                    |
| [silenciar](settings-mute.md)                                 | Especifica o recupera un valor que indica si el audio está silenciado.                                                                |
| [playCount](settings-playcount.md)                       | Especifica o recupera el número de veces que se reproducirá un elemento multimedia.                                                               |
| [Rate](settings-rate.md)                                 | Especifica o recupera la velocidad de reproducción actual.                                                                                |
| [volume](settings-volume.md)                             | Especifica o recupera el volumen actual.                                                                                       |



 

El objeto de **configuración** admite los métodos siguientes.



| Método                                                            | Descripción                                                 |
|-------------------------------------------------------------------|-------------------------------------------------------------|
| [getMode](settings-getmode.md)                                   | Determina si el modo de bucle o el modo de orden aleatorio está activo. |
| [requestMediaAccessRights](settings-requestmediaaccessrights.md) | Solicita un nivel de acceso especificado a la biblioteca.        |
| [setMode](settings-setmode.md)                                   | Establece el modo de bucle o el modo de orden aleatorio en activo o inactivo.   |



 

Se tiene acceso al objeto de **configuración** a través de la propiedad siguiente.



| Object                      | Propiedad                        |
|-----------------------------|---------------------------------|
| [Reproductor](player-object.md) | [settings](player-settings.md) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




