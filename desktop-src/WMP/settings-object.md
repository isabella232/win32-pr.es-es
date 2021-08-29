---
title: Configuración Objeto (Reproductor de Windows Media SDK)
description: El Configuración objeto proporciona una manera de modificar varios valores Reproductor de Windows Media mediante las siguientes propiedades y métodos.
ms.assetid: f22e8c37-f0c6-4268-a6ed-ce03cff5f3e5
keywords:
- Configuración Objetos Reproductor de Windows Media
topic_type:
- apiref
api_name:
- Settings Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e763a4792530b3ab0809c33277bdf92dc90fe4c0251b3d329b4c3f3f36b55f85
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "120002365"
---
# <a name="settings-object"></a>Configuración Objeto

El **Configuración** objeto proporciona una manera de modificar varios valores Reproductor de Windows Media mediante las siguientes propiedades y métodos.

El **Configuración** objeto admite las siguientes propiedades.



| Propiedad                                                  | Descripción                                                                                                                      |
|-----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------|
| [Autostart](settings-autostart.md)                       | Especifica o recupera un valor que indica si el elemento multimedia actual comienza a reproducirse automáticamente.                           |
| [equilibrar](settings-balance.md)                           | Especifica o recupera el equilibrio estéreo actual.                                                                               |
| [Baseurl](settings-baseurl.md)                           | Especifica o recupera la dirección URL base usada para la resolución de rutas de acceso relativas con comandos de script de dirección URL insertados en archivos multimedia. |
| [defaultAudioLanguage](settings-defaultaudiolanguage.md) | Recupera el identificador de configuración regional (LCID) del idioma de audio predeterminado especificado en Reproductor de Windows Media.                          |
| [defaultFrame](settings-defaultframe.md)                 | Especifica o recupera el nombre del marco utilizado para mostrar una dirección URL que se recibe en un **evento ScriptCommand.**                |
| [enableErrorDialogs](settings-enableerrordialogs.md)     | Especifica o recupera un valor que indica si los cuadros de diálogo de error se muestran automáticamente.                                    |
| [invokeURLs](settings-invokeurls.md)                     | Especifica o recupera un valor que indica si los eventos de dirección URL deben iniciar un explorador web.                                        |
| [Isavailable](settings-isavailable.md)                   | Recupera si un tipo especificado de información está disponible o si se puede realizar una acción especificada.                           |
| [mediaAccessRights](settings-mediaaccessrights.md)       | Recupera un valor que indica los derechos concedidos actualmente para el acceso a la biblioteca.                                                    |
| [Mudo](settings-mute.md)                                 | Especifica o recupera un valor que indica si el audio está silenciado.                                                                |
| [playCount](settings-playcount.md)                       | Especifica o recupera el número de veces que se reproducirá un elemento multimedia.                                                               |
| [Tasa](settings-rate.md)                                 | Especifica o recupera la velocidad de reproducción actual.                                                                                |
| [volume](settings-volume.md)                             | Especifica o recupera el volumen actual.                                                                                       |



 

El **Configuración** objeto admite los métodos siguientes.



| Método                                                            | Descripción                                                 |
|-------------------------------------------------------------------|-------------------------------------------------------------|
| [getMode](settings-getmode.md)                                   | Determina si el modo de bucle o el modo aleatorio están activos. |
| [requestMediaAccessRights](settings-requestmediaaccessrights.md) | Solicita un nivel de acceso especificado a la biblioteca.        |
| [setMode](settings-setmode.md)                                   | Establece el modo de bucle o el modo aleatorio en activo o inactivo.   |



 

Se **Configuración** acceso al objeto a través de la propiedad siguiente.



| Object                      | Propiedad                        |
|-----------------------------|---------------------------------|
| [Reproductor](player-object.md) | [settings](player-settings.md) |



 

## <a name="see-also"></a>Vea también

<dl> <dt>

[**Referencia del modelo de objetos para scripting**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




