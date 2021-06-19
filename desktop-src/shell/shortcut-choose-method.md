---
description: Elija un método de menú contextual estático o dinámico al implementar un formato de archivo personalizado en el Shell de Windows.
title: Elegir un método de menú contextual estático o dinámico
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 44227BCF-D35E-4a9e-B4E6-D50E6AFBAEDF
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: dfd73ee052594e1136fe2885ce92b682f229096b
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394780"
---
# <a name="choosing-a-static-or-dynamic-shortcut-menu-method"></a><span data-ttu-id="a0756-103">Elegir un método de menú contextual estático o dinámico</span><span class="sxs-lookup"><span data-stu-id="a0756-103">Choosing a Static or Dynamic Shortcut Menu Method</span></span>

<span data-ttu-id="a0756-104">Este tema se organiza de la siguiente manera:</span><span class="sxs-lookup"><span data-stu-id="a0756-104">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="a0756-105">Elegir un método verbo</span><span class="sxs-lookup"><span data-stu-id="a0756-105">Choose a Verb Method</span></span>](#choose-a-verb-method)
    -   [<span data-ttu-id="a0756-106">Métodos de verbo estático</span><span class="sxs-lookup"><span data-stu-id="a0756-106">Static Verb Methods</span></span>](#static-verb-methods)
    -   [<span data-ttu-id="a0756-107">Métodos de verbo dinámico preferidos</span><span class="sxs-lookup"><span data-stu-id="a0756-107">Preferred Dynamic Verb Methods</span></span>](#preferred-dynamic-verb-methods)
    -   [<span data-ttu-id="a0756-108">Métodos de verbo dinámicos desaconsejados</span><span class="sxs-lookup"><span data-stu-id="a0756-108">Discouraged Dynamic Verb Methods</span></span>](#discouraged-dynamic-verb-methods)
-   [<span data-ttu-id="a0756-109">Extender un menú contextual</span><span class="sxs-lookup"><span data-stu-id="a0756-109">Extend a Shortcut Menu</span></span>](#extend-a-shortcut-menu)
-   [<span data-ttu-id="a0756-110">Compatibilidad con métodos verbos por sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a0756-110">Support for Verb Methods by Operating System</span></span>](#support-for-verb-methods-by-operating-system)
-   [<span data-ttu-id="a0756-111">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a0756-111">Related topics</span></span>](#related-topics)

## <a name="choose-a-verb-method"></a><span data-ttu-id="a0756-112">Elegir un método verbo</span><span class="sxs-lookup"><span data-stu-id="a0756-112">Choose a Verb Method</span></span>

<span data-ttu-id="a0756-113">Se recomienda encarecidamente implementar un menú contextual mediante uno de los métodos de verbo estático.</span><span class="sxs-lookup"><span data-stu-id="a0756-113">It is strongly encouraged that you implement a shortcut menu using one of the static verb methods.</span></span>

### <a name="static-verb-methods"></a><span data-ttu-id="a0756-114">Métodos de verbo estático</span><span class="sxs-lookup"><span data-stu-id="a0756-114">Static Verb Methods</span></span>

<span data-ttu-id="a0756-115">Los verbos estáticos son los verbos más sencillos de implementar, pero todavía proporcionan una funcionalidad enriquecte.</span><span class="sxs-lookup"><span data-stu-id="a0756-115">Static verbs are the simplest verbs to implement, but they still provide rich functionality.</span></span> <span data-ttu-id="a0756-116">Elija siempre el método de menú contextual más sencillo que se adapte a sus necesidades.</span><span class="sxs-lookup"><span data-stu-id="a0756-116">Always chose the simplest shortcut menu method that meets your needs.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a0756-117">Verbo estático</span><span class="sxs-lookup"><span data-stu-id="a0756-117">Static Verb</span></span></th>
<th><span data-ttu-id="a0756-118">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0756-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a0756-119"><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess con</strong></a> parámetros de línea de comandos</span><span class="sxs-lookup"><span data-stu-id="a0756-119"><a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> with command line parameters</span></span></td>
<td><span data-ttu-id="a0756-120">Este es el medio más sencillo y familiar de implementar un verbo estático.</span><span class="sxs-lookup"><span data-stu-id="a0756-120">This is the simplest and most familiar means of implementing a static verb.</span></span> <span data-ttu-id="a0756-121">Un proceso se invoca a través de una llamada a la <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>función CreateProcess</strong></a> con los archivos seleccionados y los parámetros opcionales pasados como línea de comandos.</span><span class="sxs-lookup"><span data-stu-id="a0756-121">A process is invoked through a call to the <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa"><strong>CreateProcess</strong></a> function with the selected files and any optional parameters passed as the command line.</span></span> <span data-ttu-id="a0756-122">Se abre el archivo o la carpeta.</span><span class="sxs-lookup"><span data-stu-id="a0756-122">This opens the file or folder.</span></span><br/> <span data-ttu-id="a0756-123">Este método tiene las siguientes limitaciones:</span><span class="sxs-lookup"><span data-stu-id="a0756-123">This method has the following limitations:</span></span>
<ul>
<li><span data-ttu-id="a0756-124">La longitud de la línea de comandos está limitada a 2000 caracteres, lo que limita el número de elementos que el verbo puede controlar.</span><span class="sxs-lookup"><span data-stu-id="a0756-124">The command-line length is limited to 2000 characters, which limits the number of items that the verb can handle.</span></span></li>
<li><span data-ttu-id="a0756-125">Solo se puede usar con elementos del sistema de archivos.</span><span class="sxs-lookup"><span data-stu-id="a0756-125">Can only be used with file system items.</span></span></li>
<li><span data-ttu-id="a0756-126">No permite volver a usar un proceso que ya se está ejecutando.</span><span class="sxs-lookup"><span data-stu-id="a0756-126">Does not enable re-use of an already running process.</span></span></li>
<li><span data-ttu-id="a0756-127">Requiere que se instale un ejecutable para controlar el verbo.</span><span class="sxs-lookup"><span data-stu-id="a0756-127">Requires that an executable be installed to handle the verb.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0756-128"><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"> <strong>IDropTarget</strong></a></span><span class="sxs-lookup"><span data-stu-id="a0756-128"><strong>DropTarget</strong>/<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a></span></span></td>
<td><span data-ttu-id="a0756-129">Una activación verbo basada en COM significa que admite la activación en proceso o fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="a0756-129">A COM-based verb activation means that supports in-proc or out-of-proc activation.</span></span> <span data-ttu-id="a0756-130"><strong>DropTarget</strong> / <a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget también</strong></a> admite el nuevo uso de un controlador que ya se está ejecutando cuando un servidor local implementa la interfaz <strong>IDropTarget.</strong></span><span class="sxs-lookup"><span data-stu-id="a0756-130"><strong>DropTarget</strong>/<a href="/windows/desktop/api/oleidl/nn-oleidl-idroptarget"><strong>IDropTarget</strong></a> also supports re-use of an already running handler when the <strong>IDropTarget</strong> interface is implemented by a local server.</span></span> <span data-ttu-id="a0756-131">También expresa perfectamente los elementos a través del objeto de datos serializados y proporciona una referencia a la cadena de sitio de invocación para que pueda interactuar con el invocador a través de <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a0756-131">It also perfectly expresses the items via the marshaled data object and provides a reference to the invoking site chain so that you can interact with the invoker through the <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)"><strong>QueryService</strong></a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a0756-132">Windows 7 y versiones posteriores: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"> <strong>IExecuteCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="a0756-132">Windows 7 and later: <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a></span></span></td>
<td><span data-ttu-id="a0756-133">El método de implementación más directo.</span><span class="sxs-lookup"><span data-stu-id="a0756-133">The most direct implementation method.</span></span> <span data-ttu-id="a0756-134">Dado que se trata de un método de invocación basado en COM (como DropTarget), esta interfaz admite la activación en proceso y fuera de proceso.</span><span class="sxs-lookup"><span data-stu-id="a0756-134">Because this is a COM-based invoke method (like DropTarget) this interface supports in-proc and out-of-proc activation.</span></span> <span data-ttu-id="a0756-135">El verbo implementa <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>e IObjectWithSelection y,</strong></a>opcionalmente, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="a0756-135">The verb implements <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexecutecommand"><strong>IExecuteCommand</strong></a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iobjectwithselection"><strong>IObjectWithSelection</strong></a>, and optionally <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iinitializecommand"><strong>IInitializeCommand</strong></a>.</span></span> <span data-ttu-id="a0756-136">Los elementos se pasan directamente como una matriz de elementos de Shell y hay más parámetros del invocador disponibles para la implementación del verbo, incluidos el punto de invocación, el estado del teclado, etc.</span><span class="sxs-lookup"><span data-stu-id="a0756-136">The items are passed directly as a Shell item array and more of the parameters from the invoker are available to the verb implementation, including the invoke point, keyboard state, and so forth.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a0756-137">Windows 7 y versiones posteriores:<strong>ExplorerCommand</strong> /  <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span><span class="sxs-lookup"><span data-stu-id="a0756-137">Windows 7 and later:<strong>ExplorerCommand</strong>/ <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand"><strong>IExplorerCommand</strong></a></span></span></td>
<td><span data-ttu-id="a0756-138">Permite que los orígenes de datos que proporcionan sus comandos del módulo de comandos a través de <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> usen esos comandos como verbos en un menú contextual.</span><span class="sxs-lookup"><span data-stu-id="a0756-138">Enables data sources that provide their command module commands through <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandprovider"><strong>IExplorerCommandProvider</strong></a> to use those commands as verbs on a shortcut menu.</span></span> <span data-ttu-id="a0756-139">Dado que esta interfaz solo admite la activación en proceso, se recomienda su uso por parte de orígenes de datos de Shell que necesitan compartir la implementación entre comandos y menús contextuales.</span><span class="sxs-lookup"><span data-stu-id="a0756-139">Because this interface supports in-process activation only, it is recommended for use by Shell data sources that need to share the implementation between commands and shortcut menus.</span></span></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> <span data-ttu-id="a0756-140">[**IExplorerCommand es**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) un híbrido entre un verbo estático y dinámico.</span><span class="sxs-lookup"><span data-stu-id="a0756-140">[**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) is a hybrid between a static and dynamic verb.</span></span> <span data-ttu-id="a0756-141">**IExplorerCommand** se declaró en Windows Vista, pero su capacidad para implementar un verbo en un menú contextual es nueva en Windows 7.</span><span class="sxs-lookup"><span data-stu-id="a0756-141">**IExplorerCommand** was declared in Windows Vista, but its ability to implement a verb in a shortcut menu is new to Windows 7.</span></span>

 

<span data-ttu-id="a0756-142">Para obtener más información sobre [**las consultas IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) y Shell para los atributos de asociación de archivos, vea [Perceived Types and Application Registration](fa-perceivedtypes.md).</span><span class="sxs-lookup"><span data-stu-id="a0756-142">For more information about [**IDropTarget**](/windows/win32/api/oleidl/nn-oleidl-idroptarget) and Shell queries for file association attributes, see [Perceived Types and Application Registration](fa-perceivedtypes.md).</span></span>

### <a name="preferred-dynamic-verb-methods"></a><span data-ttu-id="a0756-143">Métodos de verbo dinámico preferidos</span><span class="sxs-lookup"><span data-stu-id="a0756-143">Preferred Dynamic Verb Methods</span></span>

<span data-ttu-id="a0756-144">Se prefieren los siguientes métodos de verbo dinámico:</span><span class="sxs-lookup"><span data-stu-id="a0756-144">The following dynamic verb methods are preferred:</span></span>



| <span data-ttu-id="a0756-145">Tipo de verbo</span><span class="sxs-lookup"><span data-stu-id="a0756-145">Verb Type</span></span>                                                                                 | <span data-ttu-id="a0756-146">Descripción</span><span class="sxs-lookup"><span data-stu-id="a0756-146">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|-------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0756-147">Verbo estático (enumerado en la tabla anterior) + Sintaxis de consulta avanzada (AQS)</span><span class="sxs-lookup"><span data-stu-id="a0756-147">Static verb (listed in the previous table) + Advanced Query Syntax (AQS)</span></span>                  | <span data-ttu-id="a0756-148">Esta opción obtiene visibilidad de verbo dinámico.</span><span class="sxs-lookup"><span data-stu-id="a0756-148">This choice gets dynamic verb visibility.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="a0756-149">Windows 7 y versiones posteriores: [ **IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)</span><span class="sxs-lookup"><span data-stu-id="a0756-149">Windows 7 and later: [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand)</span></span>                         | <span data-ttu-id="a0756-150">Esta opción permite una implementación común de verbos y comandos de explorador que se muestran en el módulo de comandos en Explorador de Windows.</span><span class="sxs-lookup"><span data-stu-id="a0756-150">This choice enables a common implementation of verbs and explorer commands that are displayed in the command module in Windows Explorer.</span></span>                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="a0756-151">Windows 7 y versiones posteriores: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + verbo estático</span><span class="sxs-lookup"><span data-stu-id="a0756-151">Windows 7 and later: [**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) + static verb</span></span> | <span data-ttu-id="a0756-152">Esta opción también obtiene visibilidad de verbo dinámico.</span><span class="sxs-lookup"><span data-stu-id="a0756-152">This choice also gets dynamic verb visibility.</span></span> <span data-ttu-id="a0756-153">Se trata de un modelo híbrido en el que se usa un controlador en proceso simple para calcular si un verbo estático determinado debe ser indiscutible.</span><span class="sxs-lookup"><span data-stu-id="a0756-153">It is a hybrid model where a simple in-process handler is used to compute if a given static verb should be displyed.</span></span> <span data-ttu-id="a0756-154">Esto se puede aplicar a todos los métodos de implementación de verbo estático para lograr un comportamiento dinámico y minimizar la exposición de la lógica en proceso.</span><span class="sxs-lookup"><span data-stu-id="a0756-154">This can be applied to all of the static verb implementation methods to achieve dynamic behavior and minimize the exposure of the in-process logic.</span></span> <span data-ttu-id="a0756-155">[**IExplorerCommandState tiene**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) la ventaja de ejecutarse en un subproceso en segundo plano y, por lo tanto, evita que la interfaz de usuario se rechace.</span><span class="sxs-lookup"><span data-stu-id="a0756-155">[**IExplorerCommandState**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommandstate) has the advantage of running on a background thread, and thereby avoids UI hangs.</span></span> <span data-ttu-id="a0756-156">Es considerablemente más sencillo que [**IContextMenu.**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu)</span><span class="sxs-lookup"><span data-stu-id="a0756-156">It is considerably simpler than [**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu).</span></span> |



 

### <a name="discouraged-dynamic-verb-methods"></a><span data-ttu-id="a0756-157">Métodos de verbo dinámicos desaconsejados</span><span class="sxs-lookup"><span data-stu-id="a0756-157">Discouraged Dynamic Verb Methods</span></span>

<span data-ttu-id="a0756-158">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) es el método más eficaz, pero también el más complicado de implementar.</span><span class="sxs-lookup"><span data-stu-id="a0756-158">[**IContextMenu**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-icontextmenu) is the most powerful but also the most complicated method to implement.</span></span> <span data-ttu-id="a0756-159">Se basa en objetos COM en proceso que se ejecutan en el subproceso del autor de la llamada, que normalmente Explorador de Windows pero puede ser cualquier aplicación que hospeda los elementos.</span><span class="sxs-lookup"><span data-stu-id="a0756-159">It is based on in-process COM objects that run on the thread of the caller, which usually Windows Explorer but can be any application hosting the items.</span></span> <span data-ttu-id="a0756-160">**IContextMenu admite** visibilidad verbal, ordenación y dibujo personalizado.</span><span class="sxs-lookup"><span data-stu-id="a0756-160">**IContextMenu** supports verb visibility, ordering, and custom drawing.</span></span> <span data-ttu-id="a0756-161">Algunas de estas características se han agregado a las características del verbo estático, como un icono que se va a asociar a un comando, e [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) para tratar con la visibilidad.</span><span class="sxs-lookup"><span data-stu-id="a0756-161">Some of these features have been added to the static verb features, such as an icon to be associated with a command, and [**IExplorerCommand**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iexplorercommand) to deal with visibility.</span></span>

<span data-ttu-id="a0756-162">Si debe extender el menú contextual de un tipo de archivo mediante el registro de un verbo dinámico para el tipo de archivo, siga las instrucciones proporcionadas en Personalización de un menú contextual mediante [verbos dinámicos.](shortcut-menu-using-dynamic-verbs.md)</span><span class="sxs-lookup"><span data-stu-id="a0756-162">If you must extend the shortcut menu for a file type by registering a dynamic verb for the file type, then follow the instructions provided in [Customizing a Shortcut Menu Using Dynamic Verbs](shortcut-menu-using-dynamic-verbs.md).</span></span>

## <a name="extend-a-shortcut-menu"></a><span data-ttu-id="a0756-163">Extender un menú contextual</span><span class="sxs-lookup"><span data-stu-id="a0756-163">Extend a Shortcut Menu</span></span>

<span data-ttu-id="a0756-164">Después de elegir un método verbo, puede extender un menú contextual para un tipo de archivo registrando un verbo estático para el tipo de archivo.</span><span class="sxs-lookup"><span data-stu-id="a0756-164">After you choose a verb method you can extend a shortcut menu for a file type by registering a static verb for the file type.</span></span> <span data-ttu-id="a0756-165">Para obtener más información, vea [Crear controladores de menú contextual.](context-menu-handlers.md)</span><span class="sxs-lookup"><span data-stu-id="a0756-165">For more information, see [Creating Context Menu Handlers](context-menu-handlers.md).</span></span>

## <a name="support-for-verb-methods-by-operating-system"></a><span data-ttu-id="a0756-166">Compatibilidad con métodos verbos por sistema operativo</span><span class="sxs-lookup"><span data-stu-id="a0756-166">Support for Verb Methods by Operating System</span></span>

<span data-ttu-id="a0756-167">En la tabla siguiente se muestra la compatibilidad con los métodos de invocación de verbos por parte del sistema operativo.</span><span class="sxs-lookup"><span data-stu-id="a0756-167">Support for verb invocation methods by operating system are listed in the following table.</span></span>



| <span data-ttu-id="a0756-168">Verb (método)</span><span class="sxs-lookup"><span data-stu-id="a0756-168">Verb Method</span></span>          | <span data-ttu-id="a0756-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="a0756-169">Windows XP</span></span> | <span data-ttu-id="a0756-170">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a0756-170">Windows Vista</span></span> | <span data-ttu-id="a0756-171">Windows 7 y versiones posteriores</span><span class="sxs-lookup"><span data-stu-id="a0756-171">Windows 7 and beyond</span></span> |
|----------------------|------------|---------------|----------------------|
| <span data-ttu-id="a0756-172">CreateProcess</span><span class="sxs-lookup"><span data-stu-id="a0756-172">CreateProcess</span></span>        | <span data-ttu-id="a0756-173">X</span><span class="sxs-lookup"><span data-stu-id="a0756-173">X</span></span>          | <span data-ttu-id="a0756-174">X</span><span class="sxs-lookup"><span data-stu-id="a0756-174">X</span></span>             | <span data-ttu-id="a0756-175">X</span><span class="sxs-lookup"><span data-stu-id="a0756-175">X</span></span>                    |
| <span data-ttu-id="a0756-176">DDE</span><span class="sxs-lookup"><span data-stu-id="a0756-176">DDE</span></span>                  | <span data-ttu-id="a0756-177">X</span><span class="sxs-lookup"><span data-stu-id="a0756-177">X</span></span>          | <span data-ttu-id="a0756-178">X</span><span class="sxs-lookup"><span data-stu-id="a0756-178">X</span></span>             | <span data-ttu-id="a0756-179">X</span><span class="sxs-lookup"><span data-stu-id="a0756-179">X</span></span>                    |
| <span data-ttu-id="a0756-180">DropTarget</span><span class="sxs-lookup"><span data-stu-id="a0756-180">DropTarget</span></span>           | <span data-ttu-id="a0756-181">X</span><span class="sxs-lookup"><span data-stu-id="a0756-181">X</span></span>          | <span data-ttu-id="a0756-182">X</span><span class="sxs-lookup"><span data-stu-id="a0756-182">X</span></span>             | <span data-ttu-id="a0756-183">X</span><span class="sxs-lookup"><span data-stu-id="a0756-183">X</span></span>                    |
| <span data-ttu-id="a0756-184">ExecuteCommand</span><span class="sxs-lookup"><span data-stu-id="a0756-184">ExecuteCommand</span></span>       |            | <span data-ttu-id="a0756-185">X</span><span class="sxs-lookup"><span data-stu-id="a0756-185">X</span></span>             | <span data-ttu-id="a0756-186">X</span><span class="sxs-lookup"><span data-stu-id="a0756-186">X</span></span>                    |
| <span data-ttu-id="a0756-187">ExplorerCommand</span><span class="sxs-lookup"><span data-stu-id="a0756-187">ExplorerCommand</span></span>      |            |               | <span data-ttu-id="a0756-188">X</span><span class="sxs-lookup"><span data-stu-id="a0756-188">X</span></span>                    |
| <span data-ttu-id="a0756-189">ExplorerCommandState</span><span class="sxs-lookup"><span data-stu-id="a0756-189">ExplorerCommandState</span></span> |            |               | <span data-ttu-id="a0756-190">X</span><span class="sxs-lookup"><span data-stu-id="a0756-190">X</span></span>                    |



 

## <a name="related-topics"></a><span data-ttu-id="a0756-191">Temas relacionados</span><span class="sxs-lookup"><span data-stu-id="a0756-191">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a0756-192">Procedimientos recomendados para controladores de menús contextuales y verbos de selección múltiple</span><span class="sxs-lookup"><span data-stu-id="a0756-192">Best Practices for Shortcut Menu Handlers and Multiple Selection Verbs</span></span>](verbs-best-practices.md)
</dt> <dt>

[<span data-ttu-id="a0756-193">Creación de controladores de menús contextuales</span><span class="sxs-lookup"><span data-stu-id="a0756-193">Creating Shortcut Menu Handlers</span></span>](context-menu-handlers.md)
</dt> <dt>

[<span data-ttu-id="a0756-194">Personalizar un menú contextual mediante verbos dinámicos</span><span class="sxs-lookup"><span data-stu-id="a0756-194">Customizing a Shortcut Menu Using Dynamic Verbs</span></span>](shortcut-menu-using-dynamic-verbs.md)
</dt> <dt>

[<span data-ttu-id="a0756-195">Menús contextuales y controladores de menús contextuales</span><span class="sxs-lookup"><span data-stu-id="a0756-195">Shortcut (Context) Menus and Shortcut Menu Handlers</span></span>](context-menu.md)
</dt> <dt>

[<span data-ttu-id="a0756-196">Referencia del menú contextual</span><span class="sxs-lookup"><span data-stu-id="a0756-196">Shortcut Menu Reference</span></span>](context-menu-reference.md)
</dt> <dt>

[<span data-ttu-id="a0756-197">Verbos y asociaciones de archivo</span><span class="sxs-lookup"><span data-stu-id="a0756-197">Verbs and File Associations</span></span>](fa-verbs.md)
</dt> </dl>

 

 
