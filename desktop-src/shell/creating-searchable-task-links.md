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
# <a name="creating-searchable-task-links-for-a-control-panel-item"></a><span data-ttu-id="58494-103">Crear vínculos de tarea que se pueden buscar para un elemento del panel de control</span><span class="sxs-lookup"><span data-stu-id="58494-103">Creating Searchable Task Links for a Control Panel Item</span></span>

<span data-ttu-id="58494-104">A partir de Windows Vista, la vista de categorías del panel de control proporciona vínculos a tareas bajo cada icono de elemento del panel de control, como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="58494-104">As of Windows Vista, the Control Panel category view provides task links beneath each Control Panel item's icon as shown here.</span></span>

![vínculos de tareas en la página categoría del sistema y mantenimiento](images/controlpaneltasklinks.png)

<span data-ttu-id="58494-106">Cuando un usuario escribe texto en el cuadro de **búsqueda** en la esquina superior derecha de la ventana, los resultados de la búsqueda incluyen estos vínculos de tarea, tal como se muestra aquí para buscar la palabra "Mostrar".</span><span class="sxs-lookup"><span data-stu-id="58494-106">When a user enters text in the **Search** box in the upper right of the window, the search results include these task links as shown here for a search on the word "display".</span></span>

![vínculos de tarea en los resultados de la búsqueda del panel de control](images/controlpanelsearchresults.png)

<span data-ttu-id="58494-108">Este tema trata lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="58494-108">This topic discusses the following:</span></span>

-   [<span data-ttu-id="58494-109">Prácticas recomendadas de vínculo de tareas</span><span class="sxs-lookup"><span data-stu-id="58494-109">Task Link Best Practices</span></span>](#task-link-best-practices)
-   [<span data-ttu-id="58494-110">Crear un archivo XML de tarea</span><span class="sxs-lookup"><span data-stu-id="58494-110">Creating a Task XML File</span></span>](#creating-a-task-xml-file)
-   [<span data-ttu-id="58494-111">Localizar vínculos de tareas</span><span class="sxs-lookup"><span data-stu-id="58494-111">Localizing Task Links</span></span>](#localizing-task-links)
-   [<span data-ttu-id="58494-112">Palabras clave y búsqueda</span><span class="sxs-lookup"><span data-stu-id="58494-112">Keywords and Searching</span></span>](#keywords-and-searching)
-   [<span data-ttu-id="58494-113">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="58494-113">Related topics</span></span>](#related-topics)

## <a name="task-link-best-practices"></a><span data-ttu-id="58494-114">Prácticas recomendadas de vínculo de tareas</span><span class="sxs-lookup"><span data-stu-id="58494-114">Task Link Best Practices</span></span>

<span data-ttu-id="58494-115">Se recomienda que proporcione vínculos de tareas para los elementos del panel de control como ayuda para que los usuarios busquen la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="58494-115">It is recommended that you provide task links for your Control Panel items as an aid to users searching for functionality.</span></span> <span data-ttu-id="58494-116">También es posible agregar palabras clave a los vínculos de tarea para que los usuarios puedan encontrarlos incluso sin conocer la terminología o el título de una tarea.</span><span class="sxs-lookup"><span data-stu-id="58494-116">It is also possible to add keywords to the task links so that a user can find them even without knowing a task's title or terminology.</span></span>

<span data-ttu-id="58494-117">Los vínculos de tarea mejores sirven para tres propósitos:</span><span class="sxs-lookup"><span data-stu-id="58494-117">The best task links serve three purposes:</span></span>

1.  <span data-ttu-id="58494-118">Proporcione un acceso directo a la funcionalidad del elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="58494-118">Provide a shortcut to the functionality of the Control Panel item.</span></span>
2.  <span data-ttu-id="58494-119">Proporcione palabras clave para que los usuarios puedan realizar búsquedas con su propio idioma.</span><span class="sxs-lookup"><span data-stu-id="58494-119">Provide keywords so that users can search using their own language.</span></span> <span data-ttu-id="58494-120">Es posible que un usuario desee escribir "compactación" porque conoce el término técnico.</span><span class="sxs-lookup"><span data-stu-id="58494-120">A user may want to type "compaction" because he or she knows the technical term.</span></span> <span data-ttu-id="58494-121">Un usuario puede escribir "BD demasiado grande" o "archivo de base de datos".</span><span class="sxs-lookup"><span data-stu-id="58494-121">A user may type "DB too big", or "database filesize".</span></span> <span data-ttu-id="58494-122">Agregar las palabras clave adecuadas a la tarea significa que los usuarios pueden encontrar el elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="58494-122">Adding suitable keywords to the task means that users can find your Control Panel item.</span></span>
3.  <span data-ttu-id="58494-123">Proporcione sugerencias sobre lo que hace el elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="58494-123">Provide hints about what the Control Panel item does.</span></span> <span data-ttu-id="58494-124">Cuando un usuario ve los vínculos situados debajo del icono de un elemento del panel de control, puede obtener más información sobre el uso del elemento del panel de control en lugar del nombre y el icono que puede proporcionar.</span><span class="sxs-lookup"><span data-stu-id="58494-124">When a user sees the links beneath a Control Panel item's icon, they can get more information about what the Control Panel item is used for than the name and icon alone can provide.</span></span>

<span data-ttu-id="58494-125">Los vínculos de tareas deben ser centrados en el usuario final, no en la tecnología o en las características.</span><span class="sxs-lookup"><span data-stu-id="58494-125">Task links should be end-user focused, not technology- or feature-focused.</span></span> <span data-ttu-id="58494-126">Por ejemplo, "habilitar la compactación de la base de datos" sería un mal texto, ya que no está familiarizado con la mayoría de los usuarios.</span><span class="sxs-lookup"><span data-stu-id="58494-126">For example, "Enable database compaction" would be bad wording because it is technical jargon unfamiliar to the majority of users.</span></span> <span data-ttu-id="58494-127">"Hacer que el archivo de base de datos sea más pequeño" es mejor porque menciona el objetivo real del usuario en lugar del mecanismo que debe obtenerse.</span><span class="sxs-lookup"><span data-stu-id="58494-127">"Make my database file smaller" is better because it mentions the user's actual end goal rather than the mechanism to get there.</span></span> <span data-ttu-id="58494-128">El objetivo no es sobresimplificar, sino que es decir, la tarea en lo que se refiere a lo que el usuario desea realizar.</span><span class="sxs-lookup"><span data-stu-id="58494-128">The goal is not to oversimplify, but rather to phrase the task in terms of what the user wants to accomplish.</span></span>

## <a name="creating-a-task-xml-file"></a><span data-ttu-id="58494-129">Crear un archivo XML de tarea</span><span class="sxs-lookup"><span data-stu-id="58494-129">Creating a Task XML File</span></span>

<span data-ttu-id="58494-130">Los vínculos de tareas se definen en un archivo XML.</span><span class="sxs-lookup"><span data-stu-id="58494-130">Task links are defined in an XML file.</span></span> <span data-ttu-id="58494-131">En esta sección se proporcionan los detalles de un archivo. XML de ejemplo que define tres vínculos de tarea para un elemento del panel de control denominado **Bloc de notas**.</span><span class="sxs-lookup"><span data-stu-id="58494-131">This section provides the details of an example .xml file that defines three task links for a Control Panel item called **Notepad**.</span></span> <span data-ttu-id="58494-132">Define títulos, palabras clave y las líneas de comandos para los vínculos de tarea.</span><span class="sxs-lookup"><span data-stu-id="58494-132">It defines titles, keywords, and the command lines for the task links.</span></span> <span data-ttu-id="58494-133">También se muestra cómo especificar los vínculos de tarea que aparecen debajo de la categoría.</span><span class="sxs-lookup"><span data-stu-id="58494-133">It also illustrates how to specify which task links appear under which category.</span></span> <span data-ttu-id="58494-134">Un elemento del panel de control que se registra para aparecer en más de una categoría tiene la opción de mostrar distintos vínculos en función de la categoría.</span><span class="sxs-lookup"><span data-stu-id="58494-134">A Control Panel item that is registered to appear in more than one category has the option of showing different links depending on the category.</span></span> <span data-ttu-id="58494-135">Las explicaciones de los distintos elementos e información proporcionada se proporcionan como comentarios en el propio XML.</span><span class="sxs-lookup"><span data-stu-id="58494-135">Explanations of the various elements and information provided are given as comments in the XML itself.</span></span>


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
> <span data-ttu-id="58494-136">A partir de Windows 7, un elemento del panel de control puede identificarse por su nombre canónico en lugar de su nombre de archivo ejecutable: el elemento **<SH: controlpanel>** puede usarse en lugar de **<sh: Command>**.</span><span class="sxs-lookup"><span data-stu-id="58494-136">As of Windows 7, a Control Panel item can be identified by its canonical name rather than its executable name: the **<sh:controlpanel>** element can be used in place of **<sh:command>**.</span></span> <span data-ttu-id="58494-137">El elemento **<SH: controlpanel>** también proporciona un atributo para especificar la página del elemento al que debe abrirse.</span><span class="sxs-lookup"><span data-stu-id="58494-137">The **<sh:controlpanel>** element also provides an attribute to specify the page of the item to which it should open.</span></span> <span data-ttu-id="58494-138">A continuación se muestra un ejemplo del elemento **<SH: controlpanel>** :</span><span class="sxs-lookup"><span data-stu-id="58494-138">The following shows an example of the **<sh:controlpanel>** element:</span></span>

 


```
<sh:controlpanel name="Microsoft.Presentation" page="pageWallpaper"/>
```



## <a name="localizing-task-links"></a><span data-ttu-id="58494-139">Localizar vínculos de tareas</span><span class="sxs-lookup"><span data-stu-id="58494-139">Localizing Task Links</span></span>

<span data-ttu-id="58494-140">El texto de los títulos y palabras clave de los vínculos de tarea se puede almacenar en una tabla de cadenas en el módulo del elemento del panel de control.</span><span class="sxs-lookup"><span data-stu-id="58494-140">The text for the task links' titles and keywords can be stored in a string table in the Control Panel item's module.</span></span> <span data-ttu-id="58494-141">En ese caso, el formato utilizado en el archivo XML se convierte en:</span><span class="sxs-lookup"><span data-stu-id="58494-141">In that case, the format used in the XML file becomes:</span></span>


```
<sh:task id="{3B75A7AE-C4E4-4E5A-9420-7CECCDA75425}"> 
    <!-- This is a generated GUID, specific to this task link -->
    <sh:name>@myTextResources.dll,-100</sh:name>
    <sh:keywords>@myTextResources.dll,-101</sh:keywords>
    <sh:command>%ProgramFiles%\Microsoft Games\Solitaire\solitaire.exe</sh:command>
</sh:task>
```



<span data-ttu-id="58494-142">En este ejemplo, el texto del nombre de la tarea aparece en el ID. de recurso de cadena 100 en myTextResources.dll y el texto de las palabras clave aparece en el ID. de recurso de cadena 101.</span><span class="sxs-lookup"><span data-stu-id="58494-142">In this example, the text for the task's name appears in string resource ID 100 in myTextResources.dll, and the text for the keywords appears in string resource ID 101.</span></span>

## <a name="keywords-and-searching"></a><span data-ttu-id="58494-143">Palabras clave y búsqueda</span><span class="sxs-lookup"><span data-stu-id="58494-143">Keywords and Searching</span></span>

<span data-ttu-id="58494-144">La búsqueda del panel de control encuentra los vínculos de tarea en función de su nombre y también de sus palabras clave.</span><span class="sxs-lookup"><span data-stu-id="58494-144">The Control Panel search finds task links based on their name and also on their keywords.</span></span> <span data-ttu-id="58494-145">Coincide con cada palabra de la búsqueda con el prefijo de las palabras en el nombre y las palabras clave.</span><span class="sxs-lookup"><span data-stu-id="58494-145">It matches each word in the search with the prefix of words in the name and keywords.</span></span> <span data-ttu-id="58494-146">Por ejemplo, la cadena de consulta "CPU" coincidiría con la tarea "ver procesos en ejecución" en el ejemplo anterior porque "CPU" está en la lista de palabras clave.</span><span class="sxs-lookup"><span data-stu-id="58494-146">For example, the query string "cpu" would match the task "See running processes" in the earlier example because "cpu" is in the keyword list.</span></span> <span data-ttu-id="58494-147">La cadena de consulta "Pro" también encontraría el resultado porque la palabra de título "procesos" comienza con esa cadena.</span><span class="sxs-lookup"><span data-stu-id="58494-147">The query string "pro" would also find that result because the title word "processes" begins with that string.</span></span> <span data-ttu-id="58494-148">Tenga en cuenta que la consulta solo coincide con los prefijos.</span><span class="sxs-lookup"><span data-stu-id="58494-148">Note that the query only matches prefixes.</span></span> <span data-ttu-id="58494-149">La cadena de consulta "rador" no coincidiría con un resultado porque esa cadena, mientras que parte de la palabra de título "proceso", no comienza con esa palabra.</span><span class="sxs-lookup"><span data-stu-id="58494-149">The query string "rocess" would not match a result because that string, while part of the title word "process", does not begin that word.</span></span>

<span data-ttu-id="58494-150">Cuando una consulta de búsqueda contiene varios tokens, todos los tokens deben coincidir con el prefijo de alguna palabra clave o parte del título de la tarea para obtener un resultado.</span><span class="sxs-lookup"><span data-stu-id="58494-150">When a search query contains multiple tokens, all the tokens must match the prefix of some keyword or part of the task title for a result.</span></span> <span data-ttu-id="58494-151">La consulta "nivel de CPU" no coincidiría, porque "LEVEL" no está en el conjunto de palabras clave.</span><span class="sxs-lookup"><span data-stu-id="58494-151">The query "cpu level" would not match, because "level" is not in the keyword set.</span></span> <span data-ttu-id="58494-152">La consulta "CPU Run" daría como resultado, porque "CPU" coincide con una palabra clave y "Run" es el prefijo de la palabra "Running" en el título de la tarea.</span><span class="sxs-lookup"><span data-stu-id="58494-152">The query "cpu run" would give a result, because "cpu" matches a keyword, and "run" is the prefix of the word "running" in the task's title.</span></span>

<span data-ttu-id="58494-153">En el panel de control no se proporciona automáticamente corrección ortográfica ni variaciones como plurales o guiones.</span><span class="sxs-lookup"><span data-stu-id="58494-153">Control Panel does not automatically provide spelling correction or variations such as plurals or hyphenation.</span></span> <span data-ttu-id="58494-154">Las coincidencias tampoco distinguen mayúsculas de minúsculas.</span><span class="sxs-lookup"><span data-stu-id="58494-154">Matches are also case-insensitive.</span></span> <span data-ttu-id="58494-155">Para asegurarse de que la lista de palabras clave sea correcta, se recomienda proporcionar variaciones, como para este vínculo de tarea que implique protectores de pantalla: "protectores de pantalla; protectores de pantalla; protectores de pantalla;"</span><span class="sxs-lookup"><span data-stu-id="58494-155">To ensure a successful keyword list, it is recommended to provide variations yourself, such as for this task link that involves screen savers: "screensavers;screen-savers;screen savers;"</span></span>

<span data-ttu-id="58494-156">No es necesario agregar el "protector de la" singular, ya que una consulta que busca "protectores de la" también encontrará "protector de la búsqueda" debido a la coincidencia de prefijo.</span><span class="sxs-lookup"><span data-stu-id="58494-156">There is no need to add the singular "screensaver", because a query that finds "screensavers" will also find "screensaver" due to the prefix match.</span></span> <span data-ttu-id="58494-157">Un usuario que escribe incluso parte de la palabra, como "pantallas", seguirá viendo una coincidencia en un vínculo de tarea que tenga "protectores de pantalla" como palabra clave.</span><span class="sxs-lookup"><span data-stu-id="58494-157">A user typing even part of the word, like "screensa" will still see a match on a task link that has "screensavers" as a keyword.</span></span> <span data-ttu-id="58494-158">En el caso de los idiomas en los que los formularios en plural cambian la palabra, es necesario colocar todos los formularios que un usuario podría esperar razonablemente para escribir en las palabras clave.</span><span class="sxs-lookup"><span data-stu-id="58494-158">For languages where plural forms change the word, it is necessary to put all the forms a user could reasonably be expected to type into the keywords.</span></span>

<span data-ttu-id="58494-159">Como Convención, Microsoft ha omitido pequeñas palabras como "cómo" o "deseo" del conjunto de palabras clave.</span><span class="sxs-lookup"><span data-stu-id="58494-159">As a convention, Microsoft has omitted small words like "how do I" or "I want to" from the set of keywords.</span></span> <span data-ttu-id="58494-160">La expectativa es que la mayoría de los usuarios simplemente escribirán las palabras más importantes, como "Mouse", "contraste alto" o "controlador de vídeo" para obtener los resultados.</span><span class="sxs-lookup"><span data-stu-id="58494-160">The expectation is that most users will simply type the most important words such as "mouse", "high contrast", or "video driver" to get results.</span></span>

## <a name="related-topics"></a><span data-ttu-id="58494-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="58494-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58494-162">Elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="58494-162">Control Panel Items</span></span>](control-panel-applications.md)
</dt> <dt>

[<span data-ttu-id="58494-163">Directrices de la experiencia de usuario</span><span class="sxs-lookup"><span data-stu-id="58494-163">User Experience Guidelines</span></span>](user-experience-guidelines.md)
</dt> <dt>

[<span data-ttu-id="58494-164">Registrar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="58494-164">Registering Control Panel Items</span></span>](registering-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="58494-165">Usar CPLApplet</span><span class="sxs-lookup"><span data-stu-id="58494-165">Using CPLApplet</span></span>](using-cplapplet.md)
</dt> <dt>

[<span data-ttu-id="58494-166">Procesamiento de mensajes del panel de control</span><span class="sxs-lookup"><span data-stu-id="58494-166">Control Panel Message Processing</span></span>](message-processing.md)
</dt> <dt>

[<span data-ttu-id="58494-167">Ejecutar elementos del panel de control</span><span class="sxs-lookup"><span data-stu-id="58494-167">Executing Control Panel Items</span></span>](executing-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="58494-168">Extender elementos del panel de control del sistema</span><span class="sxs-lookup"><span data-stu-id="58494-168">Extending System Control Panel Items</span></span>](extending-system-control-panel-items.md)
</dt> <dt>

[<span data-ttu-id="58494-169">Asignar categorías del panel de control</span><span class="sxs-lookup"><span data-stu-id="58494-169">Assigning Control Panel Categories</span></span>](assigning-control-panel-categories.md)
</dt> <dt>

[<span data-ttu-id="58494-170">Acceder al panel de control en modo seguro en Windows Vista</span><span class="sxs-lookup"><span data-stu-id="58494-170">Accessing the Control Panel in Safe Mode under Windows Vista</span></span>](accessing-the-cp-in-safe-mode-under-vista.md)
</dt> </dl>

 

 



