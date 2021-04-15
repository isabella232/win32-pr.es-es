---
title: Controlar la experiencia de reproducción
description: Controlar la experiencia de reproducción
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Listas de reproducción de metarchivo de Windows Media, controlar la reproducción
- listas de reproducción, controlar la reproducción
- listas de reproducción de metarchivos, controlar la reproducción
- Listas de reproducción de metarchivos de Windows Media, problemas de reproducción
- listas de reproducción, problemas de reproducción
- listas de reproducción de metarchivos, problemas de reproducción
- controlar la reproducción
- Windows Media Player, controlar la reproducción
- Windows Media Player, problemas de reproducción
- HTMLView, problemas de reproducción
- HTMLView, controlar la reproducción
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 6877b869be8ca38ef9266aedf9318103d0e547ca
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "105695384"
---
# <a name="controlling-the-playback-experience"></a>Controlar la experiencia de reproducción

En esta sección se tratan algunos de los problemas de reproducción que se pueden producir al usar la característica HTMLView.

## <a name="requiring-the-user-to-view-web-based-content"></a>Solicitar al usuario que vea el contenido basado en Web

Puede decidir que solo desea que los usuarios puedan disfrutar del contenido multimedia digital cuando también se muestre el contenido basado en Web de HTMLView. Puede incluir código de script en la Página Web de HTMLView que detiene la reproducción del contenido multimedia digital si el usuario cambia de la característica de **reproducción en curso** . Para ello, puede especificar un controlador de eventos para el evento **Unload** como parte del elemento **Body** , como se muestra en el siguiente código HTML:


```XML
<BODY onunload = "UnloadMe();">

```



Después, puede incluir código de script en la función de controlador de eventos para cerrar el archivo en el reproductor. En el siguiente código de ejemplo se hace esto:


```XML
function UnloadMe()
{
   Player.close();
}

```



Cuando el usuario cambia de la **reproducción** en curso haciendo clic en un botón para abrir otra característica de Windows Media Player, como la biblioteca, el reproductor cierra el explorador incrustado. Esto hace que se produzca el evento **OnUnload** , ejecutando el script en la función denominada **UnloadMe**. El método [Player. Close](player-close.md) detiene la reproducción y descarga el archivo multimedia digital actual. Para volver a ver el contenido, el usuario debe volver a abrir el archivo. ASX original. Esta técnica también detiene la reproducción cuando el usuario se desplaza fuera de la Página Web de HTMLView. Tenga en cuenta que esta técnica no puede impedir que el usuario vea el contenido multimedia digital cuando cambia al modo de máscara.

Recordará que el parámetro HTMLView se puede aplicar a cada elemento de **entrada** en un archivo. ASX. Puede aprovechar esta característica para asegurarse de que el contenido de HTMLView se muestra cada vez que se inicia un nuevo archivo multimedia digital. Para ello, asocie un elemento **param** para HTMLView con cada entrada de la lista de reproducción. ASX. Cuando se reproduce cada entrada, el reproductor vuelve al modo completo y muestra el contenido de HTMLView que especificó en la lista de reproducción.

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a>Los tipos de comandos URL y script de archivo están deshabilitados de forma predeterminada

Windows Media Player 9 series o posterior proporciona opciones de configuración que permiten al usuario especificar si los comandos de script y de tipo de archivo se pueden ejecutar. De forma predeterminada, ambos tipos de comando de script no se ejecutan. Si usa tipos de comandos de scripts personalizados, se seguirán ejecutando, independientemente de la configuración de usuario. Si debe usar comandos de script y de tipo de archivo, debe pedir al usuario que cambie la configuración. Para cambiar la configuración, haga clic en **herramientas**, **Opciones** y, a continuación, en **seguridad**.

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a>Al volver a abrir un HTMLView, no se recarga la página web

Cuando el usuario abre un archivo. ASX que incluye un parámetro HTMLView y, posteriormente, vuelve a abrir el mismo archivo, Windows Media Player no actualiza la Página Web de HTMLView. Esto también significa que si ha permitido a los usuarios salir de la Página Web de HTMLView, el reproductor no devuelve el explorador incrustado a la Página Web de HTMLView inicial.

## <a name="hiding-the-content-location"></a>Ocultar la ubicación del contenido

Puede decidir que no desea que Windows Media Player muestre la ubicación del contenido multimedia digital mientras se está reproduciendo un archivo. ASX. Normalmente, Windows Media Player solo muestra información sobre la lista de reproducción al transmitir contenido desde Internet. Sin embargo, hay pasos adicionales que puede seguir para evitar que los usuarios determinen la ubicación del contenido. Por ejemplo, una manera de asegurarse de que el reproductor no muestra la ruta de acceso al contenido es transmitir el contenido mediante listas de reproducción de Windows Media Services del servidor. De este modo, cuando el usuario ve las propiedades del contenido, ve la dirección URL del servidor y no la dirección URL de su contenido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mostrar páginas web en Windows Media Player**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Elemento PARAM**](param-element.md)
</dt> </dl>

 

 




