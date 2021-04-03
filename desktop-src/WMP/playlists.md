---
title: Reproducción
description: Reproducción
ms.assetid: b1ac9208-33d1-448f-9e2e-920fad9c6add
keywords:
- Windows Media Player, listas de reproducción
- Modelo de objetos de Windows Media Player, listas de reproducción
- modelo de objetos, listas de reproducción
- Control ActiveX de Windows Media Player, listas de reproducción
- Control ActiveX, listas de reproducción
- Control ActiveX móvil de Windows Media Player, listas de reproducción
- Windows Media Player Mobile, listas de reproducción
- listas de reproducción, migración
- Listas de reproducción de metarchivos de Windows Media, migración
- listas de reproducción de metarchivos, migración
- Guía de migración, listas de reproducción
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 124c07a6bd3aec0bebd235678e9fa8a5f069ec73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104075455"
---
# <a name="playlists"></a><span data-ttu-id="91540-114">Reproducción</span><span class="sxs-lookup"><span data-stu-id="91540-114">Playlists</span></span>

<span data-ttu-id="91540-115">El modelo de objetos de control ActiveX de Windows Media Player 6,4 incluye cuatro métodos y una propiedad para trabajar con listas de reproducción de metarchivos de Windows Media:</span><span class="sxs-lookup"><span data-stu-id="91540-115">The Windows Media Player 6.4 ActiveX control object model includes four methods and one property for working with Windows Media metafile playlists:</span></span>

-   <span data-ttu-id="91540-116">*Player6*. **GetCurrentEntry**</span><span class="sxs-lookup"><span data-stu-id="91540-116">*Player6*.**GetCurrentEntry**</span></span>
-   <span data-ttu-id="91540-117">*Player6*. **SetCurrentEntry**</span><span class="sxs-lookup"><span data-stu-id="91540-117">*Player6*.**SetCurrentEntry**</span></span>
-   <span data-ttu-id="91540-118">*Player6*. **GetMediaParameter**</span><span class="sxs-lookup"><span data-stu-id="91540-118">*Player6*.**GetMediaParameter**</span></span>
-   <span data-ttu-id="91540-119">*Player6*. **GetMediaParameterName**</span><span class="sxs-lookup"><span data-stu-id="91540-119">*Player6*.**GetMediaParameterName**</span></span>
-   <span data-ttu-id="91540-120">*Player6*. **EntryCount**.</span><span class="sxs-lookup"><span data-stu-id="91540-120">*Player6*.**EntryCount**.</span></span>

<span data-ttu-id="91540-121">Juntos, proporcionan una funcionalidad limitada para navegar por un metarchivo de lista de reproducción con una extensión de nombre de archivo. ASX y recuperar información sobre las entradas contenidas en la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="91540-121">Together, these provide limited functionality for navigating a playlist metafile with an .asx file name extension and retrieving information about the entries contained in the playlist.</span></span>

<span data-ttu-id="91540-122">Windows Media Player 7 presentó "biblioteca multimedia".</span><span class="sxs-lookup"><span data-stu-id="91540-122">Windows Media Player 7 introduced "Media Library."</span></span> <span data-ttu-id="91540-123">La biblioteca permite a los usuarios organizar su contenido multimedia digital, así como crear listas de reproducción personalizadas que se pueden administrar desde la interfaz gráfica de usuario del reproductor.</span><span class="sxs-lookup"><span data-stu-id="91540-123">The library allows users to organize their digital media content, as well as to create custom playlists that can be managed from the Player graphical user interface.</span></span> <span data-ttu-id="91540-124">El modelo de objetos de control ActiveX de Windows Media Player 7 o posterior proporciona compatibilidad para trabajar con listas de reproducción de la biblioteca, así como listas de reproducción contenidas en los metaarchivos de Windows Media con la extensión de nombre de archivo. ASX.</span><span class="sxs-lookup"><span data-stu-id="91540-124">The Windows Media Player 7 or later ActiveX control object model provides support for working with library playlists, as well as playlists contained in Windows Media metafiles with an .asx file name extension.</span></span>

> [!Note]  
> <span data-ttu-id="91540-125">Por motivos de seguridad, el usuario debe conceder derechos de acceso a la biblioteca antes de que el programa pueda manipular su contenido.</span><span class="sxs-lookup"><span data-stu-id="91540-125">For security reasons, the user must grant access rights to the library before your program can manipulate its content.</span></span> <span data-ttu-id="91540-126">Los derechos de acceso solo se pueden solicitar y conceder a través del modelo de objetos de la serie Windows Media Player 9 o posterior.</span><span class="sxs-lookup"><span data-stu-id="91540-126">Access rights can only be requested and granted through the Windows Media Player 9 Series or later object model.</span></span> <span data-ttu-id="91540-127">Para más información sobre los derechos de acceso, consulte [acceso a bibliotecas](library-access.md).</span><span class="sxs-lookup"><span data-stu-id="91540-127">For details about access rights, see [Library Access](library-access.md).</span></span>

 

<span data-ttu-id="91540-128">El modelo de objetos de Windows Media Player 7 o posterior incluye tres objetos para controlar las listas de reproducción.</span><span class="sxs-lookup"><span data-stu-id="91540-128">The Windows Media Player 7 or later object model includes three objects for handling playlists.</span></span> <span data-ttu-id="91540-129">El objeto **PlaylistCollection** proporciona funcionalidad para organizar listas de reproducción. representa toda la colección de listas de reproducción de la biblioteca del usuario.</span><span class="sxs-lookup"><span data-stu-id="91540-129">The **PlaylistCollection** object provides functionality for organizing playlists; it represents the entire collection of playlists in the user's library.</span></span> <span data-ttu-id="91540-130">El objeto **PlaylistArray** proporciona una manera de recuperar una lista de reproducción específica del objeto **PlaylistCollection** mediante un número de índice; dos de los métodos del objeto **PlaylistCollection** recuperan un objeto **PlaylistArray** .</span><span class="sxs-lookup"><span data-stu-id="91540-130">The **PlaylistArray** object provides a way to retrieve a specific playlist from the **PlaylistCollection** object by using an index number; two of the **PlaylistCollection** object methods retrieve a **PlaylistArray** object.</span></span> <span data-ttu-id="91540-131">El objeto de **lista de reproducción** proporciona las propiedades y los métodos necesarios para manipular los elementos multimedia contenidos en una sola lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="91540-131">The **Playlist** object provides the properties and methods necessary to manipulate media items contained in a single playlist.</span></span>

<span data-ttu-id="91540-132">Por ejemplo, como cada lista de reproducción de la biblioteca tiene un nombre único, puede recuperar una lista de reproducción de la biblioteca mediante *PlaylistCollection*. método **getByName** :</span><span class="sxs-lookup"><span data-stu-id="91540-132">As an example, since each playlist in the library has a unique name, you can retrieve a playlist from the library using the *PlaylistCollection*.**getByName** method:</span></span>


```C++
// Retrieve a PlaylistArray object that contains 
// exactly one Playlist object.
var plarray = WMP9.playlistCollection.getByName("MyPlaylist");

// Get the Playlist object from the PlaylistArray object.
// The Playlist object has index number zero.
var pl = plarray.item(0);

// Make the retrieved playlist the current playlist.
WMP9.currentPlaylist = pl;

```



<span data-ttu-id="91540-133">Lo más frecuente es que desee trabajar con la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="91540-133">You will most frequently want to work with the current playlist.</span></span> <span data-ttu-id="91540-134">Aunque es posible usar varios objetos de lista de reproducción, el *reproductor* solo puede recuperar uno. la propiedad **currentPlaylist** en un momento dado: la que Windows Media Player está procesando en ese momento.</span><span class="sxs-lookup"><span data-stu-id="91540-134">While it is possible to use several playlist objects, only one can be retrieved by the *Player*.**currentPlaylist** property at any given time: the one that Windows Media Player is processing at that moment.</span></span>

<span data-ttu-id="91540-135">Cuando Windows Media Player 7 o posterior reproduce un metarchivo de Windows Media con una extensión de nombre de archivo. ASX, primero crea un objeto de **lista de reproducción** .</span><span class="sxs-lookup"><span data-stu-id="91540-135">When Windows Media Player 7 or later plays a Windows Media metafile with an .asx file name extension, it first creates a **Playlist** object.</span></span> <span data-ttu-id="91540-136">A continuación, rellena el objeto con la información de la lista de reproducción. ASX y, a continuación, hace que ese objeto de **lista** de reproducción sea la lista de reproducción actual.</span><span class="sxs-lookup"><span data-stu-id="91540-136">Next, it fills the object with the information from the .asx playlist, and then makes that **Playlist** object the current playlist.</span></span> <span data-ttu-id="91540-137">Esto significa que puede usar las propiedades y los métodos asociados al objeto de **lista de reproducción** para manipular las listas de reproducción. ASX exactamente como lo haría con las listas de reproducción de la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="91540-137">This means that you can use the properties and methods associated with the **Playlist** object to manipulate .asx playlists exactly as you would handle playlists in the library.</span></span> <span data-ttu-id="91540-138">Por ejemplo, para recuperar el número de entradas de una lista de reproducción. ASX con el modelo de objetos de la versión 6,4, se usa *Player6*. Propiedad **EntryCount** :</span><span class="sxs-lookup"><span data-stu-id="91540-138">For instance, to retrieve the number of entries in an .asx playlist using the version 6.4 object model, you use the *Player6*.**EntryCount** property:</span></span>


```C++
var entrycount = WMP64.EntryCount;

```



<span data-ttu-id="91540-139">Cuando se usa el modelo de objetos de Windows Media Player 7 o posterior, se usa la *lista de reproducción*. propiedad **Count** :</span><span class="sxs-lookup"><span data-stu-id="91540-139">When using the Windows Media Player 7 or later object model, you use the *Playlist*.**count** property:</span></span>


```C++
var entrycount = WMP9.currentPlaylist.count;

```



<span data-ttu-id="91540-140">Cuando se usa el control versión 6,4, se puede utilizar *Player6*. Método **GetCurrentEntry** para recuperar el índice de la entrada actual en una lista de reproducción. ASX:</span><span class="sxs-lookup"><span data-stu-id="91540-140">When using the version 6.4 control, you can use the *Player6*.**GetCurrentEntry** method to retrieve the index of the current entry in an .asx playlist:</span></span>


```C++
var entrynum = WMP64.GetCurrentEntry();

```



<span data-ttu-id="91540-141">Puede lograr el mismo resultado mediante el modelo de objetos de Windows Media Player 7 o posterior en el script.</span><span class="sxs-lookup"><span data-stu-id="91540-141">You can achieve the same result by using the Windows Media Player 7 or later object model in script.</span></span> <span data-ttu-id="91540-142">En el ejemplo de JScript siguiente se compara el objeto multimedia actual con cada elemento de la lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="91540-142">The following JScript example compares the current media object to each item in the playlist.</span></span> <span data-ttu-id="91540-143">Cuando el *elemento multimedia*. **isIdentical** devuelve true, un cuadro de mensaje muestra el índice del elemento multimedia actual.</span><span class="sxs-lookup"><span data-stu-id="91540-143">When *Media*.**isIdentical** returns true, a message box displays the index of the current media item.</span></span>


```C++
function matchit(){
// Store the current playlist object in a variable.
var pl = WMP9.currentPlaylist;

// Loop through the playlist one entry at a time.
  for (var i = 0; i < pl.count; i++){

   // Test whether the current media item matches 
   // the item in the playlist at the current loop index.
   if (WMP9.currentmedia.isIdentical(pl.item(i))){

       // They match, display the index.
       var message = "Current media at index: " + i;
       alert(message);

       // Exit the function, don't continue looping!
       return;
      }
  }
}

```



<span data-ttu-id="91540-144">Para especificar el índice de la entrada actual en una lista de reproducción. ASX, se usa *Player6*. **SetCurrentEntry**.</span><span class="sxs-lookup"><span data-stu-id="91540-144">To specify the index of the current entry in an .asx playlist, you use *Player6*.**SetCurrentEntry**.</span></span> <span data-ttu-id="91540-145">Los índices de entrada de la lista de reproducción de la versión 6,4 empiezan por 1, por lo que para que la segunda entrada de una lista de reproducción de metarchivo sea la actual, utilice la siguiente sintaxis:</span><span class="sxs-lookup"><span data-stu-id="91540-145">Playlist entry indexes in version 6.4 start with 1, so to make the second entry in a metafile playlist the current one, use the following syntax:</span></span>


```C++
WMP6.SetCurrentEntry(2);

```



<span data-ttu-id="91540-146">Los índices de entrada de la lista de reproducción son de base cero en Windows Media Player 7 o posterior; para hacer que la segunda entrada de una lista de reproducción de metarchivo sea la actual, al usar el modelo de objetos de Windows Media Player 7 o posterior, use la sintaxis siguiente:</span><span class="sxs-lookup"><span data-stu-id="91540-146">Playlist entry indexes are zero-based in Windows Media Player 7 or later; to make the second entry in a metafile playlist the current one, when using the Windows Media Player 7 or later object model, use the following syntax:</span></span>


```C++
WMP9.controls.currentItem = WMP9.currentPlaylist.item(1);

```



<span data-ttu-id="91540-147">En el siguiente ejemplo de JScript se muestra una función que acepta un número de índice como parámetro y, a continuación, hace que la entrada de la lista de reproducción correspondiente al índice sea el elemento multimedia actual:</span><span class="sxs-lookup"><span data-stu-id="91540-147">The following JScript example demonstrates a function that accepts an index number as a parameter, and then makes the playlist entry that corresponds to the index the current media item:</span></span>


```C++
function setindex(idx){
// Store the current playlist in a variable.
var pl = WMP9.currentPlaylist;

// Get the first playlist entry.
var firstmedia = pl.item(0);

// Start the Player to allow navigation within the playlist.
WMP9.controls.playItem(firstmedia);

// Test whether idx is within a valid range.
   if (idx < pl.count && idx >= 0){

     // Set the currentItem to the desired playlist item.
     WMP9.controls.currentItem = pl.item(idx);

     // Display the name of the media item.
     alert(WMP9.currentMedia.name);
     return true;
 }

// The index is out of range, stop the Player, alert the user.
WMP9.controls.stop();
alert("Index out of range");
return false;
}

```



<span data-ttu-id="91540-148">Los metaarchivos de Windows Media pueden contener elementos de parámetro personalizados, que se especifican mediante la **<PARAM>** etiqueta.</span><span class="sxs-lookup"><span data-stu-id="91540-148">Windows Media metafiles can contain custom parameter elements, which you specify by using the **<PARAM>** tag.</span></span> <span data-ttu-id="91540-149">Al usar el modelo de objetos de la versión 6,4, puede recuperar el nombre de un parámetro determinado con el *Player6*. Método **GetMediaParameterName** .</span><span class="sxs-lookup"><span data-stu-id="91540-149">When using the version 6.4 object model, you can retrieve the name of a particular parameter with the *Player6*.**GetMediaParameterName** method.</span></span> <span data-ttu-id="91540-150">En el siguiente ejemplo de JScript se recupera el nombre del primer parámetro de la primera entrada de una lista de reproducción. ASX:</span><span class="sxs-lookup"><span data-stu-id="91540-150">The following JScript example retrieves the name of the first parameter in the first entry of an .asx playlist:</span></span>


```C++
var paramname = WMP6.GetMediaParameterName(1,1);

```



<span data-ttu-id="91540-151">Del mismo modo, puede recuperar el valor asociado al parámetro mediante *Player6*. **GetMediaParameter**:</span><span class="sxs-lookup"><span data-stu-id="91540-151">Similarly, you can retrieve the value associated with the parameter using *Player6*.**GetMediaParameter**:</span></span>


```C++
var paramvalue = WMP6.GetMediaParameter(1, paramname);

```



<span data-ttu-id="91540-152">En el siguiente ejemplo de JScript se usa el modelo de objetos de Windows Media Player 7 o posterior para recuperar el nombre de parámetro y el valor de la primera entrada de una lista de reproducción. ASX:</span><span class="sxs-lookup"><span data-stu-id="91540-152">The following JScript example uses the Windows Media Player 7 or later object model to retrieve the parameter name and value from the first entry in an .asx playlist:</span></span>


```C++
function getattribute(){
// Store the first playlist entry as a Media object.
var firstmedia = WMP9.currentplaylist.item(0);

// Get the name of the first parameter in the object named firstmedia.
var attname = firstmedia.getAttributeName(0);

// Get the value of the first parameter in the object named firstmedia.
var attval = firstmedia.getItemInfo(attname);

// Display the information.
alert(attname + ": " + attval);
}

```



<span data-ttu-id="91540-153">Puede usar *PlaylistCollection*. método **importPlaylist** para agregar una lista de reproducción. ASX a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="91540-153">You can use the *PlaylistCollection*.**importPlaylist** method to add an .asx playlist to the library.</span></span> <span data-ttu-id="91540-154">Una vez importada, la lista de reproducción del metarchivo se convierte en una lista de reproducción de la biblioteca, por lo que puede manipularla con todas las propiedades y los métodos de su disposición.</span><span class="sxs-lookup"><span data-stu-id="91540-154">Once imported, the metafile playlist becomes a library playlist, so you can manipulate it using all the properties and methods at your disposal.</span></span> <span data-ttu-id="91540-155">El usuario debe conceder derechos de acceso completo a la biblioteca para que la aplicación pueda usar el método **importPlaylist** .</span><span class="sxs-lookup"><span data-stu-id="91540-155">The user must grant full access rights to the library for your application to be able to use the **importPlaylist** method.</span></span>

<span data-ttu-id="91540-156">Puede usar *PlaylistCollection*. **getByName** para comprobar si existe una lista de reproducción.</span><span class="sxs-lookup"><span data-stu-id="91540-156">You can use *PlaylistCollection*.**getByName** to test whether a playlist exists.</span></span> <span data-ttu-id="91540-157">Este método siempre devuelve un objeto **PlaylistArray** válido.</span><span class="sxs-lookup"><span data-stu-id="91540-157">This method always returns a valid **PlaylistArray** object.</span></span> <span data-ttu-id="91540-158">Si la matriz de lista de reproducción recuperada contiene exactamente una lista de reproducción, existe una lista de reproducción con ese nombre en la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="91540-158">If the playlist array retrieved contains exactly one playlist, then there exists a playlist with that name in the library.</span></span> <span data-ttu-id="91540-159">De lo contrario, la matriz de lista de reproducción no contendrá ningún objeto de lista de reproducción; Esto significa que no hay ninguna lista de reproducción en la biblioteca con el nombre pasado como argumento al método **getByName** .</span><span class="sxs-lookup"><span data-stu-id="91540-159">Otherwise, the playlist array will contain no playlist object; this means there is no playlist in the library with the name passed as an argument to the **getByName** method.</span></span> <span data-ttu-id="91540-160">En el siguiente ejemplo de JScript se muestra esto:</span><span class="sxs-lookup"><span data-stu-id="91540-160">The following JScript example demonstrates this:</span></span>


```C++
// Specify an .asx playlist file.
WMP9.URL = "https://www.microsoft.com/someplaylist.asx";

// Open the playlist and start playing the content.
WMP9.controls.play();

// Store the current playlist object.
var pl = WMP9.currentPlaylist;

// Attempt to retrieve from the library 
// a playlist having the same name as the current playlist.
var plarray = WMP9.playlistCollection.getByName(pl.name);

// Test whether the PlaylistArray object, plarray, contains
// a Playlist object.
if (!plarray.count)
   
   // If plarray contains no playlist, then import 
   // the current one.
   WMP9.playlistCollection.importPlaylist(pl);
}

```



## <a name="related-topics"></a><span data-ttu-id="91540-161">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="91540-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="91540-162">**Administrar listas de reproducción**</span><span class="sxs-lookup"><span data-stu-id="91540-162">**Managing Playlists**</span></span>](managing-playlists.md)
</dt> <dt>

[<span data-ttu-id="91540-163">**Guía de migración del modelo de objetos**</span><span class="sxs-lookup"><span data-stu-id="91540-163">**Object Model Migration Guide**</span></span>](object-model-migration-guide.md)
</dt> <dt>

[<span data-ttu-id="91540-164">**Objeto Playlist**</span><span class="sxs-lookup"><span data-stu-id="91540-164">**Playlist Object**</span></span>](playlist-object.md)
</dt> </dl>

 

 




