---
title: Control de la experiencia de reproducción
description: Control de la experiencia de reproducción
ms.assetid: f130eee1-10ef-4cbe-b6ac-8ad24e1f0f34
keywords:
- Windows Listas de reproducción de metarchivo multimedia, controlar la reproducción
- listas de reproducción, controlar la reproducción
- listas de reproducción de metarchivo, controlar la reproducción
- Windows Listas de reproducción de metarchivo multimedia, problemas de reproducción
- listas de reproducción, problemas de reproducción
- listas de reproducción de metarchivo, problemas de reproducción
- controlar la reproducción
- Reproductor de Windows Media, controlar la reproducción
- Reproductor de Windows Media,problemas de reproducción
- HTMLView, problemas de reproducción
- HTMLView, controlar la reproducción
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: efca4d299edc40cfb94820fbb1aae7115329c0f3fcbd2859db0bbbc56d7a0d4d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "118341892"
---
# <a name="controlling-the-playback-experience"></a>Control de la experiencia de reproducción

En esta sección se de abordan algunos de los problemas de reproducción que pueden surgir al usar la característica HTMLView.

## <a name="requiring-the-user-to-view-web-based-content"></a>Requerir al usuario que vea contenido basado en web

Puede decidir que solo desea que los usuarios puedan disfrutar del contenido multimedia digital cuando también se muestre el contenido basado en web HTMLView. Puede incluir código de script en la página web HTMLView que detenga la reproducción del contenido multimedia digital si el usuario deja de usar la **característica Reproducción** ahora. Para ello, puede especificar un controlador de eventos para el evento **unload** como parte del elemento **BODY,** como se muestra en el código HTML siguiente:


```XML
<BODY onunload = "UnloadMe();">

```



A continuación, puede incluir código de script en la función de controlador de eventos para cerrar el archivo en el reproductor. El código de ejemplo siguiente hace esto:


```XML
function UnloadMe()
{
   Player.close();
}

```



Cuando el usuario  cambia de Reproducción ahora haciendo clic en un botón para abrir otra característica de Reproductor de Windows Media, como la biblioteca, el Reproductor cierra el explorador incrustado. Esto hace que se produzca el evento **onunload,** ejecutando el script en la función **denominada UnloadMe**. El [método Player.close](player-close.md) detiene la reproducción y descarga el archivo multimedia digital actual. Para volver a ver el contenido, el usuario debe volver a abrir el archivo .asx original. Esta técnica también detiene la reproducción cuando el usuario navega fuera de la página web HTMLView. Tenga en cuenta que esta técnica no puede impedir que el usuario vea el contenido multimedia digital cuando cambia al modo de máscara.

Recordará que el parámetro HTMLView se puede aplicar a cada **elemento ENTRY** de un archivo .asx. Puede aprovechar esta característica para asegurarse de que el contenido HTMLView se muestra cada vez que se inicia un nuevo archivo multimedia digital. Para ello, asocie un elemento **PARAM** para HTMLView a cada entrada de la lista de reproducción .asx. Cuando se reproduce cada entrada, el reproductor vuelve al modo completo y muestra el contenido HTMLView que especificó en la lista de reproducción.

## <a name="url-and-file-script-command-types-are-disabled-by-default"></a>Los tipos de comandos url y script FILE están deshabilitados de forma predeterminada

Reproductor de Windows Media serie 9 o posterior proporciona una configuración que permite al usuario especificar si los comandos de script de tipo URL y FILE pueden ejecutarse. De forma predeterminada, ambos tipos de comandos de script no se ejecutan. Si usa tipos de comandos de script personalizados, seguirán en ejecución, independientemente de la configuración de usuario. Si debe usar comandos de script de tipo URL y FILE, debe solicitar al usuario que cambie la configuración. Para cambiar la configuración, haga clic **en Herramientas**, después **en Opciones** y, a continuación, **en Seguridad.**

## <a name="reopening-an-htmlview-does-not-reload-the-webpage"></a>Al volver a abrir un htmlView no se vuelve a cargar la página web

Cuando el usuario abre un archivo .asx que incluye un parámetro HTMLView y, posteriormente, vuelve a abrir el mismo archivo, Reproductor de Windows Media actualiza la página web HTMLView. Esto también significa que si ha permitido a los usuarios salir de la página web HTMLView, el Reproductor no devuelve el explorador incrustado a la página web HTMLView inicial.

## <a name="hiding-the-content-location"></a>Ocultar la ubicación del contenido

Puede decidir que no desea que Reproductor de Windows Media la ubicación del contenido multimedia digital mientras reproduce un archivo .asx. Normalmente, Reproductor de Windows Media muestra información sobre la propia lista de reproducción al transmitir contenido desde Internet. Sin embargo, hay pasos adicionales que puede seguir para evitar que los usuarios determinen la ubicación del contenido. Por ejemplo, una manera de asegurarse de que el reproductor no muestra la ruta de acceso al contenido es transmitir el contenido mediante listas de reproducción Servicios de Windows Media servidor. De este modo, cuando el usuario ve las propiedades del contenido, ve la dirección URL del servidor y no la dirección URL del contenido.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[**Mostrar páginas web en Reproductor de Windows Media**](displaying-web-pages-in-windows-media-player.md)
</dt> <dt>

[**Elemento PARAM**](param-element.md)
</dt> </dl>

 

 




