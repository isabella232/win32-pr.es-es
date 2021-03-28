---
description: La barra del explorador se incorporó con Microsoft Internet Explorer 4,0 para proporcionar un área de presentación adyacente al panel del explorador.
title: Creación de barras del explorador, bandas de herramientas y bandas de escritorio personalizadas
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 4bf46b3f-f833-42e0-baf7-21bfa9e6d890
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b4adeaaf089c22bd3e1db3d60d552ccc3252545a
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 01/28/2021
ms.locfileid: "104566395"
---
# <a name="creating-custom-explorer-bars-tool-bands-and-desk-bands"></a><span data-ttu-id="e9ab9-103">Crear barras del explorador personalizadas, bandas de herramientas y bandas del Departamento de soporte técnico</span><span class="sxs-lookup"><span data-stu-id="e9ab9-103">Creating Custom Explorer Bars, Tool Bands, and Desk Bands</span></span>

<span data-ttu-id="e9ab9-104">La barra del explorador se incorporó con Microsoft Internet Explorer 4,0 para proporcionar un área de presentación adyacente al panel del explorador.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-104">The Explorer Bar was introduced with Microsoft Internet Explorer 4.0 to provide a display area adjacent to the browser pane.</span></span> <span data-ttu-id="e9ab9-105">Básicamente es una ventana secundaria dentro de la ventana de Windows Internet Explorer y se puede usar para mostrar información e interactuar con el usuario de forma muy similar.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-105">It is basically a child window within the Windows Internet Explorer window, and it can be used to display information and interact with the user in much the same way.</span></span> <span data-ttu-id="e9ab9-106">Las barras del explorador se muestran normalmente como un panel vertical en el lado izquierdo del panel del explorador.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-106">Explorer Bars are most commonly displayed as a vertical pane on the left side of the browser pane.</span></span> <span data-ttu-id="e9ab9-107">Sin embargo, también se puede mostrar una barra del explorador horizontalmente, debajo del panel del explorador.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-107">However, an Explorer Bar can also be displayed horizontally, below the browser pane.</span></span>

![Captura de pantalla que muestra las barras del explorador vertical y horizontal.](images/expl1.jpg)

<span data-ttu-id="e9ab9-109">Hay una amplia gama de usos posibles para la barra del explorador.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-109">There is a wide range of possible uses for the Explorer Bar.</span></span> <span data-ttu-id="e9ab9-110">Los usuarios pueden seleccionar la opción que desean ver de varias maneras diferentes, como seleccionarla en el submenú de la **barra del explorador** del menú **Ver** o hacer clic en un botón de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-110">Users can select which option they want to see in several different ways, including selecting it from the **Explorer Bar** submenu of the **View** menu, or clicking a toolbar button.</span></span> <span data-ttu-id="e9ab9-111">Internet Explorer proporciona varias barras del explorador estándar, como favoritos y búsqueda.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-111">Internet Explorer provides several standard Explorer Bars, including Favorites and Search.</span></span>

<span data-ttu-id="e9ab9-112">Una de las formas en que puede personalizar Internet Explorer es mediante la adición de una barra personalizada del explorador.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-112">One of the ways you can customize Internet Explorer is by adding a custom Explorer Bar.</span></span> <span data-ttu-id="e9ab9-113">Cuando se implementa y registra, se agrega al submenú de la **barra del explorador** del menú **Ver** .</span><span class="sxs-lookup"><span data-stu-id="e9ab9-113">When implemented and registered, it will be added to the **Explorer Bar** submenu of the **View** menu.</span></span> <span data-ttu-id="e9ab9-114">Cuando el usuario lo selecciona, se puede usar el área de presentación de la barra del explorador para mostrar información y tomar los datos proporcionados por el usuario de la misma manera que una ventana normal.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-114">When selected by the user, the Explorer Bar's display area can then be used to display information and take user input in much the same way as a normal window.</span></span>

![captura de pantalla de las barras del explorador](images/expl2.jpg)

<span data-ttu-id="e9ab9-116">Para crear una barra personalizada del explorador, debe implementar y registrar un *objeto de banda*.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-116">To create a custom Explorer Bar, you must implement and register a *band object*.</span></span> <span data-ttu-id="e9ab9-117">Los objetos de banda se introdujeron con la versión 4,71 del shell y proporcionan funcionalidades similares a las de las ventanas normales.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-117">Band objects were introduced with version 4.71 of the Shell and provide capabilities similar to those of normal windows.</span></span> <span data-ttu-id="e9ab9-118">Sin embargo, dado que son objetos del modelo de objetos componentes (COM) y están contenidos en Internet Explorer o en el Shell, se implementan de forma ligeramente diferente.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-118">However, because they are Component Object Model (COM) objects and contained by either Internet Explorer or the Shell, they are implemented somewhat differently.</span></span> <span data-ttu-id="e9ab9-119">Los objetos de banda simple se usaron para crear las barras del explorador de ejemplo que se muestran en el primer gráfico.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-119">Simple band objects were used to create the sample Explorer Bars displayed in the first graphic.</span></span> <span data-ttu-id="e9ab9-120">La implementación del ejemplo de la barra del explorador vertical se tratará en detalle en una sección posterior.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-120">The implementation of the vertical Explorer Bar sample will be discussed in detail in a later section.</span></span>

## <a name="tool-bands"></a><span data-ttu-id="e9ab9-121">Bandas de herramientas</span><span class="sxs-lookup"><span data-stu-id="e9ab9-121">Tool Bands</span></span>

<span data-ttu-id="e9ab9-122">Una *banda de herramientas* es un objeto de banda incluido en Microsoft Internet Explorer 5 para admitir la característica de barra de herramientas de radio de Windows.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-122">A *tool band* is a band object that was introduced with Microsoft Internet Explorer 5 to support the Windows radio toolbar feature.</span></span> <span data-ttu-id="e9ab9-123">La barra de herramientas de Internet Explorer es en realidad un [control rebar](../controls/rebar-controls.md) que contiene varios [controles de barra de herramientas](../controls/toolbar-control-reference.md).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-123">The Internet Explorer toolbar is actually a [rebar control](../controls/rebar-controls.md) that contains several [toolbar controls](../controls/toolbar-control-reference.md).</span></span> <span data-ttu-id="e9ab9-124">Al crear una banda de herramientas, puede Agregar una banda a ese control rebar.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-124">By creating a tool band, you can add a band to that rebar control.</span></span> <span data-ttu-id="e9ab9-125">Sin embargo, al igual que las barras del explorador, una banda de herramientas es una ventana de uso general.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-125">However, like Explorer Bars, a tool band is a general purpose window.</span></span>

![captura de pantalla de bandas de herramientas](images/toolband1.jpg)

<span data-ttu-id="e9ab9-127">Los usuarios muestran una barra de herramientas seleccionándola en el submenú **barras de herramientas** del menú **Ver** o en el menú contextual que se muestra al hacer clic con el botón secundario en el área de la barra de herramientas.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-127">Users display a toolbar by selecting it from the **Toolbars** submenu of the **View** menu or from the shortcut menu that is displayed by right-clicking the toolbar area.</span></span>

## <a name="desk-bands"></a><span data-ttu-id="e9ab9-128">Bandas del escritorio</span><span class="sxs-lookup"><span data-stu-id="e9ab9-128">Desk Bands</span></span>

<span data-ttu-id="e9ab9-129">Los objetos de banda también se pueden usar para crear *bandas del escritorio*.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-129">Band objects can also be used to create *desk bands*.</span></span> <span data-ttu-id="e9ab9-130">Aunque su implementación básica es similar a las barras del explorador, las bandas del escritorio no están relacionadas con Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-130">While their basic implementation is similar to Explorer Bars, desk bands are unrelated to Internet Explorer.</span></span> <span data-ttu-id="e9ab9-131">Una banda de escritorio es básicamente una manera de crear una ventana acoplable en el escritorio.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-131">A desk band is basically a way to create a dockable window on the desktop.</span></span> <span data-ttu-id="e9ab9-132">El usuario lo selecciona haciendo clic con el botón secundario en la barra de tareas y seleccionándolo en el submenú **barras de herramientas** .</span><span class="sxs-lookup"><span data-stu-id="e9ab9-132">The user selects it by right-clicking the taskbar and selecting it from the **Toolbars** submenu.</span></span>

![Captura de pantalla que muestra una banda de escritorio de ejemplo.](images/desk2.png)

<span data-ttu-id="e9ab9-134">Inicialmente, las bandas del escritorio se acoplan en la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-134">Initially, desk bands are docked on the taskbar.</span></span>

![Captura de pantalla que muestra las bandas de escritorio acopladas en la barra de tareas.](images/desk1.jpg)

<span data-ttu-id="e9ab9-136">A continuación, el usuario puede arrastrar la banda de escritorio al escritorio y aparecerá como una ventana normal.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-136">The user can then drag the desk band to the desktop, and it will appear as a normal window.</span></span>

![captura de pantalla de bandas de escritorio](images/desk3.png)

## <a name="implementing-band-objects"></a><span data-ttu-id="e9ab9-138">Implementar objetos de banda</span><span class="sxs-lookup"><span data-stu-id="e9ab9-138">Implementing Band Objects</span></span>

<span data-ttu-id="e9ab9-139">Se tratan los temas siguientes.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-139">The following topics are discussed.</span></span>

-   [<span data-ttu-id="e9ab9-140">Aspectos básicos de los objetos de banda</span><span class="sxs-lookup"><span data-stu-id="e9ab9-140">Band Object Basics</span></span>](#band-object-basics)
-   [<span data-ttu-id="e9ab9-141">Registro de banda</span><span class="sxs-lookup"><span data-stu-id="e9ab9-141">Band Registration</span></span>](#band-registration)
-   [<span data-ttu-id="e9ab9-142">Un ejemplo sencillo de una barra del explorador personalizada</span><span class="sxs-lookup"><span data-stu-id="e9ab9-142">A Simple Example of a Custom Explorer Bar</span></span>](#a-simple-example-of-a-custom-explorer-bar)

### <a name="band-object-basics"></a><span data-ttu-id="e9ab9-143">Aspectos básicos de los objetos de banda</span><span class="sxs-lookup"><span data-stu-id="e9ab9-143">Band Object Basics</span></span>

<span data-ttu-id="e9ab9-144">Aunque se pueden usar de forma muy parecida a las ventanas normales, los objetos de banda son objetos COM que existen dentro de un contenedor.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-144">Although they can be used much like normal windows, band objects are COM objects that exist within a container.</span></span> <span data-ttu-id="e9ab9-145">Las barras del explorador están contenidas en Internet Explorer y las bandas del escritorio están contenidas en el shell.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-145">Explorer Bars are contained by Internet Explorer, and desk bands are contained by the Shell.</span></span> <span data-ttu-id="e9ab9-146">Aunque sirven diferentes funciones, su implementación básica es muy similar.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-146">While they serve different functions, their basic implementation is very similar.</span></span> <span data-ttu-id="e9ab9-147">La principal diferencia radica en cómo se registra el objeto de banda, que a su vez controla el tipo de objeto y su contenedor.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-147">The primary difference is in how the band object is registered, which in turn controls the type of object and its container.</span></span> <span data-ttu-id="e9ab9-148">En esta sección se describen los aspectos de implementación comunes a todos los objetos de banda.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-148">This section discusses those aspects of implementation that are common to all band objects.</span></span> <span data-ttu-id="e9ab9-149">Vea [un ejemplo sencillo de una barra del explorador personalizada](#a-simple-example-of-a-custom-explorer-bar) para obtener más detalles sobre la implementación.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-149">See [A Simple Example of a Custom Explorer Bar](#a-simple-example-of-a-custom-explorer-bar) for additional implementation details.</span></span>

<span data-ttu-id="e9ab9-150">Además de [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) y [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), todos los objetos de banda deben implementar las interfaces siguientes.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-150">In addition to [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) and [**IClassFactory**](/windows/win32/api/unknwn/nn-unknwn-iclassfactory), all band objects must implement the following interfaces.</span></span>

-   [<span data-ttu-id="e9ab9-151">**IDeskBand**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-151">**IDeskBand**</span></span>](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband)
-   [<span data-ttu-id="e9ab9-152">**IObjectWithSite**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-152">**IObjectWithSite**</span></span>](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [<span data-ttu-id="e9ab9-153">**IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-153">**IPersistStream**</span></span>](/windows/win32/api/objidl/nn-objidl-ipersiststream)

<span data-ttu-id="e9ab9-154">Además de registrar su identificador de clase (CLSID), los objetos de la barra del explorador y de la banda del escritorio también deben estar registrados para la categoría del componente correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-154">In addition to registering their class identifier (CLSID), the Explorer Bar and desk band objects must also be registered for the appropriate component category.</span></span> <span data-ttu-id="e9ab9-155">El registro de la categoría de componentes determina el tipo de objeto y su contenedor.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-155">Registering the component category determines the object type and its container.</span></span> <span data-ttu-id="e9ab9-156">Las bandas de herramientas usan un procedimiento de registro diferente y no tienen un identificador de categoría (CATId).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-156">Tool bands use a different registration procedure and do not have a category identifier (CATID).</span></span> <span data-ttu-id="e9ab9-157">Los CATID de los tres objetos de banda que los necesitan son:</span><span class="sxs-lookup"><span data-stu-id="e9ab9-157">The CATIDs for the three band objects that require them are:</span></span>



| <span data-ttu-id="e9ab9-158">Tipo de banda</span><span class="sxs-lookup"><span data-stu-id="e9ab9-158">Band Type</span></span>               | <span data-ttu-id="e9ab9-159">Categoría de componentes</span><span class="sxs-lookup"><span data-stu-id="e9ab9-159">Component Category</span></span> |
|-------------------------|--------------------|
| <span data-ttu-id="e9ab9-160">Barra del explorador vertical</span><span class="sxs-lookup"><span data-stu-id="e9ab9-160">Vertical Explorer Bar</span></span>   | <span data-ttu-id="e9ab9-161">CATId \_ InfoBand</span><span class="sxs-lookup"><span data-stu-id="e9ab9-161">CATID\_InfoBand</span></span>    |
| <span data-ttu-id="e9ab9-162">Barra del explorador horizontal</span><span class="sxs-lookup"><span data-stu-id="e9ab9-162">Horizontal Explorer Bar</span></span> | <span data-ttu-id="e9ab9-163">CATId \_ CommBand</span><span class="sxs-lookup"><span data-stu-id="e9ab9-163">CATID\_CommBand</span></span>    |
| <span data-ttu-id="e9ab9-164">Banda de escritorio</span><span class="sxs-lookup"><span data-stu-id="e9ab9-164">Desk Band</span></span>               | <span data-ttu-id="e9ab9-165">CATId \_ DeskBand</span><span class="sxs-lookup"><span data-stu-id="e9ab9-165">CATID\_DeskBand</span></span>    |



 

<span data-ttu-id="e9ab9-166">Consulte [registro de banda](#band-registration) para obtener más información sobre cómo registrar objetos de banda.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-166">See [Band Registration](#band-registration) for further discussion of how to register band objects.</span></span>

<span data-ttu-id="e9ab9-167">Si el objeto de banda va a aceptar la entrada del usuario, también debe implementar [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-167">If the band object is to accept user input, it must also implement [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject).</span></span> <span data-ttu-id="e9ab9-168">Para agregar elementos al menú contextual de las bandas del escritorio o de la barra del explorador, el objeto de banda debe exportar [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-168">To add items to the shortcut menu for Explorer Bar or desk bands, the band object must export [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> <span data-ttu-id="e9ab9-169">Las bandas de herramientas no admiten menús contextuales.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-169">Tool bands do not support shortcut menus.</span></span>

<span data-ttu-id="e9ab9-170">Dado que los objetos de banda implementan una ventana secundaria, también deben implementar un procedimiento de ventana para controlar la mensajería de Windows.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-170">Because band objects implement a child window, they must also implement a window procedure to handle Windows messaging.</span></span>

<span data-ttu-id="e9ab9-171">Los objetos de banda pueden enviar comandos a su contenedor a través de la interfaz [**IOLECommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) del contenedor.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-171">Band objects can send commands to their container through the container's [**IOleCommandTarget**](/windows/win32/api/docobj/nn-docobj-iolecommandtarget) interface.</span></span> <span data-ttu-id="e9ab9-172">Para obtener el puntero de interfaz, llame al método [**IInputObjectSite:: QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) del contenedor y solicite IOLECOMMANDTARGET de IID \_ .</span><span class="sxs-lookup"><span data-stu-id="e9ab9-172">To obtain the interface pointer, call the container's [**IInputObjectSite::QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method and ask for IID\_IOleCommandTarget.</span></span> <span data-ttu-id="e9ab9-173">Después, envía comandos al contenedor con [**IOLECommandTarget:: exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-173">You then send commands to the container with [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec).</span></span> <span data-ttu-id="e9ab9-174">El grupo de comandos es CGID \_ DeskBand.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-174">The command group is CGID\_DeskBand.</span></span> <span data-ttu-id="e9ab9-175">Cuando se llama al método [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) de un objeto de banda, el contenedor usa el parámetro *dwBandID* para asignar el objeto de banda a un identificador que se usa para tres de los comandos.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-175">When a band object's [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) method is called, the container uses the *dwBandID* parameter to assign the band object an identifier that is used for three of the commands.</span></span> <span data-ttu-id="e9ab9-176">Se admiten cuatro identificadores de comando **IOLECommandTarget:: exec** .</span><span class="sxs-lookup"><span data-stu-id="e9ab9-176">Four **IOleCommandTarget::Exec** command IDs are supported.</span></span>

-   <span data-ttu-id="e9ab9-177">DBID \_ BANDINFOCHANGED</span><span class="sxs-lookup"><span data-stu-id="e9ab9-177">DBID\_BANDINFOCHANGED</span></span>

    <span data-ttu-id="e9ab9-178">La información de la banda ha cambiado.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-178">The band's information has changed.</span></span> <span data-ttu-id="e9ab9-179">Establezca el parámetro *pvaIn* en el identificador de banda que se recibió en la llamada más reciente a [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-179">Set the *pvaIn* parameter to the band identifier that was received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span> <span data-ttu-id="e9ab9-180">El contenedor llamará al método **IDeskBand:: GetBandInfo** del objeto de banda para solicitar la información actualizada.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-180">The container will call the band object's **IDeskBand::GetBandInfo** method to request the updated information.</span></span>

-   <span data-ttu-id="e9ab9-181">DBID \_ MAXIMIZEBAND</span><span class="sxs-lookup"><span data-stu-id="e9ab9-181">DBID\_MAXIMIZEBAND</span></span>

    <span data-ttu-id="e9ab9-182">Maximice la banda.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-182">Maximize the band.</span></span> <span data-ttu-id="e9ab9-183">Establezca el parámetro *pvaIn* en el identificador de banda que se recibió en la llamada más reciente a [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-183">Set the *pvaIn* parameter to the band identifier that was received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span>

-   <span data-ttu-id="e9ab9-184">DBID \_ SHOWONLY</span><span class="sxs-lookup"><span data-stu-id="e9ab9-184">DBID\_SHOWONLY</span></span>

    <span data-ttu-id="e9ab9-185">Activar o desactivar otras bandas del contenedor.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-185">Turn other bands in the container on or off.</span></span> <span data-ttu-id="e9ab9-186">Establezca el parámetro *pvaIn* en el \_ tipo desconocido de VT con uno de los siguientes valores:</span><span class="sxs-lookup"><span data-stu-id="e9ab9-186">Set the *pvaIn* parameter to the VT\_UNKNOWN type with one of the following values:</span></span>

    

    | <span data-ttu-id="e9ab9-187">Value</span><span class="sxs-lookup"><span data-stu-id="e9ab9-187">Value</span></span> | <span data-ttu-id="e9ab9-188">Descripción</span><span class="sxs-lookup"><span data-stu-id="e9ab9-188">Description</span></span>                                                                                                 |
    |-------|-------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="e9ab9-189">pUnk</span><span class="sxs-lookup"><span data-stu-id="e9ab9-189">pUnk</span></span>  | <span data-ttu-id="e9ab9-190">Puntero a la interfaz [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del objeto de banda.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-190">A pointer to the band object's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="e9ab9-191">Se ocultarán todas las demás bandas del escritorio.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-191">All other desk bands will be hidden.</span></span> |
    | <span data-ttu-id="e9ab9-192">0</span><span class="sxs-lookup"><span data-stu-id="e9ab9-192">0</span></span>     | <span data-ttu-id="e9ab9-193">Ocultar todas las bandas del escritorio.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-193">Hide all desk bands.</span></span>                                                                                        |
    | <span data-ttu-id="e9ab9-194">1</span><span class="sxs-lookup"><span data-stu-id="e9ab9-194">1</span></span>     | <span data-ttu-id="e9ab9-195">Mostrar todas las bandas del escritorio.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-195">Show all desk bands.</span></span>                                                                                        |

    

     

-   <span data-ttu-id="e9ab9-196">DBID \_ PUSHCHEVRON</span><span class="sxs-lookup"><span data-stu-id="e9ab9-196">DBID\_PUSHCHEVRON</span></span>

    <span data-ttu-id="e9ab9-197">[Versión 5](versions.md).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-197">[Version 5](versions.md).</span></span> <span data-ttu-id="e9ab9-198">Mostrar un menú de botón de contenido adicional.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-198">Display a chevron menu.</span></span> <span data-ttu-id="e9ab9-199">El contenedor envía un mensaje [**RB \_ PUSHCHEVRON**](../controls/rb-pushchevron.md) y el objeto Band recibe una notificación [RBN \_ CHEVRONPUSHED](../controls/rbn-chevronpushed.md) que le pide que muestre el menú de comillas angulares.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-199">The container sends an [**RB\_PUSHCHEVRON**](../controls/rb-pushchevron.md) message, and the band object receives an [RBN\_CHEVRONPUSHED](../controls/rbn-chevronpushed.md) notification that prompts it to display the chevron menu.</span></span> <span data-ttu-id="e9ab9-200">Establezca el parámetro *nCmdExecOpt* del método [**IOLECommandTarget:: exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) en el identificador de banda recibido en la llamada más reciente a [**IDeskBand:: GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-200">Set the [**IOleCommandTarget::Exec**](/windows/win32/api/docobj/nf-docobj-iolecommandtarget-exec) method's *nCmdExecOpt* parameter to the band identifier received in the most recent call to [**IDeskBand::GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband).</span></span> <span data-ttu-id="e9ab9-201">Establezca el parámetro *pvaIn* del método **IOLECommandTarget:: exec** en el tipo de la \_ aplicación VT con un valor definido por la aplicación.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-201">Set the **IOleCommandTarget::Exec** method's *pvaIn* parameter to the VT\_I4 type with an application-defined value.</span></span> <span data-ttu-id="e9ab9-202">Vuelve a pasar al objeto de banda como el valor *lAppValue* de la \_ notificación CHEVRONPUSHED de RBN.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-202">It passes back to the band object as the *lAppValue* value of the RBN\_CHEVRONPUSHED notification.</span></span>

### <a name="band-registration"></a><span data-ttu-id="e9ab9-203">Registro de banda</span><span class="sxs-lookup"><span data-stu-id="e9ab9-203">Band Registration</span></span>

<span data-ttu-id="e9ab9-204">Un objeto de banda se debe registrar como un servidor de tipo OLE en proceso que admite el subprocesamiento de apartamento.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-204">A band object must be registered as an OLE in-process server that supports apartment threading.</span></span> <span data-ttu-id="e9ab9-205">El valor predeterminado del servidor es una cadena de texto de menú.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-205">The default value for the server is a menu text string.</span></span> <span data-ttu-id="e9ab9-206">En el caso de las barras del explorador, aparecerá en el submenú de la **barra del explorador** del menú **Ver** de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-206">For Explorer Bars, it will appear in the **Explorer Bar** submenu of the Internet Explorer **View** menu.</span></span> <span data-ttu-id="e9ab9-207">En el caso de las bandas de herramientas, aparecerá en el submenú **barras de herramientas** del menú **Ver** de Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-207">For tool bands, it will appear in the **Toolbars** submenu of the Internet Explorer **View** menu.</span></span> <span data-ttu-id="e9ab9-208">En el caso de las bandas del escritorio, aparecerá en el submenú **barras de herramientas** del menú contextual de la barra de tareas.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-208">For desk bands, it will appear in the **Toolbars** submenu of the taskbar's shortcut menu.</span></span> <span data-ttu-id="e9ab9-209">Al igual que con los recursos de menú, si coloca una y comercial (&) delante de una letra, se subrayará y se habilitarán los métodos abreviados de teclado.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-209">As with menu resources, placing an ampersand (&) in front of a letter will cause it to be underlined and enable keyboard shortcuts.</span></span> <span data-ttu-id="e9ab9-210">Por ejemplo, la cadena de menú de la barra del explorador vertical que se muestra en el primer gráfico es "ejemplo &barra del explorador vertical".</span><span class="sxs-lookup"><span data-stu-id="e9ab9-210">For example, the menu string for the vertical Explorer Bar shown in the first graphic is "Sample &Vertical Explorer Bar".</span></span>

<span data-ttu-id="e9ab9-211">Inicialmente, Internet Explorer recupera una enumeración de los objetos de barra del explorador registrados del registro mediante las categorías de componentes.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-211">Initially, Internet Explorer retrieves an enumeration of the registered Explorer Bar objects from the registry using the component categories.</span></span> <span data-ttu-id="e9ab9-212">Para aumentar el rendimiento, almacena en caché esta enumeración, lo que provoca que se pasen por alto las barras del explorador agregadas posteriormente.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-212">To increase performance, it then caches this enumeration, causing subsequently added Explorer Bars to be overlooked.</span></span> <span data-ttu-id="e9ab9-213">Para forzar a Windows Internet Explorer a volver a generar la memoria caché y reconocer una nueva barra del explorador, elimine las siguientes claves del registro durante el registro de la nueva barra del explorador:</span><span class="sxs-lookup"><span data-stu-id="e9ab9-213">To force Windows Internet Explorer to rebuild the cache and recognize a new Explorer Bar, delete the following registry keys during the registration of the new Explorer Bar:</span></span>

<span data-ttu-id="e9ab9-214">**HKEY \_ Software de \_ usuario actual** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **descartable** \\ **postsetup** \\ **Component Categories** \\ **{00021493-0000-0000-C000-000000000046}** \\ **enum**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-214">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Explorer**\\**Discardable**\\**PostSetup**\\**Component Categories**\\ **{00021493-0000-0000-C000-000000000046}**\\**Enum**</span></span>

<span data-ttu-id="e9ab9-215">**HKEY \_ Software de \_ usuario actual** \\  \\ **Microsoft** \\ **Windows** \\ **CurrentVersion** \\ **Explorer** \\ **descartable** \\ **postsetup** \\ **Component Categories** \\ **{00021494-0000-0000-C000-000000000046}** \\ **enum**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-215">**HKEY\_CURRENT\_USER**\\**Software**\\**Microsoft**\\**Windows**\\**CurrentVersion**\\**Explorer**\\**Discardable**\\**PostSetup**\\**Component Categories**\\ **{00021494-0000-0000-C000-000000000046}**\\**Enum**</span></span>

> [!Note]  
> <span data-ttu-id="e9ab9-216">Dado que se crea una memoria caché de la barra del explorador para cada usuario, es posible que la aplicación de instalación tenga que enumerar todos los subárboles del registro del usuario o agregar un código auxiliar por usuario para que se ejecute cuando el usuario inicie sesión por primera vez.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-216">Because an Explorer Bar cache is created for each user, your setup application may need to enumerate all the user registry hives or add a per-user stub to run when the user first logs on.</span></span>

 

<span data-ttu-id="e9ab9-217">En general, la entrada básica del registro para un objeto de banda aparecerá de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-217">In general, the basic registry entry for a band object will appear as follows.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
```

<span data-ttu-id="e9ab9-218">Los grupos de herramientas también deben tener el CLSID del objeto registrado con Internet Explorer.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-218">Tool bands must also have their object's CLSID registered with Internet Explorer.</span></span> <span data-ttu-id="e9ab9-219">Para ello, asigne un valor en la barra de herramientas **HKEY \_ local \_ Machine** \\ **software** \\ **Microsoft** \\ **Internet Explorer** \\  denominada con el GUID de CLSID del objeto de banda de herramientas, como se muestra aquí.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-219">To do this, assign a value under **HKEY\_LOCAL\_MACHINE**\\**Software**\\**Microsoft**\\**Internet Explorer**\\**Toolbar** named with the tool band object's CLSID GUID as shown here.</span></span> <span data-ttu-id="e9ab9-220">Se omite su valor de datos, por lo que el tipo de valor no es importante.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-220">Its data value is ignored, so the value type is unimportant.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Internet Explorer
            Toolbar
               {Your Band Object's CLSID GUID}
```

<span data-ttu-id="e9ab9-221">Hay varios valores opcionales que también se pueden agregar al registro.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-221">There are several optional values that can also be added to the registry.</span></span> <span data-ttu-id="e9ab9-222">Por ejemplo, el siguiente valor es necesario si desea usar la barra del explorador para mostrar el código HTML; el valor que se muestra no es un ejemplo, sino el valor real que se debe usar.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-222">For instance, the following value is necessary if you want to use the Explorer Bar to display HTML The value shown is not an example, but the actual value that should be used.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
```

<span data-ttu-id="e9ab9-223">Cuando se usa junto con el valor mostrado anteriormente, también es necesario el siguiente valor opcional si desea utilizar la barra del explorador para mostrar el código HTML.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-223">Used in conjunction with the value shown above, the following optional value is also necessary if you want to use the Explorer Bar to display HTML.</span></span> <span data-ttu-id="e9ab9-224">Este valor debe establecerse en la ubicación del archivo que contiene el contenido HTML de la barra del explorador.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-224">This value should be set to the location of the file that contains the HTML content for the Explorer Bar.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         Instance
            InitPropertyBag
               Url
```

<span data-ttu-id="e9ab9-225">Otro valor opcional define el ancho o el alto predeterminados de la barra del explorador, en función de si es vertical u horizontal, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-225">Another optional value defines the default width or height of the Explorer Bar, depending on whether it is vertical or horizontal, respectively.</span></span>

```
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize
```

<span data-ttu-id="e9ab9-226">El valor de UpBars debe establecerse en el ancho o el alto de la barra.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-226">The BarSize value should be set to the width or height of the bar.</span></span> <span data-ttu-id="e9ab9-227">El valor requiere ocho bytes y se coloca en el registro como un valor binario.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-227">The value requires eight bytes and is placed in the registry as a binary value.</span></span> <span data-ttu-id="e9ab9-228">Los primeros cuatro bytes especifican el tamaño en píxeles, en formato hexadecimal, empezando por el byte más a la izquierda.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-228">The first four bytes specify the size in pixels, in hexadecimal format, starting from the leftmost byte.</span></span> <span data-ttu-id="e9ab9-229">Los últimos cuatro bytes están reservados y deben establecerse en cero.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-229">The last four bytes are reserved and should be set to zero.</span></span>

<span data-ttu-id="e9ab9-230">Por ejemplo, aquí se muestran las entradas del registro completas para una barra del explorador compatible con HTML con un ancho predeterminado de 291 píxeles (0x123).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-230">As an example, the full registry entries for an HTML-capable Explorer Bar with a default width of 291 (0x123) pixels are shown here.</span></span>

```
HKEY_CLASSES_ROOT
   CLSID
      {Your Band Object's CLSID GUID}
         (Default) = Menu Text String
         InProcServer32
            (Default) = DLL Path Name
            ThreadingModel = Apartment
         Instance
            CLSID
               (Default) = {4D5C8C2A-D075-11D0-B416-00C04FB90376}
            InitPropertyBag
               Url = Your HTML File
HKEY_CURRENT_USER
   Software
      Microsoft
         Internet Explorer
            Explorer Bars
               {Your Band Object's CLSID GUID}
                  BarSize = 23 01 00 00 00 00 00 00
```

<span data-ttu-id="e9ab9-231">Puede controlar el registro del CATId de un objeto de banda mediante programación.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-231">You can handle registration of a band object's CATID programmatically.</span></span> <span data-ttu-id="e9ab9-232">Cree un objeto de administrador de categorías de componentes (CLSID \_ StdComponentCategoriesMgr) y solicite un puntero a su interfaz [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) .</span><span class="sxs-lookup"><span data-stu-id="e9ab9-232">Create a component categories manager object (CLSID\_StdComponentCategoriesMgr) and request a pointer to its [**ICatRegister**](/windows/win32/api/comcat/nn-comcat-icatregister) interface.</span></span> <span data-ttu-id="e9ab9-233">Pase el CLSID del objeto de banda y el CATId a [**ICatRegister:: RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-233">Pass the band object's CLSID and CATID to [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories).</span></span>

### <a name="a-simple-example-of-a-custom-explorer-bar"></a><span data-ttu-id="e9ab9-234">Un ejemplo sencillo de una barra del explorador personalizada</span><span class="sxs-lookup"><span data-stu-id="e9ab9-234">A Simple Example of a Custom Explorer Bar</span></span>

<span data-ttu-id="e9ab9-235">Este ejemplo pasa por la implementación de la barra del explorador vertical de ejemplo que se muestra en la introducción.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-235">This example goes through the implementation of the sample vertical Explorer Bar shown in the introduction.</span></span>

<span data-ttu-id="e9ab9-236">El procedimiento básico para crear una barra personalizada del explorador es el siguiente.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-236">The basic procedure for creating a custom Explorer Bar is as follows.</span></span>

1.  <span data-ttu-id="e9ab9-237">[Implemente las funciones necesarias para la dll](#dll-functions).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-237">[Implement the functions needed by the DLL](#dll-functions).</span></span>
2.  [<span data-ttu-id="e9ab9-238">Implemente las interfaces COM necesarias.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-238">Implement the required COM interfaces.</span></span>](#required-interface-implementations)
3.  [<span data-ttu-id="e9ab9-239">Implemente las interfaces COM opcionales que desee.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-239">Implement any desired optional COM interfaces.</span></span>](#optional-interface-implementations)
4.  [<span data-ttu-id="e9ab9-240">Registre el CLSID del objeto y, si es necesario, la categoría de componente.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-240">Register the object's CLSID and, if required, component category.</span></span>](#clsid-registration)
5.  <span data-ttu-id="e9ab9-241">Cree una ventana secundaria de Internet Explorer cuyo tamaño se ajuste a la región de visualización de la barra del explorador.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-241">Create a child window of Internet Explorer, sized to fit the Explorer Bar's display region.</span></span>
6.  [<span data-ttu-id="e9ab9-242">Use la ventana secundaria para mostrar información e interactuar con el usuario.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-242">Use the child window to display information and interact with the user.</span></span>](#the-window-procedure)

<span data-ttu-id="e9ab9-243">La implementación muy sencilla que se usa en el ejemplo de la barra del explorador se podría usar realmente para cualquier tipo de barra del explorador, o una banda de escritorio, simplemente registrándose en la categoría del componente correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-243">The very simple implementation used in the Explorer Bar sample could actually be used for either type of Explorer Bar, or a desk band, by simply registering it for the appropriate component category.</span></span> <span data-ttu-id="e9ab9-244">Las implementaciones más sofisticadas deberán personalizarse para la región y el contenedor de visualización de cada tipo de objeto.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-244">More sophisticated implementations will need to be customized for each object type's display region and container.</span></span> <span data-ttu-id="e9ab9-245">Sin embargo, gran parte de esta personalización se puede llevar a cabo mediante el uso del código de ejemplo y su extensión aplicando técnicas de programación de Windows conocidas a la ventana secundaria.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-245">However, much of this customization can be accomplished by taking the sample code and extending it by applying familiar Windows programming techniques to the child window.</span></span> <span data-ttu-id="e9ab9-246">Por ejemplo, puede Agregar controles para la interacción del usuario o gráficos para una pantalla más completa.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-246">For example, you can add controls for user interaction, or graphics for a richer display.</span></span>

### <a name="dll-functions"></a><span data-ttu-id="e9ab9-247">Funciones DLL</span><span class="sxs-lookup"><span data-stu-id="e9ab9-247">DLL Functions</span></span>

<span data-ttu-id="e9ab9-248">Los tres objetos se empaquetan en un solo archivo DLL, que expone las siguientes funciones.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-248">All three objects are packaged in a single DLL, which exposes the following functions.</span></span>

-   [<span data-ttu-id="e9ab9-249">**DllMain**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-249">**DllMain**</span></span>](../dlls/dllmain.md)
-   [<span data-ttu-id="e9ab9-250">**DllCanUnloadNow**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-250">**DllCanUnloadNow**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-dllcanunloadnow)
-   [<span data-ttu-id="e9ab9-251">**DllGetClassObject**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-251">**DllGetClassObject**</span></span>](/windows/win32/api/combaseapi/nf-combaseapi-dllgetclassobject)
-   [<span data-ttu-id="e9ab9-252">**DllRegisterServer**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-252">**DllRegisterServer**</span></span>](/windows/win32/api/olectl/nf-olectl-dllregisterserver)

<span data-ttu-id="e9ab9-253">Las tres primeras funciones son implementaciones estándar y no se tratarán aquí.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-253">The first three functions are standard implementations and will not be discussed here.</span></span> <span data-ttu-id="e9ab9-254">La implementación del generador de clases también es estándar.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-254">The Class Factory implementation is also standard.</span></span>

### <a name="required-interface-implementations"></a><span data-ttu-id="e9ab9-255">Implementaciones de interfaz necesarias</span><span class="sxs-lookup"><span data-stu-id="e9ab9-255">Required Interface Implementations</span></span>

<span data-ttu-id="e9ab9-256">El ejemplo de barra del explorador vertical implementa las cuatro interfaces necesarias: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream)y [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) como parte de la clase CExplorerBar.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-256">The vertical Explorer Bar sample implements the four required interfaces: [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown), [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite), [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream), and [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) as part of the CExplorerBar class.</span></span> <span data-ttu-id="e9ab9-257">Las implementaciones de constructor, destructor e **IUnknown** son sencillas y no se tratarán aquí.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-257">The constructor, destructor, and **IUnknown** implementations are straightforward, and will not be discussed here.</span></span> <span data-ttu-id="e9ab9-258">Vea el código de ejemplo para obtener más detalles.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-258">See the sample code for details.</span></span>

<span data-ttu-id="e9ab9-259">Las siguientes interfaces se describen en detalle.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-259">The following interfaces are discussed in detail.</span></span>

-   [<span data-ttu-id="e9ab9-260">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="e9ab9-260">IObjectWithSite</span></span>](#iobjectwithsite)
-   [<span data-ttu-id="e9ab9-261">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="e9ab9-261">IPersistStream</span></span>](#ipersiststream)
-   [<span data-ttu-id="e9ab9-262">IDeskBand</span><span class="sxs-lookup"><span data-stu-id="e9ab9-262">IDeskBand</span></span>](#ideskband)

### <a name="iobjectwithsite"></a><span data-ttu-id="e9ab9-263">IObjectWithSite</span><span class="sxs-lookup"><span data-stu-id="e9ab9-263">IObjectWithSite</span></span>

<span data-ttu-id="e9ab9-264">Cuando el usuario selecciona una barra del explorador, el contenedor llama al método [**IObjectWithSite:: SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) del objeto de banda correspondiente.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-264">When the user selects an Explorer Bar, the container calls the corresponding band object's [**IObjectWithSite::SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) method.</span></span> <span data-ttu-id="e9ab9-265">El parámetro *punkSite* se establecerá en el puntero [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) del sitio.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-265">The *punkSite* parameter will be set to the site's [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) pointer.</span></span>

<span data-ttu-id="e9ab9-266">En general, una implementación de [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) debe realizar los siguientes pasos:</span><span class="sxs-lookup"><span data-stu-id="e9ab9-266">In general, a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) implementation should perform the following steps:</span></span>

1.  <span data-ttu-id="e9ab9-267">Libera todos los punteros de sitio que se están conservando actualmente.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-267">Release any site pointer that is currently being held.</span></span>
2.  <span data-ttu-id="e9ab9-268">Si el puntero que se pasa a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) se establece en **null**, se quita la banda.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-268">If the pointer passed to [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) is set to **NULL**, the band is being removed.</span></span> <span data-ttu-id="e9ab9-269">**SetSite** puede devolver S \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-269">**SetSite** can return S\_OK.</span></span>
3.  <span data-ttu-id="e9ab9-270">Si el puntero que se pasa a [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) no es **null**, se establece un nuevo sitio.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-270">If the pointer passed to [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) is non-**NULL**, a new site is being set.</span></span> <span data-ttu-id="e9ab9-271">**SetSite** debe hacer lo siguiente:</span><span class="sxs-lookup"><span data-stu-id="e9ab9-271">**SetSite** should do the following:</span></span>
    1.  <span data-ttu-id="e9ab9-272">Llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el sitio para su interfaz [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) .</span><span class="sxs-lookup"><span data-stu-id="e9ab9-272">Call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the site for its [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) interface.</span></span>
    2.  <span data-ttu-id="e9ab9-273">Llame a [**IOleWindow:: GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) para obtener el identificador de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-273">Call [**IOleWindow::GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) to obtain the parent window's handle.</span></span> <span data-ttu-id="e9ab9-274">Guarde el identificador para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-274">Save the handle for later use.</span></span> <span data-ttu-id="e9ab9-275">Libere [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) si ya no es necesario.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-275">Release [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) if it is no longer needed.</span></span>
    3.  <span data-ttu-id="e9ab9-276">Cree la ventana del objeto de banda como un elemento secundario de la ventana obtenida en el paso anterior.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-276">Create the band object's window as a child of the window obtained in the previous step.</span></span> <span data-ttu-id="e9ab9-277">No lo cree como una ventana visible.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-277">Do not create it as a visible window.</span></span>
    4.  <span data-ttu-id="e9ab9-278">Si el objeto Band implementa [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), llame a [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) en el sitio para su interfaz [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) .</span><span class="sxs-lookup"><span data-stu-id="e9ab9-278">If the band object implements [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject), call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the site for its [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) interface.</span></span> <span data-ttu-id="e9ab9-279">Almacene el puntero en esta interfaz para su uso posterior.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-279">Store the pointer to this interface for use later.</span></span>
    5.  <span data-ttu-id="e9ab9-280">Si todos los pasos se realizan correctamente, vuelva a ser correcto \_ .</span><span class="sxs-lookup"><span data-stu-id="e9ab9-280">If all steps are successful, return S\_OK.</span></span> <span data-ttu-id="e9ab9-281">En caso contrario, devuelve el código de error definido por OLE que indica el error.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-281">If not, return the OLE-defined error code indicating what failed.</span></span>

<span data-ttu-id="e9ab9-282">El ejemplo de barra del explorador implementa [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) de la siguiente manera.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-282">The Explorer Bar sample implements [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite) in the following way.</span></span> <span data-ttu-id="e9ab9-283">En el siguiente código *m \_ pSite* es una variable miembro privada que contiene el puntero [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) y *m \_ hwndParent* contiene el identificador de la ventana primaria.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-283">In the following code *m\_pSite* is a private member variable that holds the [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) pointer and *m\_hwndParent* holds the parent window's handle.</span></span> <span data-ttu-id="e9ab9-284">En este ejemplo, también se controla la creación de ventanas.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-284">In this sample, window creation is also handled.</span></span> <span data-ttu-id="e9ab9-285">Si la ventana no existe, este método crea la ventana de la barra del explorador como un elemento secundario con el tamaño adecuado de la ventana primaria obtenida por **SetSite**.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-285">If the window does not exist, this method creates the Explorer Bar's window as an appropriately sized child of the parent window obtained by **SetSite**.</span></span> <span data-ttu-id="e9ab9-286">El identificador de la ventana secundaria se almacena en *m \_ hWnd*.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-286">The child window's handle is stored in *m\_hwnd*.</span></span>


```C++
STDMETHODIMP CDeskBand::SetSite(IUnknown *pUnkSite)
{
    HRESULT hr = S_OK;

    m_hwndParent = NULL;

    if (m_pSite)
    {
        m_pSite->Release();
    }

    if (pUnkSite)
    {
        IOleWindow *pow;
        hr = pUnkSite->QueryInterface(IID_IOleWindow, reinterpret_cast<void **>(&pow));
        if (SUCCEEDED(hr))
        {
            hr = pow->GetWindow(&m_hwndParent);
            if (SUCCEEDED(hr))
            {
                WNDCLASSW wc = { 0 };
                wc.style         = CS_HREDRAW | CS_VREDRAW;
                wc.hCursor       = LoadCursor(NULL, IDC_ARROW);
                wc.hInstance     = g_hInst;
                wc.lpfnWndProc   = WndProc;
                wc.lpszClassName = g_szDeskBandSampleClass;
                wc.hbrBackground = CreateSolidBrush(RGB(255, 255, 0));

                RegisterClassW(&wc);

                CreateWindowExW(0,
                                g_szDeskBandSampleClass,
                                NULL,
                                WS_CHILD | WS_CLIPCHILDREN | WS_CLIPSIBLINGS,
                                0,
                                0,
                                0,
                                0,
                                m_hwndParent,
                                NULL,
                                g_hInst,
                                this);

                if (!m_hwnd)
                {
                    hr = E_FAIL;
                }
            }

            pow->Release();
        }

        hr = pUnkSite->QueryInterface(IID_IInputObjectSite, reinterpret_cast<void **>(&m_pSite));
    }

    return hr;
}
```



<span data-ttu-id="e9ab9-287">La implementación de [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) del ejemplo simplemente ajusta una llamada al método [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) del sitio mediante el puntero de sitio guardado por [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-287">The sample's [**GetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-getsite) implementation simply wraps a call to the site's [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) method, using the site pointer saved by [**SetSite**](/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite).</span></span>


```C++
STDMETHODIMP CDeskBand::GetSite(REFIID riid, void **ppv)
{
    HRESULT hr = E_FAIL;

    if (m_pSite)
    {
        hr =  m_pSite->QueryInterface(riid, ppv);
    }
    else
    {
        *ppv = NULL;
    }

    return hr;
}
```



### <a name="ipersiststream"></a><span data-ttu-id="e9ab9-288">IPersistStream</span><span class="sxs-lookup"><span data-stu-id="e9ab9-288">IPersistStream</span></span>

<span data-ttu-id="e9ab9-289">Internet Explorer llamará a la interfaz [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) de la barra del explorador para permitir que la barra del explorador cargue o guarde datos persistentes.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-289">Internet Explorer will call the Explorer Bar's [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream) interface to allow the Explorer Bar to load or save persistent data.</span></span> <span data-ttu-id="e9ab9-290">Si no hay datos persistentes, los métodos deben devolver un código de éxito.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-290">If there is no persistent data, the methods must still return a success code.</span></span> <span data-ttu-id="e9ab9-291">La interfaz **IPersistStream** hereda de [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), por lo que deben implementarse cinco métodos.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-291">The **IPersistStream** interface inherits from [**IPersist**](/windows/win32/api/objidl/nn-objidl-ipersist), so five methods must be implemented.</span></span>

-   [<span data-ttu-id="e9ab9-292">**IPersist:: GetClassID**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-292">**IPersist::GetClassID**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid)
-   [<span data-ttu-id="e9ab9-293">**IPersistStream:: IsDirty**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-293">**IPersistStream::IsDirty**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-isdirty)
-   [<span data-ttu-id="e9ab9-294">**IPersistStream:: Load**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-294">**IPersistStream::Load**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-load)
-   [<span data-ttu-id="e9ab9-295">**IPersistStream:: Save**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-295">**IPersistStream::Save**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-save)
-   [<span data-ttu-id="e9ab9-296">**IPersistStream:: GetSizeMax**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-296">**IPersistStream::GetSizeMax**</span></span>](/windows/win32/api/objidl/nf-objidl-ipersiststream-getsizemax)

<span data-ttu-id="e9ab9-297">El ejemplo de barra del explorador no usa ningún dato persistente y solo tiene una implementación mínima de [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-297">The Explorer Bar sample does not use any persistent data and has only a minimal implementation of [**IPersistStream**](/windows/win32/api/objidl/nn-objidl-ipersiststream).</span></span> <span data-ttu-id="e9ab9-298">[**IPersist:: GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) devuelve el CLSID del objeto (CLSID \_ SampleExplorerBar) y el resto devuelven los valores \_ correcto, s \_ false o E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-298">[**IPersist::GetClassID**](/windows/win32/api/objidl/nf-objidl-ipersist-getclassid) returns the object's CLSID (CLSID\_SampleExplorerBar), and the remainder return either S\_OK, S\_FALSE, or E\_NOTIMPL.</span></span>

### <a name="ideskband"></a><span data-ttu-id="e9ab9-299">IDeskBand</span><span class="sxs-lookup"><span data-stu-id="e9ab9-299">IDeskBand</span></span>

<span data-ttu-id="e9ab9-300">La interfaz [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) es específica de los objetos de banda.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-300">The [**IDeskBand**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband) interface is specific to band objects.</span></span> <span data-ttu-id="e9ab9-301">Además de su método, hereda de [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), que a su vez hereda de [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-301">In addition to its one method, it inherits from [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow), which in turn inherits from [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow).</span></span>

<span data-ttu-id="e9ab9-302">Hay dos métodos [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) : [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) y [**IOleWindow:: ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-302">There are two [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow) methods: [**GetWindow**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-getwindow) and [**IOleWindow::ContextSensitiveHelp**](/windows/win32/api/oleidl/nf-oleidl-iolewindow-contextsensitivehelp).</span></span> <span data-ttu-id="e9ab9-303">La implementación del ejemplo de barra del explorador de **GetWindow** devuelve el identificador de la ventana secundaria de la barra del explorador, *m \_ hWnd*.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-303">The Explorer Bar sample's implementation of **GetWindow** returns the Explorer Bar's child window handle, *m\_hwnd*.</span></span> <span data-ttu-id="e9ab9-304">No se ha implementado la ayuda contextual, por lo que **ContextSensitiveHelp** devuelve **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-304">Context-sensitive Help is not implemented, so **ContextSensitiveHelp** returns **E\_NOTIMPL**.</span></span>

<span data-ttu-id="e9ab9-305">La interfaz [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) tiene tres métodos.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-305">The [**IDockingWindow**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-idockingwindow) interface has three methods.</span></span>

-   [<span data-ttu-id="e9ab9-306">**IDockingWindow::ShowDW**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-306">**IDockingWindow::ShowDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw)
-   [<span data-ttu-id="e9ab9-307">**IDockingWindow::CloseDW**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-307">**IDockingWindow::CloseDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw)
-   [<span data-ttu-id="e9ab9-308">**IDockingWindow::ResizeBorderDW**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-308">**IDockingWindow::ResizeBorderDW**</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw)

<span data-ttu-id="e9ab9-309">El método [**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) no se usa con ningún tipo de objeto de banda y siempre debe devolver E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-309">The [**ResizeBorderDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-resizeborderdw) method is not used with any type of band object and should always return E\_NOTIMPL.</span></span> <span data-ttu-id="e9ab9-310">El método [**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) muestra u oculta la ventana de la barra del explorador, dependiendo del valor de su parámetro.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-310">The [**ShowDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-showdw) method either shows or hides the Explorer Bar's window, depending on the value of its parameter.</span></span>


```C++
STDMETHODIMP CDeskBand::ShowDW(BOOL fShow)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, fShow ? SW_SHOW : SW_HIDE);
    }

    return S_OK;
}
```



<span data-ttu-id="e9ab9-311">El método [**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) destruye la ventana de la barra del explorador.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-311">The [**CloseDW**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-idockingwindow-closedw) method destroys the Explorer Bar's window.</span></span>


```C++
STDMETHODIMP CDeskBand::CloseDW(DWORD)
{
    if (m_hwnd)
    {
        ShowWindow(m_hwnd, SW_HIDE);
        DestroyWindow(m_hwnd);
        m_hwnd = NULL;
    }

    return S_OK;
}
```



<span data-ttu-id="e9ab9-312">El método restante, [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), es específico de **IDeskBand**.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-312">The remaining method, [**GetBandInfo**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ideskband), is specific to **IDeskBand**.</span></span> <span data-ttu-id="e9ab9-313">Internet Explorer lo utiliza para especificar el identificador y el modo de visualización de la barra del explorador.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-313">Internet Explorer uses it to specify the Explorer Bar's identifier and viewing mode.</span></span> <span data-ttu-id="e9ab9-314">Internet Explorer también puede solicitar uno o más datos de la barra del explorador rellenando el miembro **dwMask** de la estructura [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) que se pasa como tercer parámetro.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-314">Internet Explorer also may request one or more pieces of information from the Explorer Bar by filling the **dwMask** member of the [**DESKBANDINFO**](/windows/desktop/api/shobjidl_core/ns-shobjidl_core-deskbandinfo) structure that is passed as the third parameter.</span></span> <span data-ttu-id="e9ab9-315">**GetBandInfo** debe almacenar el identificador y el modo de visualización y rellenar la estructura **DESKBANDINFO** con los datos solicitados.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-315">**GetBandInfo** should store the identifier and viewing mode and fill the **DESKBANDINFO** structure with the requested data.</span></span> <span data-ttu-id="e9ab9-316">El ejemplo de barra del explorador implementa **GetBandInfo** como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-316">The Explorer Bar sample implements **GetBandInfo** as shown in the following code example.</span></span>


```C++
STDMETHODIMP CDeskBand::GetBandInfo(DWORD dwBandID, DWORD, DESKBANDINFO *pdbi)
{
    HRESULT hr = E_INVALIDARG;

    if (pdbi)
    {
        m_dwBandID = dwBandID;

        if (pdbi->dwMask & DBIM_MINSIZE)
        {
            pdbi->ptMinSize.x = 200;
            pdbi->ptMinSize.y = 30;
        }

        if (pdbi->dwMask & DBIM_MAXSIZE)
        {
            pdbi->ptMaxSize.y = -1;
        }

        if (pdbi->dwMask & DBIM_INTEGRAL)
        {
            pdbi->ptIntegral.y = 1;
        }

        if (pdbi->dwMask & DBIM_ACTUAL)
        {
            pdbi->ptActual.x = 200;
            pdbi->ptActual.y = 30;
        }

        if (pdbi->dwMask & DBIM_TITLE)
        {
            // Don't show title by removing this flag.
            pdbi->dwMask &= ~DBIM_TITLE;
        }

        if (pdbi->dwMask & DBIM_MODEFLAGS)
        {
            pdbi->dwModeFlags = DBIMF_NORMAL | DBIMF_VARIABLEHEIGHT;
        }

        if (pdbi->dwMask & DBIM_BKCOLOR)
        {
            // Use the default background color by removing this flag.
            pdbi->dwMask &= ~DBIM_BKCOLOR;
        }

        hr = S_OK;
    }

    return hr;
}
```



### <a name="optional-interface-implementations"></a><span data-ttu-id="e9ab9-317">Implementaciones de interfaz opcionales</span><span class="sxs-lookup"><span data-stu-id="e9ab9-317">Optional Interface Implementations</span></span>

<span data-ttu-id="e9ab9-318">Hay dos interfaces que no son necesarias, pero que pueden ser útiles para implementar: [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) y [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-318">There are two interfaces that are not required, but that may be useful to implement: [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) and [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> <span data-ttu-id="e9ab9-319">El ejemplo de barra del explorador implementa **IInputObject**.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-319">The Explorer Bar sample implements **IInputObject**.</span></span> <span data-ttu-id="e9ab9-320">Consulte la documentación para obtener información sobre cómo implementar **IContextMenu**.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-320">Refer to the documentation for information on how to implement **IContextMenu**.</span></span>

### <a name="iinputobject"></a><span data-ttu-id="e9ab9-321">IInputObject</span><span class="sxs-lookup"><span data-stu-id="e9ab9-321">IInputObject</span></span>

<span data-ttu-id="e9ab9-322">La interfaz [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) debe implementarse si un objeto de banda acepta datos proporcionados por el usuario.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-322">The [**IInputObject**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-iinputobject) interface must be implemented if a band object accepts user input.</span></span> <span data-ttu-id="e9ab9-323">Internet Explorer implementa [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) y usa **IInputObject** para mantener el foco de entrada del usuario adecuado cuando tiene más de una ventana contenida.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-323">Internet Explorer implements [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) and uses **IInputObject** to maintain proper user input focus when it has more than one contained window.</span></span> <span data-ttu-id="e9ab9-324">Hay tres métodos que deben implementarse en una barra del explorador.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-324">There are three methods that need to be implemented by an Explorer Bar.</span></span>

-   [<span data-ttu-id="e9ab9-325">**IInputObject::UIActivateIO**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-325">**IInputObject::UIActivateIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio)
-   [<span data-ttu-id="e9ab9-326">**IInputObject::HasFocusIO**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-326">**IInputObject::HasFocusIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio)
-   [<span data-ttu-id="e9ab9-327">**IInputObject::TranslateAcceleratorIO**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-327">**IInputObject::TranslateAcceleratorIO**</span></span>](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio)

<span data-ttu-id="e9ab9-328">Internet Explorer llama a [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) para informar a la barra del explorador de que se está activando o desactivando.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-328">Internet Explorer calls [**UIActivateIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-uiactivateio) to inform the Explorer Bar that it is being activated or deactivated.</span></span> <span data-ttu-id="e9ab9-329">Cuando se activa, el ejemplo de la barra del explorador llama a [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) para establecer el foco en su ventana.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-329">When activated, the Explorer Bar sample calls [**SetFocus**](/windows/win32/api/winuser/nf-winuser-setfocus) to set the focus to its window.</span></span>

<span data-ttu-id="e9ab9-330">Internet Explorer llama a [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) cuando intenta determinar qué ventana tiene el foco.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-330">Internet Explorer calls [**HasFocusIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-hasfocusio) when it is attempting to determine which window has focus.</span></span> <span data-ttu-id="e9ab9-331">Si la ventana de la barra del explorador o uno de sus descendientes tiene el foco, **HasFocusIO** debe devolver s \_ correcto.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-331">If the Explorer Bar's window or one of its descendants has focus, **HasFocusIO** should return S\_OK.</span></span> <span data-ttu-id="e9ab9-332">Si no es así, debe devolver S \_ false.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-332">If not, it should return S\_FALSE.</span></span>

<span data-ttu-id="e9ab9-333">[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) permite al objeto procesar aceleradores de teclado.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-333">[**TranslateAcceleratorIO**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iinputobject-translateacceleratorio) allows the object to process keyboard accelerators.</span></span> <span data-ttu-id="e9ab9-334">El ejemplo de barra del explorador no implementa este método, por lo que devuelve S \_ false.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-334">The Explorer Bar sample does not implement this method, so it returns S\_FALSE.</span></span>

<span data-ttu-id="e9ab9-335">La implementación de la barra de ejemplo de [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) es la siguiente.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-335">The sample bar's implementation of [**IInputObjectSite**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinputobjectsite) is as follows.</span></span>


```C++
STDMETHODIMP CDeskBand::UIActivateIO(BOOL fActivate, MSG *)
{
    if (fActivate)
    {
        SetFocus(m_hwnd);
    }

    return S_OK;
}

STDMETHODIMP CDeskBand::HasFocusIO()
{
    return m_fHasFocus ? S_OK : S_FALSE;
}

STDMETHODIMP CDeskBand::TranslateAcceleratorIO(MSG *)
{
    return S_FALSE;
};
```



### <a name="clsid-registration"></a><span data-ttu-id="e9ab9-336">Registro de CLSID</span><span class="sxs-lookup"><span data-stu-id="e9ab9-336">CLSID Registration</span></span>

<span data-ttu-id="e9ab9-337">Al igual que con todos los objetos COM, se debe registrar el CLSID de la barra del explorador.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-337">As with all COM objects, the Explorer Bar's CLSID must be registered.</span></span> <span data-ttu-id="e9ab9-338">Para que el objeto funcione correctamente con Internet Explorer, también debe estar registrado para la categoría de componente correspondiente (CATId \_ InfoBand).</span><span class="sxs-lookup"><span data-stu-id="e9ab9-338">For the object to function properly with Internet Explorer, it must also be registered for the appropriate component category (CATID\_InfoBand).</span></span> <span data-ttu-id="e9ab9-339">En el ejemplo de código siguiente se muestra la sección de código correspondiente de la barra del explorador.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-339">The relevant code section for the Explorer Bar is shown in the following code example.</span></span>


```C++
HRESULT RegisterServer()
{
    WCHAR szCLSID[MAX_PATH];
    StringFromGUID2(CLSID_DeskBandSample, szCLSID, ARRAYSIZE(szCLSID));

    WCHAR szSubkey[MAX_PATH];
    HKEY hKey;

    HRESULT hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s", szCLSID);
    if (SUCCEEDED(hr))
    {
        hr = E_FAIL;
        if (ERROR_SUCCESS == RegCreateKeyExW(HKEY_CLASSES_ROOT,
                                             szSubkey,
                                             0,
                                             NULL,
                                             REG_OPTION_NON_VOLATILE,
                                             KEY_WRITE,
                                             NULL,
                                             &hKey,
                                             NULL))
        {
            WCHAR const szName[] = L"DeskBand Sample";
            if (ERROR_SUCCESS == RegSetValueExW(hKey,
                                                NULL,
                                                0,
                                                REG_SZ,
                                                (LPBYTE) szName,
                                                sizeof(szName)))
            {
                hr = S_OK;
            }

            RegCloseKey(hKey);
        }
    }

    if (SUCCEEDED(hr))
    {
        hr = StringCchPrintfW(szSubkey, ARRAYSIZE(szSubkey), L"CLSID\\%s\\InprocServer32", szCLSID);
        if (SUCCEEDED(hr))
        {
            hr = HRESULT_FROM_WIN32(RegCreateKeyExW(HKEY_CLASSES_ROOT, szSubkey,
                 0, NULL, REG_OPTION_NON_VOLATILE, KEY_WRITE, NULL, &hKey, NULL));
            if (SUCCEEDED(hr))
            {
                WCHAR szModule[MAX_PATH];
                if (GetModuleFileNameW(g_hInst, szModule, ARRAYSIZE(szModule)))
                {
                    DWORD cch = lstrlen(szModule);
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, NULL, 0, REG_SZ, (LPBYTE) szModule, cch * sizeof(szModule[0])));
                }

                if (SUCCEEDED(hr))
                {
                    WCHAR const szModel[] = L"Apartment";
                    hr = HRESULT_FROM_WIN32(RegSetValueExW(hKey, L"ThreadingModel", 0,  REG_SZ, (LPBYTE) szModel, sizeof(szModel)));
                }

                RegCloseKey(hKey);
            }
        }
    }

    return hr;
}
```



<span data-ttu-id="e9ab9-340">El registro de objetos de banda en el ejemplo utiliza procedimientos COM normales.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-340">Registration of band objects in the sample uses normal COM procedures.</span></span>

<span data-ttu-id="e9ab9-341">Además del CLSID, el servidor de objetos de banda también debe estar registrado para una o varias categorías de componentes.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-341">In addition to the CLSID, the band object server must also be registered for one or more component categories.</span></span> <span data-ttu-id="e9ab9-342">Esta es realmente la diferencia principal de la implementación entre los ejemplos de barras del explorador vertical y horizontal.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-342">This is actually the main difference in implementation between the vertical and horizontal Explorer Bar samples.</span></span> <span data-ttu-id="e9ab9-343">Para controlar este proceso, se crea un objeto de administrador de categorías de componentes (CLSID \_ StdComponentCategoriesMgr) y se usa el método [**ICatRegister:: RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) para registrar el servidor de objetos de banda.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-343">This process is handled by creating a component categories manager object (CLSID\_StdComponentCategoriesMgr) and using the [**ICatRegister::RegisterClassImplCategories**](/windows/win32/api/comcat/nf-comcat-icatregister-registerclassimplcategories) method to register the band object server.</span></span> <span data-ttu-id="e9ab9-344">En este ejemplo, el registro de categoría de componente se controla pasando el CLSID y el CATId de la barra del explorador a una función privada (**RegisterComCat**) como se muestra en el ejemplo de código siguiente.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-344">In this example, component category registration is handled by passing the Explorer Bar sample's CLSID and CATID to a private function—**RegisterComCat**—as shown in the following code example.</span></span>


```C++
HRESULT RegisterComCat()
{
    ICatRegister *pcr;
    HRESULT hr = CoCreateInstance(CLSID_StdComponentCategoriesMgr, NULL, CLSCTX_INPROC_SERVER, IID_PPV_ARGS(&pcr));
    if (SUCCEEDED(hr))
    {
        CATID catid = CATID_DeskBand;
        hr = pcr->RegisterClassImplCategories(CLSID_DeskBandSample, 1, &catid);
        pcr->Release();
    }
    return hr;
}
```



### <a name="the-window-procedure"></a><span data-ttu-id="e9ab9-345">El procedimiento de ventana</span><span class="sxs-lookup"><span data-stu-id="e9ab9-345">The Window Procedure</span></span>

<span data-ttu-id="e9ab9-346">Dado que un objeto de banda usa una ventana secundaria para su presentación, debe implementar un procedimiento de ventana para controlar la mensajería de Windows.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-346">Because a band object uses a child window for its display, it must implement a window procedure to handle Windows messaging.</span></span> <span data-ttu-id="e9ab9-347">El ejemplo de banda tiene una funcionalidad mínima, por lo que su procedimiento de ventana solo controla cinco mensajes:</span><span class="sxs-lookup"><span data-stu-id="e9ab9-347">The band sample has minimal functionality, so its window procedure only handles five messages:</span></span>

-   [<span data-ttu-id="e9ab9-348">**NCCREATE de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-348">**WM\_NCCREATE**</span></span>](../winmsg/wm-nccreate.md)
-   [<span data-ttu-id="e9ab9-349">**pintura de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-349">**WM\_PAINT**</span></span>](../gdi/wm-paint.md)
-   [<span data-ttu-id="e9ab9-350">**comando de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-350">**WM\_COMMAND**</span></span>](../menurc/wm-command.md)
-   [<span data-ttu-id="e9ab9-351">**SETFOCUS de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-351">**WM\_SETFOCUS**</span></span>](../inputdev/wm-setfocus.md)
-   [<span data-ttu-id="e9ab9-352">**KILLFOCUS de WM \_**</span><span class="sxs-lookup"><span data-stu-id="e9ab9-352">**WM\_KILLFOCUS**</span></span>](../inputdev/wm-killfocus.md)

<span data-ttu-id="e9ab9-353">El procedimiento se puede expandir fácilmente para dar cabida a otros mensajes para admitir más características.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-353">The procedure can easily be expanded to accommodate additional messages to support more features.</span></span>


```C++
LRESULT CALLBACK CDeskBand::WndProc(HWND hwnd, UINT uMsg, WPARAM wParam, LPARAM lParam)
{
    LRESULT lResult = 0;

    CDeskBand *pDeskBand = reinterpret_cast<CDeskBand *>(GetWindowLongPtr(hwnd, GWLP_USERDATA));

    switch (uMsg)
    {
    case WM_CREATE:
        pDeskBand = reinterpret_cast<CDeskBand *>(reinterpret_cast<CREATESTRUCT *>(lParam)->lpCreateParams);
        pDeskBand->m_hwnd = hwnd;
        SetWindowLongPtr(hwnd, GWLP_USERDATA, reinterpret_cast<LONG_PTR>(pDeskBand));
        break;

    case WM_SETFOCUS:
        pDeskBand->OnFocus(TRUE);
        break;

    case WM_KILLFOCUS:
        pDeskBand->OnFocus(FALSE);
        break;

    case WM_PAINT:
        pDeskBand->OnPaint(NULL);
        break;

    case WM_PRINTCLIENT:
        pDeskBand->OnPaint(reinterpret_cast<HDC>(wParam));
        break;

    case WM_ERASEBKGND:
        if (pDeskBand->m_fCompositionEnabled)
        {
            lResult = 1;
        }
        break;
    }

    if (uMsg != WM_ERASEBKGND)
    {
        lResult = DefWindowProc(hwnd, uMsg, wParam, lParam);
    }

    return lResult;
}
```



<span data-ttu-id="e9ab9-354">El controlador de comandos de WM \_ simplemente devuelve cero.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-354">The WM\_COMMAND handler simply returns zero.</span></span> <span data-ttu-id="e9ab9-355">El controlador de pintura de WM \_ crea la presentación de texto simple que se muestra en el ejemplo de la barra del explorador en la introducción.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-355">The WM\_PAINT handler creates the simple text display shown in the Explorer Bar example in the introduction.</span></span>


```C++
void CDeskBand::OnPaint(const HDC hdcIn)
{
    HDC hdc = hdcIn;
    PAINTSTRUCT ps;
    static WCHAR szContent[] = L"DeskBand Sample";
    static WCHAR szContentGlass[] = L"DeskBand Sample (Glass)";

    if (!hdc)
    {
        hdc = BeginPaint(m_hwnd, &ps);
    }

    if (hdc)
    {
        RECT rc;
        GetClientRect(m_hwnd, &rc);

        SIZE size;

        if (m_fCompositionEnabled)
        {
            HTHEME hTheme = OpenThemeData(NULL, L"BUTTON");
            if (hTheme)
            {
                HDC hdcPaint = NULL;
                HPAINTBUFFER hBufferedPaint = BeginBufferedPaint(hdc, &rc, BPBF_TOPDOWNDIB, NULL, &hdcPaint);

                DrawThemeParentBackground(m_hwnd, hdcPaint, &rc);

                GetTextExtentPointW(hdc, szContentGlass, ARRAYSIZE(szContentGlass), &size);
                RECT rcText;
                rcText.left   = (RECTWIDTH(rc) - size.cx) / 2;
                rcText.top    = (RECTHEIGHT(rc) - size.cy) / 2;
                rcText.right  = rcText.left + size.cx;
                rcText.bottom = rcText.top + size.cy;

                DTTOPTS dttOpts = {sizeof(dttOpts)};
                dttOpts.dwFlags = DTT_COMPOSITED | DTT_TEXTCOLOR | DTT_GLOWSIZE;
                dttOpts.crText = RGB(255, 255, 0);
                dttOpts.iGlowSize = 10;
                DrawThemeTextEx(hTheme, hdcPaint, 0, 0, szContentGlass, -1, 0, &rcText, &dttOpts);

                EndBufferedPaint(hBufferedPaint, TRUE);

                CloseThemeData(hTheme);
            }
        }
        else
        {
            SetBkColor(hdc, RGB(255, 255, 0));
            GetTextExtentPointW(hdc, szContent, ARRAYSIZE(szContent), &size);
            TextOutW(hdc,
                     (RECTWIDTH(rc) - size.cx) / 2,
                     (RECTHEIGHT(rc) - size.cy) / 2,
                     szContent,
                     ARRAYSIZE(szContent));
        }
    }

    if (!hdcIn)
    {
        EndPaint(m_hwnd, &ps);
    }
}
```



<span data-ttu-id="e9ab9-356">Los \_ controladores de WM SETFOCUS y WM \_ KILLFOCUS informan al sitio de un cambio de foco llamando al método [**IInputObjectSite:: OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) del sitio.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-356">The WM\_SETFOCUS and WM\_KILLFOCUS handlers inform the site of a focus change by calling the site's [**IInputObjectSite::OnFocusChangeIS**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-iinputobjectsite-onfocuschangeis) method.</span></span>


```C++
void CDeskBand::OnFocus(const BOOL fFocus)
{
    m_fHasFocus = fFocus;

    if (m_pSite)
    {
        m_pSite->OnFocusChangeIS(static_cast<IOleWindow*>(this), m_fHasFocus);
    }
}
```



<span data-ttu-id="e9ab9-357">Los objetos de banda proporcionan una forma flexible y eficaz de ampliar las capacidades de Internet Explorer mediante la creación de barras personalizadas del explorador.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-357">Band objects provide a flexible and powerful way to extend the capabilities of Internet Explorer by creating custom Explorer Bars.</span></span> <span data-ttu-id="e9ab9-358">La implementación de una banda de escritorio le permite ampliar las capacidades de las ventanas normales.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-358">Implementing a desk band enables you to extend the capabilities of normal windows.</span></span> <span data-ttu-id="e9ab9-359">Aunque se requiere cierta programación COM, en última instancia sirve para proporcionar una ventana secundaria para la interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-359">Although some COM programming is required, it ultimately serves to provide a child window for your user interface.</span></span> <span data-ttu-id="e9ab9-360">A partir de ahí, la mayor parte de la implementación puede usar técnicas de programación de Windows conocidas.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-360">From there, the bulk of the implementation can use familiar Windows programming techniques.</span></span> <span data-ttu-id="e9ab9-361">Aunque el ejemplo que se describe aquí solo tiene una funcionalidad limitada, ilustra todas las características necesarias de un objeto de banda y se puede ampliar fácilmente para crear una interfaz de usuario única y eficaz.</span><span class="sxs-lookup"><span data-stu-id="e9ab9-361">While the example discussed here has only limited functionality, it illustrates all the necessary features of a band object and it can be readily extended to create a unique and powerful user interface.</span></span>

 

 
