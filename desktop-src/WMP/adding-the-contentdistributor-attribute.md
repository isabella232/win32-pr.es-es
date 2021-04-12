---
title: Adición del atributo ContentDistributor
description: Adición del atributo ContentDistributor
ms.assetid: b4ba5c9b-f28f-4275-bd39-c0ad1080d122
keywords:
- Windows Media Player tiendas en línea, agregar el atributo ContentDistributor
- tiendas en línea, agregar atributo ContentDistributor
- Escriba 1 tiendas en línea, agregando atributo ContentDistributor
- Escriba 2 tiendas en línea, agregando atributo ContentDistributor
- Windows Media Player tiendas en línea, atributo ContentDistributor
- tiendas en línea, atributo ContentDistributor
- tipo 1 almacenes en línea, atributo ContentDistributor
- tipo 2 tiendas en línea, atributo ContentDistributor
- adición del atributo ContentDistributor
- ContentDistributor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1636c002affbcf1235283a22f7eb060c75f24a81
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 09/16/2019
ms.locfileid: "104357128"
---
# <a name="adding-the-contentdistributor-attribute"></a><span data-ttu-id="a29a5-113">Adición del atributo ContentDistributor</span><span class="sxs-lookup"><span data-stu-id="a29a5-113">Adding the ContentDistributor Attribute</span></span>

<span data-ttu-id="a29a5-114">Cuando el usuario intenta reproducir contenido de la tienda en línea o copiar el contenido en un CD o un dispositivo, Windows Media Player llama a determinados métodos en el objeto COM.</span><span class="sxs-lookup"><span data-stu-id="a29a5-114">When the user attempts to play online store content or to copy the content to a CD or device, Windows Media Player calls certain methods in your COM object.</span></span> <span data-ttu-id="a29a5-115">Para ello, el reproductor necesita una manera de diferenciar el contenido de otros proveedores de tiendas en línea.</span><span class="sxs-lookup"><span data-stu-id="a29a5-115">To do this, the Player needs a way to differentiate your content from that of other online store providers.</span></span> <span data-ttu-id="a29a5-116">Al agregar el nombre de la clave de la tienda en línea como valor de **ContentDistributor** (que es un alias para el atributo Windows Media Format SDK denominado **WM/ContentDistributor**) en el contenido basado en Windows Media, asegúrese de que el reproductor puede identificar el contenido asociado a su servicio.</span><span class="sxs-lookup"><span data-stu-id="a29a5-116">By adding your online store key name as the value for the **ContentDistributor** (which is an alias for the Windows Media Format SDK attribute named **WM/ContentDistributor**) attribute to your Windows Media-based content, you ensure that the Player can identify the content associated with your service.</span></span>

<span data-ttu-id="a29a5-117">La adición de un valor para **ContentDistributor** también garantiza que Windows Media Player creará un nodo en la biblioteca para el contenido que proporcione.</span><span class="sxs-lookup"><span data-stu-id="a29a5-117">Adding a value for **ContentDistributor** also ensures that Windows Media Player will create a node in the library for content you provide.</span></span> <span data-ttu-id="a29a5-118">Consulte [integración de bibliotecas](library-integration.md).</span><span class="sxs-lookup"><span data-stu-id="a29a5-118">See [Library Integration](library-integration.md).</span></span>

<span data-ttu-id="a29a5-119">Este valor se puede especificar de dos maneras:</span><span class="sxs-lookup"><span data-stu-id="a29a5-119">You can specify this value two ways:</span></span>

-   <span data-ttu-id="a29a5-120">Use el modelo de objetos de Media Player de Windows.</span><span class="sxs-lookup"><span data-stu-id="a29a5-120">Use the Windows Media Player object model.</span></span> <span data-ttu-id="a29a5-121">Al hacerlo, Windows Media Player agrega el valor especificado a la base de datos de biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a29a5-121">When you do this, Windows Media Player adds the value you specify to the library database.</span></span> <span data-ttu-id="a29a5-122">Finalmente, el reproductor también escribirá el valor de atributo en el archivo multimedia digital.</span><span class="sxs-lookup"><span data-stu-id="a29a5-122">Eventually, the Player will also write the attribute value to the digital media file.</span></span>
-   <span data-ttu-id="a29a5-123">Use el SDK de Windows Media Format para agregar mediante programación el atributo **WM/ContentDistributor** .</span><span class="sxs-lookup"><span data-stu-id="a29a5-123">Use the Windows Media Format SDK to programmatically add the **WM/ContentDistributor** attribute.</span></span> <span data-ttu-id="a29a5-124">Al hacerlo, Windows Media Player lee el valor del atributo y lo agrega a la base de datos cuando se agrega el archivo multimedia digital a la biblioteca.</span><span class="sxs-lookup"><span data-stu-id="a29a5-124">When you do this, Windows Media Player reads the attribute value and adds it to the database when the digital media file is added to the library.</span></span>

<span data-ttu-id="a29a5-125">Al crear el objeto COM de la tienda en línea, el valor del atributo de archivo establecido para **ContentDistributor** y el valor asignado a la constante KszContentDistributorID en YourProject. h deben coincidir exactamente.</span><span class="sxs-lookup"><span data-stu-id="a29a5-125">When creating your online store COM object, the file attribute value you set for **ContentDistributor** and the value assigned to the constant kszContentDistributorID in YourProject.h must match exactly.</span></span> <span data-ttu-id="a29a5-126">Recuerde que especificó este valor constante para el objeto COM al crear el proyecto mediante el Asistente para proyectos.</span><span class="sxs-lookup"><span data-stu-id="a29a5-126">Recall that you specified this constant value for your COM object when you created the project by using the project wizard.</span></span> <span data-ttu-id="a29a5-127">Puede cambiar este valor manualmente.</span><span class="sxs-lookup"><span data-stu-id="a29a5-127">You can change this value manually.</span></span> <span data-ttu-id="a29a5-128">Asegúrese de usar una cadena que identifique de forma única el servicio.</span><span class="sxs-lookup"><span data-stu-id="a29a5-128">Just be sure to use a string that uniquely identifies your service.</span></span>

## <a name="using-the-windows-media-player-object-model"></a><span data-ttu-id="a29a5-129">Usar el modelo de objetos de Media Player de Windows</span><span class="sxs-lookup"><span data-stu-id="a29a5-129">Using the Windows Media Player Object Model</span></span>

<span data-ttu-id="a29a5-130">Para especificar un valor para **ContentDistributor** con el modelo de objetos de Media Player de Windows, use el método [media. setItemInfo](media-setiteminfo.md) .</span><span class="sxs-lookup"><span data-stu-id="a29a5-130">To specify a value for **ContentDistributor** using the Windows Media Player object model, use the [Media.setItemInfo](media-setiteminfo.md) method.</span></span> <span data-ttu-id="a29a5-131">En el ejemplo de código siguiente se especifica el valor "Proseware" para **ContentDistributor** para el elemento multimedia que se está reproduciendo actualmente:</span><span class="sxs-lookup"><span data-stu-id="a29a5-131">The following example code specifies the value "Proseware" for **ContentDistributor** for the currently playing media item:</span></span>


```C++
// Retrieve the current media item.
var theMedia = Player.currentMedia;

//Test whether the media item was retrieved.
if(theMedia)
{
    // Set the ContentDistributor value.
    theMedia.setItemInfo("ContentDistributor", "Proseware");
}
```



## <a name="using-the-windows-media-format-sdk"></a><span data-ttu-id="a29a5-132">Usar el SDK de Windows Media Format</span><span class="sxs-lookup"><span data-stu-id="a29a5-132">Using the Windows Media Format SDK</span></span>

<span data-ttu-id="a29a5-133">El SDK de Windows Media Player incluye un archivo de C++ de ejemplo denominado SetContentDistributor. cpp, que muestra cómo usar el SDK de Windows Media Format 9 series para agregar el atributo **WM/ContentDistributor** .</span><span class="sxs-lookup"><span data-stu-id="a29a5-133">The Windows Media Player SDK includes a sample C++ file, named SetContentDistributor.cpp, which demonstrates how to use the Windows Media Format 9 Series SDK to add the **WM/ContentDistributor** attribute.</span></span> <span data-ttu-id="a29a5-134">Puede buscar este archivo de ejemplo en la carpeta denominada Metadata (metadatos) en la que instaló el SDK.</span><span class="sxs-lookup"><span data-stu-id="a29a5-134">You can locate this sample file in the folder named Metadata where you installed the SDK.</span></span> <span data-ttu-id="a29a5-135">Para usar este código debe seguir estos pasos:</span><span class="sxs-lookup"><span data-stu-id="a29a5-135">To use this code you must follow these steps:</span></span>

1.  <span data-ttu-id="a29a5-136">Instale el SDK de Windows Media Format 9 series y configure el tiempo de ejecución como se describe en la documentación de.</span><span class="sxs-lookup"><span data-stu-id="a29a5-136">Install the Windows Media Format 9 Series SDK and configure the runtime as described in the documentation.</span></span>
2.  <span data-ttu-id="a29a5-137">Cree un nuevo proyecto de C++ vacío en Visual Studio y agregue el archivo de ejemplo denominado SetContentDistributor. cpp al proyecto.</span><span class="sxs-lookup"><span data-stu-id="a29a5-137">Create a new empty C++ project in Visual Studio and add the sample file named SetContentDistributor.cpp to the project.</span></span>
3.  <span data-ttu-id="a29a5-138">Agregue la ruta de acceso a las carpetas de biblioteca de SDK de Windows Media Format 9 series a la lista de rutas de acceso de archivo.</span><span class="sxs-lookup"><span data-stu-id="a29a5-138">Add the path to the Windows Media Format 9 Series SDK Lib folders to your list of file paths.</span></span> <span data-ttu-id="a29a5-139">En el menú **Herramientas** , elija **Opciones**.</span><span class="sxs-lookup"><span data-stu-id="a29a5-139">From the **Tools** menu, choose **Options**.</span></span>
4.  <span data-ttu-id="a29a5-140">En el cuadro de diálogo **Opciones** , haga clic en **proyectos** y, a continuación, haga clic en **directorios de VC + +**.</span><span class="sxs-lookup"><span data-stu-id="a29a5-140">In the **Options** dialog box, click **Projects**, and then click **VC++ Directories**.</span></span>
5.  <span data-ttu-id="a29a5-141">En el cuadro de lista desplegable **Mostrar directorios para** , haga clic en **archivos de biblioteca**.</span><span class="sxs-lookup"><span data-stu-id="a29a5-141">In the **Show Directories for** drop-down list box, click **Library files**.</span></span>
6.  <span data-ttu-id="a29a5-142">Use los botones para agregar las rutas de acceso a los cuadros de lista.</span><span class="sxs-lookup"><span data-stu-id="a29a5-142">Use the buttons to add the paths to the list boxes.</span></span>
7.  <span data-ttu-id="a29a5-143">Abra el cuadro de diálogo páginas de propiedades del proyecto.</span><span class="sxs-lookup"><span data-stu-id="a29a5-143">Open the property pages dialog box for your project.</span></span> <span data-ttu-id="a29a5-144">Seleccione **propiedades de configuración**, **enlazador** y, a continuación, **Escriba**.</span><span class="sxs-lookup"><span data-stu-id="a29a5-144">Choose **Configuration Properties**, then **Linker**, and then **Input**.</span></span> <span data-ttu-id="a29a5-145">Escriba "wmvcore. lib" en el cuadro de texto **dependencias adicionales** .</span><span class="sxs-lookup"><span data-stu-id="a29a5-145">Type "wmvcore.lib" in the **Additional Dependencies** text box.</span></span>

<span data-ttu-id="a29a5-146">El código de ejemplo crea un programa de línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a29a5-146">The sample code creates a command-line program.</span></span> <span data-ttu-id="a29a5-147">Los argumentos que se proporcionan al ejecutar el programa especifican la ruta de acceso al archivo multimedia digital que se va a modificar y una cadena para el valor del atributo **ContentDistributor** .</span><span class="sxs-lookup"><span data-stu-id="a29a5-147">The arguments you provide when running the program specify the path to the digital media file to modify and a string for the **ContentDistributor** attribute value.</span></span> <span data-ttu-id="a29a5-148">El código usa **IWMHeaderInfo:: setAttribute** para agregar el atributo al archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="a29a5-148">The code uses **IWMHeaderInfo::SetAttribute** to add the attribute to the file you specified.</span></span> <span data-ttu-id="a29a5-149">Puede usar este ejemplo tal como está o usarlo como punto de partida para su propio programa.</span><span class="sxs-lookup"><span data-stu-id="a29a5-149">You can use this sample as is or use it as a starting point for your own program.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a29a5-150">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a29a5-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a29a5-151">**Información común para las tiendas en línea de tipo 1 y 2**</span><span class="sxs-lookup"><span data-stu-id="a29a5-151">**Information Common to Type 1 and Type 2 Online Stores**</span></span>](information-common-to-type-1-and-type-2-online-stores.md)
</dt> </dl>

 

 




