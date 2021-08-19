---
description: Obtenga información sobre cómo extender la cinta Windows Explorer.
title: Extensión de la cinta de opciones
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 0C043FF8-3862-4F02-8700-BB556C4F35B8
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 635698461f897a08248ea99bf68d534ea8ad24763f926460d2e9ce64181ba2a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "117860856"
---
# <a name="extending-the-ribbon"></a>Extensión de la cinta de opciones

En Windows Explorer, la cinta de opciones ayuda a facilitar y detectar actividades comunes de administración de archivos de usuario final, pero hay cambios para los desarrolladores de aplicaciones. Por ejemplo, la barra de comandos anterior era extensible libremente, pero la cinta de opciones está más restringida en este momento. Además, la cinta de opciones no se muestra de forma predeterminada para todas las extensiones de espacio de nombres, por lo que tiene que optar por obtener la cinta de opciones. De lo contrario, se obtiene la barra de comandos anterior.

Las acciones disponibles para los usuarios en la cinta de opciones se encuentran en tres categorías de extensibilidad:

-   No se necesita extensibilidad. Ejemplos: Copiar, Pegar, Eliminar. Windows estos verbos.
-   Actualmente no se permite la extensibilidad: ejemplos: Zip, Cerrar sesión y otras acciones personalizadas. Use el menú contextual para cubrir estos escenarios.
-   La extensibilidad está integrada en la propia acción. Ejemplos: Buscar, Correo electrónico, Imprimir, Nuevo elemento. Debe registrarse para que estos verbos incluyan el formato de aplicación o archivo en la cinta de opciones .

En este documento se describe cómo puede participar para obtener la cinta de opciones y cómo registrarse para controlar verbos específicos de la cinta de opciones.

## <a name="opting-in-to-the-ribbon"></a>Participar en la cinta de opciones

Para participar en la cinta de opciones, **la \_** implementación de [**IShellFolder2**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder2) debe especificar la cinta de EP en [**IExplorerPaneVisibility::GetPaneState**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iexplorerpanevisibility-getpanestate) y devolver **EPS \_ FORCE** \| **EPS \_ DEFAULT \_ ON**.

## <a name="extending-the-ribbon-for-file-extensions"></a>Extensión de la cinta de opciones para extensiones de archivo

Estos botones de la cinta de opciones son extensibles en función de las extensiones de archivo:

-   Extraer todo
-   Montaje \| de la grabación (iso)
-   Reproducir \| reproducir todo Agregar a lista de reproducción \| (verbo: Poner en cola)
-   Abrir
-   Editar
-   Propiedades

Cuando se registra para controlar estáticamente los verbos pertinentes para los nuevos tipos de archivo, la cinta de opciones controla los verbos correctamente. Se registra igual que lo haría para los verbos del menú contextual. Para obtener más información sobre las asociaciones de archivos y el registro de verbos, vea [Verbos y asociaciones](fa-verbs.md) de archivo y [Crear controladores de menús contextuales.](context-menu-handlers.md)

## <a name="registering-as-a-default-handler-for-actionids"></a>Registro como controlador predeterminado para ActionIds

En primer lugar, registre el ProgId en la subclave AssocActionId adecuada. Cada subclave AssocActionId representa un verbo o una acción que los usuarios pueden invocar desde la cinta de opciones. En este ejemplo, la aplicación se registra para zipSelection ActionID para extender el botón "Extraer todo" de la cinta de opciones.

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

Una vez completado el registro, debe registrarse para controlar los protocolos como lo haría normalmente, como se describe en [Programas predeterminados](default-programs.md).

 

 



