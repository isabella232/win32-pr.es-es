---
description: Obtenga información acerca de cómo extender la cinta de opciones del explorador de Windows.
title: Extender la cinta de opciones
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 6a0a3af3ac21e0bac0471bc9a987849536303556
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "104540454"
---
# <a name="extending-the-ribbon"></a>Extender la cinta de opciones

En el explorador de Windows, la cinta de opciones facilita más la detección de las actividades comunes de administración de archivos de usuario final, pero hay cambios afoot para los desarrolladores de aplicaciones. Por ejemplo, la antigua barra de comandos era extensible pero la cinta de opciones está más restringida en este momento. Además, la cinta no se muestra de forma predeterminada para todas las extensiones de espacio de nombres, por lo que tiene que optar por obtener la cinta de opciones. de lo contrario, obtendrá la barra de comandos anterior.

Las acciones disponibles para los usuarios de la cinta de opciones se dividen en tres categorías de extensibilidad:

-   No es necesaria la extensibilidad. Ejemplos: copiar, pegar y eliminar. Windows controla estos verbos automáticamente.
-   Actualmente no se permite la extensibilidad: ejemplos: zip, cerrar sesión y otras acciones personalizadas. Use el menú contextual para cubrir estos escenarios.
-   La extensibilidad está integrada en la propia acción. Ejemplos: buscar, correo electrónico, imprimir, nuevo elemento. Debe registrar estos verbos para incluir la aplicación o el formato de archivo en la cinta de opciones.

En este documento se describe cómo puede participar para obtener la cinta de opciones y cómo registrarse para administrar verbos de la cinta de opciones específicos.

## <a name="opting-in-to-the-ribbon"></a>Participar en la cinta de opciones

Para participar en la cinta de opciones, la implementación de [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) debe especificar la **\_ cinta de EP** en [**IExplorerPaneVisibility:: GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) y devolver el **\_** \| **\_ valor predeterminado \_ de EPS de** la fuerza EPS en.

## <a name="extending-the-ribbon-for-file-extensions"></a>Extender la cinta de opciones para extensiones de archivo

Estos botones de la cinta son extensibles en función de las extensiones de archivo:

-   Extraer todo
-   Montaje de la \| grabación (ISO)
-   Reproducir \| todo \| Agregar a lista de reproducción (verbo: enqueue)
-   Abrir
-   Editar
-   Propiedades

Cuando se registra para controlar estáticamente los verbos relevantes para los nuevos tipos de archivo, la cinta de opciones controla los verbos de manera adecuada. Se registra del mismo modo que lo haría para los verbos de menú contextual. Para obtener más información sobre las asociaciones de archivos y el registro de verbos, vea [verbos y asociaciones de archivos](fa-verbs.md) y [crear controladores de menús contextuales](context-menu-handlers.md).

## <a name="registering-as-a-default-handler-for-actionids"></a>Registro como controlador predeterminado para ActionIds

En primer lugar, registre el identificador de programa en la subclave AssocActionId adecuada. Cada subclave AssocActionId representa un verbo o una acción que los usuarios pueden invocar desde la cinta de opciones. En este ejemplo, la aplicación se registra para el ZipSelection ActionID para extender el botón "extraer todo" en la cinta de opciones.

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Classes
         Explorer.AssocActionId.ZipSelection
            shell
               open
                  command
                     (Default) = %SystemRoot%\[Your App].exe
      Microsoft
         Windows
            CurrentVersion
               Your App Name
                  Capabilities
                     URL Protocol
                     FriendlyTypeName = @%SystemRoot%\explorer.exe,-1234
```

Una vez completado el registro, debe registrarse para controlar los protocolos de la manera habitual, tal como se describe en [programas predeterminados](default-programs.md).

 

 



