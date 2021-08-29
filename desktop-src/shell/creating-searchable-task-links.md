---
description: A Windows Vista, la vista Panel de control categoría proporciona vínculos de tarea debajo del icono de cada elemento de Panel de control como se muestra aquí.
ms.assetid: 54a03536-6fe6-4304-a555-58e5bca128b9
title: Crear vínculos de tareas que se pueden buscar para un elemento Panel de control búsqueda
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7be43d98ea6c0f1cdf2d9c399aa1377d6b7b46a36fed10b3d6a4796ce49f92d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943405"
---
# <a name="creating-searchable-task-links-for-a-control-panel-item"></a>Crear vínculos de tareas que se pueden buscar para un elemento Panel de control búsqueda

A Windows Vista, la vista Panel de control categoría proporciona vínculos de tarea debajo del icono de cada elemento de Panel de control como se muestra aquí.

![vínculos de tareas en la página de categorías de mantenimiento y sistema](images/controlpaneltasklinks.png)

Cuando un usuario escribe  texto en el cuadro Buscar de la esquina superior derecha de la ventana, los resultados de la búsqueda incluyen estos vínculos de tarea, como se muestra aquí para una búsqueda en la palabra "display".

![vínculos de tareas en los resultados de búsqueda del panel de control](images/controlpanelsearchresults.png)

Este tema trata lo siguiente:

-   [Procedimientos recomendados de Vínculo de tareas](#task-link-best-practices)
-   [Crear un archivo XML de tarea](#creating-a-task-xml-file)
-   [Localización de vínculos de tareas](#localizing-task-links)
-   [Palabras clave y búsqueda](#keywords-and-searching)
-   [Temas relacionados](#related-topics)

## <a name="task-link-best-practices"></a>Procedimientos recomendados de Vínculo de tareas

Se recomienda proporcionar vínculos de tareas para los elementos de Panel de control como ayuda a los usuarios que buscan funcionalidad. También es posible agregar palabras clave a los vínculos de tarea para que un usuario pueda encontrarlos incluso sin conocer el título o la terminología de una tarea.

Los mejores vínculos de tareas sirven para tres propósitos:

1.  Proporcione un acceso directo a la funcionalidad del Panel de control elemento.
2.  Proporcione palabras clave para que los usuarios puedan buscar con su propio lenguaje. Es posible que un usuario quiera escribir "compactación" porque conoce el término técnico. Un usuario puede escribir "DB too big" o "database filesize". Agregar palabras clave adecuadas a la tarea significa que los usuarios pueden encontrar su Panel de control elemento.
3.  Proporcione sugerencias sobre lo que hace Panel de control elemento. Cuando un usuario ve los vínculos debajo del icono de un elemento de Panel de control, puede obtener más información sobre para qué se usa el elemento de Panel de control que el nombre y el icono que solo puede proporcionar.

Los vínculos de tareas deben centrarse en el usuario final, no en la tecnología ni en las características. Por ejemplo, "Habilitar compactación de base de datos" sería una redacción mal escrita porque es una jerga técnica desconocida para la mayoría de los usuarios. "Hacer que mi archivo de base de datos sea más pequeño" es mejor porque menciona el objetivo final real del usuario en lugar del mecanismo para llegar allí. El objetivo no es simplificar en exceso, sino decir la tarea en términos de lo que el usuario quiere lograr.

## <a name="creating-a-task-xml-file"></a>Crear un archivo XML de tarea

Los vínculos de tareas se definen en un archivo XML. En esta sección se proporcionan los detalles de un archivo de .xml ejemplo que define tres vínculos de tarea para un elemento Panel de control denominado **Bloc de notas**. Define títulos, palabras clave y líneas de comandos para los vínculos de tarea. También se muestra cómo especificar qué vínculos de tarea aparecen en cada categoría. Un Panel de control que está registrado para aparecer en más de una categoría tiene la opción de mostrar vínculos diferentes en función de la categoría. Las explicaciones de los distintos elementos e información proporcionados se proporcionan como comentarios en el propio XML.


```
<?xml version="1.0" ?>
<applications xmlns="http://schemas.microsoft.com/windows/cpltasks/v1" 
              xmlns:sh="http://schemas.microsoft.com/windows/tasks/v1">
    
    <!-- Notepad -->
    <application id="{0052D9FC-6764-4D29-A66F-2F3BD9E2BB40}"> 
    <!-- This GUID must match the GUID you created for your Control Panel item,
         and registered in namespace -->
    
        <!-- Solitaire -->
        <sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
            <!-- This is a generated GUID, specific to this task link -->
            <sh:name>Play solitaire</sh:name>
            <sh:keywords>solitare;game;cards;ace;diamond;heart;club;single</sh:keywords>
            <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
        </sh:task>

        <!-- Task Manager -->
        <sh:task id="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}" needsElevation="true"> 
            <!-- This is a generated GUID, specific to this task link -->
            <!-- The needsElevation="true" attribute means that the task 
                 appears with a shield icon next to it. Adding this attribute 
                 does not cause the .exe to require elevation - it just adds an 
                 icon to tell users that the command already requires it -->
            <sh:name>See running processes</sh:name>
            <sh:keywords>taskmgr;taskman;running processes;threads;cpu;</sh:keywords>
            <sh:command>taskmgr.exe</sh:command>
        </sh:task>

        <!-- IE -->
        <sh:task id="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}">
            <sh:name>Open Internet Explorer</sh:name>
            <sh:keywords>IE;web;browser;net;Internet;ActiveX;plug-in;plugin</sh:keywords>
            <sh:command>iexplore.exe</sh:command>
        </sh:task>
        
        <!-- Category assignments -->

        <!-- Appearance and Personalization -->
        <category id="1"> 
        <!-- These idref attributes refer to the GUIDs of the tasks defined above. A maximum of five tasks are shown per category. -->
            <sh:task idref="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"/>   
            <sh:task idref="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}"/>
            <sh:task idref="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}"/>
        </category>
        
        <!-- Programs -->
        <category id="8"> 
            <sh:task idref="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}">
                <sh:name>Click here to play</sh:name>
                <!-- This overrides the defined text. When the Notepad Control 
                     Panel item appears in the Programs category, it uses the 
                     "Click here to play" text for this Solitaire link, instead 
                     of "Play solitaire". -->
            </sh:task>
            <sh:task idref="{BF46D6AA-B5E6-4EE1-9E5B-ED017272B9F9}"/>
            <sh:task idref="{DE3A6DCC-C18A-4BBF-9227-11856D7B4422}"/>
       </category>
   </application>
</applications>
```



> [!Note]  
> A partir de Windows 7, un elemento Panel de control se puede identificar por su nombre canónico en lugar de por su nombre ejecutable: el elemento **>sh:controlpanel** de<se puede usar en lugar de **<sh:command>**. El **<elemento sh:controlpanel**>también proporciona un atributo para especificar la página del elemento en el que debe abrirse. A continuación se muestra un ejemplo del **<elemento sh:controlpanel>** siguiente:

 


```
<sh:controlpanel name="Microsoft.Presentation" page="pageWallpaper"/>
```



## <a name="localizing-task-links"></a>Localización de vínculos de tareas

El texto de los títulos y palabras clave de los vínculos de tarea se puede almacenar en una tabla de cadenas del módulo Panel de control del elemento. En ese caso, el formato utilizado en el archivo XML se convierte en:


```
<sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
    <!-- This is a generated GUID, specific to this task link -->
    <sh:name>@myTextResources.dll,-100</sh:name>
    <sh:keywords>@myTextResources.dll,-101</sh:keywords>
    <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
</sh:task>
```



En este ejemplo, el texto del nombre de la tarea aparece en el identificador de recurso de cadena 100 en myTextResources.dll y el texto de las palabras clave aparece en el identificador de recurso de cadena 101.

## <a name="keywords-and-searching"></a>Palabras clave y búsqueda

La Panel de control búsqueda busca vínculos de tarea en función de su nombre y también de sus palabras clave. Coincide con cada palabra de la búsqueda con el prefijo de palabras en el nombre y las palabras clave. Por ejemplo, la cadena de consulta "cpu" coincidiría con la tarea "Ver procesos en ejecución" en el ejemplo anterior porque "cpu" está en la lista de palabras clave. La cadena de consulta "pro" también encontraría ese resultado porque la palabra de título "processes" comienza con esa cadena. Tenga en cuenta que la consulta solo coincide con prefijos. La cadena de consulta "rocess" no coincidiría con un resultado porque esa cadena, mientras que parte de la palabra de título "process", no comienza esa palabra.

Cuando una consulta de búsqueda contiene varios tokens, todos los tokens deben coincidir con el prefijo de alguna palabra clave o parte del título de la tarea para un resultado. La consulta "nivel de cpu" no coincidiría, porque "level" no está en el conjunto de palabras clave. La consulta "cpu run" daría un resultado, porque "cpu" coincide con una palabra clave y "run" es el prefijo de la palabra "running" en el título de la tarea.

Panel de control no proporciona automáticamente correcciones ortográficas ni variaciones, como plurales o guiones. Las coincidencias también no tienen en cuenta mayúsculas de minúsculas. Para asegurarse de que la lista de palabras clave es correcta, se recomienda proporcionar variaciones usted mismo, como para este vínculo de tarea que implica protectores de pantalla: "screensavers;screen-savers;screen savers;".

No es necesario agregar el singular "protector de pantalla", porque una consulta que encuentre "protectores de pantalla" también encontrará "protector de pantalla" debido a la coincidencia de prefijo. Un usuario que escriba incluso parte de la palabra, como "screensa", seguirá teniendo una coincidencia en un vínculo de tarea que tenga "protectores de pantalla" como palabra clave. En el caso de los idiomas en los que los formularios plurales cambian la palabra, es necesario colocar todos los formularios que un usuario podría esperar para escribir en las palabras clave.

Como convención, Microsoft ha omitido palabras pequeñas como "how do I" o "I want to" del conjunto de palabras clave. La expectativa es que la mayoría de los usuarios simplemente escriban las palabras más importantes, como "mouse", "contraste alto" o "controlador de vídeo" para obtener resultados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Panel de control elementos](control-panel-applications.md)
</dt> <dt>

[Directrices de la experiencia de usuario](user-experience-guidelines.md)
</dt> <dt>

[Registro de Panel de control elementos](registering-control-panel-items.md)
</dt> <dt>

[Uso de CPLApplet](using-cplapplet.md)
</dt> <dt>

[Panel de control de mensajes](message-processing.md)
</dt> <dt>

[Ejecución de Panel de control elementos](executing-control-panel-items.md)
</dt> <dt>

[Extender elementos de Panel de control sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Asignación de Panel de control categorías](assigning-control-panel-categories.md)
</dt> <dt>

[Acceso al Panel de control en modo Caja fuerte en Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



