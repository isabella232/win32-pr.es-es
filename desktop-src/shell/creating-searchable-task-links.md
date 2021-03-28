---
description: A partir de Windows Vista, la vista de categorías del panel de control proporciona vínculos a tareas bajo cada icono de elemento del panel de control, como se muestra aquí.
ms.assetid: 54a03536-6fe6-4304-a555-58e5bca128b9
title: Crear vínculos de tarea que se pueden buscar para un elemento del panel de control
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b4e98e8a6e07f84e8012b58cefe8e0d249fc069
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/07/2021
ms.locfileid: "103907729"
---
# <a name="creating-searchable-task-links-for-a-control-panel-item"></a>Crear vínculos de tarea que se pueden buscar para un elemento del panel de control

A partir de Windows Vista, la vista de categorías del panel de control proporciona vínculos a tareas bajo cada icono de elemento del panel de control, como se muestra aquí.

![vínculos de tareas en la página categoría del sistema y mantenimiento](images/controlpaneltasklinks.png)

Cuando un usuario escribe texto en el cuadro de **búsqueda** en la esquina superior derecha de la ventana, los resultados de la búsqueda incluyen estos vínculos de tarea, tal como se muestra aquí para buscar la palabra "Mostrar".

![vínculos de tarea en los resultados de la búsqueda del panel de control](images/controlpanelsearchresults.png)

Este tema trata lo siguiente:

-   [Prácticas recomendadas de vínculo de tareas](#task-link-best-practices)
-   [Crear un archivo XML de tarea](#creating-a-task-xml-file)
-   [Localizar vínculos de tareas](#localizing-task-links)
-   [Palabras clave y búsqueda](#keywords-and-searching)
-   [Temas relacionados](#related-topics)

## <a name="task-link-best-practices"></a>Prácticas recomendadas de vínculo de tareas

Se recomienda que proporcione vínculos de tareas para los elementos del panel de control como ayuda para que los usuarios busquen la funcionalidad. También es posible agregar palabras clave a los vínculos de tarea para que los usuarios puedan encontrarlos incluso sin conocer la terminología o el título de una tarea.

Los vínculos de tarea mejores sirven para tres propósitos:

1.  Proporcione un acceso directo a la funcionalidad del elemento del panel de control.
2.  Proporcione palabras clave para que los usuarios puedan realizar búsquedas con su propio idioma. Es posible que un usuario desee escribir "compactación" porque conoce el término técnico. Un usuario puede escribir "BD demasiado grande" o "archivo de base de datos". Agregar las palabras clave adecuadas a la tarea significa que los usuarios pueden encontrar el elemento del panel de control.
3.  Proporcione sugerencias sobre lo que hace el elemento del panel de control. Cuando un usuario ve los vínculos situados debajo del icono de un elemento del panel de control, puede obtener más información sobre el uso del elemento del panel de control en lugar del nombre y el icono que puede proporcionar.

Los vínculos de tareas deben ser centrados en el usuario final, no en la tecnología o en las características. Por ejemplo, "habilitar la compactación de la base de datos" sería un mal texto, ya que no está familiarizado con la mayoría de los usuarios. "Hacer que el archivo de base de datos sea más pequeño" es mejor porque menciona el objetivo real del usuario en lugar del mecanismo que debe obtenerse. El objetivo no es sobresimplificar, sino que es decir, la tarea en lo que se refiere a lo que el usuario desea realizar.

## <a name="creating-a-task-xml-file"></a>Crear un archivo XML de tarea

Los vínculos de tareas se definen en un archivo XML. En esta sección se proporcionan los detalles de un archivo. XML de ejemplo que define tres vínculos de tarea para un elemento del panel de control denominado **Bloc de notas**. Define títulos, palabras clave y las líneas de comandos para los vínculos de tarea. También se muestra cómo especificar los vínculos de tarea que aparecen debajo de la categoría. Un elemento del panel de control que se registra para aparecer en más de una categoría tiene la opción de mostrar distintos vínculos en función de la categoría. Las explicaciones de los distintos elementos e información proporcionada se proporcionan como comentarios en el propio XML.


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
> A partir de Windows 7, un elemento del panel de control puede identificarse por su nombre canónico en lugar de su nombre de archivo ejecutable: el elemento **<SH: controlpanel>** puede usarse en lugar de **<sh: Command>**. El elemento **<SH: controlpanel>** también proporciona un atributo para especificar la página del elemento al que debe abrirse. A continuación se muestra un ejemplo del elemento **<SH: controlpanel>** :

 


```
<sh:controlpanel name="Microsoft.Presentation" page="pageWallpaper"/>
```



## <a name="localizing-task-links"></a>Localizar vínculos de tareas

El texto de los títulos y palabras clave de los vínculos de tarea se puede almacenar en una tabla de cadenas en el módulo del elemento del panel de control. En ese caso, el formato utilizado en el archivo XML se convierte en:


```
<sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
    <!-- This is a generated GUID, specific to this task link -->
    <sh:name>@myTextResources.dll,-100</sh:name>
    <sh:keywords>@myTextResources.dll,-101</sh:keywords>
    <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
</sh:task>
```



En este ejemplo, el texto del nombre de la tarea aparece en el ID. de recurso de cadena 100 en myTextResources.dll y el texto de las palabras clave aparece en el ID. de recurso de cadena 101.

## <a name="keywords-and-searching"></a>Palabras clave y búsqueda

La búsqueda del panel de control encuentra los vínculos de tarea en función de su nombre y también de sus palabras clave. Coincide con cada palabra de la búsqueda con el prefijo de las palabras en el nombre y las palabras clave. Por ejemplo, la cadena de consulta "CPU" coincidiría con la tarea "ver procesos en ejecución" en el ejemplo anterior porque "CPU" está en la lista de palabras clave. La cadena de consulta "Pro" también encontraría el resultado porque la palabra de título "procesos" comienza con esa cadena. Tenga en cuenta que la consulta solo coincide con los prefijos. La cadena de consulta "rador" no coincidiría con un resultado porque esa cadena, mientras que parte de la palabra de título "proceso", no comienza con esa palabra.

Cuando una consulta de búsqueda contiene varios tokens, todos los tokens deben coincidir con el prefijo de alguna palabra clave o parte del título de la tarea para obtener un resultado. La consulta "nivel de CPU" no coincidiría, porque "LEVEL" no está en el conjunto de palabras clave. La consulta "CPU Run" daría como resultado, porque "CPU" coincide con una palabra clave y "Run" es el prefijo de la palabra "Running" en el título de la tarea.

En el panel de control no se proporciona automáticamente corrección ortográfica ni variaciones como plurales o guiones. Las coincidencias tampoco distinguen mayúsculas de minúsculas. Para asegurarse de que la lista de palabras clave sea correcta, se recomienda proporcionar variaciones, como para este vínculo de tarea que implique protectores de pantalla: "protectores de pantalla; protectores de pantalla; protectores de pantalla;"

No es necesario agregar el "protector de la" singular, ya que una consulta que busca "protectores de la" también encontrará "protector de la búsqueda" debido a la coincidencia de prefijo. Un usuario que escribe incluso parte de la palabra, como "pantallas", seguirá viendo una coincidencia en un vínculo de tarea que tenga "protectores de pantalla" como palabra clave. En el caso de los idiomas en los que los formularios en plural cambian la palabra, es necesario colocar todos los formularios que un usuario podría esperar razonablemente para escribir en las palabras clave.

Como Convención, Microsoft ha omitido pequeñas palabras como "cómo" o "deseo" del conjunto de palabras clave. La expectativa es que la mayoría de los usuarios simplemente escribirán las palabras más importantes, como "Mouse", "contraste alto" o "controlador de vídeo" para obtener los resultados.

## <a name="related-topics"></a>Temas relacionados

<dl> <dt>

[Elementos del panel de control](control-panel-applications.md)
</dt> <dt>

[Directrices de la experiencia de usuario](user-experience-guidelines.md)
</dt> <dt>

[Registrar elementos del panel de control](registering-control-panel-items.md)
</dt> <dt>

[Usar CPLApplet](using-cplapplet.md)
</dt> <dt>

[Procesamiento de mensajes del panel de control](message-processing.md)
</dt> <dt>

[Ejecutar elementos del panel de control](executing-control-panel-items.md)
</dt> <dt>

[Extender elementos del panel de control del sistema](extending-system-control-panel-items.md)
</dt> <dt>

[Asignar categorías del panel de control](assigning-control-panel-categories.md)
</dt> <dt>

[Acceder al panel de control en modo seguro en Windows Vista](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



